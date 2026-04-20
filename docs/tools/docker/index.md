# Docker

Docker is an open-source platform for building, shipping, and running applications inside lightweight, portable containers. A container packages an application together with all of its dependencies, libraries, and configuration so that it runs identically on any machine with the Docker runtime installed.

In the Bitstream Evolution (v2 pico2-ice) project, Docker provides a reproducible environment for the FPGA toolchain (Yosys, nextpnr, Project IceStorm) and the evolutionary algorithm software, eliminating "works on my machine" issues across different Linux distributions and macOS versions.

[:octicons-link-external-16: Official Website](https://www.docker.com/){ .md-button .md-button--primary }
[:material-file-document: Official Docs](https://docs.docker.com/){ .md-button .md-button--seccondary }
[:octicons-mark-github-16: GitHub Repository](https://github.com/docker){ .md-button }

## Key Concepts

- **Image** --- a read-only template containing the OS, toolchain binaries, Python packages, and any other dependencies. Built once, shared via Docker Hub or a registry.
- **Container** --- a running instance of an image. Containers are isolated from the host but can mount local directories and access USB devices (important for FPGA programming).
- **Dockerfile** --- a text recipe that specifies how to build an image step by step (base OS, packages to install, files to copy, etc.).
- **Volume / Bind Mount** --- allows a container to read and write files on the host filesystem, so experiment data persists after the container stops.

## Why Docker for EHW

- **Reproducible toolchain** --- every contributor gets the exact same versions of Yosys, nextpnr, icestorm, and Python packages regardless of their host OS.
- **Simplified setup** --- instead of manually installing a dozen dependencies, a single `docker build` or `docker pull` command prepares the entire environment.
- **USB device passthrough** --- Docker on Linux supports `--device` flags to pass `/dev/ttyUSB*` and `/dev/ttyACM*` devices into the container, enabling direct communication with the iCEstick, pico2-ice, and Arduino from inside a containerized toolchain.
- **CI/CD integration** --- the same Docker image used for local development can run in GitHub Actions or other CI pipelines, ensuring experiments and tests execute in a consistent environment.

## Project Use

The Bitstream Evolution (v2 pico2-ice) repositories (including iCEFARM) use Docker to package the complete development environment. This is especially useful for onboarding new contributors who can get a working toolchain running with:

```bash
docker build -t bitstream-evolution .

```

!!! note "USB Access on Linux"
    To access FPGA and Arduino USB devices from inside a Docker container, the host user typically needs to be in the `dialout` group, and the container must be started with the appropriate `--device` flags.

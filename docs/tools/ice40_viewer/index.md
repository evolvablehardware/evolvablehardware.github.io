# iCE40 Floorplan Viewer

An interactive browser-based visualization tool for iCE40 FPGA floorplans. It renders the physical layout of logic cells, I/O blocks, and routing resources, making it possible to visually inspect how designs are placed and routed on the chip.

[:octicons-link-external-16: Open iCE40 Viewer](https://knielsen.github.io/ice40_viewer/ice40_viewer.html){ .md-button .md-button--primary }

## Key Features

- **Interactive floorplan** — zoom, pan, and click on individual tiles and cells
- **Browser-based** — no installation required, runs entirely in the browser
- **iCE40 family support** — visualize HX1K, UP5K, and other iCE40 device layouts
- **Bitstream inspection** — load `.asc` files to see how a design maps onto the physical chip

## Role in Evolvable Hardware

The iCE40 Viewer is particularly useful for evolvable hardware research because it allows researchers to visually inspect evolved bitstreams. After an evolutionary run produces a circuit, the viewer can show exactly which logic cells and routing paths the evolution utilized — including unconventional connections that exploit analog physical properties of the FPGA.

## Project Use

- [Bitstream Evolution (iCEstick)](../../projects/bitstream_evolution/index.md) — inspect evolved bitstreams on the HX1K
- [Bitstream Evolution (pico2-ice)](../../projects/bitstream_evolution_pico2-ice/index.md) — inspect evolved bitstreams on the UP5K

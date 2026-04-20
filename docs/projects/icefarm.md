---
hide:
  - toc
---

# iCEFARM

**FPGA Array Resource Manager** — a parallel evaluation system that distributes evolutionary runs across multiple pico2-ice boards simultaneously, enabling larger population sizes and faster evolutionary runs.

[:octicons-mark-github-16: evolvablehardware/iCEFARM]({{config.extra.iCEFARM_repo}}){ .md-button } 
[iCEFARM Docs]({{config.extra.iCEFARM_docs}}){ .md-button }

## Overview

iCEFARM enables simultaneous bitstream evaluation across multiple pico2-ice boards. Rather than evaluating one candidate circuit at a time on a single FPGA, iCEFARM distributes the population across an array of boards for parallel fitness evaluation.

!!! info "Documentation Coming Soon"
    The iCEFARM hardware setup guide is currently under development. Check back soon for detailed instructions on configuring an array of pico2-ice boards for parallel FPGA evaluation.

## Related Projects

- [Bitstream Evolution (pico2-ice)](./bitstream_evolution_pico2-ice/index.md)

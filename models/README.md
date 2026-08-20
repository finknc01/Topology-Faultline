# Modeled / Reference Topologies

This directory is for topology behavior that the local lab cannot measure directly.

Rules:
- label every artifact **modeled/reference**;
- cite the public architecture or specification used;
- keep modeled diagrams separate from measured laptop/host diagrams;
- never imply NVLink, NVSwitch, multi-socket NUMA, HCAs, or other enterprise features exist locally unless they were actually verified;
- use modeled cases to practice reasoning, not to manufacture evidence.

Good modeled artifacts include:
- dual-socket GPU-server locality diagrams;
- GPU/NIC placement comparisons;
- PCIe bottleneck scenarios;
- NVLink/NVSwitch reference paths;
- synthetic degraded-link investigations.

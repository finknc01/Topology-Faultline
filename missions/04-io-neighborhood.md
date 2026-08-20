# Case 04 — The I/O Neighborhood

## Briefing
The GPU is not the only device that matters. Storage and network traffic must also enter and leave the node.

## Objective
Map GPU, NIC, and NVMe locality and reason about data paths through the CPU/PCIe hierarchy.

## Tasks
Locate the GPU, primary NVMe device, and network adapter in the PCIe tree. Trace the likely path for dataset read → host memory → GPU and GPU → NIC traffic. If all devices share one simple laptop root complex, create a second modeled topology with devices split across sockets/root complexes.

## Evidence
- actual I/O neighborhood map
- modeled split-locality map
- two packet/data-path narratives

## Victory condition
You can identify when “fast GPU + fast NIC + fast SSD” can still produce an inefficient system because placement is poor.

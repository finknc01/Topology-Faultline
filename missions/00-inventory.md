# Case 00 — Inventory the Crime Scene

## Briefing
Two nodes are supposedly identical. Before comparing them, establish what “topology” actually means.

## Objective
Map the CPU, memory, PCIe devices, GPU, storage, and network adapters your real system exposes.

## Tasks
Use `lscpu`, `lspci -tv`, `lspci -vv`, `lsblk`, `/sys/bus/pci/devices`, and NVIDIA topology tools where supported. Build a diagram from CPU/root complex to each visible high-value device.

## Evidence
- raw inventory excerpts
- device BDF addresses
- first topology diagram
- note identifying which relationships are measured vs inferred

## Twist
The asset inventory says only model names. Your job is to show why model names alone cannot describe the communication path.

## Victory condition
You can point to a device in the diagram and explain how you proved where it sits.

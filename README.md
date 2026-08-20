# Topology-Faultline

> **Case File 07: The Missing Bandwidth — explain why systems with similar parts can behave differently when the paths between those parts are different.**

## Project status

| Field | Current state |
|---|---|
| **Status** | **Planned — scheduled in the 52-week roadmap** |
| **Current stage** | Casebook authored; no case completion or experimental result is claimed yet |
| **Lab environment** | Real laptop topology first; multi-socket, SXM, NVLink/NVSwitch, and HCA systems are modeled from public references |
| **Evidence rule** | Every artifact must be labeled **measured**, **derived**, **simulated**, or **modeled/reference** |
| **Last plan sync** | 2026-08-19 |

## Purpose

Topology-Faultline is a hardware-forensics lab. A fictional AI platform team reports that two supposedly equivalent compute nodes behave differently. Nothing is obviously failed; the suspected problem is topology, locality, or a degraded link.

The central question is:

> **What path does the data actually take through the machine, and where can topology make that path expensive?**

The laptop supplies real CPU, PCIe, storage, and GPU-placement evidence where exposed by the operating system. Enterprise-only topologies are reconstructed as clearly labeled models rather than presented as local hardware experience.

## Skills developed

- CPU/socket/NUMA reasoning
- PCIe trees, root complexes, bridges, link width/generation, and locality
- GPU, NIC/HCA, and NVMe placement reasoning
- `lscpu`, `lspci`, sysfs, `numactl`, and `nvidia-smi topo` where supported
- performance-path hypothesis building
- separating measured systems from modeled enterprise architectures

## Investigation casebook

The files in [`missions/`](missions/) are authoritative.

| Case | Investigation | Primary outcome |
|---|---|---|
| [00 — Inventory the Crime Scene](missions/00-inventory.md) | Map what the real system exposes | measured system inventory |
| [01 — Follow the PCIe Trail](missions/01-pcie-trail.md) | Reconstruct the PCIe hierarchy and device paths | PCIe tree + interpretation |
| [02 — The NUMA Alibi](missions/02-numa-alibi.md) | Reason about CPU/memory locality | local-vs-remote path model |
| [03 — GPU Locality](missions/03-gpu-locality.md) | Place the GPU in the host topology | GPU/CPU locality explanation |
| [04 — The I/O Neighborhood](missions/04-io-neighborhood.md) | Relate GPU, storage, and network-device paths | I/O locality map |
| [05 — The Link That Lied](missions/05-link-downgrade.md) | Diagnose a clearly labeled synthetic degraded-link case | designed-vs-observed matrix + bandwidth estimate |
| [Final — The Missing Bandwidth](missions/final-missing-bandwidth.md) | Solve a cross-layer topology case from evidence | defensible root-cause argument |

## Modeling rule

Do not claim the laptop has multiple sockets, NVSwitch, SXM GPUs, multiple HCAs, or other enterprise features it does not expose. Use official architecture references to model those systems, then explicitly compare the model with the real local topology.

Synthetic cases are valuable when the objective is reasoning that cannot be safely or physically reproduced at home. The artifact must say what is synthetic and what evidence would be collected on real hardware.

## Evidence standard

Each case should contribute one or more of the following:

- measured inventory or command output
- a topology/data-path diagram
- a derived bandwidth or locality calculation
- a hypothesis matrix
- a modeled enterprise comparison
- an escalation checklist showing what a data-center engineer would inspect next

## Completion condition

Topology-Faultline is complete when you can start with a vague complaint such as “the GPU is slow,” identify the plausible topology paths, distinguish inventory from connectivity/locality, and build an evidence-based investigation without pretending to own hardware you do not have.

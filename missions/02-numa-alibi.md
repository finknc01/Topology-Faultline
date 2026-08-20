# Case 02 — The NUMA Alibi

## Briefing
A workload is fast on one socket placement and slow on another in the production incident report. Your laptop may have only one NUMA node, but you still need to understand the mechanism.

## Objective
Learn sockets, NUMA nodes, CPU affinity, memory locality, and the cost of crossing topology boundaries.

## Tasks
Inspect `lscpu`, `numactl --hardware`, and CPU topology. If your system exposes multiple NUMA nodes, run a small repeatable memory/CPU benchmark with different bindings. If it exposes one, record that limitation and analyze a supplied or self-created two-socket reference diagram instead.

## Evidence
- real NUMA inventory
- benchmark if physically possible
- modeled two-socket path showing local vs remote memory
- explanation of why an HCA/GPU attached to one socket changes placement decisions

## Victory condition
You can explain NUMA without pretending your single-socket laptop is a dual-socket server.

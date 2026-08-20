# Case 03 — GPU Locality

## Briefing
The application team assumes every GPU-to-GPU path is equivalent. That assumption is now evidence.

## Objective
Understand GPU peer paths, PCIe relationships, and the roles of NVLink/NVSwitch in systems that have them.

## Tasks
Run `nvidia-smi topo -m` where supported and reconcile its output with your PCIe map. For a one-GPU laptop, build a measured one-GPU map plus a separately labeled modeled 8-GPU server topology. Compare PCIe-only, NVLink, and NVSwitch communication paths conceptually.

## Evidence
- actual `nvidia-smi topo` output or limitation note
- one measured diagram and one modeled enterprise diagram
- table of path types and expected implications

## Victory condition
You can explain what topology information a distributed-training engineer needs before assuming peer communication is uniform.

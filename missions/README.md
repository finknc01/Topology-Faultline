# Topology-Faultline Casebook

Case File 07 asks why “identical” compute nodes can behave differently. You will treat topology like physical evidence: measure what your laptop actually exposes, model what it cannot, and never blur the two.

## Cases
- [00 — Inventory the Crime Scene](00-inventory.md)
- [01 — Follow the PCIe Trail](01-pcie-trail.md)
- [02 — The NUMA Alibi](02-numa-alibi.md)
- [03 — GPU Locality](03-gpu-locality.md)
- [04 — The I/O Neighborhood](04-io-neighborhood.md)
- [05 — The Link That Lied](05-link-downgrade.md)
- [Final — The Missing Bandwidth](final-missing-bandwidth.md)

## Rules
Mark every artifact as **measured**, **derived**, or **modeled**. Never claim laptop hardware has NVLink, NVSwitch, multiple sockets, or multiple HCAs if it does not. The portfolio value is in reasoning correctly from evidence.

# Case 01 — Follow the PCIe Trail

## Briefing
The suspect node has the right GPU, but the data path may be narrower than expected.

## Objective
Understand PCIe generations, lanes, root ports, bridges/switches, negotiated width, and why topology matters to accelerators.

## Tasks
Trace the GPU and one other high-bandwidth device through `lspci -tv`. Inspect capability and negotiated link information with `lspci -vv`. Annotate the tree with x1/x4/x8/x16 and generation information where visible.

## Investigation question
If the GPU advertises one capability but negotiates another, what classes of cause could explain it?

Do not alter BIOS settings just to manufacture a downgrade. If your laptop does not expose a degraded link, use a clearly labeled synthetic/reference capture and diagnose it as a paper case.

## Evidence
- annotated PCIe tree
- capability vs negotiated-state table
- expected bandwidth calculation with assumptions shown

## Victory condition
You can explain why “PCIe Gen4 GPU” does not guarantee a Gen4 x16 path.

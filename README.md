# SwarmAlloc

A unified multi-agent neural solver for UAV swarm task allocation. A single
model per scale covers eight structural variants of the cooperative multiple
task assignment problem (CMTAP), combining multi-task learning with parallel
multi-agent decoding and constraint-aware action masks.

## Contents

| Path | Content |
|---|---|
| `data/main/` | Test instances for the three scales used in the main comparison, eight variants at each scale, 100 instances per variant. |
| `data/hil/` | Ground-station mission plans used in the hardware-in-the-loop validation. |
| `routes/` | Per-instance route displays, collected in a single PDF. |

```
data/main/
├── n10_m3/
├── n30_m7/
└── n50_m11/
```

## Data

Instances are compressed NumPy archives, one file per variant and scale, with
100 instances per file:

```
data/main/n30_m7/n30_m7_mbt_seed1002.npz
data/main/n30_m7/n30_m7_nodyn_mbt_seed1002.npz
```

Files sharing the same seed contain the same instance layout and differ only in
the attributes switched off by the variant. The variant flags follow
`[D, R, P]`.

## Hardware in the loop

The HIL material was collected on a ground station driving six UAVs over 40
static targets, eight dynamically released targets, and eight no-fly zones.
`data/hil/` holds the mission plans and `routes/routes.pdf` collects the
corresponding route displays. A screen recording of the session is available on
[Bilibili](https://www.bilibili.com/video/BV1aV4P6PERW/).

## License

Data and route displays are released under CC BY 4.0.

## Citation

If you use this material, please cite the accompanying manuscript:

> SwarmAlloc: A Unified Multi-Agent Neural Solver for UAV Swarm Task Allocation (2026).

# EXD-Net v1: Hopfield Drift Memory Model

This notebook models **emotional memory destabilization and transformation** using a classic Hopfield network. Memory scenes are encoded as binary patterns acting as attractors. Over time, **new associations** (e.g., "Benji") are reinforced, causing the network to **drift**, destabilize, and rewire.

The result is a computational simulation of:
- identity shift  
- memory drift  
- nonlinear transformation

EXD-Net v1 simulates how emotional recall is altered by reinforcement and shows how some memories remain resistant, while others suddenly flip. While this first release focuses on emotional memory, EXD-Net is not limited to that domain. It is part of a broader framework designed to explore how **instability**, **dissonance**, and **reinforcement** reshape memory over time. By modeling memory scenes as attractor states and introducing disruptive associations, EXD-Net demonstrates how mental representations can shift, destabilize, and reorganize.

## Core Concepts

- **Memory as Attractors**: Each scene is a 32x32 binary pattern stored in a Hopfield network
- **Memory Drift**: Reinforcing a new memory causes gradual or abrupt divergence from the original attractor
- **Destabilization Points**: Some scenes show nonlinear turning points where recall shifts
- **Energy Landscapes**: Hopfield energy is used to analyze the depth and dominance of emotional memory basins

## Features

- Binary image-based Hopfield network (32×32)
- Progressive memory reinforcement with noise-robust recall
- Cosine similarity tracking for association shift
- Turning point detection (first recall of new association)
- Hopfield energy comparison between old and new attractors
- Convergence analysis over time
- Interpretability through real emotions (e.g., denial, suppression, reattachment)

## Repo Structure

```
.
├── exdnet_v1.ipynb        # Main notebook
├── data/
│   ├── exdnet_v1.csv      # Similarity logs
│   └── energy_df.csv      # Hopfield energy + turning points
├── images/                # Raw memory inputs (ex, benji, background)
├── plots/                 # Generated visualizations (delta plots, energy maps)
├── weights/
│   ├── W_base_v1.npy      # Weights trained only on Ex
│   └── W_temp_v1.npy      # Weights after Benji reinforcement
├── requirements.txt       # Minimal dependencies
└── README.md
```


## Why It Matters

This model offers a **computational lens on memory under instability**. Not just emotional memory, but memory in flux. From simulating attachment rewiring to exploring cognitive dissonance, EXD-Net v1 shows how systems evolve through reinforcement, resistance, and collapse.

> Drift isn't linear. Transformation isn't smooth. And not all memories are equal.

## Next Steps
This is the **foundational release** before EXD-Net becomes a flexible framework for: 
- Modeling (emotional) memory as a dynamic, high-dimensional system
- Simulating cognitive dissonance, destabilization trajectories, and transformation over time
- Creating computational experiments rooted in cognitive and psychological theory

If you're interested in contributing, collaborating, or discussing aligned research directions, please reach out directly.

**Read more about the theory behind EXD-Net on Substack**:  
https://exd1000.substack.com


---
**License**: Apache License 2.0 — reuse allowed with attribution. Commercial exploitation or derivative frameworks require prior permission from the author.

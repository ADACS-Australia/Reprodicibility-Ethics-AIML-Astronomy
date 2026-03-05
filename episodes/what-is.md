---
title: "Wat do we mean by reproducibility in ML?"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---

## What do we mean by reproducibility in ML?

### Core definitions (adapted for astronomy)
- **Repeatability**  
  - Same team, same code, same data, same environment → same result
- **Reproducibility**  
  - Same data + code, different person or time → same result
- **Replicability**  
  - New data or method → consistent scientific conclusion

> Emphasise: ML often struggles even with *repeatability*.

### Why ML is especially fragile
- Random initialisation and data splits
- Hardware and software dependencies (GPUs, libraries)
- Hidden preprocessing steps
- Non‑deterministic algorithms

### ML reproducibility checklist (conceptual)
Learners should be able to answer:
- Can someone else:
  - run my code?
  - access the data (or a description)?
  - understand how hyperparameters were chosen?
- Could *I* rerun this in a year?

### TODO (lesson content)
- Add a short “bad vs better” example (e.g. undocumented train/test split)


> If you can’t rerun it, you didn’t really finish the experiment.
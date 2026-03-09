---
title: "Wat do we mean by reproducibility?"
teaching: 15 # teaching time in minutes
exercises: 10 # exercise time in minutes
---

## What do we mean by reproducibility?

The word "reproducibility" is used in many ways, often imprecisely.
In practice, misunderstandings about what *kind* of reproducibility is being claimed are a major source of confusion, frustration, and irreproducible results in computational astronomy and ML‑based research.
This section introduces a small set of definitions that are widely used across computational sciences and astronomy, and shows how they apply in practice.

### Three related but distinct concepts

Many communities now distinguish between three ideas:

**Repeatability**  
: The same researchers can rerun the same code, on the same data, in the same environment, and get the same result.

**Reproducibility**  
: A different researcher (or you, later) can rerun the same code, on the same data, and get the same result.

**Replicability**  
: A different analysis, dataset, or method leads to a consistent scientific conclusion.

In astronomy, most failures happen at the repeatability level - before we even reach reproducibility.

Remember: **If you cannot repeat your own result, no one else can reproduce it.**



### Why this matters in ML‑based astronomy

Machine learning makes reproducibility harder than many traditional analyses because it introduces:

- randomness (initialisation, data splits, stochastic optimisation)
- long, implicit preprocessing chains
- complex software stacks
- performance claims that depend on subtle choices

Common astronomy‑specific examples include:

- a transient classifier whose accuracy depends on an undocumented random seed
- a photometric redshift model trained on one survey and reused on another without retraining
- a simulation‑trained model whose domain of validity is unclear

These issues are discussed explicitly in astronomy‑adjacent reproducibility training materials such as the [MPI‑Astronomy reproducibility workshop](https://mpi-astronomy.github.io/data_science_training_materials/reproducibility).


:::: challenge

## Classifying reproducibility claims

Read the following statements and decide which category they belong to: repeatable, reproducible, or replicable.

No discussion yet; just decide for yourself.

1. "I reran my notebook on my laptop and got the same plot."
2. "My collaborator ran my code from GitHub and reproduced all figures."
3. "Another group used a different survey and found the same astrophysical trend."

After one minute, discuss briefly with a neighbour.

::::

:::: instructor

This activity usually reveals that many people conflate reproducibility and replicability.

::::


### Reproducibility is a spectrum, not a switch

In real research, reproducibility is rarely all‑or‑nothing.

For example:

- You might share code but not data
- You might share data but not preprocessing
- You might document assumptions but not environments

This is normal.
The goal is not perfection, but **making explicit what can and cannot be reproduced**.
The [Turing Way](https://book.the-turing-way.org/reproducible-research) emphasises this framing, especially for computational and ML‑based research.

Remember: **Partial reproducibility is better than implicit irreproducibility.**


### What reproducibility does *not* require

A common misconception is that reproducibility means:

- your code must be beautiful
- your results must be flawless
- everything must be public forever

None of these are true.
Reproducibility requires clarity, not elegance.
You can be reproducible while:

- using imperfect code
- reporting negative or null results
- restricting access to sensitive data (with clear conditions)


### Examples of good reproducible practice in astronomy

The following are widely cited examples of astronomy communities explicitly designing for reproducibility:

- **Astropy Collaboration**  
  [Astropy](https://www.astropy.org/) provides a reproducible, community‑maintained software ecosystem with explicit versioning, testing, and citation practices.  
  

- **IVOA standards and Virtual Observatory workflows**  
  The International Virtual Observatory Alliance ([IVOA](https://ivoa.net/)) has implemented interoperability and metadata standards that strongly align with FAIR and reproducibility principles .

- **Reproducible ML workflows in astronomy training**  
  [MPI‑Astronomy](https://mpi-astronomy.github.io/data_science_training_materials/) and similar groups explicitly teach reproducible ML pipelines, including environment capture and workflow provenance.  
  

These examples show that reproducibility is not hypothetical; it is already embedded in successful astronomy infrastructure.

:::: challenge 

## Identifying reproducibility gaps

Think about your own current project.
Silently answer the following:

- Could you rerun your main result today?
- Could someone else rerun it using your description?
- Which part would fail first?

Write down one concrete gap (e.g. "train/test split not saved", "data cleaning undocumented").

No sharing required.
::::

:::: instructor

This activity is intentionally non‑judgmental and reflective.

::::


### Reproducibility versus performance in ML papers

In ML‑based science, performance claims are often treated as evidence.
That is to say, model performance (correlation of output to "known" results) is treated as a proxy for scientific validity (the ability to understand or explain a phenomena).
This is the classic correlation vs causation confusion.

However, large‑scale reviews have shown that:
- subtle methodological errors such as data leakage are widespread, leading to an over-reporting of model performance
- claimed improvements often disappear when analyses are reproduced correctly (e.g [Kapoor and Narayanan, 2023](https://doi.org/10.1016/j.patter.2023.100804))

Performance does not imply physical understanding. 
A classifier that distinguishes galaxies from stars with high accuracy does not necessarily:

- encode meaningful morphology
- generalize across surveys
- respect physical invariants

It may instead exploit:

- PSF differences
- survey depth artefacts
- preprocessing quirks

This is not an argument against ML.
It is an argument for **clear, reproducible evidence** when ML models are used to support scientific claims.
Reproducible results are easier to interrogate, and lead to a higher confidence in the reported outcomes.


### Key takeaways

- Reproducibility, repeatability, and replicability are related but distinct
- Most failures occur at the repeatability stage
- ML increases the need for explicit documentation
- Reproducibility is about clarity, not perfection
- **If you do not state what can be reproduced, readers will assume nothing can.**

---
title: "Data, models, and FAIRness in ML astronomy"
teaching: 15 # teaching time in minutes
exercises: 10 # exercise time in minutes
---

## Data, models, and FAIR practices in ML astronomy

Machine learning workflows in astronomy produce more than papers.
They produce:

- training datasets
- labels and annotations
- trained models
- derived catalogues
- complex preprocessing pipelines

If these outputs are not shared in a FAIR way, ML results become difficult or impossible to reuse, validate, or build upon.

This section focuses specifically on **FAIR data and model sharing practices**, and how they apply to ML‑based astronomy.


### What does FAIR mean in astronomy?

FAIR stands for:

- **Findable**
- **Accessible**
- **Interoperable**
- **Reusable**

The FAIR principles were introduced by [Wilkinson et al. (2016)](https://doi.org/10.1038/s41597-019-0009-6) and are now widely adopted across scientific domains.
In astronomy, FAIR has a concrete and well‑established interpretation through:

- Virtual Observatory infrastructure
- IVOA standards
- long‑lived data archives

An overview of how FAIR maps onto astronomical practice is given by [O'Toole and Tocknell (2022)](https://arxiv.org/abs/2203.10710).

Summary: **FAIR is about making research outputs usable by humans and machines.**


### Astronomy is close to FAIR by default

Astronomy is often described as "world‑leading" in data stewardship.
This is largely true because:

- most survey data are archived
- metadata standards are well developed
- access is usually long‑term

IVOA standards were, in practice, implementing FAIR‑like ideas before the FAIR principles were formally articulated.
As a result:

- raw observational data are often FAIR
- catalogues linked to publications are often FAIR
- archive‑level metadata is usually strong

However, ML workflows introduce **new outputs that are often not FAIR**.

### Where ML workflows break FAIRness

In ML‑based astronomy, FAIR failures usually occur downstream of the archive.
Common examples include:

- private training sets derived from public data
- labels created by individuals and never shared
- preprocessing scripts that are undocumented
- trained models released without context
- catalogues published without provenance

These issues are explicitly identified in FAIR guidance for astronomy, which emphasises that **provenance, processing history, and metadata are essential for reuse** ([O'Toole and Tocknell, 2022](https://arxiv.org/abs/2203.10710)).

Remember: **FAIR does not stop at the telescope. It extends through the full analysis pipeline.**

### FAIR applies to models, not just data

A common misconception is that FAIR applies only to raw data.
In ML astronomy, FAIR should apply to:

- training datasets
- labels and annotations
- feature representations
- trained models
- evaluation datasets

If a trained model is shared without:

- its training data description
- preprocessing steps
- intended scope

then it is not reusable, even if the model file itself is available.

This point is emphasised in astronomy‑focused FAIR discussions, which note that **machine‑actionable reuse requires rich metadata and provenance**, not just file access ([Berriman, 2022](https://ci-compass.org/assets/464624/applicationoffairprinciplesinastronomygbruceberriman.pdf)).


:::: challenge 

## Is your ML output FAIR?

Think about one ML artefact you have produced or used.
For that artefact, ask:

- Can someone find it?
- Can they access it?
- Can they understand what it expects as input?
- Can they reuse it without asking you questions?

Write down one missing piece of information.

No sharing required.

::::

### FAIR does not mean open at all costs

Another common misconception is that FAIR means "everything must be open".
This is not true.
FAIR explicitly allows for:

- access controls
- embargo periods
- restricted data

The requirement is not openness, but **clarity**:

- how the data can be accessed
- under what conditions
- with what limitations

FAIR guidance for astronomy explicitly separates:

- openness (a policy choice)
- FAIRness (a technical and metadata choice)  

**Data can be FAIR without being fully open.**


### Why FAIR matters for ML reuse

ML outputs are frequently reused:

- by collaborators
- by downstream projects
- by future surveys

If ML artefacts are not FAIR:

- reuse requires personal communication
- validation becomes difficult
- results quietly decay over time

FAIR practices reduce this fragility by:

- making assumptions explicit
- preserving provenance
- supporting long‑term reuse

This is especially important in astronomy, where datasets often outlive individual projects and researchers.

:::: challenge

## One FAIR improvement

Identify one concrete change you could make to improve FAIRness:

- a README
- a data dictionary
- a provenance note
- a model description

Write it down.

That is enough for now.

::::

### Key takeaways

- FAIR applies to data, models, and derived products
- Astronomy infrastructure already supports FAIR principles
- ML workflows often fall outside existing FAIR practices
- Small documentation steps dramatically improve reuse

Thought: **"If your ML result cannot be reused without emailing you, it is not FAIR yet."**
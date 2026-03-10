---
title: "Practical takeaways for astronomers"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---

## Practical takeaways for astronomers

Reproducibility, FAIR practices, and ethical ML use can feel abstract until they are translated into concrete actions.
This section focuses on **practical minimum standards** that astronomers can apply immediately, without rewriting their entire workflow or becoming software engineers.
The goal is not perfection.
The goal is for our work to be clear, honest, and reusable *enough*.

### A minimum reproducibility standard for ML projects

For most astronomy ML projects, a reasonable minimum standard is that:

- you can rerun your own main result
- someone else could rerun it with effort, but without guessing
- limitations are stated explicitly

In practice, this usually means having:

- versioned code
- fixed or recorded randomness
- explicit data splits
- documented preprocessing
- a short description of scope and limitations

**Anything beyond this is a bonus.**

### What to document (even if you share nothing else)

If you only document a few things, make them these:

- **Data provenance**  
  - Where the data came from, including archive, release, and selection criteria.

- **Preprocessing steps**  
  - What was done to the data before training, especially filtering, scaling, and feature construction.

- **Randomness**  
  - Whether results depend on random seeds, and whether those seeds were fixed.

- **Model scope**  
  - What the model was designed to do, and where it was not tested.

This information is often more important than hyperparameter details.

Rule of thumb:  **Documentation that answers questions is more useful than documentation that looks complete.**

### FAIR does not require new infrastructure

Many astronomers assume FAIR practices require:

- specialised repositories
- complex metadata schemas
- institutional support

In reality, small steps already help a lot.
For example:

- a README.md in a Git repository
- a data dictionary for derived features
- a short "how to reproduce Figure 3" note
- a model description paragraph in the paper

FAIRness improves through **clarity**, not tooling.

:::: challenge

## The five‑minute README

Imagine someone opens your project folder in a year.
Write down the headings of a README that would help them.

For example:

- What this project does
- Where the data came from
- How to rerun the main result
- Known limitations

You do not need to write the content now.

Just the headings are enough.

::::

### How to be ethically careful without being defensive

Ethical ML practice in astronomy does not require disclaimers everywhere.

It requires:

- stating assumptions
- stating limits
- avoiding implied generality

Helpful phrases include:

- "This model was trained on…"
- "Performance was evaluated only on…"
- "We did not test…"
- "Results should not be interpreted as…"

These are not weaknesses.
They are signals of careful science.


### When full openness is not possible

Sometimes you cannot share:

- proprietary data
- sensitive observations
- intermediate products
- large files

This does not prevent reproducibility or FAIR alignment.
You can still:

- describe access conditions
- share code without data
- provide synthetic examples
- document the full workflow

Silence is the only irreproducible option.


### Reuse is where most harm (and benefit) happens

Most problems arise *after* publication, when:

- models are reused on new surveys
- catalogues are taken as ground truth
- assumptions are forgotten

You cannot control all reuse.

You can influence it by:

- writing clear limitations
- choosing careful language
- making uncertainty visible

This protects both downstream users and your future self.

:::: challenge

## One concrete improvement

Think about your current or next project.

Identify one thing you could improve:

- a clearer scope statement
- a fixed random seed
- a short README
- a note on reuse limitations

Write it down.
Do not optimise it.
Just commit to doing that one thing.

::::

### A sustainable mindset

Good practice accumulates.

Most reproducible and ethical ML workflows were not built all at once.

They evolved because:

- small habits stuck
- mistakes were documented
- clarity was rewarded

Progress is incremental.

### Key takeaways

- Aim for a clear minimum standard, not perfection
- Document decisions that affect results
- Make scope and limitations explicit
- Small improvements compound over time

Remember: **Good (ML) practice is not about doing everything right. It is about making fewer things mysterious.**
``
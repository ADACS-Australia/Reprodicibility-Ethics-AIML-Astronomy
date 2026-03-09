---
title: "Ethics of ML & AI in astronomy research"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---


# Ethics of ML & AI in astronomy research

### Focus: research ethics (not general AI ethics)

Key ethical dimensions relevant to astronomy ML:
- **Bias**
  - Training data ≠ the universe
  - Selection effects baked into models
- **Opacity**
  - Complex models used without interpretability
- **Automation bias**
  - Over‑trusting classifications or flags
- **Scope creep**
  - Models reused outside intended domain

:::: challenge
## Case study (discussion-based)

**Scenario (adaptable):**
- A classifier trained on Survey A performs well.  
- Another group applies it to Survey B without retraining.  
- Results look plausible and are published.

Discussion prompts:
- What assumptions are being made?
- Who is responsible for validation?
- What should be disclosed in the paper?
::::

### TODO (lesson content)
- Add a second case involving simulated training data vs real observations


> Ethical ML failures in science are usually quiet — until someone tries to reuse your result.


## Ethics of ML and AI in astronomy research

Ethics in ML is often discussed in the context of social or human impacts.
In astronomy, ethical issues usually look quieter and more technical.
They show up as:

- overconfident claims
- silent misuse of models
- results applied beyond their valid scope
- downstream users trusting outputs more than they should

This section focuses on **research ethics in ML‑based astronomy**, not policy or regulation.


### Ethics in astronomy is mostly about scope and responsibility

Astronomy ML models are rarely deployed directly in high‑stakes decisions.
Instead, they are used to:

- classify objects
- generate catalogues
- estimate physical parameters
- prioritise follow‑up observations

The ethical risk is not immediate harm.
The risk is that **scientific conclusions become detached from their assumptions**.

In ML‑based research, ethical problems usually arise when:

- models are reused outside their intended domain
- limitations are undocumented or forgotten
- outputs are treated as ground truth

Good news: **Most ethical failures in astronomy ML are failures of scope, not intent.**


### Automation bias in scientific workflows

Automation bias is the tendency to over‑trust automated outputs, even when they are wrong.
In astronomy, this appears when:

- ML classifications are accepted without inspection
- catalogue flags are treated as definitive
- human judgement is quietly removed from the loop

This is especially common when:

- datasets are too large for manual checking
- models perform well *on average*
- uncertainty is not visible in outputs

Automation bias does not require negligence.
It emerges naturally when tools scale faster than scrutiny.

### Example: When a model outlives its context

A common pattern in astronomy ML is:

- a model is trained for a specific survey
- it performs well and is published
- it is reused years later on a different dataset

If the original paper does not clearly state:

- training data assumptions
- preprocessing steps
- intended domain of validity

then reuse becomes guesswork.
This is an ethical issue because:

- downstream users are misled by omission
- incorrect results propagate silently
- responsibility becomes unclear

Remember: **"Silence about limitations is not neutral."**

:::: challenge

## Who is your model for?

Think about one ML model you have built or used.

Silently answer:

- What dataset was it trained on?
- What dataset was it validated on?
- Where would you hesitate to apply it?

Write down one boundary you would not cross.

No sharing required.

::::

### Over-claiming is an ethical failure

In ML‑based science, performance numbers are often used to justify scientific claims.
Problems arise when:

- predictive accuracy is treated as physical understanding
- benchmark improvements are interpreted as theoretical progress
- limitations are buried in appendices or not stated at all

Overclaiming does not require exaggeration.
It can occur simply by:

- failing to state uncertainty
- omitting evaluation caveats
- allowing readers to assume too much

In astronomy, this is particularly risky because ML outputs are often reused far beyond their original context.

### Transparency is an ethical safeguard

Ethical ML practice in astronomy is mostly about **making assumptions visible**.
This includes:

- documenting training data provenance
- stating what the model was designed to do
- stating what it was not tested on
- clarifying how outputs should be interpreted

This aligns closely with reproducibility and FAIR practices:

- ethics, reproducibility, and reuse reinforce each other
- none of them work in isolation

Best practice: **Transparency is the ethical minimum, not an optional extra.**

### Ethics without blame

It is important to be explicit about what this section is not saying.
Ethical issues in ML astronomy usually:

- are not caused by bad actors
- are not the result of incompetence
- arise from complex systems and incentives

Most problems emerge because:

- ML scales faster than documentation
- models are reused in good faith
- assumptions fade over time

Framing ethics as a systems issue, not a personal failure, is essential for changing practice.

:::: challenge

## One ethical improvement

Think of one small change you could make when reporting results that rely on ML/AI:

- a clearer limitations paragraph
- a model scope statement
- a warning in documentation
- an explicit “not tested on” list

Write it down.

That is enough.

::::

### Key takeaways

- Ethical issues in astronomy ML are usually about scope and reuse
- Automation bias can occur even with high‑performing models
- Overclaiming often happens through omission, not exaggeration
- Transparency is the most effective ethical safeguard

**Most ethical failures in ML astronomy happen when tools are trusted more than they are understood.**
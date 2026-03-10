---
title: "Why Reproducibility Matters"
teaching: 15 # teaching time in minutes
exercises: 10 # exercise time in minutes
---

## Motivation: Why should *you* care about reproducible research?

Most astronomers agree that reproducible research is “a good thing”.

Few astronomers change how they work because of it.

This lesson starts by being honest about *why* that is — and why, despite this, reproducible practices are often **worth it for you personally**, especially if you are a PhD student or early‑career researcher (ECR).

We will talk briefly about benefits to science, but we will focus mainly on **short‑term, selfish reasons** that tend to matter more day‑to‑day.


### Reproducibility is not (just) about being virtuous

You will often hear that reproducible research is important because it:

- improves trust in science
- allows others to verify your results
- makes research more reliable in the long term

All of this is true — but for many researchers, these benefits feel:

- distant
- abstract
- misaligned with immediate career pressures

Sarah Wild, in an [article for physics today](https://physicstoday.aip.org/news/irreproducible-astronomy) describes the concern many astronomers have around reproducibility and a potential erosion of trust in science.
One of the issues she points out is that our current publication systems are based on "paper and letter" based communication rather than being designed to include the publication of data, methodology as code, and results.

PhDs and ECRs are usually evaluated on:
- papers
- citations
- finishing projects on time
- surviving supervisor or project changes

So let’s reframe the question.

**What does reproducibility do for *you*, right now?**


### Selfish reason #1: Reproducibility saves *you* time

Many researchers first encounter reproducibility as a burden.

In practice, the opposite is often true.

Reproducible *workflows* make it easier to:

- pause and restart work after months away
- recover from broken laptops or lost files
- return to a project after a supervisor, postdoc, or collaborator leaves
- debug your own results

Additionally, a reproducible workflow is easier to incorporate different/new data or new analysis techniques than a non-reproducible workflow.
This means that any future projects which have some commonality with your previous projects, will have a head-start and lower barrier for entry.

For PhD students in particular, this matters because:

- projects routinely span multiple years
- interruptions are common (teaching, observing, writing, life)
- memory is unreliable, documentation is not
- future projects will likely build on your thesis work

A recurring finding in studies of early‑career researchers is that reproducible practices **reduce re‑work and dead ends**, even when they add a small amount of effort up front.

Remember: *You are the first and most frequent reuser of your own code.*

:::: challenge

## Reflection

Have you ever failed to reproduce *your own* result after a few months?

::::


:::: instructor

This is about normalising failure, not blaming individuals.

::::



### Selfish reason #2: Reproducible work is easier to defend

ML and data‑driven results are increasingly scrutinised *after* publication.
When your work is questioned, reproducibility acts as protection.
If you can point to:

- versioned code
- documented data splits
- clearly stated assumptions and limitations

then criticism becomes:

- technical, not personal
- something you can respond to, not panic about

For PhDs and ECRs, this matters because:

- you often have less institutional protection
- you are more exposed to reviewer and community criticism
- you may no longer be around when questions arise

Result: **Reproducibility shifts risk from "who did this?" to "what does the evidence show?"**


### Selfish reason #3: Reproducible work is cited more

This is one of the few incentives with **quantitative evidence**.

[Colavisa et al. 2004](https://doi.org/10.1371/journal.pone.0315776) found that:

- the early release of a publication as a preprint correlates with a significant positive citation advantage of about 20.2%,
- sharing data in an online repository correlates with a smaller yet still positive citation advantage of 4.3%.

They did not see a significant citation advantage for papers which shared *code*, but note that "Further research is needed on additional or alternative measures of impact beyond citations".

This effect has been shown even when controlling for:

- journal impact
- field differences
- publication year

The takeaway is not "do this to game citations", but:  **Visibility and reuse tend to follow clarity and accessibility.**

It is already normal practice within astronomy to post pre-prints to the [arXiv](https://arxiv.org/), and these finding should give us confidence that this is a good practice that should be continued.

In a study by [Allen et al. 2018](https://physicstoday.aip.org/news/irreproducible-astronomy), papers from 2015 were scanned for citations and links to code.
Of the 285 unique codes that were used, 58% offered source code for download - not a great success rate.
However 90% of the hyperlinks to code were found to be still working at the time of the study (three years post publication).
The lead author, Alice Allen, oversees the [Astrophysics Source Code Library](https://ascl.net/) which you can think of as "an arXiv for code", and provides a doi and permalink for people to cite code.

### What happens when reproducibility is missing?

Reproducibility failures are rarely dramatic at first.
More often, they look like:

- results that "can't quite be repeated"
- models that work once but never again
- performance that disappears when reused elsewhere

In astronomy and ML‑based science, documented failure modes include:

- random samples that cannot be regenerated
- machine‑learning models that rely on subtle data leakage
- results that vanish when preprocessing is done correctly

In many published cases:

- no fraud was involved
- no one acted in bad faith
- the problem was simply undocumented decisions

For ECRs, the risk is asymmetric:

- the cost of failure is personal and immediate
- the benefit of cutting corners is often short‑lived


### Reproducibility as career insurance

It is reasonable to think of reproducibility as a form of insurance.
You invest a small amount of effort:

- documenting choices
- fixing randomness
- structuring workflows

In return, you reduce the chance of:

- losing months of work
- being unable to answer basic questions about your own results
- inheriting an unfixable mess (or becoming one)

**Reproducibility is insurance you pay for up front — instead of with stress later.**

:::: challenge

## Take one minute to think (no sharing required):

- What is one thing in your current workflow that only *you* understand?
- How confident are you that you could rerun your main result in a year?

::::


Take-away: *"Reproducible research is not about being perfect, it's about making your future life easier."*
---
title: "Wrap‑up and next steps"
teaching: 15 # teaching time in minutes
exercises: 5 # exercise time in minutes
---

## One‑page checklist: Reproducible, FAIR, and ethical ML in astronomy

Use this as a quick self‑check for your next ML project.
You do not need to tick every box to start.
Ticking a few is already progress.


### 1. Reproducibility (can someone rerun this?)

- [ ] I can rerun my own main result today
- [ ] Code is versioned (e.g. Git, tagged release)
- [ ] Randomness is fixed or recorded (seeds noted)
- [ ] Train / validation / test splits are explicit
- [ ] Preprocessing steps are documented
- [ ] Software environment is described (versions or environment file)

Minimum goal: someone else could rerun this without guessing.


### 2. Data provenance (where did this come from?)

- [ ] Data source is stated (archive, survey, release)
- [ ] Selection criteria are described
- [ ] Any filtering or exclusions are documented
- [ ] Derived features are explained
- [ ] Labels or annotations are described

Minimum goal: a reader understands what data went in, and why.


### 3. FAIR practices (is this reusable?)

Findable

- [ ] Outputs are named clearly
- [ ] A README explains what is in the repository

Accessible

- [ ] Access conditions are stated (open, restricted, embargoed)
- [ ] Instructions for access are included if needed

Interoperable

- [ ] Standard formats are used where possible
- [ ] Units and conventions are stated

Reusable

- [ ] A short description of intended use is included
- [ ] Limitations are stated explicitly

Minimum goal: reuse does not require emailing you.


### 4. Models and outputs (what exactly is being shared?)

- [ ] Training data are described
- [ ] Preprocessing assumptions are stated
- [ ] Intended scope of the model is documented
- [ ] Known failure modes are listed
- [ ] Outputs include uncertainty where relevant

Minimum goal: users know what the model was built for.


### 5. Ethical safeguards (are assumptions visible?)

- [ ] Model scope is stated clearly
- [ ] "Not tested on" cases are listed
- [ ] Performance claims are not overgeneralised
- [ ] Automation is not treated as ground truth
- [ ] Language avoids implied universality

Minimum goal: downstream users are not misled by omission.


### 6. The five‑minute test

If you stopped working on this today:

- [ ] Could you explain the project in one page?
- [ ] Could someone rerun the main figure?
- [ ] Would limitations still be obvious?

If not, write one sentence to fix that.


### Remember

- Clarity beats completeness
- Partial reproducibility beats silence
- Small improvements compound

You are not aiming for perfect practice.  
You are aiming for fewer mysteries.

## Wrap‑up and next steps

This workshop has focused on a simple idea:

Machine learning does not change what good astronomy looks like.  
It changes how easy it is to lose track of assumptions.

Across the lessons, we have seen that:

- reproducibility is a practical skill, not a moral stance
- FAIR practices extend beyond raw data to models and workflows
- ethical issues in astronomy ML are usually about scope and reuse
- small, explicit choices prevent large downstream problems

None of these require perfect code or ideal infrastructure.
They require clarity.


### What you should take away

If you remember only a few things:

- You are the primary user of your own ML work
- Performance numbers are not self‑explanatory
- Models outlive their context unless you stop them
- Silence about limitations is never neutral

Good practice is mostly about writing things down.


### What to do next

After this workshop, consider doing just one of the following:

- Add a README to an existing project
- Write a scope and limitations paragraph for a paper
- Fix and record random seeds
- Document a preprocessing step you currently do implicitly
- Add a "not tested on" note to a model description

Choose one thing. Do it once. Let it stick.



### How this fits into your career

For PhD students and ECRs especially:

- reproducible work is easier to defend
- clear documentation saves time
- careful scope statements protect you from overclaiming
- FAIR practices increase the lifespan of your work

These benefits show up quickly.


:::: challenge

## Final reflection (optional)

Take one minute and think about:

- One assumption in your current work that could be made explicit
- One future reader you could help with a single sentence

That is enough for today.

::::

Final Thought: **Reproducible and ethical ML is not about doing more work. It is about making your work easier to trust and reuse.**
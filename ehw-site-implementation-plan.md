# Evolvable Hardware Website — Implementation Plan

## Context

This plan is for updating the MkDocs site at `https://evolvablehardware.github.io/`. The source repo is likely at `https://github.com/evolvablehardware/evolvablehardware.github.io` (confirm with the user before cloning).

The site uses MkDocs (Material theme based on the nav structure and styling). All content is in Markdown. Changes should preserve existing content and add to it — don't delete anything unless the user explicitly approves.

A thorough review was conducted from three audience perspectives (Tinkerer, Undergraduate Student, Graduate Researcher/Professional) and produced cross-cutting recommendations. This plan implements those recommendations in prioritized phases.

**IMPORTANT: Prompt the user for review and approval at the end of each phase before proceeding to the next.**

---

## Phase 0: Setup & Reconnaissance

### Steps
1. Ask the user for the correct GitHub repo URL and clone it
2. Identify the MkDocs config file (`mkdocs.yml`) and understand the site structure
3. List all existing markdown content files and their locations
4. Identify the nav structure in `mkdocs.yml`
5. Present a summary of the file tree and nav to the user for confirmation before making any changes

### Checkpoint → Ask user:
- "Here's the repo structure I found. Does this look correct?"
- "Are there any pages currently in draft/WIP that I should avoid touching?"
- "Should I create a working branch (e.g., `site-improvements`) or work on `main`?"

---

## Phase 1: Restructure the "Where Should I Start?" Pathways (Homepage)

This is the highest-impact change — it's the first thing every visitor sees.

### File to edit
The homepage markdown file (likely `docs/index.md` or similar).

### Changes to the Tinkerer tab

**Current:**
1. Watch the Intro Video
2. Read about Core Concepts
3. Review example experiments
4. Review Software/Hardware Tools
5. Get involved: Contact Us

**New version:**
1. Watch the [Intro Video](about/#watch-the-summary-video)
2. Read the essentials: [Evolutionary Computation](research/concepts/evolutionary_computation/), [Reconfigurable Hardware (FPGAs)](research/concepts/reconfigurable_hardware/), and [Approximate Computing](research/concepts/approximate_computing/) — *You don't need all 11 concept pages to get started. These three are enough to jump in.*
3. Check the [parts list and estimated costs](#) *(link to new BOM section — see Phase 2)*
4. Run your first evolution: [Variance Maximization](research/experiments/variance_maximization/) — *This is the simplest experiment. Expect ~X minutes from setup to seeing your first evolved output.*
5. Explore [more experiments](research/experiments/) and the [Software/Hardware Tools](tools/)
6. Join the community: [GitHub Discussions](#) / [Contact Us](contact/) *(update link target once community channel is confirmed)*

### Changes to the Undergraduate Student tab

**Current:**
1. Watch the Intro Video
2. Read about Core Concepts
3. Read about the History of Evolvable Hardware
4. Read Recent Papers
5. Get involved: Contact Us

**New version:**
1. Watch the [Intro Video](about/#watch-the-summary-video)
2. Read about [Core Concepts](research/) — *start with [Evolutionary Computation](research/concepts/evolutionary_computation/) and [Reconfigurable Hardware](research/concepts/reconfigurable_hardware/)*
3. See research in action: [Example Experiments](research/experiments/) — *These show what research questions look like in this field*
4. Read about the [History of Evolvable Hardware](history/)
5. Read the papers — *Start with ["Resurrecting FPGA Intrinsic Analog Evolvable Hardware" (2021)](research/publications/papers/2021/7_19_Resurrect-FPGA-EHW/) for the story of how this project began, then explore [more recent work](research/publications/)*. For deeper background, see our [recommended books](research/publications/books/).
6. Get involved: See [how students can contribute](#) *(link to new section — see Phase 3)* or [Contact Us](contact/)

### Changes to the Graduate Researcher / Professional tab

**Current:**
1. Watch the Intro Video
2. Read about the History of Evolvable Hardware
3. Read Recent Papers
4. Read about Future Research Directions
5. Get involved: Contact Us

**New version:**
1. *Already familiar with evolvable hardware?* Skip to the [Historical Review](history/historical_review/) for a research-oriented overview. *New to the field?* Watch the [Intro Video](about/#watch-the-summary-video).
2. Read about the [History of Evolvable Hardware](history/)
3. Read [Recent Papers](research/publications/) and [recommended books](research/publications/books/)
4. Read about [Future Research Directions](research/future_directions/) — *includes scoped open questions for potential research projects*
5. Explore collaboration opportunities: [iCEFARM remote access](#), [contributing experiments](#), or [Contact Us](contact/) *(links to be updated in Phase 4)*

### Implementation notes
- Preserve the existing MkDocs tab syntax (likely `=== "Tinkerers"` etc. in Material theme)
- Keep numbered list format but use the richer descriptions above
- Italicized notes are guidance text — render them as `*italic*` in markdown
- Some links point to content that doesn't exist yet (marked with `#`) — those will be created in later phases. Use placeholder anchors for now and leave a `<!-- TODO: update link -->` comment

### Checkpoint → Ask user:
- "Here are the updated pathway tabs. Review the wording and link targets."
- "For the Tinkerer pathway, what's a realistic time estimate for the Variance Maximization experiment from setup to first result? I used a placeholder."
- "What community channel should I link to — GitHub Discussions, Discord, or something else?"

---

## Phase 2: Add Practical Entry-Point Content for Tinkerers

### 2A: Bill of Materials / Cost Summary

**Create a new section** (either as a standalone page or as a prominent section within each project's page). Location suggestion: `docs/projects/getting_started.md` or a new "Quick Start" page.

Content to include:
- **iCEstick path**: iCEstick Evaluation Kit (~$XX), Arduino Nano (~$XX), breadboard, jumper wires, USB cables. Approximate total: ~$XX
- **pico2-ice path**: pico2-ice board (~$XX), plus any additional components. Approximate total: ~$XX
- Links to where to purchase each item
- A note on what tools/software are free (Project IceStorm, Python, etc.)

**Ask the user** for current pricing and preferred vendor links.

### 2B: "Your First Evolution" Quick-Start Callout

On the Variance Maximization experiment page (`docs/research/experiments/variance_maximization/`), add a callout/admonition at the top:

```markdown
!!! tip "Start Here: Your First Evolution"
    This is the simplest evolvable hardware experiment — a great first project for newcomers.
    You'll evolve a circuit that maximizes output signal variance.
    **Time estimate:** ~X minutes from powered hardware to first evolved result.
    **Prerequisites:** Completed [hardware setup](../../projects/bitstream_evolution/hardware_setup/) and [software setup](../../projects/bitstream_evolution/software_setup/).
```

### 2C: Experiment Difficulty Ordering

On the experiments index page (`docs/research/experiments/index.md` or equivalent), add difficulty indicators:

| Experiment | Difficulty |
|---|---|
| Variance Maximization | 🟢 Beginner — start here |
| Pulse Oscillation | 🟢 Beginner |
| Tone Discriminator | 🟡 Intermediate |
| Target Frequency Sweep | 🟡 Intermediate |
| Transferability | 🔴 Advanced |
| Fitness Sensitivity | 🔴 Advanced |

**Ask the user** to confirm/adjust difficulty ratings.

### Checkpoint → Ask user:
- "Here's the draft BOM page. Can you fill in current prices and vendor links?"
- "Are these difficulty ratings for the experiments approximately right?"
- "What's the right time estimate for the Variance Maximization quick start?"
- "Would you like me to add a photo/diagram placeholder for the hardware setup? (You'd supply the image later)"

---

## Phase 3: Add Scaffolding Content for Undergraduates

### 3A: Prerequisites Sidebar

Add a "What You Should Know" admonition to the Research Concepts index page (`docs/research/index.md` or `docs/research/concepts/index.md`):

```markdown
!!! info "Prerequisites"
    Most content on this site is accessible if you have:

    - **Basic programming** (Python — used by BitstreamEvolution)
    - **Intro to digital logic** (logic gates, flip-flops, basic FPGA awareness)
    - **Familiarity with Linux command line** (navigating directories, running scripts)

    Some advanced concept pages (marked 🔴) assume background in dynamical systems, control theory, or neuroscience.
```

### 3B: Concept Page Grouping and Difficulty Tags

On the Research Concepts index page, reorganize the 11 concept links into grouped categories:

**Foundations** (start here)
- 🟢 [Evolutionary Computation](concepts/evolutionary_computation/)
- 🟢 [Reconfigurable Hardware (FPGAs)](concepts/reconfigurable_hardware/)

**Inspirations**
- 🟡 [Biologically Inspired Computing](concepts/bio_inspired_computing/)
- 🟡 [Embodied Intelligence](concepts/embodied_intelligence/)
- 🟡 [Neuromorphic Hardware](concepts/neuromorphic_hardware/)
- 🟡 [Approximate Computing](concepts/approximate_computing/)

**Advanced Topics**
- 🔴 [Continuous-Time Recurrent Neural Networks](concepts/ctrnns/)
- 🔴 [Dynamical Neural Networks](concepts/dynamic_neural_networks/)
- 🔴 [Dynamical Systems](concepts/dynamical_systems/)
- 🔴 [Liquid Time-Constant Networks (LTCs)](concepts/ltc_nns/)
- 🔴 [Mortal Computation](concepts/mortal_computation/)

**Ask the user** to confirm the grouping and difficulty assignments.

### 3C: Student Contribution Guide

Create a new page or section: `docs/community/students.md` (or add to an existing page).

Draft content:

```markdown
# Contributing as a Student

## Course Projects
Evolvable hardware experiments make excellent independent study or capstone projects.
Past student contributions have included:
- [Ask user to list examples]

## How to Get Started
1. Review the [projects](../projects/) and pick a hardware platform
2. Replicate an existing [experiment](../research/experiments/) and document your results
3. Propose a variation or new fitness function
4. Submit your work as a pull request to the [BitstreamEvolution repo](https://github.com/evolvablehardware/BitstreamEvolution)

## Mentorship
Interested in a guided research experience? [Contact us](../contact/) with your background and interests.
```

**Ask the user** to provide examples of past student projects and any specific opportunities they want to advertise.

### Checkpoint → Ask user:
- "Review the concept groupings — are these categories and difficulty levels right?"
- "Can you provide 2-3 examples of past student projects for the contribution guide?"
- "Should the student page live under a new 'Community' nav section, or somewhere else?"

---

## Phase 4: Strengthen the Graduate Researcher / Professional Experience

### 4A: Recommended Reading / Related Work Section

Add to the Publications page (`docs/research/publications/index.md`) or create a new `docs/research/publications/related_work.md`:

```markdown
# Related Work & Further Reading

The following external publications provide important context for evolvable hardware research:

**Foundational**
- Thompson, A. (1997). "An evolved circuit, intrinsic in silicon, entwined with physics." *Proc. 1st Int. Conf. on Evolvable Systems (ICES)*
- Thompson, A. (1998). *Hardware Evolution: Automatic Design of Electronic Circuits in Reconfigurable Hardware by Artificial Evolution.* Springer.

**Surveys & Challenges**
- Haddow, P.C. & Tyrrell, A.M. (2011). "Challenges of evolvable hardware: past, present and the path to a promising future." *Genetic Programming and Evolvable Machines.*
- Torresen, J. (various) — survey papers on scalability in evolvable hardware

**Space & Fault Tolerance Applications**
- Stoica, A. et al. (JPL/NASA) — FPTA and radiation-tolerant evolvable hardware
- ESA RHinO project — reconfigurable hardware in orbit

**Cartesian Genetic Programming for Hardware**
- Sekanina, L. — CGP-based approaches to evolvable digital circuits

<!-- TODO: Ask user to confirm/expand this list with full citations and links -->
```

### 4B: Cite This Work Section

Add to the publications page or as a standalone snippet:

```markdown
## Citing This Work

If you use BitstreamEvolution or reference this project, please cite:

\`\`\`bibtex
@inproceedings{bitstream-evolution-2025,
  title={Bitstream Evolution: an Open-Source FPGA Intrinsic Evolvable Hardware Toolkit},
  author={[authors]},
  year={2025},
  <!-- TODO: complete citation from user -->
}
\`\`\`
```

**Ask the user** for the correct BibTeX entries.

### 4C: Collaboration / iCEFARM Page

Create `docs/community/collaborate.md` or expand the existing iCEFARM section:

```markdown
# Collaborate With Us

## Remote Access via iCEFARM
[Description of the iCEFARM infrastructure — what it is, how to request access]

## Contributing Experiments
We welcome new experiments from external researchers. To contribute:
1. Fork the [BitstreamEvolution repository](https://github.com/evolvablehardware/BitstreamEvolution)
2. Implement your experiment following the existing patterns
3. Document your setup, fitness function, and results
4. Submit a pull request

## Data Sharing
[Description of any shared datasets, evolved bitstream repositories, or benchmark results]

## Proposing Joint Research
For formal collaboration inquiries, [contact us](../contact/) with:
- Your research group and institution
- Proposed research direction
- Desired timeline and resources
```

**Ask the user** for details on iCEFARM access, data sharing policies, and what collaboration looks like in practice.

### Checkpoint → Ask user:
- "Review the related work list — should I add or remove any citations? Can you provide complete references?"
- "Please provide the correct BibTeX entry/entries for the project."
- "What details should go in the iCEFARM / collaboration section? Is remote access currently available?"
- "Is there benchmark data (evolution times, generations to converge, etc.) you'd like to surface? If so, where should it live?"

---

## Phase 5: Cross-Cutting Improvements

### 5A: Glossary Page

Create `docs/glossary.md`:

Include definitions for key terms that appear repeatedly across the site. Draft terms:

- **Bitstream** — The binary configuration file that programs an FPGA's logic cells and routing
- **Intrinsic evolution** — Evolution performed directly on physical hardware, exploiting real device characteristics
- **Extrinsic evolution** — Evolution performed in simulation, with results optionally transferred to hardware
- **Fitness function** — The objective function that evaluates how well a candidate circuit meets the design goal
- **FPGA (Field Programmable Gate Array)** — A reconfigurable integrated circuit whose logic can be reprogrammed after manufacturing
- **Genetic algorithm** — An optimization method inspired by natural selection that evolves a population of candidate solutions
- **LUT (Look-Up Table)** — The basic programmable logic element inside an FPGA
- **Phenotype / Genotype** — In EHW context: genotype is the bitstream; phenotype is the resulting circuit behavior
- **Reconfiguration** — The process of loading a new bitstream onto an FPGA to change its function

**Ask the user** to review, correct, and expand this list.

### 5B: Add Glossary and Community Pages to Navigation

Update `mkdocs.yml` to add new pages to the nav. Proposed structure:

```yaml
nav:
  - Home: index.md
  - About: about.md
  - History:
    - ...
  - Research:
    - ...
  - Projects:
    - Getting Started: projects/getting_started.md    # NEW
    - ...
  - Tools:
    - ...
  - Community:                                         # NEW section
    - For Students: community/students.md
    - Collaborate: community/collaborate.md
  - Glossary: glossary.md                              # NEW
  - Blog:
    - ...
  - Contact: contact.md
```

### 5C: Update "Contact Us" CTAs to Be Audience-Specific

In the homepage pathway tabs, the final step for each audience should use distinct language:

- **Tinkerers:** "Join the community → [GitHub Discussions / Discord / etc.] or [Contact Us]"
- **Students:** "See how students can contribute → [Student Guide] or [Contact Us]"
- **Researchers:** "Explore collaboration → [Collaborate page] or [Contact Us]"

(This should already be partially done in Phase 1, but verify the links now point to the pages created in Phases 3–4.)

### Checkpoint → Ask user:
- "Review the glossary draft — any terms to add, remove, or redefine?"
- "Does this nav structure work? Should 'Community' be a top-level section or nested under something else?"
- "Final review: I'll now do a link-check pass across all modified files. Any other changes before I commit?"

---

## Phase 6: Final QA & Cleanup

### Steps
1. Run a local MkDocs build (`mkdocs build --strict`) to catch broken links and warnings
2. Fix any broken internal links, especially the placeholder `#` links from Phase 1
3. Verify all new pages render correctly
4. Check that the nav in `mkdocs.yml` reflects all new and moved pages
5. Review all `<!-- TODO -->` comments and either resolve them or flag them for the user
6. Commit with a clear message summarizing all changes
7. Present a summary diff to the user

### Checkpoint → Ask user:
- "Here's a summary of all changes made. Ready to merge/deploy?"
- "Are there any remaining TODOs you'd like me to address before pushing?"

---

## Summary of New Files to Create

| File | Description | Phase |
|---|---|---|
| `docs/projects/getting_started.md` | BOM, costs, quick-start guide | 2 |
| `docs/community/students.md` | Student contribution guide | 3 |
| `docs/community/collaborate.md` | Collaboration & iCEFARM info | 4 |
| `docs/research/publications/related_work.md` | External references & further reading | 4 |
| `docs/glossary.md` | Key term definitions | 5 |

## Summary of Files to Modify

| File | Changes | Phase |
|---|---|---|
| Homepage (`docs/index.md`) | Rewrite all three pathway tabs | 1 |
| Experiments index | Add difficulty indicators and "start here" callout | 2 |
| Variance Maximization page | Add beginner callout admonition | 2 |
| Research Concepts index | Regroup into Foundations/Inspirations/Advanced | 3 |
| Publications index | Add related work link, cite-this-work section | 4 |
| `mkdocs.yml` | Add new pages to nav | 5 |

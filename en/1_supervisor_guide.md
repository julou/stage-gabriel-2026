# High School Internship — Quantitative Microbiology
## Supervisor Guide — Internal Use

---

## Overview

**Intern**: high school student, end of 10th grade (French lycée, elite Parisian school, math-physics-science track), ≈15 years old.  
Some self-taught Python (loops, lists, import). No numpy/matplotlib.  
Math background: discrete probability OK; logarithm and exponential not yet covered.

**Duration**: 2 weeks, 9 working days (Monday W1 → Thursday W2).  
Approximately 4–6 computational half-days scheduled during experimental downtime.

**Lab**: Quantitative microbiology, Basel.

**Learning objectives**
1. Understand the microscopic origin of exponential growth and saturation.
2. Understand that a gene can be regulated quantitatively, and measure this control.
3. Produce figures from real lab data — by writing the code oneself.

---

## Documents produced

| File | Purpose | Recipient |
|---|---|---|
| `supervisor_guide.md` | This document — context, protocols, checklist | Thomas |
| `intern_guide.md` | Welcome, simplified schedule, resources | Intern (+ parents) |
| `experimental_plan_supervisor.md` | Protocols D1–D9, plate layouts, concentration ranges | Thomas |
| `notebook_growth_complete.ipynb` | **Notebook A** — §A1–§A4 (deterministic, stochastic, Monod, diauxie) | Reference / answer key |
| `notebook_growth_intern.ipynb` | Notebook A — intern version | Intern |
| `notebook_induction_complete.ipynb` | **Notebook B** — §B1–§B3 (stochastic switch, Hill, plate reader data) | Reference / answer key |
| `notebook_induction_intern.ipynb` | Notebook B — intern version | Intern |
| `notebook_heterogeneity_complete.ipynb` | **Notebook C** [OPTIONAL] — §C1 bistability, §C2 ImageJ | Reference / answer key |
| `notebook_heterogeneity_intern.ipynb` | Notebook C — intern version | Intern |

The *intern* notebooks are the working material for the intern.  
The *complete* notebooks serve as the answer key and can be shared at the end of the internship.

---

## Day-by-day schedule

> Column **Experimental**: AM / PM detail.  
> Column **Programming**: notebook section and key content. Timing is flexible based on progress.

| Day | Experimental AM | Experimental PM | Programming |
|---|---|---|---|
| **Mon W1** | Introduction: lab tour, safety rules. Pipetting: 10-fold serial dilutions over 6 orders of magnitude, verification on spectrophotometer. Inoculation of 6 LB tubes ±sterile (contamination check the next morning). | Inoculation of LB + glucose 0.2% tubes for manual growth curve starting **Tue morning**. | Colab (or VS Code) setup. Notebook A §A1: repeated multiplication, linear plot, log scale, graphical doubling time. |
| **Tue W1** | OD600 readings every 30 min from ~9:30 to ~16:00 (min. 6 measurements: 2×1h, then 4×30 min, then every 20 min). LB + glucose at 3 concentrations. Contamination check on Monday tubes. | OD readings continued. Prepare inoculum for plate reader (Wednesday morning). | Notebook A §A2: `simulate_one`, 1 trajectory. 30 trajectories, mean, variance. During 20 min breaks. |
| **Wed W1** | Plate reader inoculation: glucose ×3 (0.02% / 0.2% / 0.4%) × 2 replicates + lactose ×2 (0.2% / 0.4%) × 2 replicates + glu+lac ×2 × 2 replicates + blanks → **diauxie overnight**. | Launch plate reader, verify readings. | Notebook A §A3: Monod, p(S) curve, `simulate_nutrients`. Verify N_max ∝ [glucose] with Tue W1 data. |
| **Thu W1** | Read diauxie data (stop in the morning). Discussion with Thomas: what does diauxie tell us about *lacZ* regulation? **TSS transformation** pUA66-lacUV5 → MG1655: prepare competent cells (AM), transformation + 1h recovery + plating at end of morning on LB + Kan50. | | Notebook A §A3 end: `simulate_nutrients` with varied parameters. §A4 start: import diauxie plate reader data, visualisation. |
| **Fri W1** | Check transformation colonies. If OK (>10 colonies, clean background): pick 2–3 colonies → LB + Kan50 overnight for glycerol stock + preculture. If failed: redo or use existing glycerol stock. | End of day: observe colonies under low-magnification microscope (optional, educational). | Notebook A §A4: Monod model vs data comparison. |
| **Sat–Sun W2** | *(Thomas)* Sunday evening: inoculate 3 mL M9 0.2% arabinose + Kan50 from Plac-GFP glycerol stock **and** pUA66-lacUV5/MG1655 colony/glycerol. Overnight 37°C. | — | — |
| **Mon W2** | Prepare induction plate and launch plate reader (≥6h kinetics). | Launch plate reader induction: Plac-GFP vs pUA66-lacUV5/MG1655 × IPTG (6 conc.) × TMG (6 conc.) × 2 replicates. | Notebook B §B1 start. |
| **Tue W2** | Read plate reader in the morning. Data evaluation: clean curves? yes → **microscopy PM** (agar pads, 2 strains, 4 [TMG]). no → redo + analysis. | If microscopy PM: prepare agar pads, mount samples, acquire phase + fluorescence. | §B1 end. §B2: Hill n=1 vs n=2. If redo: §B3 start (import plate reader data). |
| **Wed W2** | If microscopy already done → **ImageJ** (cell segmentation, Mean measurement, CSV export). If not yet → microscopy session. | ImageJ continued / data check. | §B3: RFU/OD normalisation, dose-response curves, graphical K_half fit. Overlay Hill curve. |
| **Thu W2** | Finalise measurements / ImageJ if needed. | **2-page report (3 figures)**: key figures from both notebooks + interpretation. Discussion with Thomas. | Notebook C §C1–§C2 [OPTIONAL] if time: bistability, single-cell histograms. |

---

## Narrative arc

The 9-day progression builds thematic coherence:

**Week 1 — How a population grows**  
Tuesday: manual growth curve (foundational experiment, direct contact with data).  
Wednesday: plate reader for diauxie — a simple signal hides gene regulation.  
Thursday: transformation → the intern introduces a new gene into a bacterium themselves.

**Week 2 — How a gene is regulated**  
Monday: quantitative measurement of induction (plate reader, two promoters).  
Tuesday–Wednesday: comparison to prediction (Hill curve) and single-cell visualisation.  
Thursday: presentation — linking the two weeks: the exponential growth simulated in Week 1 is the same process that dilutes GFP between generations in the induction experiment.

**Computational thread**: the same reasoning (microscopic rule → population behaviour) links Notebook A (τ-leaping) to Notebook B (stochastic switch §B1).

---

## Pre-internship checklist — Thomas's actions

### Biology (to complete before D1)

- [ ] **Preliminary IPTG curve for lacUV5-GFP**: after cloning and transformation, verify that the dose-response curve is hyperbolic (n ≈ 1, expected from the sequence). Calibrate the range: if K_half differs greatly from 15–30 µM, adjust the 6 concentrations in the experimental plan.
- [ ] **Plac-GFP/MG1655 glycerol stock**: verify availability of a functional stock. Growth + fluorescence OK with IPTG.
- [ ] **pUA66-lacUV5 transformed**: sequence verified and ordered (Eurofins Express GeneStrands, 274 bp). Upon receipt: clone into pUA66 via XhoI/BamHI, transform into MG1655, pick colony, verify fluorescence + preliminary IPTG curve (confirm n ≈ 1). Have a validated glycerol stock before D1 of the internship.
- [ ] **IPTG and TMG 10 mM stocks**: prepare in ultrapure water, filter through 0.22 µm, aliquot 500 µL, store at −20°C. See *Appendix 2* in `experimental_plan_supervisor.md`.
- [ ] **LB + Kan50 plates**: prepare 4–6 fresh plates for Thu W1 (transformation) + Fri W1 (verification).
- [ ] **BioTek plate reader**: verify availability for Wed W1 evening (diauxie overnight) **and** Mon W2 PM (induction). These two slots cannot be moved.
- [ ] **Fluorescence microscope**: verify availability for Tue W2 PM or Wed W2. GFP filters (excitation 470 nm, emission 525 nm). Plan for 60× or 100× oil objective.

### Computing (to complete before D1)

- [ ] **Test Colab** on the lab computer: create a notebook, import numpy + matplotlib, plot a simple graph.
- [ ] **Upload intern notebooks** to a Google Drive accessible from the lab.
- [ ] **Check intern has access** to a Google account (for Colab) or arrange guest access.

### Sunday W2 (mandatory)

- [ ] Inoculate Plac-GFP/MG1655: 1 colony or 5 µL glycerol → 3 mL M9 0.2% arabinose + Kan50, overnight 37°C.
- [ ] Inoculate pUA66-lacUV5/MG1655: same, from Fri W1 colony (or glycerol stock).

---

## Key biological notes

### lacUV5 construct (pUA66)

**Sequence verified and ordered from Eurofins Express GeneStrands (274 bp total).**

249 bp insert between XhoI and BamHI, with flanking buffers validated for efficient digestion.

#### Architecture of the *lac* operon

The native Plac promoter has three operators: **O1** (central region, strong),
**O3** (−82 bp upstream, moderate) and **O2** (+412 bp downstream, weak).
LacI can bind simultaneously to O1 and O3, forming a **DNA loop** of 92 bp
that cooperatively reinforces repression → sigmoidal response (n ≈ 2).
The native −10 region (TATGTT) is suboptimal and dependent on the CRP/cAMP factor —
hence the absence of expression on glucose (catabolite repression).

#### Biological consequences of the lacUV5 construct

- **O1** intact → sole functional operator → no DNA loop → n ≈ 1
- **O3** absent from the fragment (−82, outside the −60/+25 fragment) and scrambled in our construct
- **O2** absent (+412, outside the fragment)
- **lacUV5 mutations** in the −10 (TATGTT → TATAAT): strong promoter, independent of CRP
  → constitutive expression independent of carbon source
- The difference in curve shape (n ≈ 1 vs n ≈ 2) between lacUV5-GFP and Plac-GFP is
  entirely attributable to **operator architecture**, all else being equal
  (same pUA66 backbone, same synthetic RBS, same MG1655 strain, same GFPmut2 fluorophore).

**To verify before the internship**: sequence verification done. It remains to confirm biologically that the IPTG dose-response curve is indeed hyperbolic after transformation into MG1655 (see checklist).

### IPTG vs TMG for the two experiments
- **IPTG**: enters by passive diffusion, clean graded response curve → use for plate reader (quantitative fit).
- **TMG**: transported by LacY → positive feedback → bistability at intermediate concentrations → bimodal distribution visible by microscopy. Use **TMG** for microscopy (Notebook C).

The same plate reader run can contain both inducers: columns 1–6 for IPTG, columns 7–12 for TMG. See layout in `experimental_plan_supervisor.md`.

### Zaslaver reporters
Reporters from the Zaslaver library (pUA66) use a strong synthetic RBS that overrides native translation signals — they are therefore pure transcriptional probes.

---

## Pedagogical notes

### On logarithms
The logarithm is not covered in 10th grade (taught in 12th grade). Notebooks avoid any formula containing `log`. The `plt.yscale('log')` display is presented as a *visual tool* (repeated multiplication becomes a straight line) without formal justification. `np.log` appears in the doubling time calculation but is explicitly flagged "to be covered in 12th grade — verify graphically."

### On stochasticity
Introduce with "coin flip for each cell" — that is the right intuition. The τ-leaping algorithm is presented as "we flip N coins" without naming the algorithm. Emphasise emergence: individual random rules → predictable population behaviour (law of large numbers).

### On the Hill curve
The key pedagogical point of §B2 is that n=2 emerges from p₁ × p₂ (independent probability multiplication rule, 10th-grade curriculum). Do not name "cooperativity" or "Hill" first — let the intern derive the formula, then give it the name.

### On bistability (Notebook C, optional)
The connection to §B1 (stochastic noise) is important: in §B1, variability comes from molecular randomness. In **§C1**, bimodality comes from a deterministic bifurcation (two stable states). These are two distinct mechanisms that produce similar distributions. Conceptually rich if time allows.

### For the final report / presentation (Thu W2)
Orient the presentation around two questions: (1) How does a simple cell produce exponential growth? (2) How does the cell decide whether to activate a gene based on its environment? Both notebooks answer these questions with real lab data.

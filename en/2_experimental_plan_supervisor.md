# Experimental Plan — High School Internship
## Protocols D1–D9 · Plate Layouts · Stock Solutions

> **Conventions**: `[TO CHECK]` = value to confirm by Thomas before the internship.
> Volumes in µL unless otherwise stated. All incubations at 37°C unless noted.

---

## D1 — Monday W1 · Introduction and pipetting

**Objective**: master basic techniques (pipetting, dilutions, aseptic technique) and inoculate first cultures.

### Materials
- Micropipettes P20, P200, P1000 + corresponding tips
- 1.5 mL Eppendorf tubes × 10
- 15 mL Falcon tubes × 3
- Sterile liquid LB
- Dye (0.1% bromophenol blue or Congo red in water — to visualise dilutions)
- 14 mL culture tubes × 6 (3 sterile, 3 non-sterile), caps
- *E. coli* MG1655 overnight preculture in LB (OD ~2–4)

### Morning — pipetting and dilutions

1. Pipette demonstration: volume adjustment, tip attachment, pipetting technique.
2. **Serial dilution exercise**: prepare 6 successive ×10 dilutions of the dye in water (1:10 → 1:10⁶) in 1.5 mL Eppendorf tubes. Final volume = 100 µL at each step.
   - Visual check: absorbance should decrease visibly.
   - [OPTIONAL] NanoDrop or spectrophotometer measurement to quantify.
3. Discussion: what is the concentration in tube #6 if tube #1 is at 1 mg/mL?

### Afternoon — inoculation of sterile vs non-sterile tubes

4. Prepare 6 × 14 mL tubes with 3 mL LB each:
   - Tubes A1, A2: inoculate 30 µL preculture (1:100 dilution), **with** aseptic technique (Bunsen burner or biosafety cabinet).
   - Tubes B1, B2: inoculate 30 µL preculture, **without** aseptic precautions (open bench, no flame).
   - Tubes C1, C2: **uninoculated** (sterility controls — no bacteria added).
   - Incubate overnight 37°C, 200 rpm.
   - **Read results Tuesday morning (T+0 of the growth curve)**: turbidity in A (expected), B (expected), C (unexpected)?

5. Prepare tubes for **Tuesday's manual growth curve**:
   - 3 × 3 tubes of 14 mL: LB + glucose 0.02% / 0.2% / 0.4% (3 mL each).
   - Inoculate 30 µL preculture into each tube.
   - Start measurements Tuesday morning at 8:30 or upon arrival.

> **Teaching point**: explain why we work aseptically and what "sterile" really means.

---

## D2 — Tuesday W1 · Manual growth curve

**Objective**: measure a bacterial growth curve by hand; understand lag phase, exponential phase, and stationary phase.

### Materials
- 9 × 14 mL tubes inoculated Monday evening
- OD600 spectrophotometer
- Disposable cuvettes
- Graph paper or spreadsheet for recording measurements

### Measurement protocol

| Time | Measurement |
|---|---|
| T+0 (9:30) | Check Monday tubes (A/B/C turbid?) then initial OD600 for all tubes |
| T+60 min (10:30) | OD600  ← 1h interval |
| T+120 min (11:30) | OD600  ← 1h interval |
| T+150 min (12:00) | OD600  ← 30 min interval |
| T+180 min (12:30) | OD600 |
| T+210 min (13:00) | OD600 |
| T+240 min (13:30) | OD600  ← 4 measurements at 30 min complete |
| T+260 min (13:50) | OD600  ← 20 min interval |
| … | … every 20 min until ~16:00 … |
| T+≈6h30 | Last measurement of the day |

- OD measurement: transfer 1 mL of culture to a cuvette, read at 600 nm, record.
- Blank: LB only (no bacteria) — prepare 1 blank tube per glucose concentration.
- If OD > 0.8: dilute 1:2 in LB before reading, multiply the value by 2.

### Recommended data format

```
time_min, glu_002pct_r1, glu_002pct_r2, glu_002pct_r3, glu_02pct_r1, ...
0, 0.05, 0.05, 0.06, 0.05, ...
20, 0.07, 0.07, 0.08, 0.09, ...
```

Save as `.csv` — will be loaded in Notebook A §A4.

### Notes
- The 0.02% glucose tubes will reach stationary phase well before the others.
- If OD does not rise after 2h: verify that cultures were inoculated.
- Lag phase may last 30–60 min depending on preculture state.

---

## D3 — Wednesday W1 · Plate reader diauxie (overnight)

**Objective**: observe growth on two carbon sources simultaneously, demonstrate diauxie.

### Materials
- Black 96-well plate with transparent bottom (for future fluorescence) or flat transparent bottom
- Sterile liquid LB
- Sterile 20% glucose stock (autoclaved or filtered)
- Sterile 20% lactose stock
- MG1655 overnight preculture in LB (OD ~2–4)
- Parafilm

### Media preparation (final volumes 200 µL/well)

| Condition | Final concentration | Stock used |
|---|---|---|
| Glucose only | 0.02% / 0.2% / 0.4% | 20% glucose: 0.2 µL / 2 µL / 4 µL in 200 µL LB |
| Lactose only | 0.2% / 0.4% | 20% lactose: 2 µL / 4 µL in 200 µL LB |
| Glu 0.2% + Lac 0.2% | 0.2% each | 2 µL glu + 2 µL lac in 200 µL LB |
| Glu 0.4% + Lac 0.4% | 0.4% each | 4 µL glu + 4 µL lac in 200 µL LB |
| Blank (LB only) | — | Pure LB |

### Diauxie plate layout

```
        Col 1       Col 2       Col 3       Col 4       Col 5       Col 6       Col 7–12
Row A   Glu 0.02%   Glu 0.02%   Glu 0.02%   Glu 0.2%    Glu 0.2%    Glu 0.2%    …
Row B   Glu 0.4%    Glu 0.4%    Glu 0.4%    Lac 0.2%    Lac 0.2%    Lac 0.4%    …
Row C   Lac 0.4%    GluLac0.2%  GluLac0.2%  GluLac0.4%  GluLac0.4%  Blank       …
Row D–H Unused (leave empty or fill with LB to limit evaporation)
```

> **[ADAPT]** based on desired number of replicates and plate availability.
> Recommended minimum: 2 replicates per condition + 2 blanks.

### Inoculation protocol

1. Prepare a 1:100 dilution of preculture in LB (OD ~0.02–0.05).
2. Dispense 190 µL of medium (LB + glucose/lactose at final concentrations) into each well.
3. Add 10 µL of diluted preculture to each well (final inoculum ~0.002–0.005 OD).
4. Cover with lid or perforated Parafilm.
5. Launch the plate reader:
   - 37°C, strong orbital shaking (300 rpm or "normal")
   - OD600 reading every 5 min
   - Duration: 14–18h (overnight)

### BioTek plate reader settings [TO CHECK]
- OD600 reading: 600 nm filter
- Shaking: orbital, 5 sec before reading
- Temperature: 37°C
- Interval: 5 min
- Total duration: 900 min (15h) or overnight

---

## D4 — Thursday W1 · Diauxie readout + TSS Transformation

**Objective**: analyse overnight data and introduce bacterial transformation.

### Morning — diauxie readout and discussion

1. Stop the plate reader (or let run until read).
2. Export data as `.txt` (BioTek Gen5 format — see Notebook A §A4 for parsing).
3. Discussion with the intern: which wells show a "dip" in the OD curve? Why?
   Connect to *lac* operon regulation: bacteria wait for glucose exhaustion before inducing *lacZ*.

### Afternoon — TSS Transformation (pUA66-lacUV5 → MG1655)

#### Preparing TSS-competent cells

1. Inoculate 5 mL LB from glycerol stock or fresh MG1655 colony. Incubate 2h at 37°C until OD ~0.4.
2. Centrifuge 2 mL at 4000 rpm × 5 min at 4°C. Discard supernatant.
3. Resuspend pellet in 200 µL cold TSS buffer:
   ```
   TSS (100 mL):
     LB                   85 mL
     PEG 3350 10%         10 mL  (w/v — dissolve in warm LB)
     DMSO                  5 mL
     MgSO₄ 1 M             1 mL  (final concentration 10 mM)
     Adjust to pH 6.5 with 1 N HCl
     Ultrapure water: QSP 100 mL
     Filter through 0.22 µm
     Aliquot 200 µL, store at −80°C
   ```
4. Use immediately (or store on ice for max 30 min).

#### Transformation

5. Mix in a cold Eppendorf tube:
   - 50 µL competent cells
   - 1–5 µL plasmid DNA pUA66-lacUV5 (10–100 ng)
6. Incubate 30 min on ice.
7. No heat shock for TSS — keep on ice throughout.
8. Add 900 µL LB pre-warmed to 37°C. Incubate 1h at 37°C without shaking (KanR expression).
9. Centrifuge 5000 rpm × 2 min. Discard 800 µL supernatant.
10. Resuspend pellet in remaining ~150 µL. Plate on LB + Kan50.
11. Incubate overnight at 37°C. Read Friday morning.

#### Controls to include
- "−DNA" tube: cells without plasmid → should give zero (or very few) colonies.
- "+DNA control" tube: known plasmid (e.g. existing Plac-GFP) → should give colonies.

### Notes
- The recovery incubation (step 8, 1h) is a good time for Notebook A §A3.
- If no colonies on Friday: use existing pUA66-lacUV5/MG1655 glycerol stock (if available) or redo.

---

## D5 — Friday W1 · Transformation check + data analysis

**Objective**: verify transformation results, pick colonies, prepare Week 2.

### Morning

1. **Count colonies**: expected >10 on "+DNA", <2 on "−DNA".
2. **Pick 2–3 colonies** Kan-resistant into 3 mL LB + Kan50. Incubate overnight.
3. **[OPTIONAL]** Quick induction spot: streak a colony onto LB + Kan50 + 100 µM IPTG.
   Fluorescence visible under UV lamp (312 nm) the next day if transformation worked.

### Afternoon

4. Analyse manual growth curve data (D2) in the notebook.
5. Analyse diauxie data (D3): visualisation, identify the diauxie dip.
6. Start Notebook B §B1 if time allows.

---

## [Sunday W2 — Thomas only]

- Inoculate Plac-GFP/MG1655: 1 fresh colony or 5 µL glycerol → 3 mL M9 0.2% arabinose + Kan50. Overnight 37°C, 200 rpm.
- Inoculate pUA66-lacUV5/MG1655: same from Fri W1 colony.
- Verify both cultures are growing correctly Monday morning (expected OD ~2–4).

---

## D6 — Monday W2 · Induction experiment (plate reader)

**Objective**: quantitatively measure the response of both strains to IPTG and TMG.

### Morning — culture growth

1. Dilute overnight precultures 1:100 in LB + Kan50 (e.g. 30 µL preculture into 3 mL LB + Kan50).
2. Incubate at 37°C, 200 rpm for **2–3h** until OD600 ~0.2–0.3 (exponential phase).
3. During this time: Notebook A §A4 (complete diauxie analysis).

### Afternoon — prepare and launch plate reader

#### Prepare inducer stocks (see Appendix 2)

Prepare working dilutions from 10 mM stocks:

| Final concentration (µM) | Working dilution (100×) | Volume to add per well (in 200 µL) |
|---|---|---|
| 0 | Water | 2 µL water |
| 1 | 100 µM | 2 µL |
| 3 | 300 µM | 2 µL |
| 10 | 1,000 µM = 1 mM | 2 µL |
| 30 | 3,000 µM = 3 mM | 2 µL |
| 100 | 10,000 µM = 10 mM (stock) | 2 µL |

#### Induction plate layout

```
Columns      1         2    3    4    5    6  |    7         8    9   10   11   12
          [IPTG]=0*   1    3   10   30  100  | [TMG]=0*    1    3   10   30  100 µM
          (autofluo)                          | (autofluo)

Row A     Plac-GFP (replicate 1)               | Plac-GFP (replicate 1)
Row B     Plac-GFP (replicate 2)               | Plac-GFP (replicate 2)
Row C     lacUV5-GFP (replicate 1)             | lacUV5-GFP (replicate 1)
Row D     lacUV5-GFP (replicate 2)             | lacUV5-GFP (replicate 2)
Row E     Blanks LB + Kan50 (medium only)      | Blanks LB + Kan50
Row F–H   (empty)
```

\* **Columns 1 and 7 ([I]=0) = autofluorescence reference.** These wells measure endogenous
bacterial fluorescence (mainly flavins: FAD, FMN, riboflavin), independent of GFP.
They are used to correct all other RFU/OD values (see Notebook B §B3).

Total: 48 bacterial wells + 12 blanks + 36 empty = 96 wells.

#### Pipetting protocol (recommended sequence)

1. **Distribute inducer**: add 2 µL of the corresponding working dilution to each well (start with blanks = 2 µL water).
   - Use a multichannel pipette (8-channel) pipetting by columns: Col 1 = water (conc 0), Col 2 = 100 µM IPTG, etc.
2. **Distribute bacteria**: add 198 µL of culture per well (1:100 dilution in LB + Kan50 within the culture itself).
   - Multichannel pipette by rows: Row A = 198 µL Plac-GFP culture, Row D = 198 µL lacUV5-GFP culture.
   - For blanks (Row E): 198 µL LB + Kan50 only.

#### BioTek plate reader settings [TO CHECK]
- OD600 reading: 600 nm filter
- GFP reading: excitation 485/20 nm, emission 528/20 nm (or per available filter)
- Shaking: orbital, 5 sec before reading
- Temperature: 37°C
- Interval: 5–10 min
- Duration: 6–8h

> **Autofluorescence reading**: columns 1 and 7 ([I]=0) measure endogenous fluorescence.
> For reliable correction, ensure these wells are in **exponential phase** at the time
> of reading (OD ~0.1–0.4) — autofluorescence per cell is stable there.
> Avoid stationary phase where metabolic state changes.

---

## D7 — Tuesday W2 · Data readout + [OPTIONAL] microscopy

**Objective**: analyse first induction data and, if possible, observe bistability under the microscope.

### Morning — readout and evaluation

1. Read data exported from the BioTek (`.txt` file).
2. Quick check: OD curves rising? GFP signal visible at [IPTG] = 100 µM?
3. Check columns 1 and 7 ([I]=0): RFU/OD stable during exponential phase? This is the autofluorescence reference for correction (Notebook B §B3).
4. If clean data → Notebook B §B3 in the afternoon.
5. If problem (no growth, absent GFP signal, contamination) → discuss with Thomas, redo if necessary.

### Afternoon [OPTIONAL] — Agar pad microscopy

> **Prerequisite**: plate reader data must be clean (growth OK, GFP signal visible).

#### Preparing agar pads

1. Melt 1–2 mL 1% agarose in LB (microwave, ~30 sec).
2. Deposit ~30 µL on a glass slide. Place a second slide on top (sandwich).
3. Leave to solidify 5 min.
4. Gently separate slides: keep the slide with the agar pad.

#### Sample preparation

Prepare 4 TMG conditions from the lacUV5-GFP (or Plac-GFP) culture in exponential phase:
- [TMG] = 0, 5, 20, 100 µM (separate Eppendorf tubes, 100 µL each)
- Incubate 1h at 37°C without shaking.

#### Mounting and acquisition

5. Deposit 2 µL of bacteria on the agar pad. Cover with a coverslip.
6. Observe:
   - **Phase contrast**: visualise individual cells (60× or 100× objective).
   - **GFP channel**: excitation 470 nm, emission 525 nm. Exposures 50–200 ms.
7. Acquire ~5 fields per condition (min. 50 cells per field).
8. Save images as `.tif`.

---

## D8 — Wednesday W2 · ImageJ + analysis [OPTIONAL]

> This day is optional. If microscopy was not done on D7, it can be moved here.

### ImageJ analysis (if images available)

**Objective**: measure fluorescence of each cell individually.

1. Open an image in ImageJ (or FIJI).
2. Convert to 8-bit if necessary (*Image > Type > 8-bit*).
3. Segment cells on the GFP channel:
   - *Image > Adjust > Threshold* → adjust threshold so bacteria are selected.
   - *Analyze > Analyze Particles*: min area = 1 µm², max area = 20 µm², check "Display results".
4. *Analyze > Measure*: ensure "Mean" is checked in *Analyze > Set Measurements*.
5. Export table as CSV (*File > Save As > Results*).
6. Name the file: `imagej_tmg_XXuM.csv` (replace XX with the concentration).
7. Repeat for all 4 conditions.

These CSVs are loaded in Notebook C.

### Notebook B §B3 + Notebook C (if not already done)

- §B3: plate reader data loading, RFU/OD normalisation, dose-response curves, K_half fit.
- Notebook C [OPTIONAL]: single-cell histograms, bimodality.

---

## D9 — Thursday W2 · Final presentation

**Duration**: ~20 min presentation + 10 min questions.

### Suggested structure

1. **Biological question** (2 min): why do bacteria regulate the *lac* operon?
2. **Experiment 1: growth** (5 min): growth curve, stochastic simulation, diauxie.
3. **Experiment 2: induction** (8 min): dose-response curves, Hill curve, Plac vs lacUV5 comparison.
4. **[OPTIONAL]** Microscopy and bimodality (3 min).
5. **What I learned** (2 min): what was surprising, what remains open.

### Figures to prepare (minimum)

- Manual growth curve (D2) + Monod simulation overlay
- Diauxie curve (D3) + annotation of the two phases
- Dose-response curves Plac-GFP vs lacUV5-GFP + fitted Hill curves

---

## Appendix 1 — Media and antibiotics

| Medium | Composition | Sterilisation |
|---|---|---|
| Liquid LB | 10 g/L NaCl, 10 g/L tryptone, 5 g/L yeast extract | Autoclave 121°C, 20 min |
| LB + Kan50 | LB + kanamycin 50 µg/mL | Add kanamycin after cooling (< 55°C) |
| LB agar | LB + agar 15 g/L | Autoclave, pour after cooling to ~55°C |
| LB agar + Kan50 | LB agar + kanamycin 50 µg/mL | Add kanamycin before pouring (< 55°C) |

**Kanamycin stock**: 50 mg/mL in ultrapure water, filter 0.22 µm, aliquot 1 mL, store −20°C.

---

## Appendix 2 — IPTG and TMG stock preparation

### IPTG (isopropyl β-D-1-thiogalactopyranoside)
- Molecular weight: 238.3 g/mol
- 10 mM stock: weigh 2.38 mg, dissolve in 1 mL ultrapure water (or MQ water). Filter 0.22 µm.
- Aliquot 100 µL, store at −20°C. Avoid repeated freeze-thaw cycles.
- Working dilution preparation (1 mL each):

| Working dilution | Vol. 10 mM stock | Vol. water | Use (2 µL → final conc. in 200 µL) |
|---|---|---|---|
| 3 mM | 300 µL | 700 µL | → 30 µM final |
| 1 mM | 100 µL | 900 µL | → 10 µM final |
| 300 µM | 30 µL | 970 µL | → 3 µM final |
| 100 µM | 10 µL | 990 µL | → 1 µM final |
| 0 | — | 1 mL water | → 0 µM final |
| 10 mM (stock direct) | — | — | → 100 µM final |

### TMG (methyl β-D-thiogalactopyranoside)
- Molecular weight: 210.3 g/mol  (≠ IPTG — methyl group replaces isopropyl)
- 10 mM stock: weigh 2.10 mg, dissolve in 1 mL ultrapure water. Filter 0.22 µm.
- Aliquot 100 µL, store at −20°C. Avoid repeated freeze-thaw cycles.
- Same recommended final concentrations as IPTG; same working dilutions.

---

## Appendix 3 — [OPTIONAL] Agar pad microscopy protocol

### Materials
- 1% low-melting agarose in LB (or PBS)
- Cleaned glass slides + 0.17 mm coverslips (no. 1.5)
- Thin double-sided tape (optional, to space slides)
- Bacterial cultures in exponential phase (OD ~0.2–0.3)
- TMG inducers at desired concentrations

### Detailed protocol

**Agar pad preparation**
1. Melt agarose in LB (microwave, 20–30 sec at full power, watch carefully).
2. Place 2 small pieces of double-sided tape on the glass slide (~0.2 mm thickness to space the slides).
3. Pour ~30–40 µL of cooled molten agarose (~50°C) onto the slide.
4. Immediately apply a second slide, sliding perpendicular.
5. Leave to solidify 5 min at room temperature.
6. Separate slides by sliding — the agar pad remains on one slide.

**Depositing bacteria**
7. Gently vortex the culture + inducer (after 1h pre-incubation at 37°C).
8. Deposit 1–2 µL on the agar pad.
9. Leave to dry 30 sec in air (until the droplet sheen disappears).
10. Cover with a clean coverslip.

**Acquisition**
11. Observe in phase contrast to locate bacteria (60× or 100× objective, oil).
12. Switch to GFP channel:
    - Excitation filter: 470/40 nm (or Chroma ET470/40x)
    - Emission filter: 525/50 nm (or Chroma ET525/50m)
    - Exposure time: 50–500 ms depending on expression level. Adjust to avoid saturation.
13. Acquire phase contrast + GFP for each field. Save as 16-bit `.tif`.
14. Collect ≥5 fields per condition (≥50 cells per field for statistics).

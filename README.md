# q-Bio Microbiology Lab Internship — Teaching Materials
*Thomas Julou — Biozentrum, University of Basel.**

Materials for a two-week high school lab internship (French *classe de seconde*, 15 yo)
at a quantitative microbiology laboratory (Biozentrum, Basel, Switzerland).
The program combines wet-lab experiments with guided Python programming sessions
run in parallel during waiting times.

The documents were prepared with assistance of Claude.ai

## Scientific questions

1. **How does a single bacterium produce exponential growth?**
   Manual growth curve measurements, stochastic simulation (τ-leaping),
   Monod nutrient dynamics, and diauxie visualised from plate reader data.

2. **How does a bacterium quantitatively control gene expression?**
   Fluorescence induction curves (IPTG and TMG) with two *E. coli* reporter strains
   (*Plac*-GFP and *PlacUV5*-GFP in pUA66), dose–response modelling with the Hill equation,
   and optional single-cell heterogeneity analysis by microscopy and ImageJ.

## Language

All documents and notebooks are written in **French**, targeting a French high school curriculum
(programme de *seconde*, Mathématiques–Physique–Informatique stream).
Key technical terms are used in their standard French or international form.

Supervision material was translated to English.

## Files

First version written in French. 

| File | Language | Description |
|---|---|---|
| `1_doc_principal_encadrant.md` | French | **Supervisor guide** — pedagogical overview, day-by-day schedule, pre-stage checklist, biological and didactic notes |
| `1_doc_principal_stagiaire.md` | French | **Student welcome document** — programme summary, preparation resources |
| `2_plan_experimental_encadrant.md` | French | **Detailed experimental plan (supervisor)** — full protocols J1–J9, plate layouts, reagent recipes |
| `2_plan_experimental_stagiaire.md` | French | **Experimental plan (student)** — step-by-step autonomous protocols with checklists |
| `3_notebook_croissance_complet.ipynb` | French | **Notebook A — Growth dynamics (reference/answer key)** §A1 deterministic model · §A2 stochastic simulation · §A3 Monod nutrients · §A4 plate reader data |
| `3_notebook_croissance_stagiaire.ipynb` | French | **Notebook A — Growth dynamics (student version)** — code cells replaced by guided instructions |
| `4_notebook_induction_complet.ipynb` | French | **Notebook B — Gene expression and regulation (reference)** §B1 stochastic switch · §B2 Hill equation · §B3 induction data analysis; includes embedded diagrams of the *lac* operon |
| `4_notebook_induction_stagiaire.ipynb` | French | **Notebook B — Gene expression (student version)** |
| `5_notebook_heterogeneite_complet.ipynb` | French | **Notebook C — Cell-to-cell heterogeneity [OPTIONAL] (reference)** §C1 LacY bistability simulation · §C2 ImageJ single-cell fluorescence analysis |
| `5_notebook_heterogeneite_stagiaire.ipynb` | French | **Notebook C — Heterogeneity [OPTIONAL] (student version)** |

## Usage

Notebooks run in [Google Colab](https://colab.research.google.com) without any local installation.
Student versions (`*_stagiaire.ipynb`) contain commented-out instructions in place of
executable code; the reference versions (`*_complet.ipynb`) contain full working code
and can be shared with the student at the end of the internship.

## Biological system

- Organism: *Escherichia coli* MG1655
- Reporters: pUA66-*Plac*-GFP (Zaslaver transcriptional reporter library) and pUA66-*PlacUV5*-GFP (custom made derivative)
- Growth medium: M9 + 0.2 % arabinose + kanamycin 50 µg/mL
- Inducers: lactose, IPTG (plate reader dose–response) and TMG (microscopy, bistability)


## License

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to share and adapt these materials for non-commercial purposes,
provided you give appropriate credit and distribute any derivative works
under the same license.
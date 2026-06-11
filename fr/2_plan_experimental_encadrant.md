# Plan expérimental — Stage lycéen
## Protocoles J1–J9 · Layouts plaques · Solutions

> **Conventions** : `[À VÉRIFIER]` = valeur à confirmer par Thomas avant le stage.
> Volumes en µL sauf indication contraire. Toutes les incubations à 37 °C sauf mention.

---

## J1 — Lundi S1 · Introduction et pipetage

**Objectif** : maîtriser les techniques de base (pipetage, dilutions, stérilité) et inoculer les premières cultures.

### Matériel
- Micropipettes P20, P200, P1000 + cônes correspondants
- Tubes Eppendorf 1,5 mL × 10
- Tubes Falcon 15 mL × 3
- LB liquide stérile
- Colorant (bleu de bromophénol ou rouge de Congo à 0,1 % dans eau — pour visualiser les dilutions)
- Tubes de croissance 14 mL × 6 (3 stériles, 3 non stériles), bouchons
- Préculture *E. coli* MG1655 overnight en LB (OD ~2–4)

### Matin — pipetage et dilutions

1. Démonstration des pipettes : réglage, prise de cône, technique de pipetage.
2. **Exercice dilutions en série** : préparer 6 dilutions ×10 successives du colorant dans l'eau (1:10 → 1:10⁶) dans des Eppendorf de 1,5 mL. Volume final = 100 µL à chaque étape.
   - Vérification visuelle : l'absorbance doit décroître de façon visible.
   - [OPTIONNEL] Mesure au nanodrop ou spectro pour quantifier.
3. Discussion : quelle est la concentration dans le tube n°6 si le tube n°1 est à 1 mg/mL ?

### Après-midi — inoculation tubes stériles vs non stériles

4. Préparer 6 tubes de 14 mL avec 3 mL LB chacun :
   - Tubes A1, A2 : inoculer 30 µL préculture (dilution 1:100), **avec** technique stérile (brûlage bec Bunsen ou hotte).
   - Tubes B1, B2 : inoculer 30 µL préculture, **sans** précautions stériles (manipulations à l'air libre, pas de flambeau).
   - Tubes C1, C2 : **non inoculés** (témoins stérilité — pas de bactéries ajoutées).
   - Incuber overnight 37 °C, 200 rpm.
   - **Lire le résultat mardi matin (T+0 de la courbe de croissance)** : turbidité dans A (attendu), B (attendu), C (non attendu) ?

5. Préparer les tubes pour la **courbe de croissance manuelle de mardi** :
   - 3 × 3 tubes de 14 mL : LB + glucose 0,02 % / 0,2 % / 0,4 % (3 mL chacun).
   - Inoculer 30 µL préculture dans chaque tube.
   - Démarrer la mesure mardi matin à 8h30 ou dès l'arrivée.

> **Point pédagogique** : expliquer pourquoi on travaille stérilement et ce que "stérile" signifie vraiment.

---

## J2 — Mardi S1 · Courbe de croissance manuelle

**Objectif** : mesurer une courbe de croissance bactérienne à la main, comprendre la phase de latence, la phase exponentielle, et la phase stationnaire.

### Matériel
- 9 tubes de 14 mL inoculés lundi soir
- Spectrophotomètre OD600
- Cuvettes jetables
- Feuille de papier millimétré ou tableur pour noter les mesures

### Protocole de mesure

| Heure | Mesure |
|---|---|
| T+0 (9h30) | Vérifier les tubes du lundi (A/B/C turbides ?) puis OD600 initial |
| T+60 min (10h30) | OD600  ← intervalle 1h |
| T+120 min (11h30) | OD600  ← intervalle 1h |
| T+150 min (12h00) | OD600  ← intervalle 30 min |
| T+180 min (12h30) | OD600 |
| T+210 min (13h00) | OD600 |
| T+240 min (13h30) | OD600  ← 4 mesures à 30 min terminées |
| T+260 min (13h50) | OD600  ← intervalle 20 min |
| … | … toutes les 20 min jusqu'à ~16h … |
| T+≈6h30 | Dernière mesure de la journée |

- Mesure OD : vider 1 mL de culture dans une cuvette, lire à 600 nm, noter.
- Blanc : LB seul sans bactéries (préparer 1 tube blanc par concentration de glucose).
- Si OD > 0,8 : diluer 1:2 dans LB avant mesure, multiplier la valeur lue par 2.

### Notation recommandée

```
temps_min, glu_002pct_r1, glu_002pct_r2, glu_002pct_r3, glu_02pct_r1, ...
0, 0.05, 0.05, 0.06, 0.05, ...
20, 0.07, 0.07, 0.08, 0.09, ...
```

Sauvegarder en `.csv` — sera chargé dans le Notebook A §A4.

### Points d'attention
- Les tubes 0,02 % glucose seront en phase stationnaire bien avant les autres.
- Si l'OD ne monte pas après 2h : vérifier que les cultures ont été inoculées.
- La phase de latence peut durer 30–60 min selon l'état de la préculture.

---

## J3 — Mercredi S1 · Plaque reader diauxie (overnight)

**Objectif** : observer la croissance sur deux sources de carbone simultanément, mettre en évidence la diauxie.

### Matériel
- Plaque 96 puits noire à fond transparent (pour fluorescence future) ou fond plat transparent
- LB liquide stérile
- Glucose 20 % stock stérile (autoclavé ou filtré)
- Lactose 20 % stock stérile
- Préculture MG1655 overnight en LB (OD ~2–4)
- Parafilm

### Préparation des milieux (volumes finaux 200 µL/puits)

| Condition | Concentration finale | Stock utilisé |
|---|---|---|
| Glucose seul | 0,02 % / 0,2 % / 0,4 % | Glucose 20 % : 0,2 µL / 2 µL / 4 µL dans 200 µL LB |
| Lactose seul | 0,2 % / 0,4 % | Lactose 20 % : 2 µL / 4 µL dans 200 µL LB |
| Glu 0,2 % + Lac 0,2 % | 0,2 % chacun | 2 µL glu + 2 µL lac dans 200 µL LB |
| Glu 0,4 % + Lac 0,4 % | 0,4 % chacun | 4 µL glu + 4 µL lac dans 200 µL LB |
| Blanc (LB seul) | — | LB pur |

### Layout de la plaque diauxie

```
        Col 1       Col 2       Col 3       Col 4       Col 5       Col 6       Col 7–12
Row A   Glu 0.02%   Glu 0.02%   Glu 0.02%   Glu 0.2%    Glu 0.2%    Glu 0.2%    …
Row B   Glu 0.4%    Glu 0.4%    Glu 0.4%    Lac 0.2%    Lac 0.2%    Lac 0.4%    …
Row C   Lac 0.4%    GluLac0.2%  GluLac0.2%  GluLac0.4%  GluLac0.4%  Blanc       …
Row D–H Inutilisés (laisser vides ou remplir avec LB pour évaporation)
```

> **[À ADAPTER]** selon le nombre de réplicats souhaités et la disponibilité de la plaque.
> Minimum recommandé : 2 réplicats par condition + 2 blancs.

### Protocole d'inoculation

1. Préparer une dilution 1:100 de la préculture dans LB (OD ~0,02–0,05).
2. Distribuer 190 µL de milieu (LB + glucose/lactose aux concentrations finales) dans chaque puits.
3. Ajouter 10 µL de la préculture diluée dans chaque puits (inoculum final ~0,002–0,005 OD).
4. Couvrir avec un couvercle ou du Parafilm perforé.
5. Lancer le plate reader :
   - 37 °C, agitation orbitale forte (300 rpm ou "normal")
   - Lecture OD600 toutes les 5 min
   - Durée : 14–18h (overnight)

### Paramètres plate reader BioTek [À VÉRIFIER]
- Lecture OD600 : filtre 600 nm
- Agitation : orbitale, 5 sec avant lecture
- Température : 37 °C
- Intervalle : 5 min
- Durée totale : 900 min (15h) ou overnight

---

## J4 — Jeudi S1 · Lecture diauxie + Transformation TSS

**Objectif** : analyser les données de la nuit et introduire la transformation bactérienne.

### Matin — lecture et discussion diauxie

1. Arrêter le plate reader (ou laisser tourner jusqu'à lecture).
2. Exporter les données en `.txt` (format BioTek Gen5 — voir Notebook A §A4 pour le parsing).
3. Discussion avec le stagiaire : quels puits montrent un "creux" dans la courbe OD ? Pourquoi ?
   Relier à la régulation de l'opéron *lac* : la bactérie attend l'épuisement du glucose avant d'induire *lacZ*.

### Après-midi — Transformation TSS (pUA66-lacUV5 → MG1655)

#### Préparation des cellules compétentes TSS

1. Inoculer 5 mL LB depuis un glycérol ou une colonie MG1655 fraîche. Incuber 2h à 37 °C jusqu'à OD ~0,4.
2. Centrifuger 2 mL à 4000 rpm × 5 min à 4 °C. Jeter le surnageant.
3. Resuspendre le culot dans 200 µL de tampon TSS froid :
   ```
   TSS (100 mL) :
     LB                   85 mL
     PEG 3350 10 %        10 mL  (poids/volume — dissoudre dans LB chaud)
     DMSO                  5 mL
     MgSO₄ 1 M             1 mL  (concentration finale 10 mM)
     Ajuster à pH 6.5 avec HCl 1 N
     Eau ultra-pure : QSP 100 mL
     Filtrer sur 0.22 µm
     Aliquoter 200 µL, stocker à -80 °C
   ```
4. Utiliser immédiatement (ou stocker sur glace max 30 min).

#### Transformation

5. Mélanger dans un tube Eppendorf froid :
   - 50 µL cellules compétentes
   - 1–5 µL ADN plasmidique pUA66-lacUV5 (10–100 ng)
6. Incuber 30 min sur glace.
7. Pas de choc thermique pour TSS — garder sur glace tout au long.
8. Ajouter 900 µL LB pré-chaud à 37 °C. Incuber 1h à 37 °C sans agitation (expression du KanR).
9. Centrifuger 5000 rpm × 2 min. Jeter 800 µL de surnageant.
10. Resuspendre le culot dans les ~150 µL restants. Étaler sur LB + Kan50.
11. Incuber overnight à 37 °C. Lire vendredi matin.

#### Contrôles à inclure
- Tube "−ADN" : cellules sans plasmide → doit donner zéro (ou très peu de) colonies.
- Tube "+ADN contrôle" : plasmide connu (ex. Plac-GFP existant) → doit donner des colonies.

### Points d'attention
- L'incubation de récupération (étape 8, 1h) est le bon moment pour §A3 du Notebook A.
- Si aucune colonie vendredi : utiliser le stock glycérol de pUA66-lacUV5/MG1655 existant (si disponible) ou redo.

---

## J5 — Vendredi S1 · Vérification transformation + analyse données

**Objectif** : vérifier les résultats de la transformation, pick des colonies, préparer la semaine 2.

### Matin

1. **Compter les colonies** : attendu > 10 sur "+ADN", < 2 sur "−ADN".
2. **Pick 2–3 colonies** Kan-résistantes dans 3 mL LB + Kan50. Incuber overnight.
3. **[OPTIONNEL]** Spot d'induction rapide : étaler une colonie sur LB + Kan50 + IPTG 100 µM.
   Fluorescence visible sous lampe UV (312 nm) le lendemain si la transformation a fonctionné.

### Après-midi

4. Analyse des données de la courbe de croissance manuelle (J2) dans le notebook.
5. Analyse des données diauxie (J3) : visualisation, identification du creux de diauxie.
6. Début du Notebook B §B1 si le temps le permet.

---

## [Dimanche S2 — Thomas uniquement]

- Inoculer Plac-GFP/MG1655 : 1 colonie fraîche ou 5 µL glycérol → 3 mL M9 0,2 % arabinose + Kan50. Overnight 37 °C, 200 rpm.
- Inoculer pUA66-lacUV5/MG1655 : même chose depuis colonie de Ven S1.
- Vérifier que les deux cultures démarrent correctement le lundi matin (OD attendue ~2–4).

---

## J6 — Lundi S2 · Expérience d'induction (plaque reader)

**Objectif** : mesurer quantitativement la réponse des deux souches à l'IPTG et au TMG.

### Matin — croissance des cultures

1. Diluer les précultures overnight 1:100 dans LB + Kan50 (ex. 30 µL préculture dans 3 mL LB + Kan50).
2. Incuber à 37 °C, 200 rpm pendant **2–3h** jusqu'à OD600 ~0,2–0,3 (phase exponentielle).
3. Pendant ce temps : §A4 du Notebook A (analyse diauxie complète).

### Après-midi — préparation et lancement plaque reader

#### Préparation des stocks d'inducteurs (voir Annexe 2)

Préparer les dilutions de travail depuis les stocks 10 mM :

| Concentration finale (µM) | Dilution de travail (100×) | Volume à ajouter par puits (dans 200 µL) |
|---|---|---|
| 0 | Eau | 2 µL eau |
| 1 | 100 µM | 2 µL |
| 3 | 300 µM | 2 µL |
| 10 | 1 000 µM = 1 mM | 2 µL |
| 30 | 3 000 µM = 3 mM | 2 µL |
| 100 | 10 000 µM = 10 mM (stock) | 2 µL |

#### Layout de la plaque d'induction

```
Colonnes     1         2    3    4    5    6  |    7         8    9   10   11   12
          [IPTG]=0*   1    3   10   30  100  | [TMG]=0*    1    3   10   30  100 µM
          (autofluo)                          | (autofluo)

Row A     Plac-GFP (réplicat 1)                | Plac-GFP (réplicat 1)
Row B     Plac-GFP (réplicat 2)                | Plac-GFP (réplicat 2)
Row C     lacUV5-GFP (réplicat 1)              | lacUV5-GFP (réplicat 1)
Row D     lacUV5-GFP (réplicat 2)              | lacUV5-GFP (réplicat 2)
Row E     Blancs LB + Kan50 (milieu seul)      | Blancs LB + Kan50
Row F–H   (vides)
```

\* **Colonnes 1 et 7 ([I]=0) = référence autofluorescence.** Ces puits mesurent la
fluorescence endogène des bactéries (principalement les flavines : FAD, FMN, riboflavine),
indépendante de la GFP. Ils servent à corriger toutes les autres valeurs RFU/OD
(voir Notebook B §B3).

Total : 48 puits bactéries + 12 blancs + 36 vides = 96 puits.

#### Protocole de pipetage (séquence recommandée)

1. **Distribuer l'inducteur** : ajouter 2 µL de la dilution de travail correspondante dans chaque puits (commencer par les blancs = 2 µL eau).
   - Utiliser une pipette multicanal (8 canaux) en pipetant par colonnes : Col 1 = eau (conc 0), Col 2 = 100 µM IPTG, etc.
2. **Distribuer les bactéries** : ajouter 198 µL de culture par puits (dilution 1:100 en LB + Kan50 dans la culture elle-même).
   - Pipette multicanal par rangées : Row A = 198 µL culture Plac-GFP, Row D = 198 µL culture lacUV5-GFP.
   - Pour les blancs (Row G) : 198 µL LB + Kan50 seul.

#### Paramètres plate reader BioTek [À VÉRIFIER]
- Lecture OD600 : filtre 600 nm
- Lecture GFP : excitation 485/20 nm, émission 528/20 nm (ou selon filtre disponible)
- Agitation : orbitale, 5 sec avant lecture
- Température : 37 °C
- Intervalle : 5–10 min
- Durée : 6–8h

> **Lecture autofluorescence** : les colonnes 1 et 7 ([I]=0) mesurent la fluorescence
> endogène. Pour une correction fiable, s'assurer que ces puits sont en **phase
> exponentielle** lors de la lecture (OD ~0,1–0,4) — l'autofluorescence par cellule
> y est stable. Éviter la phase stationnaire où l'état métabolique change.

---

## J7 — Mardi S2 · Lecture données + [FACULTATIF] microscopie

**Objectif** : analyser les premières données d'induction et, si possible, observer la bistabilité au microscope.

### Matin — lecture et évaluation

1. Lire les données exportées depuis le BioTek (fichier `.txt`).
2. Vérification rapide : courbes OD croissantes ? Signal GFP visible à [IPTG] = 100 µM ?
3. Vérifier les colonnes 1 et 7 ([I]=0) : RFU/OD stable pendant la phase exponentielle ? C'est la référence autofluorescence pour la correction (Notebook B §B3).
4. Si données propres → Notebook B §B3 l'après-midi.
5. Si problème (pas de croissance, signal GFP absent, contamination) → discuter avec Thomas, redo si nécessaire.

### Après-midi [FACULTATIF] — Microscopie agar pads

> **Prérequis** : les données de la plaque reader doivent être propres (croissance OK, signal GFP visible).

#### Préparation agar pads

1. Faire fondre 1–2 mL agarose 1 % dans LB (microwave, ~30 sec).
2. Déposer ~30 µL sur une lame de verre. Poser une seconde lame dessus (sandwich).
3. Laisser solidifier 5 min.
4. Séparer délicatement les lames : garder la lame avec l'agar pad.

#### Préparation des échantillons

Préparer 4 conditions TMG à partir de la culture lacUV5-GFP (ou Plac-GFP) en phase exponentielle :
- [TMG] = 0, 5, 20, 100 µM (tubes Eppendorf séparés, 100 µL chacun)
- Incuber 1h à 37 °C sans agitation.

#### Montage et acquisition

5. Déposer 2 µL de bactéries sur l'agar pad. Couvrir avec une lamelle.
6. Observer :
   - **Phase contraste** : visualiser les cellules individuelles (objectif 60× ou 100×).
   - **Canal GFP** : excitation 470 nm, émission 525 nm. Expositions 50–200 ms.
7. Acquérir ~5 champs par condition (min. 50 cellules par champ).
8. Sauvegarder les images en `.tif`.

---

## J8 — Mercredi S2 · ImageJ + analyse [FACULTATIF]

> Cette journée est facultative. Si la microscopie n'a pas été faite J7, elle peut être déplacée ici.

### Analyse ImageJ (si images disponibles)

**Objectif** : mesurer la fluorescence de chaque cellule individuellement.

1. Ouvrir une image dans ImageJ (ou FIJI).
2. Convertir en 8-bit si nécessaire (*Image > Type > 8-bit*).
3. Segmenter les cellules sur le canal GFP :
   - *Image > Adjust > Threshold* → ajuster le seuil pour que les bactéries soient sélectionnées.
   - *Analyze > Analyze Particles* : Surface min = 1 µm², Surface max = 20 µm², cocher "Display results".
4. *Analyze > Measure* : s'assurer que "Mean" est coché dans *Analyze > Set Measurements*.
5. Exporter le tableau en CSV (*File > Save As > Results*).
6. Nommer le fichier : `imagej_tmg_XXuM.csv` (remplacer XX par la concentration).
7. Répéter pour les 4 conditions.

Ces CSV sont chargés dans le notebook induction Notebook C.

### Notebook B §B3 + Notebook C (si pas déjà fait)

- §B3 : chargement données plate reader, normalisation RFU/OD, courbes dose-réponse, fit K_half.
- Notebook C [FACULTATIF] : histogrammes single-cell, bimodalité.

---

## J9 — Jeudi S2 · Présentation finale

**Durée** : ~20 min de présentation + 10 min de questions.

### Structure suggérée

1. **Question biologique** (2 min) : pourquoi les bactéries régulent-elles l'opéron *lac* ?
2. **Expérience 1 : croissance** (5 min) : courbe de croissance, simulation stochastique, diauxie.
3. **Expérience 2 : induction** (8 min) : courbes dose-réponse, courbe de Hill, comparaison Plac vs lacUV5.
4. **[FACULTATIF]** Microscopie et bimodalité (3 min).
5. **Ce que j'ai appris** (2 min) : ce qui a surpris, ce qui reste ouvert.

### Figures à préparer (minimum)

- Courbe de croissance manuelle (J2) + simulation Monod superposée
- Courbe diauxie (J3) + annotation des deux phases
- Courbes dose-réponse Plac-GFP vs lacUV5-GFP + courbes de Hill ajustées

---

## Annexe 1 — Milieux et antibiotiques

| Milieu | Composition | Stérilisation |
|---|---|---|
| LB liquide | 10 g/L NaCl, 10 g/L tryptone, 5 g/L extrait de levure | Autoclave 121 °C, 20 min |
| LB + Kan50 | LB + kanamycine 50 µg/mL | Ajouter kanamycine après refroidissement (< 55 °C) |
| LB gélosé | LB + agar 15 g/L | Autoclave, couler après refroidissement à ~55 °C |
| LB gélosé + Kan50 | LB gélosé + kanamycine 50 µg/mL | Ajouter kanamycine avant coulage (< 55 °C) |

**Stock kanamycine** : 50 mg/mL dans eau ultra-pure, filtrer 0,22 µm, aliquoter 1 mL, stocker −20 °C.

---

## Annexe 2 — Préparation stocks IPTG et TMG

### IPTG (isopropyl β-D-1-thiogalactopyranoside)
- Masse molaire : 238,3 g/mol
- Stock 10 mM : peser 2,38 mg, dissoudre dans 1 mL eau ultra-pure (ou eau MQ). Filtrer 0,22 µm.
- Aliquoter 100 µL, stocker à −20 °C. Éviter les cycles gel/dégel répétés.
- Préparation des dilutions de travail (pour 1 mL chacune) :

| Dilution de travail | Vol. stock 10 mM | Vol. eau | Usage (2 µL → conc. finale dans 200 µL) |
|---|---|---|---|
| 3 mM | 300 µL | 700 µL | → 30 µM final |
| 1 mM | 100 µL | 900 µL | → 10 µM final |
| 300 µM | 30 µL | 970 µL | → 3 µM final |
| 100 µM | 10 µL | 990 µL | → 1 µM final |
| 0 | — | 1 mL eau | → 0 µM final |
| 10 mM (stock direct) | — | — | → 100 µM final |

### TMG (methyl β-D-thiogalactopyranoside)
- Masse molaire : 210,3 g/mol  (≠ IPTG — le groupement méthyle remplace l'isopropyle)
- Stock 10 mM : peser 2,10 mg, dissoudre dans 1 mL eau ultra-pure. Filtrer 0,22 µm.
- Aliquoter 100 µL, stocker à −20 °C. Éviter les cycles gel/dégel répétés.
- Mêmes concentrations finales recommandées que l'IPTG ; mêmes dilutions de travail.

---

## Annexe 3 — [FACULTATIF] Protocole microscopie agar pads

### Matériel
- Agarose low-melting 1 % dans LB (ou PBS)
- Lames de verre nettoyées + lamelles 0,17 mm (n°1.5)
- Scotch double-face fin (optionnel, pour espacer les lames)
- Cultures bactériennes en phase exponentielle (OD ~0,2–0,3)
- Inducteurs TMG aux concentrations souhaitées

### Protocole détaillé

**Préparation de l'agar pad**
1. Faire fondre l'agarose dans LB (microwave, 20–30 sec à pleine puissance, surveiller).
2. Déposer 2 petits morceaux de scotch double-face sur la lame de verre (épaisseur ~0,2 mm pour écarter les lames).
3. Couler ~30–40 µL d'agarose fondu refroidi (~50 °C) sur la lame.
4. Appliquer une seconde lame immédiatement, en glissant perpendiculairement.
5. Laisser solidifier 5 min à température ambiante.
6. Séparer les lames en glissant — l'agar pad reste sur l'une des deux lames.

**Dépôt des bactéries**
7. Vortexer doucement la culture + inducteur (1h d'incubation préalable à 37 °C).
8. Déposer 1–2 µL sur l'agar pad.
9. Laisser sécher 30 sec à l'air (jusqu'à disparition du reflet de la goutte).
10. Couvrir avec une lamelle propre.

**Acquisition**
11. Observer en phase contraste pour localiser les bactéries (objectif 60× ou 100×, huile).
12. Basculer sur le canal GFP :
    - Filtre d'excitation : 470/40 nm (ou Chroma ET470/40x)
    - Filtre d'émission : 525/50 nm (ou Chroma ET525/50m)
    - Temps d'exposition : 50–500 ms selon le niveau d'expression. Ajuster pour éviter la saturation.
13. Acquérir phase contraste + GFP pour chaque champ. Enregistrer en `.tif` 16-bit.
14. Collecter ≥ 5 champs par condition (≥ 50 cellules par champ pour avoir des statistiques).

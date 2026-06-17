# Plan expérimental — Stage microbiologie quantitative
### Ce document est à toi · Garde-le avec toi pendant tout le stage

---

**Comment lire ce document**

- ✓ = tu peux faire cette étape seul·e
- ⚠️ = demande l'aide ou la supervision de Thomas
- ☑ = case à cocher quand c'est fait

---

## J1 — Lundi S1 · Introduction et pipetage

**Objectif** : apprendre à utiliser les pipettes et à travailler stérilement. Inoculer tes premières cultures.

### Matin — Pipetage et dilutions ⚠️ (démonstration Thomas)

**Exercice — dilutions en série**

On prépare 6 dilutions successives au facteur 10 d'un colorant. À chaque étape, 10 µL prélevés → ajoutés à 90 µL d'eau.

Matériel sur la paillasse : pipettes P20, P200, P1000 + cônes · 10 tubes Eppendorf · solution colorée (tube 0) · eau.

1. ☑ Distribuer **90 µL d'eau** dans les tubes 1 à 6. Changer de cône à chaque tube.
2. ☑ Prélever **10 µL du tube 0** → tube 1. Mélanger 5× de haut en bas. Changer de cône.
3. ☑ Prélever **10 µL du tube 1** → tube 2. Mélanger. Changer de cône.
4. ☑ Répéter jusqu'au tube 6.
5. ☑ Observer : la couleur diminue-t-elle régulièrement ?

> Si le tube 6 est encore très coloré : une erreur s'est produite. Recommencer.

**Exercice — utiliser la densité optique pour mesure la concentration bactérienne**
Utiliser la dilution en série pour mesurer la relation entre concentration bactérienne et DO600: 
1. Préparer 6 dilutions ×10 successives d'une culture de nuit dans du MgSO4 10mM (1 → 1:10⁶) dans des Eppendorf de 1,5 mL. Volume final = 900 µL à chaque étape.
2. Mesure au spectro.
3. Tracer DO600 vs concentration relative, en utilisant une echelle log-log. Dans quelle gamme de DO la relation est-elle linéaire?


### Après-midi — Inoculation tubes stériles vs non stériles ✓ / ⚠️

> **Ce que "stérile" signifie vraiment** : l'air de cette pièce contient des centaines de bactéries et spores
> par mètre cube. La surface de la paillasse en contient des millions. Une culture contient ~10⁹ bactéries/mL —
> si une seule tombe dans ton tube ce soir, ses descendants seront peut-être des millions après une nuit à 37 °C.
> La flamme du bec Bunsen crée un flux d'air chaud ascendant qui éloigne les particules. C'est pour ça
> qu'on travaille juste au-dessus et qu'on rebouche rapidement.

**Étape 1 — 6 tubes LB (test de stérilité)** ⚠️

| Tube | Que faire | Résultat attendu mardi matin |
|---|---|---|
| A1, A2 | Inoculer 30 µL préculture · technique stérile | Turbide ✓ |
| B1, B2 | Ne rien ajouter · technique stérile | Limpide ✓ |
| C1, C2 | Ne rien ajouter · sans technique stérile | Turbide = contamination de l'air |

Incuber overnight 37 °C, 200 rpm. **Lire mardi matin.**

**Étape 2 — Préculture overnight pour mardi** ⚠️

2 tubes de 14 mL avec 3 mL M9 + glycérol 0,4 % :
- Tube A : inoculer 30 µL depuis colonie ou préculture. Incuber overnight 37 °C.
- Tube B : témoin stérilité (sans bactéries).

**Étape 3 — Préparer les flasques pour mardi** ⚠️

Préparer 4 erlenmeyers de 250 mL avec 50 mL de milieu chacun :
M9 + glucose 0,02 % · M9 + glucose 0,2 % · M9 + glucose 0,4 % · LB (sans glucose).
Ne pas inoculer ce soir — **inoculation mardi matin dès l'arrivée**.

### Programmation — Notebook A §A1 ✓

§A1 : multiplication répétée, tracé linéaire et logarithmique, lecture graphique du temps de doublement.
Durée estimée : 1h30-2h. Si le temps manque, finir pendant les pauses de mardi.

### À la fin de J1, tu dois avoir
- ☑ 6 tubes LB (A/B/C) à l'incubateur
- ☑ 2 tubes M9 glycérol (culture de nuit + témoin) à l'incubateur
- ☑ 4 erlenmeyers préparés (pas encore inoculés)
- ☑ §A1 commencé ou terminé

---

## J2 — Mardi S1 · Courbe de croissance manuelle

**Objectif** : mesurer à la main comment les bactéries croissent selon la quantité de nutriments.

### Avant de commencer (9h)
- ☑ Vérifier les tubes A/B/C du lundi : turbidité correcte ?
- ☑ ⚠️ Inoculer les 3 flasques M9 + glucose avec la culture de nuit, dilution 1:100
- ☑ Commencer immédiatement les mesures OD (T+0) et mettre les flasques à incuber (37 °C, 200 rpm)

> **Flasque LB** : inoculer seulement à T+120 min (après 2h), dilution 1:200, car elle pousse plus vite.

### Protocole de mesure OD ✓

| Heure | Intervalle |
|---|---|
| T+0 (9h30) | Mesure initiale + vérification tubes lundi |
| T+60 min (10h30) | 1h |
| T+120 min (11h30) | 1h · **inoculer flasque LB ici** |
| T+150 min (12h00) | 30 min |
| T+180 min (12h30) | 30 min |
| T+210 min (13h00) | 30 min |
| T+240 min (13h30) | 30 min |
| T+260 min (13h50) | 20 min |
| … | 20 min jusqu'à ~16h |

**Comment mesurer :**
1. ☑ Prélever 1 mL de culture dans une cuvette propre
2. ☑ Insérer dans le spectrophotomètre, lire à 600 nm
3. ☑ Tourner la cuvette de 180° et lire à nouveau — noter les 2 valeurs
4. ☑ Jeter la cuvette (déchets biologiques)

> ⚠️ Si OD > 0,8 : diluer 1:5 dans le même milieu, multiplier le résultat par 5.
> Attention aux bulles dans la cuvette — elles faussent la lecture.

**Blanc** : cuvette de LB seul ou M9 seul (sans bactéries), à remettre à zéro avant chaque série.

### Notation ✓

```
temps_min, glu_002, glu_02, glu_04, LB
0,    0.05, 0.05, 0.05,
60,   0.06, 0.07, 0.08,
120,  0.09, 0.12, 0.15, 0.05
...
```

Sauvegarder en `.csv` — sera chargé dans le Notebook A §A4.
(1 flasque par condition. Les réplicats seront mesurés mercredi avec le lecteur de plaque.)

### Programmation — Notebook A §A2 ✓

**Quand** : pendant les pauses entre les mesures (20–30 min chacune).

§A2 : `simulate_one` (une trajectoire stochastique), puis 30 trajectoires, moyenne et variance.
Ne pas interrompre les mesures pour finir une cellule — avancer au rythme des pauses.

### Points d'attention
- La flasque glucose 0,02 % entrera en phase stationnaire bien avant les autres — prévu.
- La flasque LB pousse plus vite et à un OD plus élevé — milieu riche, normal.
- Si OD ne monte pas après 2h : appeler Thomas.

### Préparation pour mercredi ⚠️

En fin d'après-midi : préparer 1 tube 14 mL avec 3 mL M9 + glycérol 0,4 %, inoculer MG1655. Overnight 37 °C.

### À la fin de J2, tu dois avoir
- ☑ Tableau de mesures complet (≥ 10 points par flasque), sauvegardé en CSV
- ☑ §A2 avancé ou terminé
- ☑ Culture overnight MG1655 à l'incubateur

---

## J3 — Mercredi S1 · Diauxie en lecteur de plaque (overnight)

**Objectif** : comparer la croissance sur différentes sources de carbone ; observer la diauxie.

### Préparation des milieux ⚠️ (Thomas prépare les stocks)

| Condition | Volume pour 1mL M9 |
|---|---|
| Glucose 0,02 % | 1 µL glucose 20 % |
| Glucose 0,1 % | 5 µL glucose 20 % |
| Glucose 0,2 % | 10 µL glucose 20 % |
| Lactose 0,02 % | 1 µL lactose 20 % |
| Lactose 0,1 % | 5 µL lactose 20 % |
| Glu 0,02 % + Lac 0,1 % | 1 µL glu + 5 µL lac |
| Glu 0,1 % + Lac 0,1 % | 5 µL glu + 5 µL lac |
| Blanc M9 | M9 + 10 µL glucose 20 % |

### Layout de la plaque ✓

Règle : laisser les bordures (Row A, Row F–H, Col 1, Col 10–12) et le séparateur (Col 5) vides.

```
           Col 2        Col 3       Col 4   Col 5  Col 6             Col 7             Col 8   Col 9
Row B      Glu 0,02 %   Glu 0,02 %  2nd biol repl  Lac 0,02 %        Lac 0,02 %        2nd biol repl
Row C      Glu 0,1 %    Glu 0,1 %   2nd biol repl  Lac 0,1 %         Lac 0,1 %         2nd biol repl
Row D      Glu 0,2 %    Glu 0,2 %   2nd biol repl  Glu0,02+Lac0,1 %  Glu0,02+Lac0,1 %  2nd biol repl
Row E      Blanc M9     Blanc M9    2nd biol repl  Glu0,1+Lac0,1 %   Glu0,1+Lac0,1 %   2nd biol repl
```

### Protocole d'inoculation ✓ / ⚠️

1. ☑ ⚠️ Dilution 1:20 de la culture overnight dans 5 mL M9 (250 µL dans 4750 µL).
2. ☑ Distribuer **195 µL de milieu** dans chaque puits avec la P200.
3. ☑ Ajouter **5 µL de préculture diluée** dans chaque puits.
4. ☑ Laisser les puits blancs avec M9 seul (pas de bactéries).
5. ☑ Couvrir avec le couvercle maintenu avec du parafilm.
6. ☑ ⚠️ Lancer le plate reader avec Thomas (37 °C · OD600 toutes les 3 min · 30h max).

### Programmation — Notebook A §A3 ✓

**Quand** : après le lancement du plate reader (≈ 14h–17h).

§A3 : modèle de Monod, courbe p(S), `simulate_nutrients`. Vérification N_max ∝ [glucose] si données mardi disponibles. Durée estimée : 2h.

### À la fin de J3, tu dois avoir
- ☑ Plaque lancée dans le plate reader
- ☑ §A3 avancé ou terminé

---

## J4 — Jeudi S1 · Lecture diauxie + Transformation bactérienne

**Objectif** : comprendre ce que les données de la nuit révèlent sur la régulation des gèns *lac* ; introduire un nouveau gène dans une bactérie.

### Matin — Transformation TSS ⚠️ (Thomas supervise toutes les étapes)

La **transformation** permet d'introduire un plasmide (ADN circulaire portant le gène GFP) dans une bactérie.
Si ça marche, les bactéries brilleront en vert sous UV.

Grandes étapes (protocole détaillé fourni par Thomas) :
1. ☑ Mélanger cellules compétentes + ADN plasmidique sur glace — 30 min.
2. ☑ Ajouter LB pré-chaud. Incuber **1h** à 37 °C sans agiter. → Programmation pendant ce temps.
3. ☑ Centrifuger, jeter le surnageant, remettre en suspension.
4. ☑ Étaler sur LB + kanamycine. Incuber overnight.

### Programmation — Notebook A §A3 fin + §A4 début ✓

**Quand** : pendant l'incubation de récupération (1h — étape 2) et après-midi.

§A3 fin : `simulate_nutrients` avec paramètres variés.
§A4 début : importer les données diauxie, premier tracé.

### Après-midi — Lecture et discussion diauxie ✓ / ⚠️

1. ☑ ⚠️ Arrêter le plate reader avec Thomas.
2. ☑ Exporter les données en `.txt` → copier dans Google Drive.
3. ☑ Notebook A §A4 : charger et tracer les données.

> Questions à explorer : Dans quels puits voit-on un creux dans la courbe OD ?
> Pourquoi la bactérie s'arrête-t-elle avant de repartir ?
> La hauteur du premier plateau dépend-elle de la concentration en glucose ?

### À la fin de J4, tu dois avoir
- ☑ Plaque de transformation à l'incubateur
- ☑ Données diauxie chargées dans §A4
- ☑ §A4 commencé

---

## J5 — Vendredi S1 · Vérification transformation + analyse données

**Objectif** : vérifier la transformation ; terminer l'analyse de données.

### Matin ✓ / ⚠️

1. ☑ Compter les colonies sur les plaques.
   - **> 10 colonies** sur "+ADN" → transformation réussie ✓
   - **0 colonie** sur "−ADN" → contrôle OK ✓
2. ☑ ⚠️ Piquer 2–3 colonies résistantes dans 3 mL LB + Kan50. Overnight.
3. ☑ [OPTIONNEL] Passer une colonie sous la lampe UV (312 nm) : fluorescence verte ?

### Programmation — Notebook A §A4 ✓

**Quand** : toute la journée.

§A4 : comparaison simulation Monod vs données expérimentales (courbe croissance + diauxie).
Si §A4 terminé avant 14h → commencer §B1 (interrupteur stochastique).

### À la fin de J5, tu dois avoir
- ☑ Colonies vérifiées
- ☑ Tubes LB + Kan50 à l'incubateur
- ☑ §A4 terminé

---

## [Dimanche S2 — Thomas uniquement]

Thomas inocule les précultures overnight Plac-GFP et lacUV5-GFP dans M9 + glycérol 0,4 % + Kan50.

---

## J6 — Lundi S2 · Expérience d'induction (lecteur de plaque)

**Objectif** : mesurer comment les deux souches répondent quantitativement à l'IPTG et au TMG (voir les explications dans le notebook B).

### Matin — Plaque d'induction ✓ / ⚠️

#### Dilutions d'inducteur

| Concentration finale | Volume à ajouter par puits |
|---|---|
| 0 µM | 2 µL eau |
| 1 µM | 2 µL depuis tube 100 µM |
| 3 µM | 2 µL depuis tube 300 µM |
| 10 µM | 2 µL depuis tube 1 mM |
| 30 µM | 2 µL depuis tube 3 mM |
| 100 µM | 2 µL depuis stock 10 mM |

#### Layout de la plaque d'induction

```
Colonnes     1         2    3    4    5    6  |    7         8    9   10   11   12
          [IPTG]=0*   1    3   10   30  100  | [TMG]=0*    1    3   10   30  100 µM

Row A     Plac-GFP (réplicat 1)               | Plac-GFP (réplicat 1)
Row B     Plac-GFP (réplicat 2)               | Plac-GFP (réplicat 2)
Row C     lacUV5-GFP (réplicat 1)             | lacUV5-GFP (réplicat 1)
Row D     lacUV5-GFP (réplicat 2)             | lacUV5-GFP (réplicat 2)
Row E     Blancs (M9 + glycérol + Kan50)      | Blancs
```

\* Colonnes 1 et 7 ([I]=0) = référence autofluorescence (fluorescence naturelle sans inducteur).

#### Séquence de pipetage ✓

> Règle : toujours des concentrations faibles vers les fortes. Ne jamais revenir en arrière.

**Étape 1 — Inducteur (2 µL/puits)** : commencer par les blancs et [I]=0, puis colonne par colonne.
Changer de cône entre chaque concentration.

**Étape 2 — Bactéries (198 µL/puits)** :
- ☑ Dilution 1:1000 des cultures de nuit dans milieu minimum M9 + glycerol 0,4 % + Kan50
- ☑ Rows A–B : 198 µL culture Plac-GFP (pipette multicanal par rangées).
- ☑ Rows C–D : 198 µL culture lacUV5-GFP.
- ☑ Row E : 198 µL M9 + glycérol + Kan50 seul.

- ☑ ⚠️ Couvrir et lancer avec Thomas (OD600 + GFP toutes les 3 min · 37 °C · 30h max).

### Après-midi – Programmation §B1 ✓

**Quand** : Après lancement plate reader PM.

§B1 : interrupteur stochastique, courbe probabilité p vs [I].
Si avancé : débuter §B2 (équation de Hill, n=1 vs n=2).

### À la fin de J6, tu dois avoir
- ☑ Plaque d'induction lancée
- ☑ §B1 avancé ou terminé

---

## J7 — Mardi S2 · Lecture données + [FACULTATIF] Microscopie

**Objectif** : analyser les données d'induction ; observer si possible la bistabilité.

### Matin ✓ / ⚠️

1. ☑ ⚠️ Arrêter le plate reader, exporter `.txt`, copier dans Drive.
2. ☑ Vérifications dans Notebook B §B3 :
   - Courbes OD croissantes pour rows A–D ?
   - Signal GFP visible à [I] = 100 µM ?
   - Colonnes 1 et 7 : RFU/OD stable en phase exponentielle ?
3. ☑ Si données correctes → §B3 l'après-midi. Si problème → discuter avec Thomas.

### Programmation — Notebook B §B1 fin + §B2 ✓

**Quand** : pendant la lecture AM + après-midi.

§B1 fin + §B2 : équation de Hill, effet de K et de n.
Si données prêtes : commencer §B3 (normalisation RFU/OD).

### [FACULTATIF] Après-midi — Microscopie agar pads ⚠️

> Uniquement si les données de la plaque sont correctes.

Préparer 4 concentrations de TMG (0, 5, 20, 100 µM) pour chaque souche dans M9 + glycérol + Kan50.
Incuber 1h à 37 °C. Puis agar pads + acquisition (voir protocole complet avec Thomas).

---

## J8 — Mercredi S2 · ImageJ + Analyse [FACULTATIF]

**Objectif** : mesurer la fluorescence cellule par cellule ; construire les histogrammes de distribution.

### [FACULTATIF] Analyse ImageJ ⚠️ (prise en main avec Thomas)

1. ☑ Ouvrir `.tif` dans FIJI · *Image > Type > 8-bit*.
2. ☑ *Image > Adjust > Threshold* → ajuster pour sélectionner les bactéries.
3. ☑ *Analyze > Analyze Particles* : taille 1–20 µm², "Display results".
4. ☑ *Analyze > Set Measurements* : cocher "Mean Gray Value". Puis *Measure*.
5. ☑ *File > Save As > Results* → nommer `imagej_tmg_XXuM.csv`.
6. ☑ Répéter pour les 4 concentrations × 2 souches.

### Programmation — Notebook B §B3 + Notebook C [FACULTATIF] ✓

§B3 : normalisation RFU/OD, courbes dose-réponse, lecture graphique K_half, superposition Hill.
Notebook C §C1 (simulation bistabilité) + §C2 (histogrammes depuis CSV ImageJ).

### À la fin de J8, tu dois avoir
- ☑ §B3 terminé
- ☑ Figures finales prêtes pour le rapport/la présentation

---

## J9 — Jeudi S2 · Rapport et/ou présentation

**Structure suggérée (≈ 20 min)**

1. Question biologique (2 min) : comment les bactéries utilisent-elles différents nutriments ?
2. Expérience 1 — Croissance (5 min) : courbe de croissance + simulation Monod + diauxie
3. Expérience 2 — Induction (8 min) : courbes dose-réponse + Hill + K_half
4. [FACULTATIF] Microscopie (3 min) : distributions de fluorescence, bimodalité TMG
5. Ce que j'ai appris / ce qui m'a surpris (2 min)

**Figures à préparer (minimum 3)**
- ☑ Courbe de croissance manuelle + simulation Monod
- ☑ Courbe diauxie + annotation des deux phases
- ☑ Courbes dose-réponse Plac-GFP vs lacUV5-GFP + Hill ajusté

> Pour exporter une figure du notebook : clic droit sur la figure → "Enregistrer l'image sous".

---

## Annexe — Tableau des notebooks

| Notebook | Sections | Quand | Durée estimée |
|---|---|---|---|
| **A** — Croissance | §A1 (Lun S1) · §A2 (Mar S1) · §A3 (Mer S1) · §A4 (Jeu–Ven S1) | Semaine 1 | ~4 demi-journées |
| **B** — Induction | §B1 (Lun S2) · §B2 (Mar S2) · §B3 (Mar–Mer S2) | Semaine 2 | ~3 demi-journées |
| **C** — Hétérogénéité [FACULTATIF] | §C1 bistabilité · §C2 ImageJ | Mer–Jeu S2 | ~1–2 demi-journées |

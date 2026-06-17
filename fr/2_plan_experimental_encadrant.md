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
- Boite de petri avec colonies (*E. coli* MG1655).

### Matin — pipetage et dilutions

1. Démonstration des pipettes : réglage, prise de cône, technique de pipetage.
2. **Exercice dilutions en série** : préparer 6 dilutions ×10 successives du colorant dans l'eau (1:10 → 1:10⁶) dans des Eppendorf de 1,5 mL. Volume final = 100 µL à chaque étape.
   - Vérification visuelle : l'absorbance doit décroître de façon visible.
   - [OPTIONNEL] Mesure au nanodrop ou spectro pour quantifier.
3. Discussion : quelle est la concentration dans le tube n°6 si le tube n°1 est à 1 mg/mL ?

Utiliser la dilution en série pour mesurer la relation entre concentration bacterienne et DO600: 
   - Préparer 6 dilutions ×10 successives d'une culture de nuit dans du MgSO4 10mM (1 → 1:10⁶) dans des Eppendorf de 1,5 mL. Volume final = 900 µL à chaque étape.
   - Mesure au spectro.
   - Tracer DO600 vs concentration relative, en utilisant une echelle log-log.


### Après-midi — inoculation tubes stériles vs non stériles

4. Préparer 6 tubes de 14 mL avec 3 mL LB chacun :
   - Tubes A1, A2 : inoculer 30 µL préculture (dilution 1:100), **avec** technique stérile (brûlage bec Bunsen ou hotte).
   - Tubes B1, B2 : non inoculés, **avec** technique stérile (témoins stérilité — pas de bactéries ajoutées).
   - Tubes C1, C2 : non inoculés, **sans** technique stérile  (témoins stérilité — pas de bactéries ajoutées).
   [OPTIONNEL] toucher furtivement le cône pour B2.
   - Incuber overnight 37 °C, 200 rpm.
   - **Lire le résultat mardi matin** : turbidité dans A (attendu), B (non attendu), C (attendu ou non) ?

5. Préparer une culture pour la **courbe de croissance manuelle de mardi** ("culture de nuit"), avec technique stérile :
   - 2 tubes de 14 mL : milieu minimum M9 + glucose 0,2 % (3 mL).
   - Inoculer un tube avec une colonie – le second tube est un controle de stérilité.
   - Incuber overnight 37 °C, 200 rpm.

6. Préparer les flasques pour les **courbe de croissance manuelle de mardi** :
   - 4 flasques (erlenmeyer) de 250 mL : milieu minimum M9 + glucose 0,02 % / 0,2 % / 0,4 % et LB (50 mL chacun).
   - Le mardi matin dès l'arrivée, inoculer avec la "culture de nuit" et démarrer la mesure.

> **Point pédagogique** : expliquer pourquoi on travaille stérilement et ce que "stérile" signifie vraiment.

### Programmation — Notebook A §A1

**Quand** : après l'inoculation des tubes (≈ 15h–17h).

§A1 complet : multiplication répétée, tracé linéaire et logarithmique, lecture graphique du temps de doublement.
Durée estimée : 1h–1h30. Pas de pression — si le temps manque, §A1 peut déborder sur les pauses de mardi.

---

## J2 — Mardi S1 · Courbe de croissance manuelle

**Objectif** : mesurer une courbe de croissance bactérienne à la main, comprendre la phase de latence, la phase exponentielle, et la phase stationnaire.

### Matériel
- 4 flasques de 250 mL inoculés lundi soir
- Spectrophotomètre OD600
- Cuvettes jetables
- Feuille de papier millimétré et/ou tableur pour noter les mesures

### Protocole de mesure

- Inoculer les 3 flasques avec milieu minimum M9 avec la culture de nuit, dilution 1:100. Commencer les mesures et incuber overnight 37 °C, 200 rpm.
- Après 2h, inoculer la flasque avec LB avec la culture de nuit, dilution 1:200. Inclure dans les mesures à partir de ce point et incuber overnight 37 °C, 200 rpm.

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

NB: augmenter la frequence de mesure (après 1 h) pour la condition LB.

- Mesure OD : pipetter 1 mL de culture dans une cuvette, lire à 600 nm, tourner la cuvette de 180º et lire à nouveau noter les 2 valeurs. Attention aux bulles!
- Blanc : LB seul ou milieu minimum M9 seul sans bactéries (préparer 1 tube blanc par concentration de glucose).
- Si OD > 0,8 : diluer 1:5 dans le milieu correspondant avant mesure, multiplier la valeur lue par 5.

### Notation recommandée

```
temps_min, glu_002, glu_02, glu_04, LB
0,    0.05, 0.05, 0.05, (mesures LB démarrent à T+120 min)
60,   0.06, 0.07, 0.08,
120,  0.09, 0.12, 0.15, 0.05
...
```
NB : 1 flasque par condition. Les réplicats seront faits lors de l'expérience en plaque reader (J3).

Sauvegarder en `.csv` — sera chargé dans le Notebook A §A4.

### Points d'attention
- Les valeurs vont augmenter plus tôt et beaucoup plus vite pour la flasque avec LB – c'est pour ça qu'on l'inocule plus tard.
- La flasque 0,02 % glucose seront en phase stationnaire bien avant les autres flasques avec milieu minimum M9.
- Si l'OD ne monte pas après 2h : vérifier que les cultures ont été inoculées.
- La phase de latence peut durer 30 min ou plusieurs heures selon l'état de la préculture et la dilution de la culture de nuit.


### Programmation — Notebook A §A2

**Quand** : pendant les pauses entre les mesures OD (20–30 min chacune).

§A2 : `simulate_one` (une trajectoire stochastique), puis 30 trajectoires, moyenne, variance.
Ne pas interrompre les mesures pour la programmation — avancer au rythme des pauses.

---

### Préparation pour Mercredi
- Préparer une culture pour la **courbe de croissance pour la manip en plaque reader** ("culture de nuit"), avec technique stérile – cf point 5 de Lundi après-midi.

---

## J3 — Mercredi S1 · Plaque reader diauxie (overnight)

**Objectif** : comparer la croissance sur différents nutriments (sources de carbone); observer la croissance sur deux sources de carbone mélangées – mettre en évidence la diauxie.

### Matériel
- Plaque 96 puits noire à fond transparent (pour fluorescence future) ou fond plat transparent
- M9 Minimal Salts 5× (Difco) + glycérol 50 % + MgSO₄ 1 M (voir Annexe 1)
- Glucose 20 % stock stérile (autoclavé ou filtré)
- Lactose 20 % stock stérile
- Préculture *E. coli* MG1655 overnight en M9 + glycérol 0,4 % (OD ~1–2)
- Parafilm

### Préparation des milieux (volumes finaux 200 µL/puits)

| Condition | Concentration finale | Stock utilisé |
|---|---|---|
| Glucose seul | 0,02 % / 0,1 % / 0,2 % | Glucose 20 % : 1 µL / 5 µL / 10 µL dans 1 mL M9 |
| Lactose seul | 0,02% / 0,1 % | Lactose 20 % : 1 µL / 5 µL dans 1 mL M9 |
| Glu 0,02 % + Lac 0,1 % |   | 1 µL glu + 5 µL lac dans 200 µL M9 |
| Glu 0,2 % + Lac 0,1 % |   | 5 µL glu + 5 µL lac dans 200 µL M9 |
| Blanc (M9 0,2% glucose, pour controle contamination) | — | Glucose 20 % : 10 µL dans 1 mL M9 |

### Layout de la plaque diauxie
Règle : laisser les bordures (Row A, Row F–H, Col 1, Col 10–12) vides.

```
           Col 2        Col 3       Col 4   Col 5  Col 6             Col 7             Col 8   Col 9
Row B      Glu 0,02 %   Glu 0,02 %  2nd biol repl  Lac 0,02 %        Lac 0,02 %        2nd biol repl
Row C      Glu 0,1 %    Glu 0,1 %   2nd biol repl  Lac 0,1 %         Lac 0,1 %         2nd biol repl
Row D      Glu 0,2 %    Glu 0,2 %   2nd biol repl  Glu0,02+Lac0,1 %  Glu0,02+Lac0,1 %  2nd biol repl
Row E      Blanc M9     Blanc M9    2nd biol repl  Glu0,1+Lac0,1 %   Glu0,1+Lac0,1 %   2nd biol repl
```

> 2 réplicats techniques x 2 réplicats biologiques par condition + 4 blancs. Peut être adapté.

8 conditions × 4 réplicats = 32 puits.

### Protocole d'inoculation

1. Préparer une dilution 1:20 de la culture de nuit (OD ~0,02–0,05) dans 5 mL de milieu minimum M9.
2. Distribuer 195 µL de milieu (M9 + glucose/lactose aux concentrations finales) dans chaque puits.
3. Ajouter 5 µL de la préculture diluée dans chaque puits (inoculum final ~0,002–0,005 OD).
4. Couvrir avec un couvercle ou du Parafilm perforé.
5. Lancer le plate reader :
   - 37 °C, agitation orbitale forte (300 rpm ou "normal")
   - Lecture OD600 toutes les 3 min
   - Durée : 30h maximum — interrompre dès que toutes les conditions ont atteint la phase stationnaire.


### Programmation — Notebook A §A3

**Quand** : après le lancement du plate reader (≈ 14h–17h).

§A3 : modèle de Monod, courbe p(S), `simulate_nutrients`.
Si les données de mardi sont disponibles : commencer la vérification N_max ∝ [glucose].
Durée estimée : 2h.

---

## J4 — Jeudi S1 · Lecture diauxie + Transformation TSS

**Objectif** : analyser les données de la nuit et introduire la transformation bactérienne.

### Matin — Transformation TSS (pUA66-lacUV5 → MG1655)

Le protocole detaillé sera communiqué par Thomas.

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
- L'incubation de récupération (étape 8, 1h) est le bon moment pour la programmation (voir bloc ci-dessous).
- Si aucune colonie vendredi : utiliser le stock glycérol de pUA66-lacUV5/MG1655 existant (si disponible) ou redo.


### Programmation — Notebook A §A3 fin + §A4 début

**Quand** : pendant l'incubation de récupération post-transformation (étape 8 — 1h).

§A3 fin : `simulate_nutrients` avec paramètres variés.
§A4 début : import des données diauxie, premier tracé.

---

### Après-midi — lecture et discussion diauxie

1. Arrêter le plate reader.
2. Exporter les données en `.txt` (format BioTek Gen5 — voir Notebook A §A4 pour le parsing).
3. Discussion avec le stagiaire : quels puits montrent un "creux" dans la courbe OD ? Pourquoi ?
   Relier à la régulation de l'opéron *lac* : la bactérie attend l'épuisement du glucose avant d'induire *lacZ*.
4. Analyse des données diauxie (J3) : visualisation, identification du creux de diauxie.
---

## J5 — Vendredi S1 · Vérification transformation + analyse données

**Objectif** : vérifier les résultats de la transformation, finaliser l'analyse de données, préparer la semaine 2.

Et refaire une des experiences si necessaire.

### Matin

1. **Compter les colonies** : attendu > 10 sur "+ADN", < 2 sur "−ADN".
2. **Pick 2–3 colonies** Kan-résistantes dans 3 mL LB + Kan50. Incuber overnight pour preparation d'un stock glycérol.
3. **[OPTIONNEL]** Spot d'induction rapide : étaler une colonie sur LB + Kan50 + IPTG 100 µM.
   Fluorescence visible sous lampe UV (312 nm) le lendemain si la transformation a fonctionné.
4. Comparer les courbes de croissance manuelles (J2) et les mesures automatisées (J3) dans le notebook.
5. §A4 (suite et fin). Si §A4 terminé : commencer §B1 en option.


### Programmation — Notebook A §A4

**Quand** : après la vérification des colonies (≈ 10h30 et tout l'après-midi).

§A4 : comparaison simulation Monod vs données plate reader (diauxie incluse).
Si §A4 est terminé avant la fin de journée : commencer §B1 (interrupteur stochastique, courbe p vs [I]).

---

## [Dimanche S2 — Thomas uniquement]

- Inoculer Plac-GFP/MG1655 : 1 colonie fraîche ou 5 µL glycérol → 3 mL M9 0,2 % arabinose + Kan50. Overnight 37 °C, 200 rpm.
- Inoculer pUA66-lacUV5/MG1655 : même chose depuis 2 colonies de Ven S1 (pour stock glycerol et sequencage).

---

## J6 — Lundi S2 · Expérience d'induction (plaque reader)

**Objectif** : mesurer quantitativement la réponse des deux souches à l'IPTG et au TMG.

### Matin — préparation et lancement lecteur de plaque

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
Row E     Blancs M9 + Kan50 (milieu seul)      | Blancs M9 + Kan50
Row F–H   (vides)
```

\* **Colonnes 1 et 7 ([I]=0) = référence autofluorescence.** Ces puits mesurent la fluorescence endogène des bactéries (principalement les flavines), indépendante de la GFP. Ils servent à corriger toutes les autres valeurs RFU/OD (voir Notebook B §B3).

Total : 48 puits bactéries + 12 blancs + 36 vides = 96 puits.

#### Protocole de pipetage (séquence recommandée)

1. **Distribuer l'inducteur** : ajouter 2 µL de la dilution de travail correspondante dans chaque puits (commencer par les blancs = 2 µL eau).
   - Utiliser une pipette multicanal (8 canaux) en pipetant par colonnes : Col 1 = eau (conc 0), Col 2 = 100 µM IPTG, etc.
2. **Distribuer les bactéries** : ajouter 198 µL de culture par puits (dilution 1:1000 des cultures de nuit dans milieu minimum M9 + glycerol 0,4 % + Kan50).
   - Pipette multicanal par rangées : Row A = 198 µL culture Plac-GFP, Row D = 198 µL culture lacUV5-GFP.
   - Pour les blancs (Row E) : 198 µL M9 + glycérol 0,4 % + Kan50 seul.

#### Paramètres plate reader BioTek [À VÉRIFIER]
- Lecture OD600 : filtre 600 nm
- Lecture GFP : excitation 470/20 nm, émission 525/20 nm
- Agitation : orbitale, 30 sec avant lecture
- Température : 37 °C
- Intervalle : 3 min
- Durée : 30h

> **Lecture autofluorescence** : les colonnes 1 et 7 ([I]=0) mesurent la fluorescence
> endogène. Pour une correction fiable, s'assurer que ces puits sont en **phase
> exponentielle** lors de la lecture (OD ~0,1–0,4) — l'autofluorescence par cellule
> y est stable. Éviter la phase stationnaire où l'état métabolique change.

### Après-midi — Programmation

- Notebook B **§B1** (interrupteur stochastique, courbe p vs [I]).
- Si avancé : débuter **§B2** (équation de Hill, n=1 vs n=2).

---

## J7 — Mardi S2 · Lecture données + [FACULTATIF] microscopie

**Objectif** : analyser les premières données d'induction et, si possible, observer la bistabilité au microscope.

### Matin — lecture et évaluation

1. Lire les données exportées depuis le BioTek (fichier `.txt`).
2. Vérification rapide : courbes OD croissantes ? Signal GFP visible à [IPTG] = 100 µM ?
3. Vérifier les colonnes 1 et 7 ([I]=0) : RFU/OD stable pendant la phase exponentielle ? C'est la référence autofluorescence pour la correction (Notebook B §B3).
4. Si données propres → Notebook B §B3 l'après-midi.
5. Si problème (pas de croissance, signal GFP absent, contamination) → discuter avec Thomas, refaire si nécessaire.

### Après-midi [FACULTATIF] — Microscopie agar pads

> **Prérequis** : les données de la plaque reader doivent être propres (croissance OK, signal GFP visible). Sinon refaire l'experience de Lundi.

#### Préparation des cultures

Préparer 4 conditions TMG pour la culture lacUV5-GFP et pour la culture Plac-GFP en phase exponentielle :
- [TMG] = 0, 5, 20, 100 µM (tubes Eppendorf séparés, 100 µL chacun)
- milieu minimum M9 + glycerol 0,4 % + Kan 50.
- Incuber à 37 °C, 200 rpm.

#### Préparation agar pads

1. Faire fondre 1–2 mL agarose 1 % dans milieu minimum M9 (microwave, ~30 sec).
2. Déposer ~30 µL sur une lame de verre. Poser une seconde lame dessus (sandwich).
3. Laisser solidifier 5 min.
4. Séparer délicatement les lames : garder la lame avec l'agar pad.

#### Montage et acquisition

5. Déposer 2 µL de bactéries sur l'agar pad. Laisser evaporer la goutte. Couvrir avec une lamelle.
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
7. Répéter pour les 4 conditions et les 2 souches.

Ces CSV sont chargés dans le notebook induction Notebook C.

### Notebook B §B3 + Notebook C (si pas déjà fait)

- §B3 : chargement données plate reader, normalisation RFU/OD, courbes dose-réponse, fit K_half.
- Notebook C [FACULTATIF] : histogrammes single-cell, bimodalité.

---

## J9 — Jeudi S2 · Preparation rapport et/ou présentation

**Durée** : ~20 min de présentation + 10 min de questions.

### Structure suggérée

1. **Question biologique** (2 min) : comment les bactéries utilisent-elles différent nutriments ?
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

> Ces milieux sont préparés par le labo avant le stage.

| Milieu | Composition | Stérilisation |
|---|---|---|
| LB liquide | 10 g/L NaCl, 10 g/L tryptone, 5 g/L extrait de levure | Autoclave 121 °C, 20 min |
| LB + Kan50 | LB + kanamycine 50 µg/mL | Ajouter kanamycine après refroidissement (< 55 °C) |
| LB gélosé | LB + agar 15 g/L | Autoclave, couler après refroidissement à ~55 °C |
| LB gélosé + Kan50 | LB gélosé + kanamycine 50 µg/mL | Ajouter kanamycine avant coulage (< 55 °C) |
| M9 Minimal Salts 5× | Disodium phosphate 33,9 g/L + KH₂PO₄ 15 g/L + NaCl 2,5 g/L + NH₄Cl 5 g/L | Autoclave 121 °C, 15 min |
| M9 1× + glycérol 0,4 % | M9 5× : 200 mL + eau stérile : 750 mL + glycérol 50 % stérile : 8 mL + MgSO₄ 1 M stérile : 2 mL (± CaCl₂ 1 M : 0,1 mL) qsp 1 L | Dilution aseptique |
| M9 + glycérol + Kan50 | M9 1× + glycérol 0,4 % + kanamycine 50 µg/mL | Ajouter Kan après assemblage |

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

### Glycérol (stock 50 %)
- Mélanger 50 g de glycérol pur + eau ultra-pure qsp 100 mL.
- Filtrer sur 0,22 µm (ne **pas** autoclaver — le glycérol est hygroscopique).
- Aliquoter 10 mL, stocker à température ambiante ou à 4 °C.
- Pour M9 + glycérol 0,4 % (1 L) : ajouter **8 mL** de stock 50 %.

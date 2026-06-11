# Plan expérimental — Stage · Microbiologie quantitative
### Ce document est à toi. Garde-le avec toi pendant tout le stage.

---

**Comment lire ce plan**
- ✓ = tu peux faire cette étape seul·e
- ⚠️ = demande l'aide ou la supervision de Thomas
- ☑ = case à cocher quand c'est fait

---

## Lundi S1 — Prise en main du laboratoire

### Objectif de la journée
Apprendre à utiliser les pipettes et à travailler stérilement.
Inoculer tes premières cultures bactériennes.

---

### Matin — Règles de sécurité et pipetage ⚠️ (avec Thomas)

**Règles essentielles** :
- Blouse et gants obligatoires dès que tu manipules des bactéries ou des réactifs
- Ne jamais manger, boire, ou toucher ton visage au labo
- Tout ce qui a touché des bactéries va dans la poubelle déchets biologiques (sac orange ou autoclave)
- Si tu renverses quelque chose : ne pas paniquer, appeler Thomas

**Exercice de pipetage — dilutions en série**

Tu vas apprendre à utiliser les trois pipettes du labo (P20, P200, P1000).
L'objectif est de préparer 6 dilutions successives au facteur 10 d'un colorant.

Matériel sur la paillasse :
- Pipettes P20 (0–20 µL), P200 (20–200 µL), P1000 (200–1000 µL)
- Cônes (pointes) correspondants — changer de cône à chaque prélèvement
- 7 tubes Eppendorf 1,5 mL numérotés 0 à 6
- Solution de colorant concentré (tube 0 = 1 mg/mL)
- Eau dans un petit flacon

Protocole :
1. ☑ Prélever 900 µL d'eau avec la P1000 et les mettre dans les tubes 1 à 6
2. ☑ Prélever **100 µL du tube 0** (colorant pur) et les ajouter dans le tube 1
   → Mélanger en pipetant 5× de haut en bas. Changer de cône.
3. ☑ Prélever **100 µL du tube 1** et les ajouter dans le tube 2. Mélanger. Changer de cône.
4. ☑ Répéter jusqu'au tube 6.
5. ☑ Observer : la couleur doit diminuer progressivement à chaque tube.

> Si la couleur du tube 6 est encore visible, quelque chose s'est mal passé — recommencer et chercher où.

---

### Après-midi — Inoculation de tubes de culture ✓

**Ce qu'on fait** : tu vas inoculer des tubes de milieu LB avec des bactéries *E. coli*.
Certains tubes seront inoculés en travaillant stérilement, d'autres sans précaution.
Le résultat sera visible mercredi matin (contamination ou non).

Matériel :
- 6 tubes de 14 mL avec 3 mL LB chacun (préparés par Thomas)
- Préculture *E. coli* MG1655 dans LB (tube jaune-orange, turbide)
- Bec Bunsen (ou hotte à flux laminaire)
- Pipette P200 + cônes
- Marqueur pour étiqueter

Protocole :
1. ☑ Étiqueter les 6 tubes : A1, A2 (stérile), B1, B2 (non stérile), C1, C2 (blanc)

**Tubes A1 et A2 — technique stérile :**
2. ⚠️ Allumer le bec Bunsen. Travailler dans le flux d'air chaud au-dessus de la flamme.
3. ☑ Flamber brièvement le bouchon du tube de préculture.
4. ☑ Prélever **30 µL** de préculture avec la P200. Changer de cône.
5. ☑ Ouvrir le tube A1 rapidement, ajouter les 30 µL, reboucher. Répéter pour A2.

**Tubes B1 et B2 — sans précaution stérile :**
6. ☑ Sans flamme, sans changer de cône : prélever 30 µL de préculture et inoculer B1 et B2.
   (Poser le bouchon sur la paillasse, laisser le tube ouvert quelques secondes)

**Tubes C1 et C2 — blancs (pas de bactéries) :**
7. ☑ Ne rien ajouter dans C1 et C2. Garder fermés.

8. ☑ Mettre les 6 tubes à l'incubateur (37 °C, 200 rpm).

**Inoculation des tubes pour la courbe de croissance de mardi :**
9. ⚠️ Avec Thomas : préparer 9 tubes LB + glucose (3 concentrations × 3 réplicats).
   Thomas prépare le glucose, tu inocules.

---

### En fin d'après-midi — Notebook A §A1 ✓
→ Ouvrir le **Notebook A** sur Google Colab.
→ Faire **§A1** complet : multiplication répétée, tracé linéaire, échelle logarithmique, lecture graphique du temps de doublement.

### À la fin de la journée, tu dois avoir
- ☑ Réussi à faire les 6 dilutions (couleur progressivement plus claire)
- ☑ 6 tubes inoculés (A1-A2, B1-B2, C1-C2) à l'incubateur
- ☑ 9 tubes pour la courbe de croissance à l'incubateur
- ☑ §A1 du Notebook A terminé

---

## Mardi S1 — Courbe de croissance bactérienne

### Objectif de la journée
Mesurer toi-même comment une population bactérienne croît dans le temps.
Tu prendras une mesure toutes les 20 minutes pendant ~6 heures.

---

### Avant de commencer
- ☑ Tes 9 tubes de culture (glucose 0,02 % / 0,2 % / 0,4 %, 3 réplicats chacun) sont à l'incubateur depuis hier soir
- ☑ Spectrophotomètre allumé et réglé sur **600 nm**
- ☑ Cuvettes jetables disponibles (en prendre 20)
- ☑ Feuille de données ou tableur ouvert (voir ci-dessous)

**Tableau de données à remplir** (exemple) :

| Temps (min) | Glu 0.02% R1 | Glu 0.02% R2 | Glu 0.02% R3 | Glu 0.2% R1 | … |
|---|---|---|---|---|---|
| 0 | | | | | |
| 20 | | | | | |
| 40 | | | | | |
| … | | | | | |

---

### Protocole — à répéter toutes les 20 minutes ✓

**Préparer le blanc (une seule fois) :**
1. ☑ Remplir une cuvette avec 1 mL de LB + glucose (même concentration que tes cultures, sans bactéries)
2. ☑ Glisser dans le spectrophotomètre → appuyer sur **Blanc/Zero**. Garder cette cuvette.

**Mesure de chaque tube :**
3. ☑ Prélever **1 mL** de culture avec la P1000 et le mettre dans une cuvette propre
4. ☑ Glisser dans le spectrophotomètre, lire la valeur OD600
5. ☑ Écrire dans le tableau
6. ☑ Jeter la cuvette (poubelle déchets biologiques)
7. ☑ Répéter pour les 9 tubes, dans le même ordre à chaque fois

> ⚠️ **Si OD > 0,8** : diluer le tube 1:2 avant de mesurer (500 µL culture + 500 µL LB dans la cuvette), puis **multiplier la valeur lue par 2**.

Programmer le minuteur selon la fréquence adaptée (20 min en phase exponentielle).

---

### Pendant les pauses entre les mesures
→ **§A2** (Notebook A) : `simulate_one`, une trajectoire, puis 30 trajectoires + moyenne + variance.
→ **§A2** : `simulate_one`, une trajectoire, puis 30 trajectoires + moyenne + variance.

---

### À la fin de la journée, tu dois avoir
- ☑ ~18 mesures par tube (une toutes les 20 min sur ~6h)
- ☑ Un tableau de données complet, sauvegardé en CSV
- ☑ Vu la courbe en forme de "S" (latence → exponentielle → plateau)

---

## Mercredi S1 — Observation de la diauxie (plate reader)

### Objectif de la journée
Vérifier tes expériences de lundi.
Lancer une expérience automatisée de croissance overnight pour observer la **diauxie**.

---

### Matin — Résultats de lundi ✓

1. ☑ Sortir les tubes A, B, C de l'incubateur.
2. ☑ Regarder la turbidité :
   - A1, A2 (stérile) : doivent être **turbides** (bactéries ont poussé) ✓
   - B1, B2 (non stérile) : normalement turbides aussi
   - C1, C2 (blanc) : doivent être **transparents** (pas de bactéries) ✓
3. ☑ Si C1 ou C2 est turbide → contamination. Discuter avec Thomas.

---

### Après-midi — Préparer la plaque pour la diauxie ⚠️ (avec Thomas pour la première fois)

**Ce que tu prépares** : une plaque 96 puits avec *E. coli* dans différentes sources de carbone.
L'objectif est de voir si les bactéries consomment glucose et lactose simultanément,
ou l'un après l'autre (diauxie).

**Plan de la plaque** (lignes = conditions, colonnes = réplicats) :

```
        Col 1    Col 2    Col 3    Col 4    Col 5    Col 6
Row A   Glu 0,02%   Glu 0,02%   Glu 0,02%   Glu 0,2%    Glu 0,2%    Glu 0,2%
Row B   Glu 0,4%   Glu 0,4%   Glu 0,4%   Lac 0,2%    Lac 0,2%    Lac 0,4%
Row C   Lac 0,4%  Glu+Lac     Glu+Lac     Glu+Lac     Glu+Lac     Blanc
```

**Protocole de remplissage :**
1. ☑ Commencer par les **blancs** : pipetter 200 µL de LB pur dans les puits blancs.
2. ☑ Pour chaque condition (ex. glucose 0,2 %) :
   a. Préparer le milieu dans un tube : LB + glucose à la bonne concentration
   b. Distribuer **190 µL** dans chaque puits de cette condition avec la P200
3. ⚠️ Ajouter **10 µL de bactéries** (culture diluée 1:100 préparée par Thomas) dans chaque puits avec bactéries
4. ☑ Couvrir la plaque avec un couvercle ou du parafilm perforé
5. ⚠️ Placer dans le plate reader BioTek. Thomas configure le programme :
   - Lecture OD600 toutes les 5 min, 37 °C, agitation orbitale, durée : nuit entière

---

### Pendant l'après-midi (en attendant)
→ Notebook A **§A3** : courbe de Monod, `simulate_nutrients`, vérification N_max ∝ [glucose] avec les données de mardi.

### À la fin de la journée, tu dois avoir
- ☑ Plaque lancée dans le plate reader pour la nuit
- ☑ §A2 complété dans le Notebook A

---

## Jeudi S1 — Diauxie + Transformation bactérienne

### Objectif de la journée
Lire et analyser les données de la nuit.
Apprendre à introduire un nouveau gène dans une bactérie (transformation).

---

### Matin — Lecture des données de diauxie ✓

1. ☑ Arrêter le plate reader avec Thomas.
2. ☑ Exporter les données en `.txt` (menu du logiciel Gen5 → Export).
3. ☑ Copier le fichier dans le dossier Google Drive du stage.
4. ☑ Ouvrir Notebook A **§A4** → charger et tracer les données.

> **Question à explorer** : trouve les puits "glucose + lactose".
> Est-ce qu'il y a un creux ou un plateau dans la courbe OD entre les deux phases de croissance ?
> Pourquoi la bactérie s'arrête-t-elle de croître avant de repartir ?

---

### Après-midi — Transformation bactérienne ⚠️ (Thomas supervise toutes les étapes)

La **transformation** permet d'introduire un plasmide (ADN circulaire) dans une bactérie.
Ici, tu vas mettre un plasmide qui code pour une protéine fluorescente verte (GFP).
Si ça marche, certaines bactéries vont briller en vert quand on les éclaire en UV.

> Cette étape est technique. Lis les étapes une par une, et ne commence pas l'étape suivante
> avant d'avoir terminé la précédente.

**Matériel (préparé par Thomas) :**
- Cellules *E. coli* MG1655 compétentes (dans la glace)
- Plasmide pUA66-lacUV5 (ADN purifié, tube Eppendorf)
- LB chaud (37 °C)
- Plaques LB + kanamycine 50 µg/mL

**Protocole :**
1. ☑ Mettre **50 µL** de cellules compétentes dans un tube Eppendorf froid
2. ☑ Ajouter **2 µL** de plasmide. Ne pas vortexer — mélanger doucement.
3. ☑ Incuber **30 min sur glace**. Minuteur = 30 min.
4. *(Pas de choc thermique pour ce protocole)*
5. ☑ Ajouter **900 µL de LB** à 37 °C. Mélanger doucement.
6. ☑ Incuber **1h à 37 °C** sans agitation. Minuteur = 60 min.
   → **Pendant cette heure** : Notebook A **§A3 fin** + **§A4 début** (import données diauxie, visualisation)
7. ☑ Centrifuger 2 min à 5000 rpm. Jeter 800 µL de surnageant.
8. ☑ Remettre en suspension dans les ~150 µL restants en pipetant doucement.
9. ☑ Étaler tout sur une plaque LB + kanamycine.
10. ☑ Retourner la plaque (couvercle en bas), la placer à l'incubateur 37 °C overnight.

> **Demain matin** : si la transformation a marché, tu verras des colonies bactériennes
> (petits points blancs) sur la plaque.

### À la fin de la journée, tu dois avoir
- ☑ Données diauxie chargées et représentées dans Notebook A §A4
- ☑ Plaque de transformation à l'incubateur

---

## Vendredi S1 — Vérification + analyse des données

### Matin — Résultats de la transformation ✓

1. ☑ Sortir la plaque de l'incubateur.
2. ☑ Compter les colonies (petits points blancs) :
   - **> 10 colonies** sur ta plaque → transformation réussie ✓
   - **< 5 colonies** → transformation peu efficace. Discuter avec Thomas.
3. ☑ Avec Thomas, piquer 2–3 colonies et les inoculer dans 3 mL LB + kanamycine overnight.
4. [OPTIONNEL] Passer une colonie sous la lampe UV (312 nm) : fluorescence verte visible ?

### Après-midi — Notebook A §A4 ✓

5. ☑ **§A4** : comparaison Monod vs données, analyse complète.
6. ☑ Comparer les courbes glucose seul vs glucose + lactose.

### À la fin de la journée, tu dois avoir
- ☑ Notebook A §A4 terminé
- ☑ Colonies inoculées overnight pour lundi

---

## [Dimanche S2 — Thomas seulement]
Thomas inocule les précultures overnight pour Plac-GFP et lacUV5-GFP dans M9 0,2 % arabinose + Kan50.

---

## Lundi S2 — Lancement de l'expérience d'induction

### Objectif de la journée
Mesurer comment deux souches bactériennes (Plac-GFP et lacUV5-GFP) répondent
à différentes doses d'inducteur. C'est l'expérience principale de la semaine 2.

---

### Matin — Vérification des cultures + Notebook B ✓

1. ☑ Vérifier les deux tubes overnight : turbides = bactéries ont bien poussé.
2. ☑ Avec Thomas : diluer chaque culture 1:100 dans M9 0,2 % arabinose + kanamycine.
   Les cultures doivent croître 2–3h supplémentaires avant l'expérience.
3. ☑ Pendant la croissance : Notebook B **§B1** (interrupteur stochastique, courbe p vs [IPTG]).

---

### Après-midi — Préparer la plaque d'induction ⚠️ (premier pipetage, avec Thomas)

**Ce que tu prépares** : une plaque 96 puits avec tes deux souches × 6 concentrations d'IPTG × 6 concentrations de TMG × 3 réplicats chacun.

**Plan de la plaque :**

```
           Col 1      Col 2  Col 3  Col 4  Col 5  Col 6 | Col 7      Col 8  Col 9  Col10  Col11  Col12
        [IPTG]=0*     1 µM   3 µM  10 µM  30 µM 100 µM | [TMG]=0*   1 µM   3 µM  10 µM  30 µM 100 µM
        (autofluo)                                       | (autofluo)

Row A   Plac-GFP (réplicat 1)                           | Plac-GFP (réplicat 1)
Row B   Plac-GFP (réplicat 2)                           | Plac-GFP (réplicat 2)
Row C   lacUV5-GFP (réplicat 1)                         | lacUV5-GFP (réplicat 1)
Row D   lacUV5-GFP (réplicat 2)                         | lacUV5-GFP (réplicat 2)
Row E   Blancs (M9 0,2 % arabinose + kanamycine, pas de bactéries)      | Blancs
Row F–H (vides)
```

> *Les colonnes 1 et 7 ([I]=0) mesurent la fluorescence naturelle des bactéries
> (autofluorescence des flavines) — une correction importante pour l'analyse.

**Dilutions d'inducteur préparées par Thomas :**

| Colonne | Concentration finale | Tube à utiliser |
|---|---|---|
| 1 et 7 | 0 µM | Tube "eau" |
| 2 et 8 | 1 µM | Tube "1 µM" |
| 3 et 9 | 3 µM | Tube "3 µM" |
| 4 et 10 | 10 µM | Tube "10 µM" |
| 5 et 11 | 30 µM | Tube "30 µM" |
| 6 et 12 | 100 µM | Tube "100 µM" |

**Protocole de remplissage — séquence stricte ✓**

> Règle d'or : **des concentrations faibles vers les concentrations fortes**. Ne jamais revenir en arrière.

**Étape 1 : ajouter les blancs (Row G)**
1. ☑ Prélever 200 µL de LB + kanamycine avec la P200
2. ☑ Distribuer dans chaque puits de la Row G (G1 à G12)

**Étape 2 : ajouter l'inducteur dans toutes les lignes A–F**

Travailler colonne par colonne, de la Col 1 à la Col 12 :

3. ☑ **Col 1** (IPTG = 0) : prélever 2 µL d'eau avec la **P20**. Déposer dans A1, B1, C1, D1, E1, F1. Changer de cônes entre rangées A–C et D–F (deux souches différentes).
4. ☑ **Col 2** (IPTG = 1 µM) : prélever 2 µL du tube "1 µM IPTG". Distribuer dans A2, B2, C2, D2, E2, F2. Changer de cône.
5. ☑ Répéter pour Col 3 à 6 (IPTG 3, 10, 30, 100 µM).
6. ☑ Répéter pour Col 7 à 12 (TMG, mêmes concentrations).

**Étape 3 : ajouter les bactéries**

7. ☑ Vérifier avec Thomas que les cultures sont à OD ~0,2–0,3 (phase exponentielle).
8. ☑ Rows A, B, C → Plac-GFP : prélever 198 µL de culture Plac-GFP avec la P200 multicanal.
   Distribuer dans chaque puits A1–A12, puis B1–B12, puis C1–C12.
9. ☑ Rows D, E, F → lacUV5-GFP : même chose avec la culture lacUV5-GFP.
10. ☑ Rows G (blancs) → ne rien ajouter (déjà remplis de LB seul).

11. ☑ Couvrir la plaque. ⚠️ Thomas lance le plate reader :
    - OD600 + GFP toutes les 5–10 min, 37 °C, agitation, durée 6–8h.

---

### À la fin de la journée, tu dois avoir
- ☑ Plaque d'induction lancée dans le plate reader
- ☑ §B1 et §B2 du Notebook B terminés

---

## Mardi S2 — Lecture et analyse des données d'induction

### Objectif de la journée
Analyser les courbes dose-réponse de tes deux souches.
Comparer avec le modèle de Hill appris dans §B2.

---

### Matin — Lecture et vérification ✓

1. ☑ Arrêter le plate reader avec Thomas.
2. ☑ Exporter les données en `.txt` (Gen5 → Export → sauvegarder dans le dossier Drive).
3. ☑ Vérifications rapides dans le Notebook B §B3 :
   - Les courbes OD montent bien pour toutes les rangées A–F ?
   - Est-ce qu'on voit de la fluorescence dans les puits [IPTG] = 100 µM (col 6) ?
   - Les puits blancs (Row G) restent-ils plats ?
4. ☑ Regarder les colonnes 1 et 7 ([I] = 0) : RFU/OD stable pendant la phase exponentielle ?
   C'est le niveau d'autofluorescence à soustraire.

> Si une des vérifications échoue → discuter avec Thomas avant de continuer.

---

### Après-midi — Notebook B §B3 et [FACULTATIF] microscopie ✓ / ⚠️

**Si les données sont propres :**
5. ☑ **§B1 fin** + **§B2** : Hill n=1 vs n=2, lecture graphique K_half.
   Si données pas encore prêtes → commencer §B3 (chargement des données).
6. ☑ Lire K_half pour chaque promoteur sur le graphe (concentration à 50 % d'activité).

**[FACULTATIF] Microscopie agar pads ⚠️ (avec Thomas)**
Si Thomas estime que c'est le bon moment (données propres, temps disponible) :
- Observer les bactéries au microscope à fluorescence (objectif 100×)
- Comparer l'aspect de Plac-GFP et lacUV5-GFP à différentes concentrations de TMG

---

### À la fin de la journée, tu dois avoir
- ☑ Données chargées et vérifiées
- ☑ Courbes dose-réponse tracées avec autofluorescence corrigée
- ☑ K_half estimé graphiquement pour les deux promoteurs

---

## Mercredi S2 — Analyse ImageJ [FACULTATIF] + finalisation

### Si microscopie faite mardi ⚠️ (avec Thomas pour ImageJ)

**Analyse ImageJ — segmenter les cellules et mesurer la fluorescence**

1. ☑ Ouvrir FIJI (ImageJ) sur l'ordinateur du labo.
2. ☑ File → Open → ouvrir l'image `.tif` de ta première condition ([TMG] = 0).
3. ☑ Image → Type → **8-bit** (si pas déjà en 8-bit).
4. ☑ Image → Adjust → **Threshold** :
   - Ajuster les curseurs jusqu'à ce que les bactéries apparaissent en rouge sur le fond noir
   - Cliquer **Apply**
5. ☑ Analyze → **Analyze Particles** :
   - Size : mettre `1-20` (µm²) pour ne garder que les tailles de bactéries
   - Cocher "Display Results" et "Add to Manager"
   - Cliquer **OK**
6. ☑ Analyze → Set Measurements → cocher **Mean Gray Value** (fluorescence moyenne)
7. ☑ Analyze → **Measure** → un tableau apparaît
8. ☑ File → Save As → **Results** → nommer `imagej_tmg_XXuM.csv`
9. ☑ Répéter pour chaque concentration de TMG.

**Analyse dans le Notebook C :**
10. ☑ Notebook C §C2 : charger les CSV ImageJ, tracer les histogrammes, comparer les distributions.

---

### Si pas encore de données propres — redo ⚠️

→ Relancer la plaque d'induction avec Thomas (même protocole que lundi PM).
→ Continuer §B3 pendant la mesure.

---

### À la fin de la journée, tu dois avoir
- ☑ §B3 : normalisation RFU/OD, courbes dose-réponse, fit graphique K_half, superposition Hill.
- ☑ [FACULTATIF] Notebook C §C1 et §C2 avancés ou terminés
- ☑ Figures finales préparées pour la présentation

---

## Jeudi S2 — Présentation orale

### Objectif
Produire un rapport de 2 pages (3 figures) et/ou une présentation (~20 minutes).

---

### Structure du rapport ou de la présentation

1. **Pourquoi les bactéries régulent-elles leurs gènes ?** (2 min)
   → La diauxie : E. coli ne consomme pas glucose et lactose simultanément

2. **Comment la croissance fonctionne-t-elle ?** (5 min, Notebook A)
   → Courbe de croissance (données de mardi)
   → Modèle Monod : N_max ∝ [glucose]
   → Ce que la simulation stochastique ajoute par rapport au modèle déterministe

3. **Comment un gène répond-il à un inducteur ?** (8 min, Notebook B)
   → Courbes dose-réponse Plac-GFP vs lacUV5-GFP
   → Courbe de Hill : n=1 vs n=2, pourquoi ?
   → Valeurs de K_half mesurées vs prédites

4. **[FACULTATIF] Hétérogénéité** (3 min, Notebook C)
   → Distributions single-cell au TMG
   → Pourquoi la distribution est-elle bimodale ?

5. **Ce que j'ai appris / ce qui m'a surpris** (2 min)

---

### Figures à préparer (minimum)

- ☑ Courbe de croissance (données mardi + droite Y·[glucose])
- ☑ Courbe diauxie (OD vs temps, deux phases visibles)
- ☑ Courbes dose-réponse Plac-GFP vs lacUV5-GFP + courbes de Hill ajustées
- ☑ [FACULTATIF] Histogrammes de fluorescence single-cell

> **Conseil** : imprimer ou préparer les figures dans un document avant la présentation.
> Les figures du notebook peuvent être exportées avec un clic droit → "Enregistrer l'image".

---

## Annexe — Résumé des notebooks

| Notebook | Sections | Quand | Durée estimée |
|---|---|---|---|
| **A** — Croissance | §A1 (Lun S1), §A2 (Mar S1), §A3 (Mer S1), §A4 (Jeu–Ven S1) | Lun S1 → Ven S1 | ~4 demi-journées |
| **B** — Induction | §B1 (Lun S2), §B2 (Mar S2), §B3 (Mar–Mer S2) | Lun S2 → Mer S2 | ~3 demi-journées |
| **C** — Hétérogénéité [FACULTATIF] | §C1 bistabilité, §C2 ImageJ | Mer S2 → Jeu S2 | ~1–2 demi-journées |

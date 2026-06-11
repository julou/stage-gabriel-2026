# Stage lycéen — Microbiologie quantitative
## Document encadrant — usage interne

---

## Vue d'ensemble

**Stagiaire** : lycéen/ne fin de seconde, lycée parisien d'élite, profil MPI, ≈15 ans.
Quelques bases de Python autodidactes (boucles, listes, import). Pas de numpy/matplotlib.
Mathématiquement : probabilités discrètes OK, logarithme et exponentielle hors programme.

**Durée** : 2 semaines, 9 jours ouvrés (lundi S1 → jeudi S2).
Environ 4–6 demi-journées computationnelles intercalées dans les temps morts expérimentaux.

**Labo** : microbiologie quantitative, Basel.

**Objectifs pédagogiques**
1. Comprendre l'origine microscopique de la croissance exponentielle et de la saturation.
2. Comprendre qu'un gène peut être régulé quantitativement et mesurer ce contrôle.
3. Produire des figures à partir de vraies données du labo — en écrivant le code soi-même.

---

## Documents produits

| Fichier | Usage | Destinataire |
|---|---|---|
| `doc_principal_encadrant.md` | Ce document — contexte, protocoles, checklist | Thomas |
| `doc_principal_stagiaire.md` | Bienvenue, programme allégé, ressources | Stagiaire (+ parents) |
| `plan_experimental_encadrant.md` | Protocoles J1–J9, layouts plaques, gammes | Thomas |
| `notebook_croissance_complet.ipynb` | **Notebook A** — §A1–§A4 (déterministe, stochastique, Monod, diauxie) | Référence / corrigé |
| `notebook_croissance_stagiaire.ipynb` | Notebook A — version stagiaire | Stagiaire |
| `notebook_induction_complet.ipynb` | **Notebook B** — §B1–§B3 (interrupteur stochastique, Hill, données plaque reader) | Référence / corrigé |
| `notebook_induction_stagiaire.ipynb` | Notebook B — version stagiaire | Stagiaire |
| `notebook_heterogeneite_complet.ipynb` | **Notebook C** [FACULTATIF] — §C1 bistabilité, §C2 ImageJ | Référence / corrigé |
| `notebook_heterogeneite_stagiaire.ipynb` | Notebook C — version stagiaire | Stagiaire |

Les deux notebooks *stagiaire* sont le matériel de travail du stagiaire.
Les deux notebooks *complet* servent de corrigé et peuvent être partagés en fin de stage.

---

## Programme jour par jour

> Colonne **Expérimental** : détail AM / PM.
> Colonne **Programmation** : section du notebook et contenu clé. Timing flexible selon avancement.

| Jour | Expérimental AM | Expérimental PM | Programmation |
|---|---|---|---|
| **Lun S1** | Introduction : présentation labo, règles de sécurité. Pipetage : dilutions en série ×10 sur 6 ordres de grandeur, vérification au spectro. Inoculation de 6 tubes LB ±stérile (vérification contamination le lendemain). | Inoculation tubes LB + glucose 0,2 % pour courbe de croissance manuelle démarrant **Mar matin**. | Setup Colab (ou VS Code). Notebook A §A1 : multiplication répétée, tracé linéaire, échelle log, temps de doublement graphique |
| **Mar S1** | Lecture OD600 toutes les 30 min de ~9h30 à ~16h (6 mesures min, 2×1h puis 4×30 min puis toutes les 20 min). Tubes LB + glucose 3 concentrations.  Vérification contamination des tubes du lundi. | Lecture OD suite. Préparation inoculum pour plaque reader (mercredi matin). | Notebook A §A2 : `simulate_one`, 1 trajectoire. 30 trajectoires, moyenne, variance. Pendant les pauses de 20 min. |
| **Mer S1** | Inoculation plaque reader : glucose ×3 (0,02 % / 0,2 % / 0,4 %) × 2 réplicats + lactose ×2 (0,2 % / 0,4 %) × 2 réplicats + glu+lac ×2 × 2 réplicats + blancs → **diauxie overnight**. | Lancement plate reader, vérification lecture. | Notebook A §A3 : Monod, courbe p(S), `simulate_nutrients`. Vérification N_max ∝ [glucose] avec données Mar S1. |
| **Jeu S1** | Lecture données diauxie (arrêt le matin). Discussion avec Thomas : qu'est-ce que la diauxie dit sur la régulation de *lacZ* ? **TSS transformation** pUA66-lacUV5 → MG1655 : préparation cellules compétentes AM, transformation + incubation 1h + plating fin de matinée sur LB + Kan50. | | Notebook A §A3 fin : `simulate_nutrients` avec paramètres variés. §A4 début : import données diauxie plate reader, visualisation. |
| **Ven S1** | Vérification colonies de transformation. Si OK (>10 colonies, fond propre) : pick 2–3 colonies → LB + Kan50 overnight pour glycérol + préculture. Si échec : redo ou utiliser stock glycérol existant. | Fin de journée : observation des colonies au microscope à faible grossissement (optionnel, pédagogique). | Notebook A §A4 : comparaison Monod vs données. |
| **Sam–Dim S2** | *(Thomas)* Dimanche soir : inoculer 3 mL M9 0,2 % arabinose + Kan50 depuis glycérol Plac-GFP **et** colonie/glycérol pUA66-lacUV5/MG1655. Overnight 37 °C. | — | — |
| **Lun S2** | préparation plaque d'induction et lancement plate reader (≥6h de cinétique).  | Lancement plate reader induction : Plac-GFP vs pUA66-lacUV5/MG1655 × IPTG (6 conc.) × TMG (6 conc.) × 2 réplicats. |  Notebook B §B1 début. |
| **Mar S2** | Lecture plate reader le matin. Évaluation des données : courbes propres ? oui → **microscopie PM** (agar pads, 2 souches, 4 [TMG]). non → redo + analyse. | Si microscopie PM : préparation agar pads, mise en place échantillons, acquisition phase + fluorescence. | §B1 fin. §B2 : Hill n=1 vs n=2. Si redo : §B3 début (import données plaque reader). |
| **Mer S2** | Si microscopie déjà faite → **ImageJ** (segmentation cellules, mesure Mean, export CSV). Si pas encore → session microscopie. | ImageJ suite / vérification données. | §B3 : normalisation RFU/OD, courbes dose-réponse, fit graphique K_half. Superposition courbe de Hill. |
| **Jeu S2** | Finalisation mesures / ImageJ si besoin. | **Rapport 2 pages (3 figures)** : figures clés des deux notebooks + interprétation. Discussion avec Thomas. | Notebook C §C1–§C2 [FACULTATIF] si temps : bistabilité, histogrammes single-cell. |

---

## Arc narratif

La progression en 9 jours construit une cohérence thématique :

**Semaine 1 — Comment une population croît**
Mardi : courbe de croissance manuelle (expérience fondatrice, contact direct avec les données).
Mercredi : plaque reader pour la diauxie — un signal simple cache de la régulation génique.
Jeudi : transformation → le stagiaire introduit lui-même un nouveau gène dans une bactérie.

**Semaine 2 — Comment un gène est régulé**
Lundi : mesure quantitative de l'induction (plaque reader, deux promoteurs).
Mardi–Mercredi : comparaison à la prédiction (courbe de Hill) et visualisation single-cell.
Jeudi : présentation — relier les deux semaines : la croissance exponentielle qu'on a simulée
est la même qui dilue la GFP entre les générations dans l'expérience d'induction.

**Fil rouge computationnel** : le même raisonnement (règle microscopique → comportement de population)
relie le notebook croissance (τ-leaping) au notebook induction (interrupteur stochastique §B1).

---

## Checklist pré-stage — actions Thomas

### Biologie (à faire avant J1)

- [ ] **Courbe IPTG préliminaire lacUV5-GFP** : après clonage et transformation, vérifier que la courbe dose-réponse est bien hyperbolique (n ≈ 1, attendu vu la séquence). Calibrer la gamme : si K_half très différent de 15–30 µM, ajuster les 6 concentrations dans le plan expérimental.
- [ ] **Glycérol Plac-GFP/MG1655** : vérifier disponibilité d'un stock fonctionnel. Croissance + fluorescence OK à l'IPTG.
- [ ] **pUA66-lacUV5 transformé** : séquence vérifiée et commandée (Eurofins Express GeneStrands, 274 bp). Dès réception : cloner dans pUA66 via XhoI/BamHI, transformer dans MG1655, pick colonie, vérifier fluorescence + courbe IPTG préliminaire (confirmer n ≈ 1). Avoir un stock glycérol validé avant J1 du stage.
- [ ] **Stocks IPTG et TMG 10 mM** : préparer dans eau ultra-pure, filtrer sur 0,22 µm, aliquoter 500 µL, stocker à −20 °C. Voir *Annexe 2* dans `plan_experimental_encadrant.md`.
- [ ] **Plaques LB + Kan50** : préparer 4–6 plaques fraîches pour Jeu S1 (transformation) + Ven S1 (vérification).
- [ ] **Plaque reader BioTek** : vérifier disponibilité pour Mer S1 soir (diauxie overnight) **et** Lun S2 PM (induction). Ces deux créneaux ne peuvent pas être déplacés.
- [ ] **Microscope fluorescent** : vérifier disponibilité Mar S2 PM ou Mer S2. Filtres GFP (excitation 470 nm, émission 525 nm). Prévoir objectif 60× ou 100× à huile.

### Informatique (à faire avant J1)

- [ ] **Tester Colab** sur l'ordinateur du labo : créer un notebook, importer numpy + matplotlib, tracer un graphe simple.
- [ ] **Uploader les notebooks stagiaire** sur un Google Drive accessible depuis le labo.
- [ ] **Vérifier que le stagiaire a accès** à un compte Google (pour Colab) ou prévoir un accès invité.

### Dimanche S2 (obligatoire)

- [ ] Inoculer Plac-GFP/MG1655 : 1 colonie ou 5 µL glycérol → 3 mL M9 0,2 % arabinose + Kan50, overnight 37 °C.
- [ ] Inoculer pUA66-lacUV5/MG1655 : même chose depuis colonie Ven S1 (ou glycérol).

---

## Notes biologiques importantes

### Construct lacUV5 (pUA66)

**Séquence vérifiée et commandée chez Eurofins Express GeneStrands (274 bp total).**

Insert de 249 bp entre XhoI et BamHI, avec buffers flanquants validés pour une digestion efficace.

#### Architecture de l'opéron *lac*

Le promoteur Plac natif possède trois opérateurs : **O1** (région centrale, fort),
**O3** (−82 bp en amont, modéré) et **O2** (+412 bp en aval, faible).
LacI peut se fixer simultanément sur O1 et O3, formant une **boucle d'ADN** de 92 pb
qui renforce la répression de façon coopérative → réponse sigmoïde (n ≈ 2).
La région −10 native (TATGTT) est sous-optimale et dépendante du facteur CRP/AMPc —
d'où l'absence d'expression sur glucose (catabolite repression).

#### Conséquences biologiques du construct lacUV5

- **O1** intact → seul opérateur fonctionnel → pas de boucle ADN → n ≈ 1
- **O3** absent du fragment (−82, hors du fragment −60/+25) et scramblé dans notre construct
- **O2** absent (+412, hors du fragment)
- Mutations **lacUV5** dans la −10 (TATGTT → TATAAT) : promoteur fort, indépendant de CRP
  → expression constitutive indépendante de la source de carbone

La différence de forme de courbe (n ≈ 1 vs n ≈ 2) entre lacUV5-GFP et Plac-GFP est
entièrement attribuable à l'**architecture des opérateurs**, toutes choses égales par ailleurs
(même backbone pUA66, même RBS synthétique, même souche MG1655, même fluorophore GFPmut2).

**À vérifier avant le stage** : vérification séquence faite. Il reste à confirmer biologiquement
que la courbe dose-réponse IPTG est bien hyperbolique après transformation dans MG1655 (voir checklist).


### IPTG vs TMG pour les deux expériences
- **IPTG** : entre par diffusion passive, courbe gradée propre → utiliser pour la plaque reader (fit quantitatif).
- **TMG** : transporté par LacY → rétroaction positive → bistabilité aux concentrations intermédiaires → distribution bimodale visible en microscopie. Utiliser **TMG** pour la microscopie (Notebook C).

La même plaque reader peut contenir les deux inducteurs : colonnes 1–6 pour IPTG, colonnes 7–12 pour TMG. Voir layout dans `plan_experimental_encadrant.md`.

### Reporters Zaslaver
Les reporters de la librairie Zaslaver (pUA66) utilisent un RBS synthétique fort qui override les signaux de traduction natifs, donc ce sont des sondes transcriptionnelles pures.

---

## Notes pédagogiques

### Sur les logarithmes
Le logarithme est hors programme en seconde (enseigné en terminale). Les notebooks évitent toute formule avec `log`. La représentation `plt.yscale('log')` est présentée comme un *outil visuel* (la multiplication répétée devient une droite) sans justification formelle. `np.log` apparaît dans le calcul du temps de doublement mais est explicitement marqué "à voir en terminale — vérifiez graphiquement".

### Sur la stochasticité
Introduire avec "pile ou face pour chaque cellule" — c'est l'intuition juste. L'algorithme τ-leaping est présenté comme "on tire N fois pile-ou-face" sans nommer l'algorithme. Insister sur l'émergence : des règles individuelles aléatoires → comportement de population prévisible (loi des grands nombres).

### Sur la courbe de Hill
Le point clé pédagogique de §B2 est que n=2 émerge de p₁ × p₂ (règle de multiplication des probabilités indépendantes, programme de seconde). Ne pas nommer "coopérativité" ou "Hill" en premier — laisser le stagiaire dériver la formule, puis lui donner le nom.

### Sur la bistabilité (Notebook C (facultatif))
La connexion avec §B1 (bruit stochastique) est importante : dans §B1, la variabilité vient du hasard moléculaire. Dans §D, la bimodalité vient d'une bifurcation déterministe (deux états stables). Ce sont deux mécanismes distincts qui produisent des distributions similaires. C'est un point conceptuellement riche si le temps le permet.

### Pour le rapport / la présentation final/e (Jeu S2)
Orienter la présentation autour de deux questions : (1) Comment une cellule simple produit une croissance exponentielle ? (2) Comment la cellule décide-t-elle d'activer un gène selon son environnement ? Les deux notebooks répondent à ces deux questions avec des données réelles du labo.

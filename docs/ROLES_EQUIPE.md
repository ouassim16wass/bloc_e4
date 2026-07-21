# 👥 Les rôles de l'équipe projet MobilityPulse — fiche de révision oral

> ⚠️ Contexte : le candidat passe l'épreuve **seul**, mais le scénario fictif impose une équipe
> projet de 6 rôles (+ 1 transverse). À l'oral, il faut savoir expliquer **qui fait quoi et
> pourquoi** pour chacun. Cette fiche sert aussi de base à la matrice RACI (Livrable 1 §6).

---

## Vue d'ensemble : l'équipe imposée par le brief direction

Le brief est explicite : *« Équipe projet limitée : 1 PO, 1 lead data, 1 data engineer, 1 MLOps,
1 représentant métier, 1 référent support »* — plus le **référent accessibilité** qui apparaît
dans les parties prenantes et dans la matrice RACI officielle (rôle transverse, hors équipe cœur).

```
                    ┌─────────────────────┐
                    │  Direction mobilité  │  ← reçoit le reporting, arbitre
                    └─────────┬───────────┘
                              │
                    ┌─────────▼───────────┐
                    │   Product Owner     │  ← priorise, porte la vision
                    └─────────┬───────────┘
        ┌───────────┬─────────┼──────────┬────────────┐
   ┌────▼────┐ ┌────▼────┐ ┌──▼───┐ ┌────▼─────┐ ┌────▼────┐
   │Lead Data│ │  Data   │ │MLOps │ │ Référent │ │ Référent│
   │         │ │Engineer │ │      │ │  métier  │ │ support │
   └─────────┘ └─────────┘ └──────┘ └──────────┘ └─────────┘
        ▲ transverse sur tout : Référent accessibilité ▲
```

---

## Fiche par rôle

### 1. 🎯 Product Owner (PO)

- **Sa mission :** porter la vision produit et **prioriser** ce qui sera fait. C'est lui qui dit
  « on fait B01 avant B05, et voici pourquoi ».
- **Dans MobilityPulse :** owner du backlog priorisé (story **B09**), anime les arbitrages avec le
  métier et l'IT (répond au risque **R02** « conflit de priorités »), valide les critères
  d'acceptation des user stories.
- **Rituels :** sprint planning (décide du contenu), revue de sprint (valide), comité d'arbitrage hebdo.
- **RACI typique :** **A** sur la priorisation du backlog, **R** sur la planification, **C** sur les KPI.
- **Phrase pour l'oral :** *« Le PO est le gardien de la valeur : il traduit les besoins de la
  direction et des utilisateurs en priorités concrètes pour l'équipe. »*

### 2. 🧭 Lead Data

- **Sa mission :** responsable technique de la chaîne de données ; il garantit la **qualité et la
  fiabilité des données** et encadre techniquement l'équipe data.
- **Dans MobilityPulse :** garant de la qualité data nécessaire à la story **B06** (tendances par
  ligne), owner du canal de feedback structuré (**B10**), définit les formules des KPI avec le PO
  (répond au risque **R06** « KPI non exploitables »).
- **Rituels :** daily, revue technique, comité d'arbitrage (voix technique).
- **RACI typique :** **A** sur la définition des KPI (formules), **R** sur la qualité data, **C** sur la priorisation.
- **Phrase pour l'oral :** *« Le Lead Data est le garant que les chiffres qu'on montre à la
  direction veulent vraiment dire quelque chose. »*

### 3. 🔧 Data Engineer

- **Sa mission :** réaliser les évolutions de la chaîne de données (dans notre dossier, on ne code
  pas — mais on **planifie et charge ses tâches** dans les sprints).
- **Dans MobilityPulse :** réalisation des stories produit **B05** (export CSV des anomalies,
  dépendance : permissions) et **B06** (tendances par ligne), contribue à la documentation des alertes (**B01**).
- **Rituels :** daily, sprint planning (estime la complexité), rétrospective.
- **RACI typique :** **R** sur les tâches de réalisation produit, **I** sur le reporting direction.
- **Phrase pour l'oral :** *« Dans ce dossier de pilotage, le Data Engineer apparaît comme une
  capacité de réalisation à planifier : j'estime ses charges et je séquence ses tâches, je ne code pas. »*

### 4. ⚙️ MLOps

- **Sa mission :** fiabiliser le **modèle de détection d'anomalies en production** : monitoring,
  performance, dérive du modèle.
- **Dans MobilityPulse :** en première ligne sur le KPI **« taux de faux positifs perçu »**
  (28 % → 15 %) — c'est LA attente du persona Sarah (« alertes fiables, peu de faux positifs ») ;
  contribue à la mesure de l'**empreinte numérique** (story **B08**, KPI RSE) car il connaît les
  ressources consommées par les traitements.
- **Rituels :** daily, revue technique, point mensuel RSE.
- **RACI typique :** **R** sur le monitoring du modèle et l'indicateur RSE, **C** sur les KPI produit.
- **Phrase pour l'oral :** *« Le MLOps fait le pont entre le modèle et la réalité : moins de
  fausses alertes = plus de confiance = plus d'adoption. »*

### 5. 🏢 Référent métier

- **Sa mission :** représenter les **utilisateurs finaux** (supervision, analystes, exploitants)
  dans l'équipe projet ; valider que ce qui est produit est utilisable sur le terrain.
- **Dans MobilityPulse :** valide les **libellés métier** des alertes (feedback **F01** :
  « vocabulaire trop technique »), co-construit les formations avec les agents (mitigation du
  risque **R01** « non-adoption »), relaie les retours terrain.
- **Rituels :** revue de sprint (teste), ateliers de co-construction, comité d'arbitrage (voix métier).
- **RACI typique :** **C** sur la priorisation et les KPI, **R** sur la validation métier des livrables, **A** possible sur le plan d'accompagnement.
- **Phrase pour l'oral :** *« Le référent métier est l'assurance anti-contournement : si le terrain
  n'est pas écouté, l'outil ne sera pas utilisé (risque R01). »*

### 6. 🛟 Référent support

- **Sa mission :** préparer et opérer le **support utilisateur** : documentation, FAQ, procédure
  d'escalade, gestion des tickets.
- **Dans MobilityPulse :** owner de la **procédure d'escalade incident** (story **B03**, feedback
  **F04** « aucune procédure en cas de mauvaise alerte »), organise les niveaux 1 et 2 (mitigation
  du risque **R05** « surcharge support au démarrage »), suit le KPI **« tickets bloquants ≤ 3/semaine »**.
- **Rituels :** daily (remonte les irritants), point support hebdo post-déploiement.
- **RACI typique :** **R** sur la documentation support et l'escalade, **C** sur le plan d'accompagnement.
- **Phrase pour l'oral :** *« Le support, c'est ce qui fait tenir l'adoption dans la durée : la
  formation crée l'adoption, le support l'empêche de retomber. »*

### 7. ♿ Référent accessibilité (transverse)

- **Sa mission :** garantir que la solution ET les supports (formation, documentation, slides)
  sont **accessibles à tous**, y compris aux utilisateurs en situation de handicap.
- **Dans MobilityPulse :** valide la documentation compatible lecteur d'écran (story **B04**,
  feedback **F05**, persona **Jules**), effectue la **validation type RGAA** des supports
  (mitigation du risque **R04**), conseille sur contrastes, sous-titres, alternatives textuelles.
- **Particularité :** il n'est PAS dans l'équipe cœur des 6 — c'est un rôle **transverse**
  consulté à chaque étape, avec un pouvoir de validation (**A**) sur l'activité « Validation
  accessibilité » de la RACI.
- **Phrase pour l'oral :** *« L'accessibilité n'est pas une option de fin de projet : le référent
  intervient dès la conception des supports, pas après. »*

---

## 🎤 Spécial travail individuel : le candidat est le Lead Data

Consigne de l'épreuve : s'attribuer un rôle parmi ceux de l'équipe définie. **Rôle choisi :
Lead Data**, en cohérence avec le titre Data Engineer visé. Cadrage qui rend ce choix solide :
le sujet dit *« Vous intervenez comme équipe Data Engineering chargée de piloter le
déploiement »* — et le responsable d'une équipe Data Engineering, c'est le Lead Data. Posture :
**pilote du déploiement côté data**. Légitimité donnée par le sujet lui-même : la story **B10**
dit « En tant que lead data, je veux un canal de feedback structuré » ; le feedback **F03**
(définitions des KPI) et le risque **R06** (owner et formule de chaque KPI) relèvent
directement de sa responsabilité.

Couverture des 5 compétences :
- **C19** : il construit le plan projet car il connaît les dépendances techniques (« Qualité
  data » pour B06, « Permissions » pour B05) et peut estimer les durées.
- **C20** : « Encadrer le développement avec des méthodes agiles » est littéralement le métier
  d'un lead — il encadre le Data Engineer et le MLOps, anime daily et rétrospectives.
- **C22** : il rend compte à la direction, en traduisant le technique en langage décisionnel
  (glossaire contre le risque R03).
- **C23** : son cœur de légitimité — garant des formules, owners et fiabilité des KPI (R06, F03).
- **C24** : il fiabilise les contenus d'accompagnement (glossaire KPI, documentation des alertes
  B01, canal de feedback B10), en coordination avec le référent métier et le support.

Trois réflexes pour l'oral :

1. **Parlez pilotage, jamais technique :** *« En tant que Lead Data, j'ai planifié..., encadré...,
   garanti la fiabilité des indicateurs..., rendu compte à la direction... »* La question piège
   sera *« parlez-moi de votre architecture »* → réponse : *« La solution existe en prototype ;
   mon rôle dans ce déploiement est le pilotage : planifier, encadrer, mesurer — pas développer. »*
2. **Respectez le territoire du PO :** la priorisation finale du backlog reste au PO fictif
   (A sur cette ligne de la RACI) ; vous êtes Consulté : *« j'éclaire les arbitrages du PO avec
   les complexités et dépendances techniques »*. En échange, vous êtes **A** sur la définition
   des KPI et la qualité data.
3. **Anticipez la question piège :** *« Vous êtes seul, comment pouvez-vous parler de gestion
   d'équipe ? »* → Réponse : *« Le sujet fournit une équipe fictive ; en tant que Lead Data,
   mon travail consiste précisément à encadrer et coordonner cette équipe — un lead réel ne
   fait pas tout lui-même, il organise le travail des autres. »*

## 🔗 Traçabilité rôles ↔ dossier documentaire (à citer en Q/R)

| Rôle | Stories | Feedbacks | Risques | KPI |
|---|---|---|---|---|
| PO | B09 | F02 | R02 | Respect jalons |
| Lead Data | B06, B10 | F03 | R06 | (formules des KPI) |
| Data Engineer | B05, B06, B01 | F01 | — | — |
| MLOps | B08 | F06 | — | Faux positifs, empreinte numérique |
| Référent métier | B01, B07 | F01 | R01 | Adoption, satisfaction formation |
| Référent support | B03 | F04 | R05 | Tickets bloquants |
| Référent accessibilité | B04 | F05 | R04 | (validation des supports) |

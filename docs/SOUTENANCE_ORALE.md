# 🎤 Préparation soutenance orale — E4 MobilityPulse

> **Format de l'épreuve : 10 minutes de présentation + 10 minutes de questions/réponses.**
> Vous êtes le **Lead Data**, pilote du déploiement. Parlez en « je ».
> Version complète : alignée sur les slides finales (Livrable 3) et enrichie des
> Livrables 1, 2 et 4. Contient le déroulé minuté, les anti-sèches, les chiffres
> à connaître par cœur et 18 questions de jury avec réponses rédigées.

---

## 1. Phrase d'ouverture (à apprendre par cœur)

> « Bonjour. Je suis le **Lead Data** du projet MobilityPulse. La direction de NovaVille a confié
> le passage à l'échelle de la solution à l'équipe Data Engineering, dont je suis le responsable.
> Ma mission : **sécuriser le déploiement pilote sur 12 semaines** — organisation, gouvernance,
> indicateurs et accompagnement des utilisateurs. La solution existe déjà en prototype :
> mon travail n'est pas de la développer, mais de **piloter son adoption**. »

*(≈ 30 secondes — elle pose votre rôle, le contexte, le périmètre ET votre bouclier anti-technique.)*

---

## 2. Déroulé minuté des 10 minutes (aligné sur les slides finales)

| # | Slide | Temps | Ce que vous dites (points clés) |
|---|---|---|---|
| 0 | Titre | 0:30 | Phrase d'ouverture ci-dessus. Statut global : VERT |
| 1 | Message clé | 1:00 | Les 3 limites constatées par la direction, et « ce dossier y répond point par point » : un plan (organisation), une RACI (rôles), un accompagnement (formation). Message à retenir : *« la solution existe, ce dossier organise son adoption »* |
| 2 | Planning | 1:30 | 4 phases, 5 jalons. Cadrage S1-S2 → J1 gouvernance validée. 3 sprints S3-S8. Accompagnement S6-S10 **en parallèle**. Pilote S11-S12 → J5 go/no-go. **Insister : « les formations se terminent AVANT le pilote »** |
| 3 | Gouvernance | 1:30 | Hybride Scrum/Kanban : sprints pour le produit (planifiable), Kanban pour le support (flux imprévisible). Comité d'arbitrage hebdo = les conflits se règlent chaque semaine. RACI : PO priorise, moi je planifie/garantis les KPI/reporte, référent accessibilité valide. **Décision attendue n°1** |
| 4 | KPI | 1:30 | 4 catégories. Citer 3 chiffres de tête : adoption de 35 à 75 %, alerte de 5 à 2 min, faux positifs de 28 à 15 %. « Chaque KPI a un owner, une formule documentée, une action si dérive » — c'est mon cœur de métier de Lead Data |
| 5 | Risques | 1:00 | Top 3 : R01 non-adoption, R02 conflit IT/métier, R04 accessibilité. Mitigation préventive + plan de contingence à seuil défini (« adoption sous 50 % en S8 : ateliers ciblés et binômes ») |
| 6 | Feedbacks | 1:00 | Priorisation impact et fréquence. F01 vocabulaire, F04 escalade, F03 glossaire traités en premier. F05 accessibilité remonté : exigence d'inclusion, pas une option. « L'ordre des sprints reflète ces priorités » |
| 7 | Accompagnement | 1:00 | 4 profils = 4 parcours. Ateliers 45 min (contrainte temps). Session accessibilité dédiée, supports validés RGAA avant diffusion. Binômes sur poste. Support 2 niveaux + escalade. **Décision attendue n°4** |
| 8 | Décisions demandées | 1:00 | Les 4 décisions : gouvernance, calendrier, backlog (S2), accompagnement (S4). « Voilà ce que j'attends du comité aujourd'hui. » Puis : « je suis prêt pour vos questions » |

**Total : ≈ 10 minutes.** Répétez au chrono au moins 2 fois. Si vous dépassez, coupez dans les slides 5-6 — **jamais la slide 8** (les décisions doivent toujours passer).

---

## 3. Anti-sèches par compétence

- **C19 (organiser)** : « 5 objectifs SMART issus des KPI fournis ; un plan en 4 phases et 5 jalons
  calé sur les dépendances du backlog ; l'accessibilité intégrée dès la planification. »
- **C20 (encadrer)** : « Méthode hybride justifiée ; 6 rituels dont le comité d'arbitrage hebdo ;
  une RACI avec un seul Accountable par activité ; des mesures d'inclusion dans le fonctionnement
  d'équipe : tour de parole, supports accessibles, charge suivie en sprint planning. »
- **C22 (reporter)** : « J'applique la charte : 8 slides, un message par slide, un tableau maximum,
  statut vert/orange/rouge, une décision attendue formulée. Reporting hebdo des KPI (B02, F02)
  et comité de direction à chaque jalon. »
- **C23 (mesurer)** : « 7 KPI en 4 catégories, chacun avec formule, owner et action si dérive
  (mitigation R06). Les 6 feedbacks priorisés par impact et fréquence, retraduits en backlog. »
- **C24 (accompagner)** : « Un parcours progressif en 5 étapes : informer, former par profil,
  session accessibilité dédiée, binômes sur poste, autonomie avec support 2 niveaux.
  Formats courts imposés par la contrainte de temps. Validation RGAA avant diffusion.
  6 KPI d'adoption avec plan de contingence. »

---

## 4. Les chiffres à connaître par cœur

### Chiffres du projet (Livrable 1)

| Chiffre | Signification |
|---|---|
| **12 semaines** | Durée du déploiement pilote (contrainte du brief) |
| **6 rôles** (+1 transverse) | PO, Lead Data, Data Engineer, MLOps, référent métier, support + référent accessibilité |
| **4 phases / 5 jalons / 3 sprints** | Structure du plan projet |
| **35 % → 75 %** | Taux d'adoption hebdomadaire (objectif O1) |
| **5 min → 2 min** | Délai de compréhension d'une alerte (O2, persona Malik) |
| **28 % → 15 %** | Taux de faux positifs perçu (KPI produit) |
| **85 % minimum** | Respect des jalons (KPI projet) |
| **3 maximum/semaine** | Tickets support bloquants |
| **S2 / S4 / S10** | Gouvernance opérationnelle / indicateur RSE défini / fin des formations |

### Chiffres de l'accompagnement (Livrable 2)

| Chiffre | Signification |
|---|---|
| **45 minutes** | Durée d'un atelier de formation par profil (story B07) |
| **4/5 minimum** | Satisfaction après chaque atelier |
| **90 % minimum** | Taux de participation aux ateliers |
| **2 fois 30 minutes** | Prise en main accompagnée en binôme sur poste (agents) |
| **3 à 5 minutes** | Durée d'un tutoriel vidéo (sous-titré et transcrit) |
| **15 minutes** | Démonstration de lancement (S6) |
| **4 heures ouvrées** | Objectif de première réponse du support niveau 1 |
| **10 pages maximum** | Guide de démarrage par profil |
| **5 étapes** | Parcours d'accompagnement (informer, former, adapter, accompagner, autonomiser) |

---

## 5. Questions probables du jury et réponses préparées

### Sur le rôle et la posture

**« Pourquoi avoir choisi le rôle de Lead Data ? »**
> C'est le rôle cohérent avec le titre Data Engineer que je vise. Le brief confie le pilotage à
> l'équipe Data Engineering, j'en suis le responsable. Et le dossier m'ancre directement :
> la story B10 est écrite « en tant que lead data », le feedback F03 et le risque R06
> (fiabilité des KPI) relèvent de ma responsabilité.

**« Vous êtes seul : comment pouvez-vous parler de gestion d'équipe ? »**
> Le sujet fournit une équipe fictive de 6 rôles. Mon travail consiste précisément à organiser
> leur collaboration : un lead réel ne fait pas tout lui-même, il encadre et coordonne.

**« Parlez-moi de votre architecture technique. »** *(piège)*
> La solution existe en prototype : chaîne de données, modèle d'anomalies, API. Mon rôle dans ce
> déploiement est le pilotage — planifier, encadrer, mesurer, accompagner — pas le développement.
> C'est d'ailleurs le périmètre de l'épreuve E4.

**« Combien coûte votre projet ? »** *(piège)*
> L'analyse financière relève de l'épreuve E5 et n'est pas dans le périmètre de ce dossier.
> En revanche, je pilote la charge : le plan tient avec l'équipe de 6 imposée par le brief,
> et le comité d'arbitrage ajuste le périmètre si nécessaire.

### Sur la gouvernance et le planning (Livrable 1)

**« Pourquoi Scrum ET Kanban ? »**
> Deux natures de travail différentes : les évolutions produit sont planifiables, les sprints de
> 2 semaines donnent une cadence lisible pour la direction. Le flux support et pilote est
> imprévisible : un Kanban avec limite d'encours est plus honnête qu'un sprint qu'on casserait
> en permanence. Et le rythme court force les arbitrages, ce qui traite le risque R02.

**« D'où viennent vos chiffres ? »**
> Du dossier documentaire : le fichier kpi_initial.csv fournit les valeurs de départ et les
> cibles à 12 semaines validées par la direction. Je n'ai rien inventé.

**« Pourquoi terminer les formations en semaine 10 et pas pendant le pilote ? »**
> Un pilote avec des utilisateurs non formés mesurerait l'échec de la formation, pas la valeur
> de l'outil. Le pilote doit tester la solution en conditions réelles, pas l'improvisation.

**« Pourquoi B08 (RSE) en sprint 1 alors qu'il est priorité moyenne ? »**
> Sa complexité est grande (L) et mon objectif O5 impose un indicateur défini en semaine 4.
> Attendre aurait mis l'engagement RSE du brief en danger. C'est un arbitrage assumé.

**« Quelle différence entre Responsible et Accountable ? »**
> Responsible réalise la tâche ; Accountable en répond — il n'y en a qu'un seul par activité.
> Exemple : sur la définition des KPI, le MLOps est Responsible pour instrumenter les métriques,
> moi je suis Accountable de leur fiabilité.

**« Pourquoi le PO garde-t-il la priorisation du backlog ? »**
> C'est le cœur de son rôle (story B09) : il porte la valeur métier. Moi, je l'éclaire sur les
> complexités et dépendances techniques. Chacun son territoire, c'est ça une gouvernance claire.

**« Que faites-vous si l'adoption stagne à 50 % en semaine 8 ? »**
> C'est prévu dans mon plan de contingence R01 : ateliers ciblés supplémentaires, accompagnement
> en binôme, simplification des écrans prioritaires. Et le canal de feedback B10 me dit pourquoi
> ça bloque.

**« Comment mesurez-vous l'empreinte numérique ? »**
> Par une estimation relative des ressources consommées par run. La formule est définie en
> semaine 4 par le MLOps et validée par moi, puis relevée mensuellement. L'objectif du pilote
> est une tendance stable ou en baisse, pas une valeur absolue.

### Sur l'accompagnement (Livrable 2)

**« Comment formez-vous des agents qui n'ont pas le temps ? »**
> Tout est calibré pour ça : un seul atelier de 45 minutes par profil, des tutoriels de 3 à
> 5 minutes consultables entre deux incidents, une fiche réflexe, et la prise en main se fait
> en binôme sur leur poste, pendant leur travail réel — pas dans une salle de formation.

**« Que prévoyez-vous concrètement pour les utilisateurs en situation de handicap ? »**
> Une session dédiée à rythme adapté, des supports compatibles lecteur d'écran avec alternatives
> textuelles pour chaque graphique, des vidéos sous-titrées et transcrites, chaque contenu en
> deux formats minimum, et surtout : la validation type RGAA par le référent accessibilité
> AVANT toute diffusion — l'accessibilité est en amont, pas en rattrapage.

**« Un agent signale une alerte fausse : que se passe-t-il ? »**
> Il ouvre un ticket au niveau 1, qui qualifie. Si c'est bloquant, escalade au niveau 2 selon la
> procédure B03. Et l'alerte jugée erronée est transmise au MLOps pour analyse du modèle : le
> signalement terrain améliore le produit. La boucle est fermée — c'est aussi comme ça qu'on
> fait baisser les faux positifs de 28 à 15 %.

**« Comment savez-vous que votre accompagnement fonctionne ? »**
> Six indicateurs : participation aux ateliers (90 % minimum), satisfaction (4/5 minimum),
> adoption hebdomadaire (vers 75 %), délai de compréhension d'une alerte (vers 2 minutes),
> tickets bloquants (3 maximum par semaine) et consultation des supports. Si un indicateur
> dérive, le plan de contingence R01 s'applique.

### Sur le reporting (Livrable 3)

**« Pourquoi ne présentez-vous que 3 risques sur 6 ? »**
> C'est la charte de reporting : messages courts, orientés décision. Je présente les trois
> risques de niveau élevé qui demandent l'attention du comité ; les six sont documentés au
> registre en annexe, avec mitigation et contingence pour chacun.

**« Votre statut est vert : qu'est-ce qui le ferait passer à l'orange ? »**
> Des seuils définis à l'avance : adoption sous 50 % en semaine 8, plus de 3 tickets bloquants
> par semaine, un jalon manqué, ou un support recalé à la validation accessibilité. Le statut
> n'est pas une impression, il découle des KPI.

---

## 6. Règles de langage (charte de reporting)

- Phrases courtes. Un message par slide. Zéro jargon technique.
- Toujours un **statut** : vert, orange, rouge.
- Toujours finir un sujet par **la décision attendue**.
- Bannir : pipeline, API, Docker, architecture, modèle ML (dire « la solution », « les alertes », « les indicateurs »).
- Dire « je » (vous êtes le pilote), et nommer les rôles fictifs pour le reste (« le référent métier anime les ateliers »).

## 7. Erreurs à ne pas commettre

1. Glisser vers le technique (hors périmètre E4, piège classique).
2. Parler budget ou ROI (c'est l'épreuve E5/C21, explicitement exclu).
3. Réciter le dossier au lieu de le raconter : le jury a lu, il veut vous entendre **justifier**.
4. Dépasser les 10 minutes : la slide 8 (décisions) doit TOUJOURS passer.
5. Oublier les fils rouges : accessibilité et RSE doivent apparaître au moins une fois chacun à l'oral.

## 8. Checklist de répétition (à faire avant le jour J)

- [ ] Répétition 1 : lire les slides avec les notes orateur, sans chrono (appropriation)
- [ ] Répétition 2 : au chrono, viser 10 minutes (couper slides 5-6 si besoin, jamais la 8)
- [ ] Répétition 3 : sans les notes, seulement les slides à l'écran
- [ ] Faire poser 5 questions de la section 5 par quelqu'un (ou piochez au hasard)
- [ ] Vérifier : je sais dire les 3 chiffres clés (35→75 %, 5→2 min, 28→15 %) sans hésiter
- [ ] Vérifier : je sais réciter les 4 décisions demandées dans l'ordre
- [ ] Le jour J : PDF des slides ouvert + une copie de secours sur clé USB

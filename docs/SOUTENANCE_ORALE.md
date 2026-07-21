# 🎤 Préparation soutenance orale — E4 MobilityPulse

> **Format de l'épreuve : 10 minutes de présentation + 10 minutes de questions/réponses.**
> Vous êtes le **Lead Data**, pilote du déploiement. Parlez en « je ».
> Ce document est alimenté au fil des livrables — il contient le déroulé minuté,
> les anti-sèches par compétence, les chiffres à connaître par cœur et la préparation Q/R.

---

## 1. Phrase d'ouverture (à apprendre par cœur)

> « Bonjour. Je suis le **Lead Data** du projet MobilityPulse. La direction de NovaVille a confié
> le passage à l'échelle de la solution à l'équipe Data Engineering, dont je suis le responsable.
> Ma mission : **sécuriser le déploiement pilote sur 12 semaines** — organisation, gouvernance,
> indicateurs et accompagnement des utilisateurs. La solution existe déjà en prototype :
> mon travail n'est pas de la développer, mais de **piloter son adoption**. »

*(≈ 30 secondes — elle pose votre rôle, le contexte, le périmètre ET votre bouclier anti-technique.)*

---

## 2. Déroulé minuté des 10 minutes (calé sur les 8 slides)

| # | Slide | Temps | Ce que vous dites (points clés) |
|---|---|---|---|
| 0 | Titre | 0:30 | Phrase d'ouverture ci-dessus |
| 1 | Message clé | 1:00 | Les 3 limites constatées par la direction (organisation, rôles, formation) ; annonce : « mon dossier répond à ces 3 limites » ; statut global vert |
| 2 | Planning | 1:30 | 4 phases, 5 jalons : Cadrage S1-S2 (gouvernance) ; 3 sprints S3-S8 (produit) ; Accompagnement S6-S10 **en parallèle** ; Pilote S11-S12. Insister : « les formations finissent AVANT le pilote » |
| 3 | Gouvernance | 1:30 | Méthode hybride Scrum/Kanban justifiée (sprints pour le produit, flux pour le support) ; comité d'arbitrage hebdo (répond au risque de conflit IT/métier) ; RACI : moi Accountable sur planification/KPI/reporting, le PO sur la priorisation |
| 4 | KPI | 1:30 | 4 catégories : projet, produit, adoption, RSE. Citer 3 chiffres : adoption 35 → 75 %, alerte 5 → 2 min, faux positifs 28 → 15 %. « Chaque KPI a un owner et une action si dérive » |
| 5 | Risques | 1:00 | Top 3 : non-adoption (R01), conflit de priorités (R02), accessibilité (R04) — chacun : mitigation + contingence. Une décision attendue par risque |
| 6 | Feedbacks | 1:00 | Priorisation impact et fréquence : F01/F03/F04 d'abord ; F05 remonté (obligation d'inclusion) ; « le terrain influence directement l'ordre des sprints » |
| 7 | Accompagnement | 1:00 | 4 profils = 4 parcours ; ateliers 45 min (contrainte temps des agents) ; supports accessibles validés RGAA ; support niveaux 1 et 2 après déploiement |
| 8 | Décisions demandées | 1:00 | Les 4 décisions du brief : gouvernance, calendrier, priorités backlog, dispositif d'accompagnement. « Voilà ce que j'attends du comité aujourd'hui » |

**Total : ≈ 10 minutes.** Répétez au chrono au moins 2 fois. Si vous dépassez, coupez dans les slides 5-6 (jamais dans la 8).

---

## 3. Anti-sèches par compétence (si le jury sonde une compétence précise)

- **C19 (organiser)** : « J'ai posé 5 objectifs SMART issus des KPI fournis, un plan en 4 phases
  et 5 jalons calé sur les dépendances du backlog, et intégré l'accessibilité dès la planification. »
- **C20 (encadrer)** : « Méthode hybride justifiée, 6 rituels dont un comité d'arbitrage hebdo,
  une RACI avec un seul Accountable par activité, et des mesures d'inclusion dans le
  fonctionnement d'équipe (tour de parole, supports accessibles, charge suivie). »
- **C22 (reporter)** : « J'applique la charte : 8 slides maximum, un message par slide, statut
  vert/orange/rouge, une décision attendue formulée. Le reporting hebdo des KPI répond au
  feedback F02 et à la story B02. »
- **C23 (mesurer)** : « 7 KPI en 4 catégories, chacun avec formule, owner et action si dérive —
  c'est la mitigation du risque R06, et c'est mon cœur de métier de Lead Data. Les feedbacks
  sont priorisés par impact et fréquence et retraduits en backlog. »
- **C24 (accompagner)** : « 4 profils, 4 parcours, formats courts imposés par la contrainte de
  temps des agents, supports validés type RGAA par le référent accessibilité, et un support
  post-déploiement en 2 niveaux avec escalade. »

---

## 4. Les chiffres à connaître par cœur

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
| **4/5 minimum** | Satisfaction formation (O4) |
| **45 minutes** | Durée d'un atelier de formation (B07) |
| **S2 / S4 / S10** | Gouvernance opérationnelle / indicateur RSE défini / fin des formations |

---

## 5. Questions probables du jury et réponses préparées

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

**« Que faites-vous si l'adoption stagne à 50 % en semaine 8 ? »**
> C'est prévu dans mon plan de contingence R01 : ateliers ciblés supplémentaires, accompagnement
> en binôme, simplification des écrans prioritaires. Et le canal de feedback B10 me dit pourquoi
> ça bloque.

**« Qui valide l'accessibilité et pourquoi ? »**
> Le référent accessibilité est Accountable sur cette activité : validation type RGAA de chaque
> support. Il est consulté dès la priorisation pour anticiper, pas seulement en fin de chaîne.
> C'est la mitigation du risque R04 et la réponse au persona Jules.

**« Comment mesurez-vous l'empreinte numérique ? »**
> Par une estimation relative des ressources consommées par run. La formule est définie en
> semaine 4 par le MLOps et validée par moi, puis relevée mensuellement. L'objectif du pilote
> est une tendance stable ou en baisse, pas une valeur absolue.

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

---

*À compléter après le Livrable 2 (détails accompagnement) et le Livrable 3 (slides finales).*

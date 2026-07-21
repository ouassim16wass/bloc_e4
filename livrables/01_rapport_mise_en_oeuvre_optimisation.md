# Rapport de mise en oeuvre et d'optimisation - E4 MobilityPulse_V1

> **Livrable 1** : couvre C19 (organisation), C20 (gouvernance agile), C23 (KPI et amélioration continue).
> Rédigé du point de vue du **Lead Data**, responsable de l'équipe Data Engineering à qui la
> direction a confié le pilotage du déploiement. Chaque choix est justifié par le dossier
> documentaire (IDs B/F/R, personas, brief direction).

---

## 1. Synthèse exécutive

- **Contexte :** La métropole de NovaVille exploite un réseau de transport multimodal (bus, tramways, parkings relais, pistes cyclables et vélos en libre-service). Un prototype avancé de la solution MobilityPulse permet déjà de collecter les signaux de mobilité, de détecter les anomalies et d'exposer des indicateurs via une interface interne. Jugé prometteur, ce prototype se heurte à trois limites : l'organisation du passage à l'échelle n'est pas définie, les rôles entre les équipes data, IT, métier et exploitation ne sont pas formalisés, et les utilisateurs finaux demandent davantage de formation, de lisibilité et de support. Le Comité de Direction demande donc un dossier de pilotage permettant de sécuriser le déploiement pilote de MobilityPulse sur 12 semaines.

- **Enjeux :**
  - Réussir l'adoption par les utilisateurs finaux (seuls 35 % sont actifs aujourd'hui, avec un risque de contournement de l'outil, R01) ;
  - Clarifier la gouvernance pour éviter les conflits de priorités entre IT et métier (R02) ;
  - Donner à la direction un pilotage fiable grâce à des KPI définis et un reporting orienté décision (R03, R06) ;
  - Garantir un déploiement inclusif, accessible aux utilisateurs en situation de handicap (R04), et responsable, avec un suivi de l'impact environnemental de la solution.

- **Décisions attendues :** À la fin de ce rapport, la direction est invitée à prendre les décisions suivantes :
  - Valider le mode de gouvernance proposé ;
  - Valider le calendrier de déploiement sur 12 semaines ;
  - Arbitrer les priorités du backlog ;
  - Valider le dispositif d'accompagnement des utilisateurs.

---

## 2. Objectifs SMART

Chaque objectif répond à un enjeu identifié dans la synthèse exécutive ; toutes les cibles chiffrées proviennent du dossier documentaire (kpi_initial.csv, brief direction).

| # | Objectif | Spécifique | Mesurable | Acceptable | Réaliste | Temporel |
|---|---|---|---|---|---|---|
| O1 | Porter le taux d'adoption hebdomadaire de MobilityPulse de 35 % à 75 % d'utilisateurs actifs | Adoption de l'outil par les utilisateurs cibles : agents de supervision, analystes, managers | Utilisateurs actifs sur utilisateurs cibles : de 35 % à 75 % (kpi_initial.csv) | Validé par la direction et le centre de supervision ; répond au risque R01 (non-adoption) | Atteignable via formations courtes, co-construction et support terrain | Fin de semaine 12 (fin du déploiement pilote) |
| O2 | Réduire le délai moyen de compréhension d'une alerte critique de 5 à 2 minutes | Lisibilité des alertes pour les agents du centre de supervision | Délai moyen de compréhension : de 5 min à 2 min (kpi_initial.csv) | Demande directe des agents (persona Malik, feedback F01) | Via libellés métier, aide contextuelle et tutoriel court (story B01) | Fin de semaine 12 |
| O3 | Rendre la gouvernance projet opérationnelle : matrice RACI validée, comité d'arbitrage hebdomadaire, rituels agiles en place | Formalisation des rôles entre data, IT, métier et exploitation (limite n°2 du brief) | 3 éléments livrés et validés : RACI, comité d'arbitrage, rituels | Répond au risque R02 (conflits de priorités) ; soumis à la validation de la direction (décision n°1) | Ne nécessite que de l'organisation, aucun développement | Fin de semaine 2 (prérequis du reste du projet) |
| O4 | Former 100 % des utilisateurs cibles des 4 profils avec une satisfaction de 4/5 minimum et des supports accessibles | Montée en compétence des 4 profils : superviseur, agent, analyste, utilisateur avec besoin d'accessibilité | 100 % formés ; satisfaction de 4/5 minimum (kpi_initial.csv) ; supports validés accessibilité (type RGAA) | Répond à la limite n°3 du brief et au risque R04 ; validé par le référent accessibilité | Formats courts (ateliers de 45 min, story B07) compatibles avec le peu de temps de formation des agents | Fin de semaine 10, avant le démarrage du pilote |
| O5 | Définir puis suivre mensuellement un indicateur d'empreinte numérique du service | Mesure de l'impact environnemental de la solution (exigence du brief) | 1 indicateur défini (formule et owner) puis 1 relevé mensuel | Demande de la direction RSE (feedback F06) | Estimation relative des ressources par run, sans outillage lourd (story B08) | Défini en semaine 4, suivi mensuel ensuite |

---

## 3. Plan projet (12 semaines)

Le déploiement est découpé en **4 phases** et **5 jalons**. Le séquencement suit les dépendances du backlog fourni : la gouvernance (RACI) précède la procédure d'escalade (B03), la définition des KPI précède le reporting hebdomadaire (B02), la qualité des données précède les tendances par ligne (B06). Les phases 2 et 3 se chevauchent volontairement : les formations s'étalent car les agents disposent de peu de temps (contrainte du brief), et doivent être terminées **avant** le pilote.

| Phase | Objectif | Tâches principales | Durée | Jalons | Dépendances | Responsable |
|---|---|---|---|---|---|---|
| **Phase 1 : Cadrage et gouvernance** (S1 à S2) | Rendre la gouvernance opérationnelle (O3) | Ateliers RACI ; mise en place du comité d'arbitrage hebdomadaire ; choix des rituels et de l'outil de suivi ; définition des KPI (formules, owners) ; priorisation initiale du backlog avec le PO (B09) ; plan de charge de l'équipe | 2 sem. | **J1 (fin S2)** : gouvernance validée par la direction (décision n°1), backlog priorisé v1, tableau KPI v1 | Aucune (point de départ) | Lead Data (avec PO) |
| **Phase 2 : Itérations produit et données** (S3 à S8) | Livrer les évolutions prioritaires (O2, O5) | 3 sprints de 2 semaines. Sprint 1 (S3-S4) : B02 reporting hebdo KPI, B03 procédure d'escalade, B08 définition indicateur RSE. Sprint 2 (S5-S6) : B01 libellés métier et aide contextuelle, B10 canal de feedback. Sprint 3 (S7-S8) : B04 documentation accessible, B05 export CSV, B06 tendances par ligne | 6 sem. | **J2 (fin S4)** : reporting hebdo en place, indicateur RSE défini. **J3 (fin S8)** : stories haute priorité livrées, produit prêt pour le pilote | J1 ; B02 dépend de la définition des KPI ; B03 dépend de la RACI ; B06 dépend de la qualité data ; B05 dépend des permissions | Lead Data (encadrement) ; Data Engineer et MLOps (réalisation) ; PO (priorisation) |
| **Phase 3 : Accompagnement et formation** (S6 à S10, en parallèle) | Former 100 % des profils (O4) | Plan d'accompagnement détaillé ; création des supports (guide, FAQ, tutoriels, glossaire KPI) ; validation accessibilité type RGAA (R04) ; ateliers de 45 min par profil (B07) ; mise en place du support niveaux 1 et 2 | 5 sem. | **J4 (fin S10)** : 100 % des profils formés, satisfaction de 4/5 minimum, dispositif d'accompagnement validé (décision n°4) | Contenus de la phase 2 (documentation B01, glossaire) ; les ateliers B07 dépendent du plan d'accompagnement | Référent métier, support et référent accessibilité ; Lead Data (fiabilisation des contenus) |
| **Phase 4 : Déploiement pilote et bilan** (S11 à S12) | Déployer en conditions réelles et mesurer (O1) | Ouverture du pilote au centre de supervision ; suivi quotidien des KPI ; collecte des feedbacks (canal B10) ; traitement des tickets (procédure B03) ; bilan chiffré et reporting final | 2 sem. | **J5 (fin S12)** : bilan du pilote, décision go/no-go de généralisation | J3 et J4 (produit prêt et utilisateurs formés) | Lead Data (pilotage) ; toute l'équipe mobilisée |

**Arbitrage de séquencement assumé :** les stories haute priorité et faible complexité (B02, B03, des gains rapides) passent en sprint 1 ; B08 (complexité L) démarre tôt malgré sa priorité moyenne car l'objectif O5 impose un indicateur défini en S4 ; B05 et B06 (priorité moyenne, statut prototype) passent en sprint 3 car aucune story haute priorité n'en dépend.

---

## 4. Parties prenantes

| Partie prenante | Rôle dans le projet | Attentes | Niveau d'influence | Besoins d'inclusion / accessibilité |
|---|---|---|---|---|
| Direction mobilité | Sponsor et décideur : valide la gouvernance, le calendrier et les arbitrages | Visibilité, KPI fiables, décisions rapides | Élevé | Reporting non technique, statuts explicites (charte de reporting) |
| Centre de supervision (personas Sarah et Malik) | Utilisateurs principaux au quotidien | Alertes lisibles et fiables, procédures simples, peu de faux positifs | Élevé (leur adoption conditionne le succès, R01) | Formations courtes (peu de temps disponible), faible charge cognitive en incident |
| Équipe Data/IT (Data Engineer, MLOps) | Réalisation des évolutions et exploitation de la chaîne de données | Gouvernance technique claire, priorités arbitrées, charge soutenable | Moyen | Rituels courts et cadrés, arbitrages documentés (R02) |
| Service support | Exploitation quotidienne après déploiement | Documentation à jour, procédure d'escalade formalisée (B03) | Moyen | Formation anticipée avant le pilote pour éviter la saturation (R05) |
| Référent handicap / accessibilité | Validation transverse de l'accessibilité | Supports compatibles lecteur d'écran, alternatives textuelles | Moyen, avec pouvoir de validation (RACI) | C'est lui qui porte l'exigence : validation type RGAA de chaque support (R04, persona Jules) |
| Exploitants terrain | Utilisateurs secondaires, sources de retours | Informations actionnables, retours pris en compte | Faible à moyen | Canal de feedback simple et accessible (B10) |

---

## 5. Méthode agile et gouvernance

- **Méthode choisie :** hybride Scrum et Kanban (dite Scrumban).
- **Justification :** l'équipe est réduite (6 personnes) et pluridisciplinaire, avec un délai fixe de 12 semaines. Le coeur du déploiement (phase 2) se prête à Scrum : 3 sprints de 2 semaines donnent une cadence prévisible, des jalons lisibles par la direction, et la revue de sprint sert de point de contact avec le métier. En revanche, le flux de la phase pilote et du support (tickets, demandes d'accompagnement) est imprévisible et ne se planifie pas en sprint : un tableau Kanban avec limite d'encours est plus adapté. Ce choix hybride répond aussi au risque R02 : le rythme court des sprints force des arbitrages réguliers plutôt qu'un conflit larvé.
- **Rituels :** daily de 15 min (équipe data) ; sprint planning (2 h, début de sprint) ; revue de sprint (1 h, démonstration avec le référent métier) ; rétrospective (45 min) ; comité d'arbitrage hebdomadaire (30 min : PO, Lead Data, référent métier, mitigation directe de R02) ; point support hebdomadaire en phase pilote.
- **Outil de suivi :** tableau agile partagé (type Jira ou Trello) pour le backlog et les sprints ; tableau de bord KPI partagé pour le pilotage ; les deux accessibles à tous les rôles, y compris en lecture pour la direction.
- **Cadence de reporting :** reporting hebdomadaire court des KPI avec statut vert/orange/rouge (story B02, feedback F02) ; comité de direction à chaque jalon avec le support conforme à la charte de reporting (6 à 8 slides, une décision attendue par sujet).
- **Mesures d'inclusion dans le fonctionnement d'équipe :** horaires de rituels compatibles avec les contraintes de chacun ; supports de réunion partagés à l'avance et accessibles (compatibles lecteur d'écran) ; tour de parole systématique en rétrospective ; charge de travail suivie en sprint planning ; retours du terrain traités via un canal structuré (B10).

---

## 6. Matrice RACI

R = Responsible (réalise) ; A = Accountable (rend compte, un seul par activité) ; C = Consulted ; I = Informed.

| Activité | PO | Lead Data | Data Engineer | MLOps | Référent métier | Support | Référent accessibilité |
|---|---|---|---|---|---|---|---|
| Planification projet | C | **A / R** | C | C | C | I | I |
| Priorisation backlog | **A / R** | C | C | C | C | I | C |
| Définition KPI | C | **A / R** | I | R | C | I | I |
| Plan accompagnement | C | C | I | I | **A / R** | R | C |
| Validation accessibilité | I | I | I | I | C | C | **A / R** |
| Reporting direction | C | **A / R** | I | I | C | I | I |

**Justification des choix clés :**
- **Lead Data Accountable sur la planification, les KPI et le reporting** : la direction a confié le pilotage du déploiement à l'équipe Data Engineering ; son responsable planifie, garantit la fiabilité des indicateurs (formule et owner par KPI, mitigation de R06 et réponse au feedback F03) et rend compte.
- **PO Accountable sur la priorisation du backlog** : c'est le coeur de son rôle (story B09) ; le Lead Data est consulté pour éclairer les arbitrages avec les complexités et dépendances techniques.
- **Référent métier Accountable sur le plan d'accompagnement** : il connaît les profils utilisateurs et leurs contraintes (mitigation de R01) ; le support est Responsible sur la partie post-déploiement.
- **Référent accessibilité Accountable sur la validation accessibilité** : pouvoir de validation type RGAA sur chaque support (mitigation de R04) ; consulté dès la priorisation pour anticiper (B04).
- **MLOps Responsible sur la définition des KPI** : il instrumente les métriques du modèle (faux positifs) et de l'empreinte numérique (B08).

---

## 7. Risques et mitigations

Niveau = croisement probabilité et impact. Les six risques initiaux du registre fourni sont repris et complétés d'un plan de contingence.

| ID | Risque | Probabilité | Impact | Niveau | Mesure préventive | Plan de contingence |
|---|---|---|---|---|---|---|
| R01 | Non-adoption par les agents | Moyenne | Élevé | **Élevé** | Co-construction avec le terrain, formations courtes par profil, support de proximité, canal de feedback (B10) | Si l'adoption est inférieure à 50 % en semaine 8 : ateliers ciblés supplémentaires, accompagnement individuel en binôme, simplification des écrans prioritaires |
| R02 | Conflit de priorités entre IT et métier | Moyenne | Élevé | **Élevé** | Comité d'arbitrage hebdomadaire, backlog priorisé avec justifications écrites (B09) | Escalade à la direction (décision n°3) avec dossier d'arbitrage documenté ; décision tranchée en comité de jalon |
| R03 | Reporting trop technique | Élevée | Moyen | **Élevé** | Application stricte de la charte de reporting, glossaire KPI, statut vert/orange/rouge (F02) | Relecture de chaque support par un non-technicien avant présentation ; reformulation systématique |
| R04 | Accessibilité insuffisante | Moyenne | Élevé | **Élevé** | Validation type RGAA de chaque support, référent accessibilité impliqué dès la conception (B04) | Plan de remédiation prioritaire ; formats alternatifs immédiats (transcription, session dédiée) |
| R05 | Surcharge du support au démarrage | Moyenne | Moyen | Moyen | FAQ, support niveau 1, procédure d'escalade (B03), formation du support avant le pilote | Renfort temporaire de l'équipe data au support ; gel des évolutions non critiques le temps de résorber |
| R06 | KPI non exploitables | Faible | Élevé | Moyen | Owner et formule documentés pour chaque KPI (garantie Lead Data), glossaire partagé (F03) | Audit des indicateurs, correction des formules, revalidation en comité |

---

## 8. KPI et amélioration continue

Le tableau couvre les quatre catégories demandées : projet, produit, adoption et RSE. Chaque KPI a un owner et une action définie en cas de dérive (mitigation de R06). Les définitions détaillées figurent au glossaire KPI (réponse au feedback F03).

| KPI | Catégorie | Définition | Valeur initiale | Cible | Fréquence | Owner | Action si dérive |
|---|---|---|---|---|---|---|---|
| Taux d'adoption hebdomadaire | Adoption | Utilisateurs actifs sur utilisateurs cibles | 35 % | 75 % (S12) | Hebdomadaire | Référent métier | Si l'adoption est sous les 50 % en S8 : ateliers ciblés, analyse des freins via le canal de feedback |
| Délai de compréhension d'une alerte | Adoption | Temps moyen pour comprendre une alerte critique (test panel agents) | 5 min | 2 min | Mensuelle | Référent métier (mesure) et Lead Data (fiabilité) | Renforcement des libellés métier et de l'aide contextuelle (B01) |
| Taux de faux positifs perçu | Produit | Part des alertes jugées non pertinentes par les agents | 28 % | 15 % | Hebdomadaire | MLOps | Revue des seuils du modèle, boucle de qualification des alertes par le terrain |
| Respect des jalons | Projet | Jalons tenus sur jalons planifiés | N/A | 85 % minimum | À chaque jalon | Lead Data | Replanification, arbitrage de périmètre au comité hebdomadaire |
| Tickets support bloquants | Support | Nombre de tickets bloquants ouverts par semaine | N/A | 3 par semaine maximum | Hebdomadaire | Référent support | Renfort niveau 2, analyse de cause racine, mise à jour FAQ |
| Satisfaction formation | Accompagnement | Score moyen recueilli après chaque atelier | N/A | 4/5 minimum | Après chaque atelier | Référent métier | Refonte du format, sessions complémentaires courtes |
| Empreinte numérique du projet | RSE | Estimation relative des ressources consommées par run (formule définie en S4) | N/A | Suivi mensuel, tendance stable ou en baisse | Mensuelle | MLOps (formule validée par le Lead Data) | Plan de sobriété : optimisation des traitements, purge des données inutiles |

**Amélioration continue :** les KPI sont revus au comité hebdomadaire (statut vert/orange/rouge) ; chaque dérive déclenche l'action définie et, si nécessaire, une entrée au backlog d'amélioration (section 9). Les rétrospectives de sprint alimentent l'amélioration du fonctionnement d'équipe.

---

## 9. Feedbacks utilisateurs et priorisation

**Feedbacks majeurs :** six retours utilisateurs ont été recueillis après le prototype (fichier feedbacks_utilisateurs.csv). Ils sont priorisés par croisement impact et fréquence.

| Priorité | Feedback | Impact / Fréquence | Décision | Story liée | Sprint cible |
|---|---|---|---|---|---|
| 1 | F01 : vocabulaire des alertes trop technique | Élevé / Fréquent | Libellés métier et aide contextuelle | B01 | Sprint 2 (S5-S6) |
| 1 | F04 : aucune procédure en cas de mauvaise alerte | Élevé / Fréquent | Procédure d'escalade et ticketing | B03 | Sprint 1 (S3-S4) |
| 1 | F03 : définitions des KPI non explicites | Élevé / Fréquent | Glossaire KPI, formule et owner par indicateur | Définition KPI (phase 1) | Phase 1 puis continu |
| 2 | F05 : graphiques illisibles au lecteur d'écran | Élevé / Occasionnel | Descriptions textuelles et alternatives ; validation RGAA | B04 | Sprint 3 (S7-S8) |
| 3 | F02 : reporting sans statut global | Moyen / Occasionnel | Statut synthèse vert/orange/rouge dans le reporting hebdo | B02 | Sprint 1 (S3-S4) |
| 3 | F06 : impact environnemental non mesuré | Moyen / Occasionnel | KPI de sobriété numérique | B08 | Sprint 1 (définition) puis mensuel |

**Analyse :** trois retours combinent impact élevé et fréquence élevée (F01, F03, F04) : ils sont traités en premier. F05 est remonté en priorité 2 malgré sa fréquence occasionnelle, car l'accessibilité est une exigence transverse du projet (R04) et une obligation d'inclusion. F02 et F06 sont absorbés par des chantiers déjà planifiés (reporting B02, indicateur RSE B08).

**Décisions de priorisation :** proposées par le PO en comité d'arbitrage, éclairées par le Lead Data sur les complexités et dépendances techniques ; l'ordre des sprints du plan projet (section 3) reflète ces décisions.

**Backlog d'amélioration :** le canal de feedback structuré (B10, en place au sprint 2) alimente en continu un backlog d'amélioration revu à chaque sprint planning ; les nouvelles demandes sont qualifiées (impact et fréquence) selon la même grille.

---

## 10. Conclusion et arbitrages demandés

Ce dossier propose une organisation complète du déploiement de MobilityPulse : une gouvernance formalisée dès la semaine 2, un plan en 4 phases et 5 jalons sur 12 semaines, un dispositif de mesure couvrant le projet, le produit, l'adoption et l'impact environnemental, et un accompagnement adapté à chaque profil d'utilisateur, accessibilité comprise.

- **Arbitrage 1 (gouvernance, décision n°1, échéance S2) :** valider la méthode hybride Scrum/Kanban, la matrice RACI et le comité d'arbitrage hebdomadaire.
- **Arbitrage 2 (calendrier, décision n°2, échéance S2) :** valider le découpage en 4 phases et 5 jalons, dont le chevauchement des phases produit et accompagnement.
- **Arbitrage 3 (priorités du backlog, décision n°3, échéance S2 puis en continu) :** valider l'ordre des sprints proposé (gains rapides B02 et B03 en premier, B08 anticipé pour l'objectif RSE).
- **Arbitrage 4 (accompagnement, décision n°4, échéance S4) :** valider le dispositif de formation par profils en formats courts et les exigences d'accessibilité des supports.

**Prochaines étapes :** lancement de la phase 1 (ateliers RACI, comité d'arbitrage, définition des KPI), premier reporting hebdomadaire à S3, point de jalon J1 avec la direction en fin de semaine 2.

# Rapport de mise en œuvre et d'optimisation — E4 MobilityPulse_V1

> **Livrable 1** — couvre C19 (organisation), C20 (gouvernance agile), C23 (KPI et amélioration continue).
> Structure imposée par le template officiel : 10 sections.
> Règle d'or : chaque choix est justifié en citant le dossier documentaire (IDs B/F/R, personas, brief).

---

## 1. Synthèse exécutive

- **Contexte :** La métropole de NovaVille exploite un réseau de transport multimodal (bus, tramways, parkings relais, pistes cyclables et vélos en libre-service). Un prototype avancé de la solution MobilityPulse permet déjà de collecter les signaux de mobilité, de détecter les anomalies et d'exposer des indicateurs via une interface interne. Jugé prometteur, ce prototype se heurte à trois limites : l'organisation du passage à l'échelle n'est pas définie, les rôles entre les équipes data, IT, métier et exploitation ne sont pas formalisés, et les utilisateurs finaux demandent davantage de formation, de lisibilité et de support. Le Comité de Direction demande donc un dossier de pilotage permettant de sécuriser le déploiement pilote de MobilityPulse sur 12 semaines.

- **Enjeux :** Réussir l'adoption par les utilisateurs finaux (seuls 35 % sont actifs aujourd'hui, avec un risque de contournement de l'outil — R01) ; clarifier la gouvernance pour éviter les conflits de priorités entre IT et métier (R02) ; donner à la direction un pilotage fiable grâce à des KPI définis et un reporting orienté décision (R03, R06) ; garantir un déploiement inclusif, accessible aux utilisateurs en situation de handicap (R04), et responsable, avec un suivi de l'impact environnemental de la solution.

- **Décisions attendues :** À l'issue de ce rapport, la direction est invitée à : 1) valider le mode de gouvernance proposé ; 2) valider le calendrier de déploiement sur 12 semaines ; 3) arbitrer les priorités du backlog ; 4) valider le dispositif d'accompagnement des utilisateurs.

---

## 2. Objectifs SMART

Chaque objectif répond à un enjeu identifié dans la synthèse exécutive ; toutes les cibles chiffrées proviennent du dossier documentaire (`kpi_initial.csv`, brief direction).

| # | Objectif | Spécifique | Mesurable | Acceptable | Réaliste | Temporel |
|---|---|---|---|---|---|---|
| O1 | Porter le taux d'adoption hebdomadaire de MobilityPulse de 35 % à 75 % d'utilisateurs actifs | Adoption de l'outil par les utilisateurs cibles : agents de supervision, analystes, managers | Utilisateurs actifs / utilisateurs cibles : 35 % → 75 % (kpi_initial.csv) | Validé par la direction et le centre de supervision ; répond au risque R01 (non-adoption) | Atteignable via formations courtes, co-construction et support terrain | Fin de semaine 12 (fin du déploiement pilote) |
| O2 | Réduire le délai moyen de compréhension d'une alerte critique de 5 à 2 minutes | Lisibilité des alertes pour les agents du centre de supervision | Délai moyen de compréhension : 5 min → 2 min (kpi_initial.csv) | Demande directe des agents (persona Malik, feedback F01) | Via libellés métier, aide contextuelle et tutoriel court (story B01) | Fin de semaine 12 |
| O3 | Rendre la gouvernance projet opérationnelle : matrice RACI validée, comité d'arbitrage hebdomadaire, rituels agiles en place | Formalisation des rôles entre data, IT, métier et exploitation (limite n°2 du brief) | 3 éléments livrés et validés : RACI, comité d'arbitrage, rituels | Répond au risque R02 (conflits de priorités) ; soumis à la validation de la direction (décision n°1) | Ne nécessite que de l'organisation, aucun développement | Fin de semaine 2 (prérequis du reste du projet) |
| O4 | Former 100 % des utilisateurs cibles des 4 profils avec une satisfaction ≥ 4/5 et des supports accessibles | Montée en compétence des 4 profils : superviseur, agent, analyste, utilisateur avec besoin d'accessibilité | 100 % formés ; satisfaction ≥ 4/5 (kpi_initial.csv) ; supports validés accessibilité (type RGAA) | Répond à la limite n°3 du brief et au risque R04 ; validé par le référent accessibilité | Formats courts (ateliers 45 min — story B07) compatibles avec le peu de temps de formation des agents | Fin de semaine 10, avant le démarrage du pilote |
| O5 | Définir puis suivre mensuellement un indicateur d'empreinte numérique du service | Mesure de l'impact environnemental de la solution (exigence du brief) | 1 indicateur défini (formule + owner) puis 1 relevé mensuel | Demande de la direction RSE (feedback F06) | Estimation relative ressources/run, sans outillage lourd (story B08) | Défini en semaine 4, suivi mensuel ensuite |

---

## 3. Plan projet (12 semaines)

| Phase | Objectif | Tâches principales | Durée | Jalons | Dépendances | Responsable |
|---|---|---|---|---|---|---|
| <!-- TODO --> | | | | | | |

<!-- Piste de découpage :
Phase 1 Cadrage (S1-S2) : gouvernance, RACI, backlog priorisé, définition KPI → J1 gouvernance validée
Phase 2 Itérations (S3-S8) : sprints sur B01-B04, B07... → J2, J3
Phase 3 Accompagnement (S6-S10) : formations, supports, FAQ → J4
Phase 4 Pilote (S11-S12) : déploiement pilote, mesure, bilan → J5 go/no-go
-->

---

## 4. Parties prenantes

| Partie prenante | Rôle | Attentes | Niveau d'influence | Besoins d'inclusion/accessibilité |
|---|---|---|---|---|
| Direction mobilité | | Visibilité, KPI, décisions rapides | | |
| Centre de supervision | | Alertes lisibles, procédures simples | | |
| Équipe Data/IT | | Gouvernance, priorités claires | | |
| Service support | | Documentation, escalade | | |
| Référent handicap/accessibilité | | Supports accessibles | | |
| Exploitants terrain | | Informations actionnables | | |

<!-- TODO : compléter rôle, influence, besoins d'inclusion pour chaque ligne -->

---

## 5. Méthode agile et gouvernance

- **Méthode choisie :** <!-- TODO : Scrum / Kanban / hybride -->
- **Justification :** <!-- TODO : appuyée sur équipe de 6, 12 semaines, risque R02, story B09 -->
- **Rituels :** <!-- TODO : daily, planning, revue, rétro, comité d'arbitrage hebdo (→ R02) -->
- **Outil de suivi :** <!-- TODO -->
- **Cadence de reporting :** <!-- TODO : hebdo direction (→ B02, charte reporting) -->

---

## 6. Matrice RACI

> Voir [`annexes/matrice_raci.csv`](../annexes/matrice_raci.csv) — insérer ici la version finale.

| Activité | PO | Lead Data | Data Engineer | MLOps | Référent métier | Support | Référent accessibilité |
|---|---|---|---|---|---|---|---|
| Planification projet | | | | | | | |
| Priorisation backlog | | | | | | | |
| Définition KPI | | | | | | | |
| Plan accompagnement | | | | | | | |
| Validation accessibilité | | | | | | | |
| Reporting direction | | | | | | | |

<!-- Rappel : un seul A (Accountable) par ligne. Justifier les choix clés sous le tableau. -->

---

## 7. Risques et mitigations

| ID | Risque | Probabilité | Impact | Niveau | Mesure préventive | Plan de contingence |
|---|---|---|---|---|---|---|
| R01 | Non-adoption par les agents | Moyenne | Élevé | | | |
| R02 | Conflit de priorités IT/métier | Moyenne | Élevé | | | |
| R03 | Reporting trop technique | Élevée | Moyen | | | |
| R04 | Accessibilité insuffisante | Moyenne | Élevé | | | |
| R05 | Surcharge support au démarrage | Moyenne | Moyen | | | |
| R06 | KPI non exploitables | Faible | Élevé | | | |

<!-- TODO : calculer le niveau (proba × impact), compléter mitigations + contingences, ajouter risques identifiés par l'équipe -->

---

## 8. KPI et amélioration continue

| KPI | Catégorie | Définition | Valeur initiale | Cible | Fréquence | Owner | Action si dérive |
|---|---|---|---|---|---|---|---|
| Taux adoption hebdomadaire | Adoption | | 35% | 75% | | | |
| Délai compréhension alerte | Adoption | | 5 min | 2 min | | | |
| Taux faux positifs perçu | Produit | | 28% | 15% | | | |
| Respect jalons | Projet | | N/A | ≥85% | | | |
| Tickets support bloquants | Support | | N/A | ≤3/sem | | | |
| Satisfaction formation | Accompagnement | | N/A | ≥4/5 | | | |
| Empreinte numérique projet | RSE | | N/A | Suivi mensuel | | | |

<!-- TODO : compléter définitions, owners, actions si dérive. Les 4 catégories projet/produit/adoption/RSE doivent être couvertes. -->

---

## 9. Feedbacks utilisateurs et priorisation

**Feedbacks majeurs :** <!-- TODO : synthèse des 6 feedbacks F01-F06 -->

**Analyse :** <!-- TODO : matrice Impact × Fréquence → F01, F03, F04 en tête -->

**Décisions de priorisation :** <!-- TODO : lien feedbacks → backlog (F01→B01, F04→B03, F05→B04, F06→B08...) -->

**Backlog d'amélioration :** voir [`annexes/backlog_priorise.csv`](../annexes/backlog_priorise.csv)

---

## 10. Conclusion et arbitrages demandés

**Arbitrage 1 :** <!-- TODO -->
**Arbitrage 2 :** <!-- TODO -->
**Prochaines étapes :** <!-- TODO -->

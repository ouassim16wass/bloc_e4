# Rapport de mise en œuvre et d'optimisation — E4 MobilityPulse_V1

> **Livrable 1** — couvre C19 (organisation), C20 (gouvernance agile), C23 (KPI et amélioration continue).
> Structure imposée par le template officiel : 10 sections.
> Règle d'or : chaque choix est justifié en citant le dossier documentaire (IDs B/F/R, personas, brief).

---

## 1. Synthèse exécutive

**Contexte :**

La métropole de NovaVille exploite un réseau de transport multimodal : bus, tramways, parkings relais, pistes cyclables et vélos en libre-service. Un prototype avancé de la solution MobilityPulse permet déjà de collecter les signaux de mobilité, de détecter les anomalies et d'exposer des indicateurs via une interface interne. Ce prototype a été jugé prometteur, mais la direction constate trois limites : l'organisation du passage à l'échelle n'est pas définie, les rôles entre les équipes data, IT, métier et exploitation ne sont pas formalisés, et les utilisateurs finaux demandent davantage de formation, de lisibilité et de support. Le Comité de Direction demande un dossier de pilotage permettant de sécuriser le déploiement pilote de MobilityPulse sur 12 semaines.

**Enjeux :**

- **Adoption** : seuls 35 % des utilisateurs cibles utilisent aujourd'hui l'outil ; sans accompagnement adapté, le risque est la non-adoption et le contournement de la solution (R01).
- **Gouvernance** : sans rôles formalisés, le projet s'expose à des conflits de priorités entre IT et métier et à une surcharge des équipes (R02).
- **Pilotage** : la direction a besoin d'indicateurs fiables et d'un reporting orienté décision pour arbitrer rapidement (R03, R06).
- **Inclusion et responsabilité** : le déploiement doit être accessible à tous, y compris aux utilisateurs en situation de handicap (R04), et son impact environnemental doit être suivi (exigence du brief).

**Décisions attendues :**

À l'issue de ce rapport, la direction est invitée à : **1)** valider le mode de gouvernance proposé, **2)** valider le calendrier de déploiement sur 12 semaines, **3)** arbitrer les priorités du backlog, **4)** valider le dispositif d'accompagnement des utilisateurs.

---

## 2. Objectifs SMART

| # | Objectif | Spécifique | Mesurable | Acceptable | Réaliste | Temporel |
|---|---|---|---|---|---|---|
| O1 | <!-- TODO --> | | | | | |
| O2 | | | | | | |
| O3 | | | | | | |
| O4 | | | | | | |

<!-- Pistes (à valider ensemble) :
O1 adoption : 35% → 75% d'utilisateurs actifs en 12 semaines
O2 compréhension alerte : 5 min → 2 min avant fin du pilote
O3 gouvernance : RACI + comité d'arbitrage opérationnels en S2
O4 accompagnement : 100% des profils formés avant S10, satisfaction ≥ 4/5
O5 RSE : KPI empreinte numérique défini et suivi mensuellement dès S4
-->

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

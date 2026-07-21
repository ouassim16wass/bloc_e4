---
marp: true
theme: default
paginate: true
size: 16:9
header: 'MobilityPulse_V1 — Reporting direction'
footer: 'Équipe [NomEquipe] — Semaine [X]/12'
style: |
  section {
    font-size: 26px;
  }
  h1 {
    color: #1a5276;
  }
  .statut-vert { color: #1e8449; font-weight: bold; }
  .statut-orange { color: #ca6f1e; font-weight: bold; }
  .statut-rouge { color: #c0392b; font-weight: bold; }
---

<!--
============================================================
LIVRABLE 3 — SUPPORT DE REPORTING DIRECTION (C22)
Format : 8 slides max (charte : 6-8), oral 10 min + 10 min Q/R
Règles de la charte_reporting :
  - Messages courts
  - 1 graphique ou tableau MAXIMUM par slide
  - Statut explicite vert / orange / rouge
  - Une décision attendue clairement formulée
  - Vocabulaire compréhensible par les non-techniciens
Ce fichier est alimenté AU FUR ET À MESURE du travail sur les livrables :
chaque section terminée dans le rapport → on remplit la slide correspondante.
============================================================
-->

# MobilityPulse — Reporting de déploiement

## Comité de direction — NovaVille

**Équipe :** [NomEquipe]
**Date :** [JJ/MM/AAAA]
**Statut global : <span class="statut-vert">🟢 VERT</span>** <!-- TODO: à ajuster -->

<!-- Notes orateur (≈1 min) :
- Se présenter, rappeler la mission en 1 phrase :
  "Sécuriser le déploiement organisationnel de MobilityPulse sur 12 semaines"
- Annoncer le plan de la présentation
-->

---

# Slide 1 — Message clé

<!-- TODO : à remplir quand la synthèse exécutive du Livrable 1 est prête -->

- **Objectif du déploiement :** [1 phrase — ex. rendre MobilityPulse adopté par les 3 profils d'utilisateurs en 12 semaines]
- **Où nous en sommes :** [1 phrase]
- **Statut global : 🟢 / 🟠 / 🔴**

> 💬 Message à retenir : [LA phrase que la direction doit retenir]

<!-- Notes orateur (≈1 min) : -->

---

# Slide 2 — Planning et jalons

<!-- TODO : à remplir quand le plan projet 12 semaines est prêt (Livrable 1 §3) -->

| Phase | Semaines | Jalon | Statut |
|---|---|---|---|
| [Cadrage] | S1–S2 | [J1 : gouvernance validée] | 🟢 |
| [Itérations produit] | S3–S8 | [J2 : ...] | 🟢 |
| [Accompagnement] | S6–S10 | [J3 : ...] | 🟠 |
| [Pilote] | S11–S12 | [J4 : go/no-go pilote] | ⬜ |

<!-- Notes orateur (≈1 min) : avancement vs les 12 semaines, écarts éventuels -->

---

# Slide 3 — Gouvernance

<!-- TODO : à remplir quand méthode agile + RACI sont prêtes (Livrable 1 §5-6) -->

- **Méthode :** [Scrum / Kanban / hybride] — [justification en 1 ligne]
- **Rituels :** [daily 15 min, sprint 2 sem., comité d'arbitrage hebdo...]
- **Équipe :** PO, Lead Data, Data Engineer, MLOps, Référent métier, Support (+ Référent accessibilité en transverse)
- **Circuit de décision :** [qui arbitre quoi, en 1 ligne]

<!-- Notes orateur (≈1 min) : répondre à la limite n°2 du brief (rôles non formalisés) -->

---

# Slide 4 — KPI

<!-- TODO : à remplir quand le tableau KPI est prêt (Livrable 1 §8 / annexes/tableau_kpi.csv) -->

| KPI | Initial | Cible S12 | Tendance |
|---|---|---|---|
| Taux adoption hebdomadaire (Adoption) | 35% | 75% | [→] |
| Délai compréhension alerte (Adoption) | 5 min | 2 min | [→] |
| Faux positifs perçus (Produit) | 28% | 15% | [→] |
| Respect jalons (Projet) | — | ≥ 85% | [→] |
| Empreinte numérique (RSE) | — | suivi mensuel | [→] |

<!-- Notes orateur (≈1,5 min) : 1 KPI par catégorie, insister sur adoption + RSE -->

---

# Slide 5 — Risques et alertes

<!-- TODO : à remplir quand le registre des risques est prêt (Livrable 1 §7) -->

**Top 3 risques :**

| Risque | Niveau | Mitigation |
|---|---|---|
| [R01 Non-adoption agents] | 🟠 | [Co-construction, formation courte] |
| [R02 Conflit priorités IT/métier] | 🟠 | [Comité d'arbitrage hebdo] |
| [R04 Accessibilité insuffisante] | 🟠 | [Validation type RGAA] |

**➡️ Décision attendue :** [ex. valider le comité d'arbitrage hebdomadaire]

<!-- Notes orateur (≈1,5 min) : chaque risque → sa mitigation → la décision demandée -->

---

# Slide 6 — Feedbacks utilisateurs

<!-- TODO : à remplir quand l'analyse des feedbacks est prête (Livrable 1 §9) -->

**Principaux retours du prototype :**

- 🔴 [F01] Vocabulaire des alertes trop technique → **libellés métier + aide contextuelle**
- 🔴 [F04] Pas de procédure d'escalade → **procédure + ticketing**
- 🔴 [F03] Définitions KPI implicites → **glossaire KPI**
- 🟠 [F05] Graphiques inaccessibles au lecteur d'écran → **alternatives textuelles**

**Impact sur le backlog :** [ex. B01, B03, B04 priorisés en sprint 1-2]

<!-- Notes orateur (≈1 min) : montrer que le terrain influence la suite -->

---

# Slide 7 — Accompagnement utilisateurs

<!-- TODO : à remplir quand le Livrable 2 est prêt -->

- **4 profils, 4 parcours :** superviseurs, agents, analystes, utilisateurs avec besoins d'accessibilité
- **Formats courts** (contrainte : peu de temps de formation) : atelier 45 min, tutoriels, FAQ, glossaire
- **Accessibilité :** supports lecteur d'écran, contrastes, sous-titres
- **Support post-déploiement :** niveau 1 → niveau 2 → escalade

<!-- Notes orateur (≈1 min) : répondre à la limite n°3 du brief (demande de formation/support) -->

---

# Slide 8 — Décisions demandées

<!-- TODO : consolider à la fin — reprendre les 4 décisions attendues du brief -->

| # | Décision attendue | Échéance |
|---|---|---|
| 1 | Valider le mode de gouvernance | [S1] |
| 2 | Valider le calendrier de déploiement | [S1] |
| 3 | Arbitrer les priorités du backlog | [S2] |
| 4 | Valider le dispositif d'accompagnement | [S4] |

**Prochaines étapes :** [3 bullets max]

<!-- Notes orateur (≈1 min) : finir sur les décisions = la direction sait ce qu'on attend d'elle.
Puis ouvrir la séance de Q/R (10 min). -->

---

<!--
============================================================
ANNEXE PRÉPARATION Q/R (non présentée — anti-sèche pour les 10 min de questions)
À alimenter au fur et à mesure. Questions probables du jury :
- Pourquoi Scrum plutôt que Kanban (ou l'inverse) ?
- Que faites-vous si l'adoption stagne à 50% en semaine 8 ?
- Comment mesurez-vous l'empreinte numérique ?
- Qui est Accountable sur la validation accessibilité ?
- Plan de contingence si le support sature ?
- Comment gérez-vous le peu de temps de formation des agents ?
============================================================
-->

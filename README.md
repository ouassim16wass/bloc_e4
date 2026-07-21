# 🚀 Bloc E4 — MobilityPulse_V1 (RNCP 38919 Data Engineer)

Dépôt de travail pour l'examen **E4 — Bloc 4 : « Piloter un projet d'architecture technique de gestion de données »**.

> 📖 **Commencer ici :** [`docs/ANALYSE_EXAMEN.md`](docs/ANALYSE_EXAMEN.md) — analyse complète du sujet, du contexte et des attendus.

## 🎯 La mission en une phrase

Piloter le déploiement organisationnel de **MobilityPulse** (solution d'analyse de mobilité urbaine de la métropole fictive NovaVille) sur **12 semaines** : organisation, gouvernance agile, reporting, KPI et accompagnement des utilisateurs. **Aucun code — c'est un examen de pilotage de projet.**

> ⚠️ **Travail passé en INDIVIDUEL** : le sujet est conçu pour un groupe, mais le candidat est seul.
> Consigne : s'attribuer un rôle parmi ceux de l'équipe définie → **rôle choisi : Lead Data**,
> en cohérence avec le titre Data Engineer visé. Cadrage : le brief confie le pilotage à
> « l'équipe Data Engineering », dont le Lead Data est le responsable → posture de **pilote du
> déploiement côté data** : il planifie (C19), encadre le développement en agile (C20), rend
> compte à la direction (C22), garantit la fiabilité des KPI (C23) et fiabilise les contenus
> d'accompagnement (C24). La priorisation finale du backlog reste au PO fictif (le Lead Data
> éclaire ses arbitrages). À l'oral : parler en « je » comme Lead Data, savoir expliquer tous
> les rôles de l'équipe fictive. La RACI reste inchangée : ces rôles sont ceux du scénario du brief.

## 📁 Structure du dépôt

```
bloc_e4/
├── docs/
│   └── ANALYSE_EXAMEN.md            ← Analyse approfondie du sujet (référence)
├── livrables/
│   ├── 01_rapport_mise_en_oeuvre_optimisation.md   ← Livrable 1 (C19+C20+C23)
│   ├── 02_plan_accompagnement_utilisateurs.md      ← Livrable 2 (C24)
│   └── 04_fiche_contribution_individuelle.md       ← Livrable 4 (1 seule — travail individuel)
├── slides/
│   └── slides_reporting_direction.md ← Livrable 3 (C22) — slides Marp, alimenté au fil du travail
└── annexes/
    ├── matrice_raci.csv             ← RACI à compléter
    ├── backlog_priorise.csv         ← Backlog priorisé avec justifications
    ├── registre_risques.csv         ← Registre des risques
    └── tableau_kpi.csv              ← Tableau de pilotage KPI
```

## 📊 Suivi d'avancement

| # | Tâche | Compétence | Statut |
|---|---|---|---|
| 1 | Analyse du sujet et du dossier documentaire | — | ✅ Fait |
| 1b | Synthèse exécutive (Livrable 1 §1) | C19/C22 | ✅ Fait |
| 2 | Objectifs SMART | C19 | ✅ Fait |
| 3 | Plan projet 12 semaines (phases, jalons, dépendances) | C19 | ✅ Fait |
| 4 | Parties prenantes et inclusion | C19 | ✅ Fait |
| 5 | Registre des risques + mitigations | C19/C20 | ✅ Fait |
| 6 | Méthode agile justifiée + rituels | C20 | ✅ Fait |
| 7 | Matrice RACI | C20 | ✅ Fait |
| 8 | Backlog priorisé + justifications | C19/C23 | ✅ Fait |
| 9 | Tableau KPI (projet, produit, adoption, RSE) | C23 | ✅ Fait |
| 10 | Analyse feedbacks + axes d'amélioration | C23 | ✅ Fait |
| 11 | Plan d'accompagnement utilisateurs | C24 | 🔲 À faire |
| 12 | Slides reporting direction (8 slides, 10 min) | C22 | 🟡 Squelette créé |
| 13 | Fiche de contribution individuelle (1 seule — travail individuel) | Qualité | 🔲 À faire |
| 14 | Export PDF + archive `E4_MobilityPulse_NomEquipe.zip` | Qualité | 🔲 À faire |

## 🎤 Générer les slides à partir du .md

Le fichier `slides/slides_reporting_direction.md` est au format **[Marp](https://marp.app/)** :

```bash
# Avec l'extension VS Code "Marp for VS Code" : ouvrir le .md → bouton export PDF/PPTX
# Ou en ligne de commande :
npx @marp-team/marp-cli slides/slides_reporting_direction.md --pdf --allow-local-files
npx @marp-team/marp-cli slides/slides_reporting_direction.md --pptx --allow-local-files
```

## ⛔ Rappels hors-périmètre (critique)

- ❌ Pas de code, ETL, API, Docker, architecture technique (E2/E3)
- ❌ Pas d'analyse financière / budget / ROI (C21/E5)
- ❌ Pas de veille ni cahier des charges (E1)
- ✅ Fils rouges partout : **accessibilité/inclusion** + **impact environnemental (RSE)** + **orientation décision**

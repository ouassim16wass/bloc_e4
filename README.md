# 🚀 Bloc E4 — MobilityPulse_V1 (RNCP 38919 Data Engineer)

Dépôt de travail pour l'examen **E4 — Bloc 4 : « Piloter un projet d'architecture technique de gestion de données »**.

> 📖 **Commencer ici :** [`docs/ANALYSE_EXAMEN.md`](docs/ANALYSE_EXAMEN.md) — analyse complète du sujet, du contexte et des attendus.

## 🎯 La mission en une phrase

Piloter le déploiement organisationnel de **MobilityPulse** (solution d'analyse de mobilité urbaine de la métropole fictive NovaVille) sur **12 semaines** : organisation, gouvernance agile, reporting, KPI et accompagnement des utilisateurs. **Aucun code — c'est un examen de pilotage de projet.**

## 📁 Structure du dépôt

```
bloc_e4/
├── docs/
│   └── ANALYSE_EXAMEN.md            ← Analyse approfondie du sujet (référence)
├── livrables/
│   ├── 01_rapport_mise_en_oeuvre_optimisation.md   ← Livrable 1 (C19+C20+C23)
│   ├── 02_plan_accompagnement_utilisateurs.md      ← Livrable 2 (C24)
│   └── 04_fiche_contribution_individuelle.md       ← Livrable 4 (1 par membre)
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
| 2 | Objectifs SMART | C19 | 🔲 À faire |
| 3 | Plan projet 12 semaines (phases, jalons, dépendances) | C19 | 🔲 À faire |
| 4 | Parties prenantes et inclusion | C19 | 🔲 À faire |
| 5 | Registre des risques + mitigations | C19/C20 | 🔲 À faire |
| 6 | Méthode agile justifiée + rituels | C20 | 🔲 À faire |
| 7 | Matrice RACI | C20 | 🔲 À faire |
| 8 | Backlog priorisé + justifications | C19/C23 | 🔲 À faire |
| 9 | Tableau KPI (projet, produit, adoption, RSE) | C23 | 🔲 À faire |
| 10 | Analyse feedbacks + axes d'amélioration | C23 | 🔲 À faire |
| 11 | Plan d'accompagnement utilisateurs | C24 | 🔲 À faire |
| 12 | Slides reporting direction (8 slides, 10 min) | C22 | 🟡 Squelette créé |
| 13 | Fiches de contribution individuelles | Qualité | 🔲 À faire |
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

# 📘 ANALYSE APPROFONDIE — Examen E4 « MobilityPulse_V1 » (Bloc 4, RNCP 38919 Data Engineer)

> Document d'analyse complet de tous les dossiers, fichiers et contenus de l'examen,
> avec synthèse, contexte, explication des attendus et croisements entre les données.

---

## Table des matières

1. [Synthèse exécutive de l'examen](#1-synthèse-exécutive-de-lexamen)
2. [Qu'est-ce que le RNCP 38919 et le Bloc 4 ?](#2-quest-ce-que-le-rncp-38919-et-le-bloc-4-)
3. [Cartographie complète des dossiers et fichiers](#3-cartographie-complète-des-dossiers-et-fichiers)
4. [Le contexte fictif : NovaVille et MobilityPulse](#4-le-contexte-fictif--novaville-et-mobilitypulse)
5. [Les 5 compétences évaluées en détail](#5-les-5-compétences-évaluées-en-détail)
6. [Ce qui est explicitement HORS PÉRIMÈTRE](#6-ce-qui-est-explicitement-hors-périmètre)
7. [Les 4 livrables attendus — analyse détaillée](#7-les-4-livrables-attendus--analyse-détaillée)
8. [Analyse approfondie du dossier documentaire (les données)](#8-analyse-approfondie-du-dossier-documentaire-les-données)
9. [Croisements stratégiques entre les données (la clé de la note)](#9-croisements-stratégiques-entre-les-données-la-clé-de-la-note)
10. [Les templates fournis et comment les utiliser](#10-les-templates-fournis-et-comment-les-utiliser)
11. [Organisation sur 3 jours (hackathon)](#11-organisation-sur-3-jours-hackathon)
12. [Critères d'évaluation et checklist finale](#12-critères-dévaluation-et-checklist-finale)
13. [Pièges à éviter et conseils stratégiques](#13-pièges-à-éviter-et-conseils-stratégiques)

---

## 1. Synthèse exécutive de l'examen

| Élément | Détail |
|---|---|
| **Titre visé** | RNCP 38919 — Data Engineer |
| **Bloc évalué** | Bloc 4 : « Piloter un projet d'architecture technique de gestion de données » |
| **Épreuve** | E4 (examen blanc) |
| **Sujet** | MobilityPulse_V1 — piloter le déploiement organisationnel d'une solution d'analyse de mobilité urbaine |
| **Compétences** | C19, C20, C22, C23, C24 |
| **Format** | Hackathon 3 jours, travail en groupe + fiche individuelle |
| **Durée du projet fictif** | 12 semaines de déploiement pilote |
| **Restitution orale** | 10 minutes de présentation + 10 minutes de questions/réponses |
| **Rendu** | Archive `E4_MobilityPulse_NomEquipe.zip` contenant 4 livrables PDF + annexes CSV |

### L'idée centrale en une phrase

> **La solution technique existe déjà (prototype avancé). Votre mission n'est PAS de coder,
> mais de PILOTER : structurer le projet, coordonner les parties prenantes, suivre la
> performance et préparer l'adoption par les utilisateurs.**

C'est un examen de **chef de projet / management de projet data**, pas un examen de développement.
Tout ce qui est technique (code, ETL, API, Docker, Kubernetes) est explicitement interdit de périmètre.
Tout ce qui est financier (budget, ROI) relève d'une autre épreuve (E5/C21) et ne doit pas être traité.

### Les 3 fils rouges transversaux (présents dans TOUT le sujet)

1. **♿ Accessibilité et inclusion** — apparaît dans C19, C20, C24, dans le persona Jules, le risque R04, le feedback F05, la user story B04, la matrice RACI (colonne « Référent accessibilité »)… C'est LE critère transversal du sujet.
2. **🌱 Impact environnemental (RSE)** — KPI « Empreinte numérique », feedback F06, user story B08, contrainte du brief direction.
3. **🎯 Orientation décision** — le vocabulaire doit être celui d'un reporting de direction : court, clair, statuts vert/orange/rouge, décisions attendues explicites.

---

## 2. Qu'est-ce que le RNCP 38919 et le Bloc 4 ?

- **RNCP** = Répertoire National des Certifications Professionnelles. Un titre RNCP est une
  certification professionnelle reconnue par l'État français, découpée en **blocs de compétences**.
- **RNCP 38919** = titre « **Data Engineer** » (niveau 7, équivalent Bac+5).
- **Bloc 4** = « **Piloter un projet d'architecture technique de gestion de données** ».
  Ce bloc valide la capacité à **manager un projet data** : organisation, gouvernance agile,
  reporting, mesure de performance et conduite du changement.
- **E4** = l'épreuve qui valide ce bloc. Chaque bloc a son épreuve (E1 = analyse du besoin,
  E2/E3 = réalisation technique, E5 = analyse financière, etc.).

Le dossier insiste lourdement sur **l'indépendance E1/E4** (un document entier y est consacré :
`note_independance_E1_E4.docx`) : vous n'avez PAS besoin d'avoir fait E1, et vous ne devez PAS
refaire une veille, un cahier des charges ou une analyse de besoin. Le cadrage minimal est fourni.

---

## 3. Cartographie complète des dossiers et fichiers

```
bloc E4_RNCP_wass/
└── Bloc 4 - E4_MobilityPulse_V1_RNCP38919/
    └── Bloc 4 - E4/
        ├── README.docx                          ← Vue d'ensemble du dossier d'examen
        │
        ├── 01_sujet_etudiant/                   ← LE SUJET (ce qu'on vous demande)
        │   ├── sujet_examen_blanc_E4_mobilitypulse.docx   ← Sujet principal (LE document maître)
        │   ├── consignes_rendu.docx                       ← Format et nommage du rendu
        │   ├── checklist_candidat.docx                    ← Auto-vérification par compétence
        │   └── planning_hackathon_3_jours.docx            ← Organisation conseillée des 3 jours
        │
        ├── 03_templates_candidat/               ← MODÈLES À REMPLIR (facultatifs, recommandés)
        │   ├── README_templates.docx                      ← Liste des templates
        │   ├── rapport_mise_en_oeuvre_optimisation_template.docx  ← Squelette du Livrable 1
        │   ├── plan_accompagnement_utilisateurs_template.docx     ← Squelette du Livrable 2
        │   ├── support_reporting_direction_template.docx          ← Canevas 8 slides du Livrable 3
        │   ├── fiche_contribution_individuelle_template.docx      ← Squelette du Livrable 4
        │   ├── matrice_raci_template.csv                  ← RACI vide (7 rôles × 6 activités)
        │   ├── backlog_priorise_template.csv              ← Backlog à prioriser (vide)
        │   ├── registre_risques_template.csv              ← Registre de risques (vide)
        │   └── tableau_kpi_template.csv                   ← Tableau KPI (vide)
        │
        └── dossier_documentaire/                ← VOS DONNÉES DE TRAVAIL (la matière première)
            ├── brief_direction_mobilitypulse.docx         ← Commande de la direction, contraintes
            ├── parties_prenantes_et_personas.docx         ← 6 parties prenantes + 4 personas
            ├── annexes_metier/
            │   ├── charte_reporting.docx                  ← Règles du reporting direction
            │   └── note_independance_E1_E4.docx           ← Périmètre : E4 est autonome
            └── donnees_pilotage/
                ├── backlog_initial.csv                    ← 10 user stories à prioriser
                ├── feedbacks_utilisateurs.csv             ← 6 retours utilisateurs à analyser
                ├── kpi_initial.csv                        ← 7 KPI avec valeurs et cibles
                └── risques_initial.csv                    ← 6 risques initiaux à compléter
```

> ℹ️ Le README mentionne aussi `02_correcteur/` et `04_solution_indicative/` — ces dossiers sont
> **réservés à l'équipe pédagogique** et ne sont (logiquement) pas dans votre copie du dossier.

### Rôle de chaque fichier en une ligne

| Fichier | Rôle | Comment l'utiliser |
|---|---|---|
| `README.docx` | Présentation générale, compétences visées, hors-périmètre | Lire une fois pour cadrer |
| `sujet_examen_blanc_E4_mobilitypulse.docx` | **Document maître** : contexte, compétences, livrables, critères | À relire en continu — tout part de là |
| `consignes_rendu.docx` | Nommage de l'archive, liste des PDF attendus | Vérifier avant le rendu final |
| `checklist_candidat.docx` | 27 cases à cocher réparties par compétence | Auto-contrôle qualité avant rendu |
| `planning_hackathon_3_jours.docx` | Répartition conseillée du travail sur 3 jours | Organiser l'équipe |
| `brief_direction_mobilitypulse.docx` | La « commande client » : contexte, contraintes, décisions attendues | Base de la synthèse exécutive et des objectifs |
| `parties_prenantes_et_personas.docx` | Qui sont les acteurs et les utilisateurs | Base des sections parties prenantes et accompagnement |
| `charte_reporting.docx` | Règles imposées pour le support de direction | Contraintes du Livrable 3 |
| `note_independance_E1_E4.docx` | Délimite le périmètre | Éviter le hors-sujet |
| `backlog_initial.csv` | 10 user stories avec priorités/complexité/dépendances | À prioriser et planifier en sprints |
| `feedbacks_utilisateurs.csv` | 6 retours du terrain sur le prototype | À analyser → axes d'amélioration (C23) |
| `kpi_initial.csv` | 7 indicateurs avec valeurs initiales et cibles à 12 semaines | Base du tableau de pilotage (C23) |
| `risques_initial.csv` | 6 risques avec signaux faibles et mesures attendues | Base du registre de risques (C19/C20) |
| Templates `.docx`/`.csv` | Squelettes pré-structurés des livrables | Remplir plutôt que partir de zéro |

---

## 4. Le contexte fictif : NovaVille et MobilityPulse

### Le décor

**NovaVille** est une métropole fictive qui exploite un réseau de transport complet :
bus, tramways, parkings relais, pistes cyclables, vélos en libre-service et capteurs de trafic.

**MobilityPulse** est une solution d'analyse de mobilité urbaine dont le **prototype existe déjà** :
- une chaîne de collecte de données (signaux de mobilité),
- un modèle de détection d'anomalies,
- une API de consultation et une interface interne exposant des indicateurs.

### Le problème (pourquoi on vous appelle)

Le prototype est jugé **prometteur**, mais la direction constate **3 limites** :

1. **Organisation** — les équipes ne savent pas comment organiser le passage à l'échelle ;
2. **Rôles** — les responsabilités entre data, IT, métier et exploitation ne sont pas formalisées ;
3. **Adoption** — les utilisateurs finaux réclament plus de formation, de lisibilité et de support.

→ Ces 3 limites correspondent exactement aux 3 axes de votre travail :
**plan projet (C19) + gouvernance/RACI (C20) + accompagnement (C24)**, le tout mesuré (C23) et reporté (C22).

### La commande de la direction

Produire un **dossier de pilotage** pour sécuriser le déploiement de MobilityPulse sur **12 semaines**, avec 6 objectifs :

1. Mettre en place une gouvernance claire
2. Prioriser les évolutions du produit
3. Organiser le travail de l'équipe projet
4. Suivre la performance projet et produit
5. Préparer l'adoption par les utilisateurs finaux
6. Intégrer l'accessibilité et l'inclusion dans le dispositif

### Les contraintes imposées (à respecter et à citer dans vos livrables)

| Contrainte | Conséquence pour vous |
|---|---|
| Déploiement pilote dans **12 semaines** | Votre plan projet doit tenir sur 12 semaines, jalons datés |
| Équipe limitée : **1 PO, 1 lead data, 1 data engineer, 1 MLOps, 1 représentant métier, 1 référent support** | La RACI et le plan de charge doivent utiliser exactement ces rôles |
| Les agents ont **peu de temps de formation** | Formats courts : tutoriels, ateliers de 45 min, aide contextuelle |
| La solution doit rester **compréhensible par des non-techniques** | Vocabulaire métier, glossaire, reporting simplifié |
| L'**impact environnemental** doit être suivi | Au moins 1 KPI RSE dans le tableau de bord |

### Les décisions attendues de la hiérarchie (à faire figurer dans le reporting)

Le brief liste 4 décisions que la direction devra prendre — votre Livrable 3 (reporting) doit
explicitement les demander :
1. Valider le mode de gouvernance
2. Valider le calendrier de déploiement
3. Arbitrer les priorités du backlog
4. Valider le dispositif d'accompagnement utilisateurs

---

## 5. Les 5 compétences évaluées en détail

### C19 — Définir la structure organisationnelle du projet

**Ce qu'on attend :** structurer et planifier le projet.
- Objectifs **SMART** (Spécifique, Mesurable, Acceptable/Atteignable, Réaliste, Temporel)
- Plan projet : **phases, jalons, tâches, priorités, durées estimées, dépendances**
- Identification des **parties prenantes** avec rôles et attentes
- Prise en compte des **situations de handicap** dès la planification

**Où trouver la matière :** brief direction (contraintes, 12 semaines), parties prenantes et personas,
backlog initial (dépendances), risques initiaux.

### C20 — Encadrer le développement avec des méthodes agiles

**Ce qu'on attend :** la gouvernance de l'équipe.
- **Méthode agile argumentée** : Scrum, Kanban ou hybride — le choix doit être JUSTIFIÉ
  (ex. équipe de 6, cadence 12 semaines, besoin de rituels courts → Scrum avec sprints de 2 semaines,
  ou Kanban pour le flux support…)
- **Rituels** : daily, sprint planning, revue, rétrospective, comité d'arbitrage hebdo (répond au risque R02)
- **Matrice RACI** complète et justifiée (7 rôles × activités clés)
- **Mesures d'inclusion** dans le fonctionnement d'équipe
- Risques de coordination identifiés

### C22 — Communiquer l'avancement à la hiérarchie

**Ce qu'on attend :** le reporting.
- Reporting **adapté à la hiérarchie** (non technique, orienté décision)
- Synthèse claire : avancement, risques, décisions attendues
- Support compatible avec un **oral de 10 minutes**, préparation des **Q/R (10 minutes)**
- Respect strict de la **charte de reporting** fournie : 6–8 slides max, messages courts,
  1 graphique/tableau max par slide, statut vert/orange/rouge, décision attendue formulée

### C23 — Évaluer la performance du projet

**Ce qu'on attend :** le pilotage par indicateurs.
- KPI en **4 catégories obligatoires** : projet, produit, adoption, **RSE**
- Pour chaque KPI : définition, valeur initiale, cible, fréquence, owner, **action si dérive**
- **Analyse des feedbacks utilisateurs** (les 6 fournis) et transformation en
  **axes d'amélioration priorisés** (backlog d'amélioration)
- **Mesure d'impact environnemental** intégrée

### C24 — Former et accompagner les utilisateurs finaux

**Ce qu'on attend :** la conduite du changement.
- **Typologies d'utilisateurs** définies (s'appuyer sur les 4 personas)
- **Parcours de formation par profil** (besoins différents selon Sarah, Malik, Elena, Jules)
- **Supports** : guide de démarrage, ateliers (45 min — cf. B07), FAQ, tutoriels courts, glossaire KPI
- **Calendrier de déploiement** de l'accompagnement + **support post-déploiement**
  (niveau 1, niveau 2, escalade — répond à F04 et R05)
- **Accessibilité des supports vérifiée** : lecteur d'écran, contraste, sous-titres,
  alternatives textuelles (répond à Jules, F05, R04, B04)

---

## 6. Ce qui est explicitement HORS PÉRIMÈTRE

⛔ Le sujet le répète dans 4 documents différents (README, sujet, consignes, note d'indépendance) —
c'est donc un critère d'élimination du hors-sujet :

| Interdit | Relève de | Pourquoi c'est un piège |
|---|---|---|
| Analyse financière, budget, ROI | **C21 / épreuve E5** | Réflexe classique dans un rapport de pilotage — ici NON évalué |
| Analyse du besoin, veille technologique, cahier des charges d'architecture | **Épreuve E1** | Le cadrage est déjà fourni dans le dossier documentaire |
| Code, ETL, API, Docker, Kubernetes, architecture technique détaillée | **Épreuves E2/E3** | « Ne transformez pas l'épreuve en dossier technique » (citation du sujet) |

> Le message des correcteurs est clair : du temps passé sur ces sujets = du temps perdu
> qui ne rapporte aucun point, et un signe de mauvaise compréhension de la consigne.

---

## 7. Les 4 livrables attendus — analyse détaillée

### 📄 Livrable 1 — `rapport_mise_en_oeuvre_optimisation.pdf`

**Le document principal.** Il couvre C19 + C20 + C23. Le template fourni impose 10 sections :

1. **Synthèse exécutive** — contexte, enjeux, décisions attendues (reprendre le brief direction)
2. **Objectifs SMART** — tableau avec les 5 critères S/M/A/R/T explicités par objectif
3. **Plan projet** — phases, objectifs, tâches, durées, jalons, dépendances, responsables (sur 12 semaines)
4. **Parties prenantes** — rôle, attentes, niveau d'influence, **besoins d'inclusion/accessibilité**
5. **Méthode agile et gouvernance** — méthode choisie + justification, rituels, outil de suivi, cadence de reporting
6. **Matrice RACI** — complète (utiliser le CSV template)
7. **Risques et mitigations** — probabilité, impact, niveau, mesure préventive, plan de contingence
8. **KPI et amélioration continue** — définition, valeur initiale, cible, fréquence, owner, action si dérive
9. **Feedbacks utilisateurs et priorisation** — analyse des 6 feedbacks → décisions → backlog d'amélioration
10. **Conclusion et arbitrages demandés** — les décisions que la direction doit prendre

**Style attendu :** « structuré, synthétique et exploitable par une direction de programme ».

### 📄 Livrable 2 — `plan_accompagnement_utilisateurs.pdf`

**Couvre C24.** Le template impose 7 sections :

1. Objectif du plan
2. **Profils utilisateurs** — besoin, niveau initial, freins, adaptations (→ utiliser les 4 personas)
3. **Parcours d'accompagnement** — étapes, public, format, durée, support, responsable, indicateur de succès
4. **Supports prévus** — guide de démarrage, FAQ, tutoriels courts, atelier pratique, glossaire KPI, canal support
5. **Accessibilité et inclusion** — lecteur d'écran, contraste, sous-titres/transcriptions, temps d'appropriation, modalités alternatives
6. **Support post-déploiement** — niveau 1, niveau 2, escalade, collecte de feedback
7. **KPI d'adoption** — cible, fréquence, responsable

### 📄 Livrable 3 — `support_reporting_direction.pdf`

**Couvre C22.** Présentation orale **10 min + 10 min Q/R**. Le canevas fourni propose 8 slides :

| Slide | Contenu |
|---|---|
| 1 | Message clé : objectif du projet et statut global (vert/orange/rouge) |
| 2 | Planning et jalons : avancement par rapport aux 12 semaines |
| 3 | Gouvernance : équipe, rituels, RACI, circuit de décision |
| 4 | KPI prioritaires : projet, produit, adoption, RSE |
| 5 | Risques et alertes : top 3 risques, mitigation, décisions attendues |
| 6 | Feedbacks utilisateurs : principaux retours et impacts sur le backlog |
| 7 | Accompagnement : plan formation, support, accessibilité |
| 8 | Décisions demandées : arbitrages, prochaines étapes, calendrier |

**⚠️ Contraintes de la charte de reporting (imposées) :**
- 6 à 8 slides **maximum**
- Messages courts, **1 graphique ou tableau maximum par slide**
- Un **statut explicite vert/orange/rouge**
- Une **décision attendue clairement formulée**
- Vocabulaire **compréhensible par les non-techniciens**

La charte définit aussi les 6 questions auxquelles le reporting doit répondre :
où en sommes-nous / quels livrables / quels risques demandent une décision /
quels indicateurs progressent / quels retours utilisateurs / quels arbitrages demandés.

### 📄 Livrable 4 — `fiche_contribution_individuelle_NOM.pdf` (une par membre)

**1 page par candidat.** Le template impose :
1. Contributions réalisées
2. Décisions/arbitrages auxquels j'ai contribué
3. Compétences mobilisées (une ligne par compétence C19, C20, C22, C23, C24)
4. Difficultés rencontrées et solutions proposées
5. Auto-évaluation (points forts / points à améliorer)

> C'est ce qui permet au jury de **noter individuellement** dans un travail de groupe.
> Chaque membre doit pouvoir montrer une contribution réelle sur PLUSIEURS compétences.

### 📦 Contraintes de rendu (consignes_rendu.docx)

- Archive : **`E4_MobilityPulse_NomEquipe.zip`**
- Formats : **PDF** pour les rapports finaux, fichiers sources en annexe si utiles
- Annexes utiles : RACI, backlog priorisé, tableau KPI, registre des risques (les CSV remplis)
- Le dossier doit être **lisible sans outils externes**
- **Chaque choix doit être justifié** : « une simple liste d'outils ou de tâches ne suffit pas »

---

## 8. Analyse approfondie du dossier documentaire (les données)

### 8.1 Les parties prenantes (6 acteurs)

| Acteur | Attentes | Risque si ignoré |
|---|---|---|
| **Direction mobilité** | Visibilité, KPI, décisions rapides | Perte de confiance dans la solution |
| **Centre de supervision** | Alertes lisibles, procédures simples | Non-adoption, contournement de l'outil |
| **Équipe Data/IT** | Gouvernance technique, priorités claires | Dette projet, surcharge, conflits de priorité |
| **Service support** | Documentation et escalade | Saturation après mise en production |
| **Référent handicap/accessibilité** | Supports accessibles, outils compatibles | Exclusion de certains utilisateurs |
| **Exploitants terrain** | Informations actionnables | Retours terrain non exploités |

> 💡 La colonne « Risques si non pris en compte » est un cadeau : elle justifie directement
> votre registre de risques et votre priorisation.

### 8.2 Les 4 personas utilisateurs

| Persona | Rôle | Besoin | Contrainte | Attente |
|---|---|---|---|---|
| **Sarah** | Responsable supervision | Tableau de bord clair, indicateurs critiques, reporting quotidien | Décisions rapides en heure de pointe | Alertes fiables, peu de faux positifs |
| **Malik** | Agent centre opérationnel | Comprendre une alerte en **moins de 2 minutes** | Forte charge cognitive lors des incidents | Tutoriel court + procédure d'escalade |
| **Elena** | Analyste mobilité | Analyser les tendances, exporter les KPI | Articulation avec les rapports mensuels existants | Données fiables, définitions d'indicateurs explicites |
| **Jules** | Utilisateur avec besoin d'accessibilité | Lecteur d'écran, contraste suffisant, alternatives textuelles | Graphiques illisibles sans description | Documentation accessible, formations sous-titrées |

> 💡 Chaque persona correspond à un **parcours de formation différent** dans le Livrable 2 :
> Sarah → prise en main dashboard + reporting ; Malik → tutoriel express + escalade ;
> Elena → glossaire KPI + export ; Jules → supports accessibles RGAA.

### 8.3 Le backlog initial (10 user stories)

| ID | Epic | User story (résumé) | Priorité | Complexité | Dépendances |
|---|---|---|---|---|---|
| B01 | Adoption | Agent : comprendre une alerte en < 2 min | **Haute** | M | Documentation alertes |
| B02 | Reporting | Direction : reporting hebdomadaire des KPI | **Haute** | S | Définition KPI |
| B03 | Support | Support : procédure d'escalade incident | **Haute** | S | Rôles RACI |
| B04 | Accessibilité | Utilisateur lecteur d'écran : documentation compatible | **Haute** | M | Validation référent accessibilité |
| B05 | Produit | Analyste : exporter les anomalies en CSV | Moyenne | M | Permissions |
| B06 | Produit | Manager : tendance des anomalies par ligne | Moyenne | M | Qualité data |
| B07 | Formation | Formateur : support atelier de 45 minutes | **Haute** | S | Plan accompagnement |
| B08 | RSE | Direction RSE : suivre l'empreinte numérique | Moyenne | L | Définition indicateur |
| B09 | Gouvernance | PO : backlog priorisé avec arbitrages | **Haute** | S | Comité projet |
| B10 | Qualité | Lead data : canal de feedback structuré | Moyenne | S | Formulaire feedback |

**Lecture stratégique :**
- 6 stories **Haute** priorité, dont 4 de complexité **S** (Small) → quick wins des premiers sprints : B02, B03, B07, B09.
- Les **dépendances forment une chaîne logique** : B09 (backlog priorisé) dépend du comité projet
  → B03 dépend de la RACI → B02 dépend de la définition des KPI → cela DICTE l'ordre des sprints.
- B08 (RSE) est la seule complexité **L** (Large) → à démarrer tôt malgré sa priorité moyenne,
  ou à découper.
- Statuts : seuls B05 et B06 sont « Prototype » (déjà partiellement là) ; le reste est « À cadrer ».

### 8.4 Les feedbacks utilisateurs (6 retours)

| ID | Profil | Feedback | Impact | Fréquence | Suggestion fournie |
|---|---|---|---|---|---|
| F01 | Agent supervision | Vocabulaire des alertes trop technique | **Élevé** | **Fréquent** | Libellés métier + aide contextuelle |
| F02 | Manager | Reporting sans statut global pour décider vite | Moyen | Occasionnel | Statut synthèse vert/orange/rouge |
| F03 | Analyste | Définitions des KPI pas explicites | **Élevé** | **Fréquent** | Glossaire KPI |
| F04 | Support | Aucune procédure claire en cas de mauvaise alerte | **Élevé** | **Fréquent** | Procédure escalade + ticketing |
| F05 | Référent accessibilité | Graphiques non interprétables au lecteur d'écran | **Élevé** | Occasionnel | Descriptions textuelles + alternatives |
| F06 | Direction RSE | Impact environnemental non mesuré | Moyen | Occasionnel | KPI sobriété numérique |

**Lecture stratégique :** une matrice **Impact × Fréquence** donne la priorisation attendue :
1. **F01, F03, F04** (élevé + fréquent) → à traiter en premier
2. **F05** (élevé + occasionnel, et obligation d'inclusion) → haut de liste aussi
3. **F02, F06** (moyen) → traités via le reporting et le KPI RSE

### 8.5 Les KPI initiaux (7 indicateurs)

| KPI | Définition | Valeur initiale | Cible 12 semaines | Catégorie |
|---|---|---|---|---|
| Délai compréhension alerte | Temps moyen pour comprendre une alerte critique | 5 min | **2 min** | Adoption |
| Taux adoption hebdomadaire | Utilisateurs actifs / utilisateurs cibles | 35% | **75%** | Adoption |
| Taux faux positifs perçu | Alertes jugées non pertinentes par les agents | 28% | **15%** | Produit |
| Respect jalons | Jalons tenus / jalons planifiés | N/A | **≥ 85%** | Projet |
| Tickets support bloquants | Tickets bloquants ouverts | N/A | **≤ 3/semaine** | Support |
| Satisfaction formation | Score moyen après atelier | N/A | **≥ 4/5** | Accompagnement |
| Empreinte numérique projet | Estimation relative ressources/run | N/A | **Suivi mensuel** | RSE |

**Lecture stratégique :**
- Les 4 catégories demandées par le sujet (projet, produit, adoption, RSE) sont couvertes —
  vous pouvez enrichir mais la base est là.
- Les valeurs « N/A » signifient : **à instrumenter dès le début du projet** (la mesure fait partie du plan).
- La cible « 2 min de compréhension d'alerte » vient **directement du persona Malik** et de la story B01.

### 8.6 Le registre de risques initial (6 risques)

| ID | Risque | Probabilité | Impact | Signaux faibles | Mesure attendue |
|---|---|---|---|---|---|
| R01 | Non-adoption par les agents | Moyenne | **Élevé** | Faible participation aux ateliers | Co-construction, formation courte, support terrain |
| R02 | Conflit de priorités IT/métier | Moyenne | **Élevé** | Backlog non arbitré | Comité d'arbitrage hebdomadaire |
| R03 | Reporting trop technique | **Élevée** | Moyen | Questions récurrentes de la direction | Synthèse exécutive + glossaire |
| R04 | Accessibilité insuffisante | Moyenne | **Élevé** | Retours du référent handicap | Validation type RGAA des supports |
| R05 | Surcharge support au démarrage | Moyenne | Moyen | Hausse des tickets incidents | FAQ, niveau 1, procédure d'escalade |
| R06 | KPI non exploitables | Faible | **Élevé** | Indicateurs contradictoires | Owner et formule définis pour chaque KPI |

**Lecture stratégique :** la colonne « Mesure attendue » est encore un cadeau — elle vous dit
littéralement ce que le correcteur attend de trouver dans vos livrables (comité hebdo, glossaire,
validation RGAA, FAQ + escalade, owners de KPI…).

---

## 9. Croisements stratégiques entre les données (la clé de la note)

**C'est ici que se joue la différence entre une copie moyenne et une excellente copie.**
Le dossier documentaire est construit pour que tout se recoupe. Chaque choix que vous faites
doit citer ses sources. Exemples de chaînes de justification complètes :

### Chaîne 1 — L'alerte compréhensible (fil « adoption »)
> **Persona Malik** (comprendre une alerte en < 2 min) → **Feedback F01** (vocabulaire trop
> technique, impact élevé, fréquent) → **Story B01** (priorité haute) → **KPI « Délai
> compréhension alerte »** (5 min → 2 min) → **Risque R01** (non-adoption) → **Livrable 2**
> (tutoriel court pour Malik) → **Slide 6 du reporting** (feedback → backlog).

### Chaîne 2 — L'accessibilité (fil « inclusion »)
> **Persona Jules** (lecteur d'écran) → **Partie prenante « Référent accessibilité »** →
> **Feedback F05** (graphiques illisibles) → **Story B04** (priorité haute) → **Risque R04**
> (validation RGAA) → **RACI** (colonne Référent accessibilité) → **Livrable 2 section 5**
> (supports accessibles, sous-titres) → exigence C19/C20/C24.

### Chaîne 3 — Le reporting lisible (fil « direction »)
> **Feedback F02** (pas de statut global) → **Charte de reporting** (statut vert/orange/rouge
> obligatoire) → **Risque R03** (reporting trop technique, probabilité élevée) → **Story B02**
> (reporting hebdo) → **Livrable 3** (8 slides, statuts, décisions demandées).

### Chaîne 4 — Le support qui tient (fil « après-déploiement »)
> **Feedback F04** (pas de procédure d'escalade) → **Story B03** (priorité haute, dépend de la
> RACI) → **Risque R05** (surcharge support) → **KPI « Tickets bloquants ≤ 3/semaine »** →
> **Livrable 2 section 6** (niveau 1, niveau 2, escalade).

### Chaîne 5 — La RSE (fil « environnement »)
> **Contrainte du brief** (impact environnemental suivi) → **Feedback F06** → **Story B08**
> (complexité L → anticiper) → **KPI « Empreinte numérique »** (suivi mensuel) → exigence C23.

### Chaîne 6 — La gouvernance (fil « arbitrage »)
> **Limite n°2 du brief** (rôles non formalisés) → **Risque R02** (conflit IT/métier) →
> **Story B09** (backlog priorisé avec arbitrages) → **Comité d'arbitrage hebdomadaire** (rituel
> C20) → **RACI** → **Décision attendue n°1 et n°3 du brief** (valider gouvernance, arbitrer backlog).

> 📌 **Méthode pratique :** dans chaque livrable, référencez les IDs (F01, B03, R04, persona Malik…).
> C'est la preuve visible que vos choix s'appuient sur le dossier documentaire — exactement ce que
> le sujet exige (« Appuyez chaque choix sur les contraintes du dossier documentaire »).

---

## 10. Les templates fournis et comment les utiliser

Les templates sont **facultatifs mais fortement recommandés** (dixit le README templates).
Les utiliser garantit de ne rien oublier — chaque colonne vide est un attendu du correcteur.

| Template | Colonnes/sections imposées | Compétence |
|---|---|---|
| `matrice_raci_template.csv` | 7 rôles (PO, Lead Data, Data Engineer, MLOps, Référent métier, Support, Référent accessibilité) × 6 activités (planification, priorisation backlog, définition KPI, plan accompagnement, validation accessibilité, reporting direction) | C20 |
| `backlog_priorise_template.csv` | ID, Epic, User story, **Priorité finale, Justification**, Sprint cible, Owner, Dépendances | C19/C23 |
| `registre_risques_template.csv` | ID, Risque, Probabilité, Impact, Niveau, Mitigation, Owner, Statut | C19/C20 |
| `tableau_kpi_template.csv` | KPI, Catégorie, Définition, Valeur initiale, Cible, Fréquence, Owner, **Action si dérive** | C23 |

**Points d'attention sur la RACI :**
- R = Responsible (réalise), A = Accountable (rend compte, **un seul A par ligne**),
  C = Consulted, I = Informed.
- La colonne « Référent accessibilité » n'est pas dans l'équipe des 6 du brief → c'est un rôle
  transverse à faire intervenir en C (consulté) ou A sur « Validation accessibilité ».

**Points d'attention sur le backlog :** les colonnes « Priorité finale » et « Justification »
montrent qu'on attend un **arbitrage argumenté**, pas une simple recopie du backlog initial
(ex. méthode MoSCoW ou WSJF, croisée avec les feedbacks et les risques).

---

## 11. Organisation sur 3 jours (hackathon)

| Jour | Thème | Matin | Après-midi | Livrables produits |
|---|---|---|---|---|
| **J1** | Structurer le projet | Lecture du dossier documentaire, clarification du périmètre, objectifs SMART | Plan projet, jalons, dépendances, parties prenantes, premiers risques | Sections 1–4 et 7 du Livrable 1, RACI v1 |
| **J2** | Gouverner et mesurer | Méthode agile, RACI, rituels, outils de pilotage | KPI, feedbacks utilisateurs, axes d'amélioration, reporting direction | Sections 5–6, 8–9 du Livrable 1, Livrable 3 v1 |
| **J3** | Accompagner et restituer | Plan d'accompagnement utilisateurs, inclusion, support post-déploiement | Consolidation des livrables, préparation du reporting 10 min et Q/A | Livrable 2, Livrable 3 final, fiches individuelles, archive ZIP |

> ⏱️ Conseil : réservez du temps le J3 pour **répéter l'oral** (10 min chrono) et préparer
> les réponses aux questions probables (voir section 13).

---

## 12. Critères d'évaluation et checklist finale

### Critères du sujet (poids indicatifs non chiffrés dans le sujet)

| Compétence | Attendus principaux |
|---|---|
| C19 | Plan projet structuré, parties prenantes, objectifs SMART, durées, priorités, inclusion |
| C20 | Méthode agile argumentée, RACI, coordination d'équipe, rituels, gestion inclusive |
| C22 | Reporting clair, synthétique, adapté à la hiérarchie, qualité orale et Q/A |
| C23 | KPI pertinents, feedbacks exploités, amélioration continue, impact environnemental |
| C24 | Plan d'accompagnement complet, progressif, adapté aux profils, accessible |
| Qualité | Cohésion du dossier, cohérence globale, contribution individuelle, professionnalisme |

### Checklist candidat complète (27 points, issue de checklist_candidat.docx)

**C19 — Organisation projet**
- [ ] Objectifs SMART formulés
- [ ] Phases et jalons explicites
- [ ] Tâches priorisées et durées estimées
- [ ] Parties prenantes identifiées avec rôles et attentes
- [ ] Contraintes d'accessibilité et situations de handicap prises en compte

**C20 — Gouvernance agile**
- [ ] Méthode agile justifiée
- [ ] Rituels et outils de suivi proposés
- [ ] Matrice RACI complète
- [ ] Mesures d'inclusion dans le fonctionnement d'équipe
- [ ] Risques de coordination identifiés

**C22 — Reporting**
- [ ] Reporting adapté à la hiérarchie
- [ ] Synthèse claire de l'avancement, risques, décisions attendues
- [ ] Support oral compatible avec 10 minutes de présentation
- [ ] Préparation de questions/réponses

**C23 — KPI et amélioration continue**
- [ ] KPI projet, produit, adoption et RSE
- [ ] Feedbacks utilisateurs analysés
- [ ] Axes d'amélioration priorisés
- [ ] Mesure d'impact environnemental intégrée

**C24 — Accompagnement**
- [ ] Typologies d'utilisateurs définies
- [ ] Parcours de formation par profil
- [ ] Supports prévus
- [ ] Calendrier de déploiement et support post-déploiement
- [ ] Accessibilité des supports vérifiée

**Qualité globale**
- [ ] Tous les fichiers sont dans l'archive
- [ ] Les annexes sont lisibles
- [ ] Chaque membre a remis sa fiche individuelle

---

## 13. Pièges à éviter et conseils stratégiques

### ❌ Les 5 pièges principaux

1. **Faire du technique** — décrire l'architecture, proposer du code, des pipelines, du Docker.
   → Hors périmètre E2/E3, explicitement interdit, temps perdu.
2. **Faire du financier** — chiffrer un budget, calculer un ROI.
   → Hors périmètre C21/E5, explicitement exclu.
3. **Refaire E1** — veille technologique, analyse de besoin, cahier des charges.
   → Le cadrage est fourni ; le refaire est du hors-sujet.
4. **Lister sans justifier** — « on utilisera Scrum et Jira » sans dire pourquoi.
   → Le sujet exige des arbitrages argumentés appuyés sur le dossier documentaire.
5. **Oublier les fils transversaux** — accessibilité et RSE absents ou traités en une ligne.
   → Ils apparaissent dans TOUTES les compétences et dans les données ; le correcteur les cherchera.

### ✅ Les 5 réflexes gagnants

1. **Citer les IDs** (B01, F03, R04, persona Malik…) dans chaque justification — traçabilité visible.
2. **Respecter les templates** — chaque colonne vide est un attendu explicite du correcteur.
3. **Parler « direction »** — phrases courtes, statuts vert/orange/rouge, décisions demandées,
   zéro jargon (la charte de reporting est un barème déguisé).
4. **Tenir les 12 semaines** — tout jalon, sprint, calendrier de formation doit rentrer dans
   les 12 semaines du brief, avec l'équipe de 6 imposée.
5. **Préparer la Q/R** — questions probables du jury : « Pourquoi Scrum plutôt que Kanban ? »,
   « Que faites-vous si l'adoption stagne à 50% en semaine 8 ? », « Comment mesurez-vous
   l'empreinte numérique ? », « Qui est Accountable sur la validation accessibilité ? »,
   « Quel est votre plan de contingence si le support sature ? ».

### 🧭 Vue d'ensemble finale

```
   BRIEF DIRECTION (12 semaines, équipe de 6, contraintes)
          │
          ▼
   ┌─────────────────────────────────────────────────┐
   │  LIVRABLE 1 : Rapport mise en œuvre (C19+C20+C23)│
   │  SMART → Plan projet → RACI → Risques → KPI →    │
   │  Feedbacks → Axes d'amélioration                 │
   └─────────────────────────────────────────────────┘
          │                                    │
          ▼                                    ▼
   ┌──────────────────────────┐   ┌──────────────────────────┐
   │ LIVRABLE 2 :             │   │ LIVRABLE 3 :             │
   │ Plan accompagnement (C24)│   │ Reporting direction (C22)│
   │ Personas → formations →  │   │ 8 slides, 10 min oral,   │
   │ supports → post-déploiem.│   │ statuts, décisions       │
   └──────────────────────────┘   └──────────────────────────┘
          │                                    │
          └────────────────┬───────────────────┘
                           ▼
   ┌─────────────────────────────────────────────────┐
   │ LIVRABLE 4 : Fiches individuelles (1/membre)     │
   │ + Annexes CSV : RACI, backlog, KPI, risques      │
   │ → Archive E4_MobilityPulse_NomEquipe.zip         │
   └─────────────────────────────────────────────────┘
```

---

*Document généré le 21/07/2026 à partir de l'analyse exhaustive des 14 documents (.docx) et
8 fichiers de données (.csv) du dossier « Bloc 4 - E4_MobilityPulse_V1_RNCP38919 ».*

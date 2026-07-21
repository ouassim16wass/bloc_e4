# Plan d'accompagnement utilisateurs - MobilityPulse_V1

> **Livrable 2** : couvre C24 (former et accompagner les utilisateurs finaux).
> Rédigé par le **Lead Data**, en coordination avec le référent métier (pilote du plan),
> le référent support et le référent accessibilité. Le calendrier correspond à la
> phase 3 du plan projet (semaines 6 à 10), pour que tous les profils soient formés
> avant le démarrage du pilote (S11).

---

## 1. Objectif du plan

Rendre les quatre profils d'utilisateurs autonomes sur MobilityPulse avant le démarrage du déploiement pilote (semaine 11), avec une satisfaction de 4/5 minimum après chaque formation et des supports accessibles à tous, y compris aux utilisateurs en situation de handicap. Ce plan répond à la troisième limite constatée par la direction (les utilisateurs demandent davantage de formation, de lisibilité et de support), à l'objectif O4 du rapport de mise en oeuvre, et au risque R01 (non-adoption). Il contribue directement à la cible d'adoption : passer de 35 % à 75 % d'utilisateurs actifs en fin de pilote.

---

## 2. Profils utilisateurs

Les profils sont issus des personas du dossier documentaire.

| Profil | Besoin principal | Niveau initial | Freins possibles | Adaptations nécessaires |
|---|---|---|---|---|
| Responsable supervision (persona Sarah) | Tableau de bord clair, indicateurs critiques, reporting quotidien | Moyen : utilise déjà le prototype | Décisions rapides en heure de pointe, très peu de temps disponible | Prise en main individuelle courte, fiche réflexe sur les indicateurs critiques, alertes fiables (peu de faux positifs) |
| Agent centre opérationnel (persona Malik) | Comprendre une alerte en moins de 2 minutes | Faible : vocabulaire du prototype jugé trop technique (feedback F01) | Forte charge cognitive lors des incidents, peu de temps de formation (contrainte du brief) | Tutoriel court, libellés métier et aide contextuelle (B01), fiche réflexe procédure d'escalade (B03) |
| Analyste mobilité (persona Elena) | Analyser les tendances, exporter les KPI | Bon : à l'aise avec les données | Définitions des KPI non explicites (feedback F03), articulation avec les rapports mensuels existants | Glossaire KPI avec formules et owners, atelier dédié aux exports et à l'analyse (B05, B06) |
| Utilisateur avec besoin d'accessibilité (persona Jules) | Supports compatibles lecteur d'écran, contraste suffisant, alternatives textuelles | Variable selon l'outil | Graphiques non interprétables sans description (feedback F05) | Documentation accessible validée type RGAA (B04), formations sous-titrées, temps d'appropriation supplémentaire |

---

## 3. Parcours d'accompagnement

Le parcours est progressif : informer, former, accompagner sur poste, puis rendre autonome avec un support pérenne. Les formats sont volontairement courts car les agents disposent de peu de temps (contrainte du brief).

| Étape | Public cible | Format | Durée | Support | Responsable | Indicateur de succès |
|---|---|---|---|---|---|---|
| 1. Communication de lancement (S6) | Tous les profils | Message d'annonce et démonstration courte | 15 min | Présentation simple et guide de démarrage | Référent métier | 80 % des utilisateurs cibles informés |
| 2. Ateliers de prise en main par profil (S7 à S9) | Superviseurs, agents, analystes (sessions séparées) | Atelier pratique sur cas réels (B07) | 45 min | Support d'atelier, fiches réflexes, glossaire KPI | Référent métier, contenus fiabilisés par le Lead Data | Satisfaction de 4/5 minimum, 90 % de participation |
| 3. Session adaptée accessibilité (S8 à S9) | Utilisateurs avec besoin d'accessibilité | Session dédiée, formats adaptés et sous-titrés | 45 min, rythme adapté | Documentation accessible validée type RGAA | Référent accessibilité | Supports validés, satisfaction de 4/5 minimum |
| 4. Prise en main accompagnée sur poste (S9 à S10) | Agents du centre de supervision | Accompagnement en binôme sur situations réelles | 2 fois 30 min | Fiche réflexe alerte et escalade | Référent support | Délai de compréhension d'une alerte en baisse vers la cible de 2 min |
| 5. Autonomie et support continu (S11 et suivantes, pilote) | Tous les profils | Support à la demande, FAQ, canal de feedback | En continu | FAQ, tutoriels courts, canal support | Référent support | 3 tickets bloquants maximum par semaine, adoption en progression vers 75 % |

---

## 4. Supports prévus

- **Guide de démarrage :** document court (10 pages maximum) par profil, orienté gestes essentiels, disponible en version accessible.
- **FAQ :** évolutive, alimentée par les tickets du support et les questions posées en atelier ; revue chaque semaine pendant le pilote.
- **Tutoriels courts :** vidéos de 3 à 5 minutes par cas d'usage (lire une alerte, escalader un incident, exporter les anomalies), sous-titrées et transcrites.
- **Atelier pratique :** 45 minutes par profil (story B07), sur cas réels du réseau NovaVille, avec un temps de manipulation individuelle.
- **Glossaire KPI :** définition, formule et owner de chaque indicateur (réponse au feedback F03, sous la responsabilité du Lead Data).
- **Canal support :** outil de tickets avec la procédure d'escalade (B03) et une permanence du référent support pendant le pilote.

---

## 5. Accessibilité et inclusion

Ce volet est validé par le référent accessibilité avant toute diffusion (mitigation du risque R04, réponse au feedback F05 et au persona Jules).

- **Supports compatibles lecteur d'écran :** documents structurés et balisés, alternatives textuelles pour chaque graphique et capture d'écran.
- **Contraste et lisibilité :** contrastes vérifiés sur tous les supports, taille de police suffisante, pas d'information portée par la couleur seule.
- **Sous-titres et transcriptions :** tous les tutoriels vidéo sont sous-titrés et accompagnés d'une transcription texte.
- **Temps d'appropriation :** rythme adapté lors de la session dédiée, possibilité de sessions individuelles complémentaires sans limite de nombre pendant la phase 3.
- **Modalités alternatives :** chaque contenu existe en au moins deux formats (atelier ou tutoriel, vidéo ou texte) ; sessions possibles en présentiel comme à distance.
- **Validation :** contrôle de type RGAA effectué par le référent accessibilité sur chaque support avant diffusion, avec correction obligatoire avant publication.

---

## 6. Support post-déploiement

- **Niveau 1 :** référent support ; répond via la FAQ et les gestes simples, qualifie et enregistre chaque ticket ; objectif de première réponse sous 4 heures ouvrées.
- **Niveau 2 :** équipe data (Data Engineer pour les questions produit et données, MLOps pour les alertes et le modèle) ; traite les tickets qualifiés bloquants en priorité.
- **Escalade :** procédure formalisée (story B03, réponse au feedback F04) : qualification du ticket, niveau de priorité, délai cible, information de l'utilisateur ; les alertes jugées erronées sont transmises au MLOps pour analyse.
- **Collecte de feedback :** canal structuré (story B10) ouvert à tous les profils ; les retours sont qualifiés par impact et fréquence, revus chaque semaine au comité d'arbitrage et intégrés au backlog d'amélioration.

---

## 7. KPI d'adoption

Ces indicateurs sont extraits du tableau de pilotage global (Livrable 1, section 8) et suivis pendant et après l'accompagnement.

| KPI | Cible | Fréquence | Responsable |
|---|---|---|---|
| Taux d'adoption hebdomadaire | 75 % en semaine 12 | Hebdomadaire | Référent métier |
| Satisfaction formation | 4/5 minimum | Après chaque atelier | Référent métier |
| Taux de participation aux ateliers | 90 % minimum des utilisateurs cibles | Par session | Référent métier |
| Délai de compréhension d'une alerte | 2 minutes | Mensuelle | Référent métier et Lead Data |
| Tickets support bloquants | 3 par semaine maximum | Hebdomadaire | Référent support |
| Utilisation des supports (FAQ, tutoriels) | Consultation en hausse pendant le pilote | Mensuelle | Référent support |

En cas d'écart (satisfaction sous 4/5, participation faible, adoption qui stagne), le plan de contingence du risque R01 s'applique : ateliers ciblés supplémentaires, accompagnement individuel en binôme et simplification des écrans prioritaires.

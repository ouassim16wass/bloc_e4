# Cahier des charges des slides et pitch complet - Présentation orale E4 MobilityPulse

> **Document autonome.** Il contient tout le contexte, le contenu exact des 8 slides à créer,
> et le pitch mot à mot du candidat. Il peut être donné tel quel à un assistant ou un outil
> pour générer les slides : toutes les données nécessaires sont incluses, rien d'externe n'est requis.

---

## PARTIE A : CONTEXTE (à lire avant de créer les slides)

### Le cadre

- **Épreuve :** E4 du titre RNCP 38919 Data Engineer, bloc 4 (piloter un projet de gestion de données).
- **Format :** présentation orale de **10 minutes** devant un jury jouant le rôle du comité de direction, suivie de 10 minutes de questions.
- **Présentateur :** Ouassim Megrad, équipe Megslab, rôle tenu : **Lead Data** (responsable de l'équipe Data Engineering, pilote du déploiement).
- **Scénario fictif :** la métropole de NovaVille possède un prototype de MobilityPulse, une solution d'analyse de mobilité urbaine (bus, tramways, vélos, capteurs de trafic) qui détecte des anomalies et expose des indicateurs. La direction demande un dossier de pilotage pour sécuriser le déploiement sur 12 semaines. Le candidat ne code pas : il organise, gouverne, mesure et accompagne.

### Les règles imposées par la charte de reporting (à respecter absolument)

1. **8 slides maximum.**
2. **Un message par slide**, phrases courtes.
3. **Un seul tableau ou graphique maximum par slide.**
4. **Un statut explicite vert / orange / rouge** sur l'avancement.
5. **Une décision attendue clairement formulée** quand le sujet en appelle une.
6. **Vocabulaire compréhensible par des non-techniciens** : ne jamais écrire pipeline, API, Docker, architecture, modèle ML. Dire : la solution, les alertes, les indicateurs.

### Style visuel recommandé

- Sobre et professionnel : fond clair, une couleur d'accent (bleu foncé type #1a5276), police lisible.
- Statuts sous forme de pastilles de couleur (verte, orange, rouge).
- Peu de texte par slide : les détails sont dits à l'oral, pas écrits.
- Pied de page : « Ouassim Megrad, Lead Data, équipe Megslab » et le numéro de slide.

---

## PARTIE B : LES 8 SLIDES EN DÉTAIL

### Slide 1 : Titre et message clé

**Objectif de la slide :** poser le sujet, le rôle du présentateur et le statut global en une seule vue. C'est la slide qui reste affichée pendant l'introduction.

**Contenu à afficher :**
- Titre : « MobilityPulse : sécuriser le déploiement en 12 semaines »
- Sous-titre : « Reporting au comité de direction »
- Présentateur : Ouassim Megrad, Lead Data, équipe Megslab
- Statut global : pastille VERTE, « lancement conforme »
- En bas, les 3 réponses du dossier en 3 mots-clés : Organisation, Gouvernance, Accompagnement

**🗣️ Pitch (1 minute 30) :**

> « Bonjour à tous. Je suis Ouassim Megrad, Lead Data de l'équipe Megslab. La direction de
> NovaVille a confié le passage à l'échelle de MobilityPulse à l'équipe Data Engineering,
> dont je suis le responsable. Ma mission : sécuriser le déploiement pilote sur 12 semaines.
> Un point important avant de commencer : la solution existe déjà, sous forme de prototype
> qui collecte les signaux de mobilité, détecte les anomalies et affiche des indicateurs.
> Mon travail n'est donc pas de la développer, mais d'organiser son adoption.
> La direction a constaté trois limites : personne ne sait organiser le passage à l'échelle,
> les rôles entre les équipes ne sont pas formalisés, et les utilisateurs demandent de la
> formation et du support. Mon dossier répond à ces trois limites, point par point :
> un plan projet, une gouvernance claire, et un accompagnement par profil.
> Le statut global du projet est vert. Je vous présente le dispositif en huit points,
> et je terminerai par les quatre décisions que j'attends de ce comité. »

**Transition :** « Commençons par le calendrier. »

---

### Slide 2 : Planning, 12 semaines, 4 phases, 5 jalons

**Objectif de la slide :** montrer que le délai imposé est tenu par un découpage crédible. Compétence démontrée : organisation et planification (C19).

**Contenu à afficher (un seul tableau) :**

| Phase | Semaines | Jalon | Statut |
|---|---|---|---|
| Cadrage et gouvernance | S1 à S2 | J1 : gouvernance validée | pastille verte, en cours |
| Itérations produit (3 sprints) | S3 à S8 | J2 : reporting en place. J3 : produit prêt | à venir |
| Accompagnement et formation | S6 à S10 | J4 : 100 % des profils formés | à venir |
| Déploiement pilote | S11 à S12 | J5 : bilan et go/no-go | à venir |

- Phrase clé sous le tableau : « Les formations se terminent avant le début du pilote. »

**🗣️ Pitch (1 minute 15) :**

> « Le déploiement tient en 12 semaines, découpé en quatre phases et cinq jalons.
> Deux semaines de cadrage pour installer la gouvernance. Puis six semaines de travail
> produit, en trois sprints de deux semaines. En parallèle, à partir de la semaine 6,
> l'accompagnement des utilisateurs démarre. Et les deux dernières semaines sont le
> déploiement pilote en conditions réelles.
> Vous remarquez que les phases produit et formation se chevauchent : c'est volontaire.
> Les agents ont peu de temps disponible, donc j'étale les formations sur cinq semaines.
> Et surtout, tout le monde est formé avant le pilote : un pilote avec des utilisateurs
> non formés mesurerait l'échec de la formation, pas la valeur de l'outil.
> L'ordre des tâches suit les dépendances réelles : on ne peut pas faire de reporting
> sans avoir défini les indicateurs, ni de procédure d'escalade sans avoir défini les rôles. »

**Transition :** « Justement, parlons des rôles. »

---

### Slide 3 : Gouvernance, qui décide quoi

**Objectif de la slide :** répondre à la limite « rôles non formalisés ». Compétence démontrée : encadrement agile (C20). Première décision attendue.

**Contenu à afficher :**
- Méthode : hybride Scrum et Kanban. Sprints de 2 semaines pour le produit, flux Kanban pour le support.
- Comité d'arbitrage hebdomadaire : PO, Lead Data, référent métier.
- Répartition des responsabilités (3 lignes, pas la RACI complète) :
  - Priorisation du backlog : le Product Owner
  - Planification, fiabilité des KPI, reporting : le Lead Data
  - Validation accessibilité : le référent accessibilité
- Encadré : « Décision attendue : valider ce mode de gouvernance »

**🗣️ Pitch (1 minute 15) :**

> « Pour la gouvernance, j'ai choisi une méthode hybride. Les évolutions du produit sont
> planifiables : je les organise en sprints de deux semaines, ce qui donne une cadence
> lisible pour vous, la direction. Le support, lui, est un flux imprévisible : je le gère
> en continu avec une file de priorités. Deux natures de travail, deux modes adaptés.
> Le point central du dispositif, c'est le comité d'arbitrage hebdomadaire. Le principal
> risque identifié dans ce projet, ce sont les conflits de priorités entre l'IT et le
> métier. Avec un arbitrage chaque semaine, les désaccords se règlent en jours, pas en mois.
> Chaque activité a un seul responsable : le Product Owner priorise, moi je planifie,
> je garantis la fiabilité des indicateurs et je vous rends compte, et le référent
> accessibilité valide chaque support. La matrice complète est dans le dossier.
> Première décision que je vous demande : valider ce mode de gouvernance. »

**Transition :** « Une gouvernance pilote avec des chiffres. Voici les nôtres. »

---

### Slide 4 : KPI, des cibles chiffrées en 4 catégories

**Objectif de la slide :** démontrer le pilotage par indicateurs (C23). C'est la slide où le Lead Data est le plus légitime.

**Contenu à afficher (un seul tableau) :**

| Indicateur | Départ | Cible en S12 | Catégorie |
|---|---|---|---|
| Taux d'adoption hebdomadaire | 35 % | 75 % | Adoption |
| Temps pour comprendre une alerte | 5 min | 2 min | Adoption |
| Fausses alertes perçues | 28 % | 15 % | Produit |
| Jalons tenus | mesure en cours de projet | 85 % minimum | Projet |
| Empreinte numérique | définie en S4 | suivi mensuel | RSE |

- Phrase clé : « Chaque indicateur a un responsable, une formule documentée, et une action prévue en cas de dérive. »

**🗣️ Pitch (1 minute 30) :**

> « Le pilotage repose sur des indicateurs en quatre catégories : le projet, le produit,
> l'adoption et l'impact environnemental. Tous les chiffres que vous voyez viennent du
> dossier fourni par la direction, je n'ai rien inventé.
> Trois chiffres à retenir. L'adoption d'abord : 35 % des utilisateurs cibles utilisent
> l'outil aujourd'hui, l'objectif est 75 % en fin de pilote. Le temps de compréhension
> d'une alerte ensuite : 5 minutes aujourd'hui, 2 minutes en cible, parce qu'un agent en
> pleine heure de pointe n'a pas 5 minutes. Et les fausses alertes : 28 % aujourd'hui,
> 15 % en cible, parce que la confiance dans l'outil conditionne son adoption.
> En tant que Lead Data, c'est mon coeur de métier : chaque indicateur a un responsable
> désigné, une formule documentée dans un glossaire, et une action prévue si la mesure
> dérive. Un chiffre sans définition claire, c'est un chiffre qu'on ne peut pas défendre.
> Et l'engagement environnemental est tenu : l'indicateur d'empreinte numérique est
> défini en semaine 4 et suivi chaque mois. »

**Transition :** « Des chiffres pour piloter, et des risques sous contrôle. »

---

### Slide 5 : Risques, top 3 et parades

**Objectif de la slide :** montrer l'anticipation (C19, C20). Uniquement les 3 risques majeurs, les 6 sont au registre en annexe.

**Contenu à afficher (un seul tableau) :**

| Risque | Niveau | Parade |
|---|---|---|
| Non-adoption par les agents | orange, élevé | Formations courtes, co-construction, canal de retours |
| Conflits de priorités IT et métier | orange, élevé | Comité d'arbitrage hebdomadaire |
| Accessibilité insuffisante | orange, élevé | Validation de chaque support avant diffusion |

- Phrase clé : « Chaque risque a aussi un plan B avec un seuil déclencheur défini à l'avance. »

**🗣️ Pitch (1 minute 15) :**

> « Six risques sont documentés au registre, je vous présente les trois majeurs.
> Le premier, c'est la non-adoption par les agents : c'est le risque qui tuerait le projet.
> Mes parades : des formations courtes, de la co-construction avec le terrain, et un canal
> de retours structuré. Le deuxième, ce sont les conflits de priorités entre l'IT et le
> métier : c'est le comité d'arbitrage hebdomadaire qui le traite. Le troisième, c'est une
> accessibilité insuffisante : chaque support est validé par le référent accessibilité
> avant diffusion, pas après coup.
> Et j'insiste sur un point : chaque risque a aussi un plan de contingence avec un seuil
> défini à l'avance. Un exemple concret : si l'adoption est sous les 50 % en semaine 8,
> je déclenche des ateliers ciblés et de l'accompagnement individuel en binôme.
> Pas d'improvisation en cours de pilote : les décisions difficiles sont préparées avant. »

**Transition :** « Ces risques, ce sont aussi les utilisateurs qui nous les signalent. »

---

### Slide 6 : Feedbacks utilisateurs, le terrain guide le backlog

**Objectif de la slide :** montrer que les retours utilisateurs sont exploités (C23) et influencent les priorités.

**Contenu à afficher (liste, pas de tableau) :**
- Titre de section : « 6 retours recueillis sur le prototype, priorisés par impact et fréquence »
- Vocabulaire des alertes trop technique : libellés métier et aide contextuelle (sprint 2)
- Aucune procédure en cas de mauvaise alerte : procédure d'escalade (sprint 1)
- Définitions des indicateurs imprécises : glossaire KPI (dès la phase 1)
- Graphiques illisibles au lecteur d'écran : alternatives textuelles (sprint 3)
- Phrase clé : « L'ordre des sprints reflète directement ces priorités. »

**🗣️ Pitch (1 minute) :**

> « Six retours utilisateurs ont été recueillis sur le prototype. Je les ai priorisés en
> croisant deux critères : l'impact et la fréquence.
> Trois retours cumulent impact fort et fréquence élevée : le vocabulaire des alertes est
> trop technique, il n'existe aucune procédure en cas de mauvaise alerte, et les
> définitions des indicateurs sont imprécises. Ils sont traités en premier.
> Le retour sur les graphiques illisibles au lecteur d'écran est moins fréquent, mais je
> l'ai remonté en priorité : l'accessibilité est une exigence d'inclusion de ce projet,
> pas une option.
> Ce que je veux que vous reteniez : l'ordre de mes sprints n'est pas arbitraire, il
> reflète directement ce que le terrain nous a dit. »

**Transition :** « Écouter le terrain, c'est aussi le former. »

---

### Slide 7 : Accompagnement, 4 profils, 4 parcours

**Objectif de la slide :** présenter le plan d'accompagnement (C24). Deuxième décision attendue.

**Contenu à afficher :**
- 4 profils : superviseurs, agents, analystes, utilisateurs avec besoin d'accessibilité
- Un atelier de 45 minutes par profil, sur cas réels
- Session dédiée accessibilité : lecteur d'écran, sous-titres, rythme adapté
- Prise en main en binôme sur poste pour les agents
- Après le déploiement : support en 2 niveaux avec procédure d'escalade
- Cible : 100 % formés avant le pilote, satisfaction 4 sur 5 minimum
- Encadré : « Décision attendue : valider ce dispositif d'accompagnement »

**🗣️ Pitch (1 minute 15) :**

> « L'accompagnement suit une logique simple : informer, former, accompagner sur le poste,
> puis rendre autonome. Quatre profils, quatre parcours adaptés : le superviseur pressé,
> l'agent en salle opérationnelle, l'analyste, et l'utilisateur en situation de handicap.
> La contrainte principale, c'est le temps : les agents en ont très peu. Donc tout est
> court : un seul atelier de 45 minutes par profil, des tutoriels de 3 à 5 minutes, et la
> prise en main se fait en binôme, sur leur poste, pendant leur travail réel.
> Pour l'accessibilité : une session dédiée à rythme adapté, des supports compatibles
> lecteur d'écran, des vidéos sous-titrées, et chaque support est validé avant diffusion.
> Après le déploiement, un support en deux niveaux prend le relais, avec une procédure
> d'escalade claire. La formation crée l'adoption, le support l'empêche de retomber.
> La cible : 100 % des profils formés avant le pilote, avec une satisfaction de 4 sur 5
> minimum. C'est ma deuxième demande de validation. »

**Transition :** « Je récapitule ce que j'attends de vous. »

---

### Slide 8 : Les 4 décisions demandées

**Objectif de la slide :** conclure sur l'action. C'est la slide la plus importante : un reporting de direction se termine toujours par les décisions attendues. Ne jamais la sacrifier au chrono.

**Contenu à afficher (un seul tableau) :**

| Numéro | Décision demandée | Échéance |
|---|---|---|
| 1 | Valider le mode de gouvernance | S2 |
| 2 | Valider le calendrier (4 phases, 5 jalons) | S2 |
| 3 | Arbitrer les priorités du backlog | S2 |
| 4 | Valider le dispositif d'accompagnement | S4 |

- Dessous : « Prochaines étapes : lancement du cadrage, premier reporting hebdomadaire en S3, point de jalon J1 en fin de semaine 2. »
- Dernière ligne : « Merci. Je suis prêt à répondre à vos questions. »

**🗣️ Pitch (1 minute) :**

> « Pour conclure, voici les quatre décisions que j'attends de ce comité.
> Deux dès cette semaine : valider le mode de gouvernance, et valider le calendrier en
> quatre phases et cinq jalons. Ensuite : arbitrer les priorités du backlog que je vous ai
> proposées, et d'ici la semaine 4, valider le dispositif d'accompagnement des utilisateurs.
> Si vous validez aujourd'hui, le cadrage démarre immédiatement, vous recevez le premier
> reporting hebdomadaire en semaine 3, et nous nous retrouvons au jalon 1 en fin de
> semaine 2 pour constater que la gouvernance est en place.
> Un prototype prometteur, un plan en 12 semaines, des indicateurs fiables et des
> utilisateurs accompagnés : voilà comment nous sécurisons MobilityPulse.
> Merci de votre attention. Je suis prêt à répondre à vos questions. »

---

## PARTIE C : RÉCAPITULATIF DU MINUTAGE

| Slide | Sujet | Durée | Cumul |
|---|---|---|---|
| 1 | Titre et message clé | 1:30 | 1:30 |
| 2 | Planning | 1:15 | 2:45 |
| 3 | Gouvernance | 1:15 | 4:00 |
| 4 | KPI | 1:30 | 5:30 |
| 5 | Risques | 1:15 | 6:45 |
| 6 | Feedbacks | 1:00 | 7:45 |
| 7 | Accompagnement | 1:15 | 9:00 |
| 8 | Décisions | 1:00 | 10:00 |

Si vous êtes en retard au chrono : raccourcissez les slides 5 et 6 (dire seulement le premier exemple de chaque). Ne touchez jamais à la slide 8.

## PARTIE D : CONSEILS DE LIVRAISON

1. **Débit :** environ 140 mots par minute. Les pitchs ci-dessus sont calibrés pour ça. Répétez au chrono.
2. **Regard :** parlez au jury, pas à l'écran. Un coup d'oeil à la slide pour lancer le sujet, puis face au jury.
3. **Les chiffres se pointent :** quand vous dites « de 35 à 75 % », montrez la ligne du tableau.
4. **Le mot interdit :** aucun terme technique (pipeline, API, modèle). Si un mot technique vous échappe, reformulez aussitôt : « autrement dit, la solution... ».
5. **Assumez le « je » :** vous êtes le Lead Data, pilote du déploiement. « J'ai choisi », « je garantis », « je vous demande ».
6. **Les transitions font le liant :** chaque fin de slide annonce la suivante (elles sont écrites dans les pitchs).
7. **Après la slide 8 :** silence, sourire, et laissez le jury ouvrir les questions. Les 18 questions probables et leurs réponses sont dans le document SOUTENANCE_ORALE.md.

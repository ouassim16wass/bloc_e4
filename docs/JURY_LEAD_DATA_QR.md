# 🎓 Jury blanc : questions sur le rôle de Lead Data (avec réponses modèles)

> Document de préparation à la séance de questions/réponses (10 minutes après l'oral).
> Entraînement : cachez la réponse, répondez à voix haute, puis comparez.
> Les réponses sont écrites en « je », prêtes à dire. Restez toujours dans la posture :
> **je pilote le socle data, je ne le développe pas** (le développement = épreuves E2/E3).

---

## PARTIE 1 : Le rôle de Lead Data

### Q1. « Qu'est-ce qu'un Lead Data, concrètement ? »

> Le Lead Data est le responsable technique de l'équipe data : il encadre les profils qui
> réalisent (Data Engineer, MLOps), garantit la qualité et la fiabilité des données et des
> indicateurs, et fait le pont entre l'équipe technique et la direction. Dans ce projet, la
> direction a confié le déploiement à l'équipe Data Engineering : j'en suis le responsable,
> donc je planifie, j'encadre, je mesure et je rends compte.

### Q2. « Quelle différence entre un Lead Data et un Data Engineer ? »

> Le Data Engineer construit : il développe les traitements, les exports, les évolutions de
> la chaîne de données. Moi, je garantis : je fixe les priorités techniques avec le PO,
> je valide la qualité de ce qui est livré, j'estime les charges et je réponds de la fiabilité
> des indicateurs devant la direction. En une phrase : il code, je réponds de ce que son code
> produit.

### Q3. « Et la différence avec le MLOps ? »

> Le MLOps est spécialisé sur le modèle de détection d'anomalies en production : son
> monitoring, ses seuils, sa dérive éventuelle. Il est Responsible sur ces sujets ; moi je
> suis Accountable : je valide ses choix de seuils car ils impactent directement le KPI de
> fausses alertes, qui conditionne la confiance des agents et donc l'adoption.

### Q4. « Pourquoi avoir choisi ce rôle plutôt que Product Owner ? »

> Deux raisons. D'abord la cohérence : je vise un titre de Data Engineer, le Lead Data est
> le rôle senior de cette filière. Ensuite le dossier m'y ancre : la story B10 est écrite
> « en tant que lead data », et le risque R06, garantir la formule et le responsable de
> chaque KPI, est exactement ma responsabilité. Le PO, lui, porte la valeur métier : c'est
> un autre métier, que je respecte en lui laissant la priorisation finale du backlog.

### Q5. « Que faites-vous au quotidien dans ce projet ? »

> Ma semaine type : le daily de 15 minutes avec l'équipe data ; le comité d'arbitrage du
> lundi où j'éclaire les choix du PO avec les charges et dépendances techniques ; la revue
> des indicateurs du tableau de bord avant le reporting hebdomadaire ; la validation des
> livrables data du sprint ; et en fin de sprint, la rétrospective. Plus, en continu,
> la fiabilisation des contenus : glossaire des KPI, documentation des alertes.

---

## PARTIE 2 : Questions data et techniques

### Q6. « D'où viennent les données de MobilityPulse ? »

> Des systèmes de transport de NovaVille : les bus et tramways remontent leur position et
> leur fréquentation, les stations de vélos en libre-service leur disponibilité, et les
> capteurs de trafic les flux routiers. Ces signaux sont collectés en continu et centralisés
> dans un entrepôt de données, où ils sont nettoyés et croisés avant d'alimenter la détection
> d'anomalies et les indicateurs.

### Q7. « Qu'est-ce qu'un entrepôt de données ? »

> C'est la base centrale où toutes les données collectées sont rassemblées, historisées et
> organisées pour l'analyse. L'intérêt : une seule source de vérité partagée. Quand la
> direction, un analyste et un agent regardent un indicateur, ils regardent le même chiffre,
> calculé au même endroit, avec la même formule.

### Q8. « Comment garantissez-vous la qualité des données ? »

> Par des contrôles automatisés à l'entrée de la chaîne : la complétude, est-ce que toutes
> les données attendues sont bien arrivées ; la cohérence, est-ce que les valeurs sont
> plausibles, pas de bus à 300 km/h ; et les doublons. En cas d'anomalie de qualité, la
> donnée est mise en quarantaine et une alerte interne est levée. C'est un prérequis absolu :
> la story des tendances par ligne, B06, dépend explicitement de la qualité data. Sans
> qualité, pas d'indicateur fiable, et sans indicateur fiable, pas de confiance.

### Q9. « Comment fonctionne la détection d'anomalies ? »

> Le principe : le modèle apprend le comportement normal du réseau, par ligne, par heure,
> par jour de la semaine. Quand un signal s'écarte trop de ce comportement attendu, une
> alerte est levée. Le réglage clé, c'est le seuil de déclenchement : trop sensible, on noie
> les agents sous les fausses alertes ; pas assez, on rate des incidents. C'est exactement
> le travail que je pilote avec le MLOps pour passer de 28 % à 15 % de fausses alertes.

### Q10. « Concrètement, comment faites-vous baisser les fausses alertes de 28 % à 15 % ? »

> Par une boucle de qualification : chaque alerte jugée non pertinente par un agent est
> marquée dans l'outil, avec la raison. Le MLOps analyse ces retours chaque semaine, ajuste
> les seuils ligne par ligne, et on mesure l'effet au tableau de bord hebdomadaire. C'est du
> pilotage par la donnée appliqué au modèle lui-même : le terrain nous dit où le modèle se
> trompe, et on corrige là où ça compte.

### Q11. « Qu'est-ce que l'API de consultation ? »

> C'est la porte d'entrée standardisée vers les données : l'interface interne l'utilise pour
> afficher les tableaux de bord, et les exports des analystes passent par elle. L'avantage :
> un point d'accès unique, sécurisé, avec gestion des permissions, chacun ne voit que ce à
> quoi il a droit. C'est la dépendance de la story B05 sur les exports CSV.

### Q12. « Comment mesurez-vous l'empreinte numérique ? »

> Par une estimation relative des ressources consommées par exécution des traitements :
> temps de calcul, volume stocké, volume transféré. Pas besoin d'outillage lourd : la formule
> est définie en semaine 4 par le MLOps et validée par moi, puis relevée chaque mois.
> L'objectif du pilote n'est pas une valeur absolue mais une tendance : stable ou en baisse,
> par exemple en purgeant les données inutiles et en optimisant les traitements les plus
> coûteux.

### Q13. « Les données de mobilité, ce sont des données personnelles ? Et le RGPD ? »

> Bonne question : les signaux utilisés sont des données de flux, agrégées et anonymisées,
> comptages, positions de véhicules, disponibilité de stations, pas des données nominatives
> de voyageurs. Le principe que j'applique est la minimisation : on ne collecte que ce qui
> sert les indicateurs. Et si une évolution future touchait à des données individuelles,
> je déclencherais une analyse d'impact avec le délégué à la protection des données de la
> métropole avant tout développement.

---

## PARTIE 3 : KPI et gouvernance de la donnée

### Q14. « Qu'est-ce qui fait un bon KPI selon vous ? »

> Quatre choses : une définition sans ambiguïté, une formule documentée, un responsable
> désigné, et une action prévue si la mesure dérive. Un indicateur qui n'a pas ces quatre
> attributs est un chiffre décoratif. C'est le risque R06 du registre, KPI non exploitables,
> et c'est pour ça que j'ai imposé un glossaire : les analystes se plaignaient justement de
> définitions imprécises, feedback F03.

### Q15. « Deux indicateurs se contredisent : que faites-vous ? »

> C'est le signal d'un problème de définition ou de qualité. Ma procédure : d'abord vérifier
> les formules au glossaire, souvent les deux indicateurs ne mesurent pas la même chose sous
> le même nom ; ensuite auditer la chaîne de calcul ; enfin corriger, documenter et
> revalider en comité. C'est exactement le plan de contingence prévu pour le risque R06.

### Q16. « Qui a accès aux données ? »

> L'accès suit les rôles : les agents voient les alertes de leur périmètre, les analystes
> ont l'accès aux exports, la direction voit les tableaux de bord agrégés. Les permissions
> sont gérées au niveau de l'API, c'est d'ailleurs la dépendance identifiée de la story
> B05 : avant d'ouvrir les exports CSV, il faut que les droits soient en place.

---

## PARTIE 4 : Encadrement d'équipe

### Q17. « Comment encadrez-vous le Data Engineer et le MLOps ? »

> Par le cadre agile et par la délégation claire : au sprint planning, on estime ensemble
> les charges, je ne les impose pas ; au daily, je lève les blocages ; à la revue, on
> démontre au référent métier ; à la rétrospective, on améliore le fonctionnement. La RACI
> précise qui répond de quoi : eux sont Responsible sur la réalisation, moi Accountable sur
> le résultat. Mon rôle n'est pas de faire à leur place, c'est de créer les conditions pour
> qu'ils livrent bien.

### Q18. « Un membre de votre équipe est en désaccord technique avec vous : que se passe-t-il ? »

> Je l'écoute d'abord, parce que le Data Engineer connaît souvent mieux le terrain technique
> que moi sur son sujet. Si le désaccord persiste, on objective : un test rapide, une mesure,
> des données. Et si ça impacte le planning ou le produit, ça remonte au comité d'arbitrage
> avec les deux options documentées. Un désaccord technique se tranche par les faits, pas
> par la hiérarchie.

### Q19. « Comment gérez-vous la charge de votre équipe ? »

> Elle est suivie à chaque sprint planning : on ne prend dans le sprint que ce que l'équipe
> peut absorber, et le plan de charge fait partie de la phase 1 du projet. C'est aussi une
> mesure d'inclusion du fonctionnement d'équipe : rituels courts, horaires compatibles avec
> les contraintes de chacun. Et le risque de surcharge du support au démarrage, R05, a son
> plan : renfort temporaire de l'équipe data et gel des évolutions non critiques.

---

## PARTIE 5 : Les pièges (gardez la posture)

### Q20. « Montrez-nous votre architecture technique détaillée. » *(piège)*

> Volontairement, le dossier n'en contient pas : le périmètre de l'épreuve E4 est le
> pilotage, et la charte de reporting impose un vocabulaire non technique pour la direction.
> Je peux en revanche vous présenter l'annexe : la chaîne de données, la qualité, la
> détection d'anomalies et la restitution, avec mon rôle de garant sur chaque brique.
> Le développement détaillé, lui, relève des épreuves E2 et E3.

### Q21. « Combien coûte votre projet ? » *(piège)*

> L'analyse financière relève de l'épreuve E5 et n'est pas dans le périmètre de ce dossier.
> Ce que je pilote en revanche, c'est la charge : le plan tient avec l'équipe de 6 personnes
> imposée par le brief, et le comité d'arbitrage ajuste le périmètre si nécessaire.

### Q22. « Vous êtes seul : comment pouvez-vous parler d'équipe ? » *(piège)*

> Le sujet définit une équipe fictive de 6 rôles ; en tant que Lead Data, mon travail
> consiste précisément à organiser leur collaboration : un lead réel ne fait pas tout
> lui-même, il encadre et coordonne. Et chaque rôle du dossier a des responsabilités
> précises, tracées dans la RACI.

---

## 🧠 Les 5 réflexes à garder en Q/R

1. **Toujours finir côté pilotage** : même une réponse technique se conclut par « et mon rôle est d'en garantir la fiabilité ».
2. **Citer les sources du dossier** : B05, B06, B10, F03, R06 sont VOS ancrages de Lead Data.
3. **Ne jamais inventer un chiffre** : si vous ne savez pas, dites « ce serait à mesurer, et voici comment je le mesurerais ».
4. **Le droit de dire non** : budget (E5) et code (E2/E3) sont hors périmètre, dites-le calmement.
5. **Une réponse = 30 secondes à 1 minute** : répondez, illustrez d'un exemple, arrêtez-vous.

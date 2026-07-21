---
marp: true
theme: default
paginate: true
size: 16:9
header: 'MobilityPulse, reporting direction'
footer: 'Lead Data, comité de direction, semaine 2'
style: |
  section {
    font-size: 24px;
  }
  h1 {
    color: #1a5276;
  }
  table {
    font-size: 20px;
  }
---

<!--
LIVRABLE 3 : SUPPORT DE REPORTING DIRECTION (C22)
Format : oral de 10 minutes puis 10 minutes de questions.
Conforme a la charte de reporting : 8 slides maximum, un message par slide,
un tableau maximum par slide, statut vert/orange/rouge, une decision attendue.
Les notes orateur sont dans les commentaires sous chaque slide.
Export : Marp (extension VS Code ou marp-cli), sortie PDF ou PPTX.
-->

# MobilityPulse

## Reporting de déploiement au comité de direction

**[Nom Prénom], Lead Data**

Statut global du projet : 🟢 **VERT**

<!--
Notes orateur (30 secondes) :
Bonjour. Je suis le Lead Data du projet MobilityPulse. La direction de NovaVille a confie
le passage a l echelle de la solution a l equipe Data Engineering, dont je suis le responsable.
Ma mission : securiser le deploiement pilote sur 12 semaines. La solution existe deja en
prototype : mon travail n est pas de la developper, mais de piloter son adoption.
-->

---

# 1. Message clé

**Mission : sécuriser le déploiement pilote de MobilityPulse en 12 semaines.**

La direction a constaté 3 limites, ce dossier y répond point par point :

- Pas d'organisation du passage à l'échelle **:** un plan en 4 phases et 5 jalons
- Des rôles non formalisés **:** une gouvernance agile et une matrice RACI
- Des utilisateurs en demande de formation **:** un plan d'accompagnement par profil

Statut global : 🟢 vert, lancement conforme

<!--
Notes orateur (1 minute) :
Le message a retenir : la solution existe, ce dossier organise son adoption.
Chaque limite constatee par la direction trouve sa reponse dans un livrable.
-->

---

# 2. Planning : 12 semaines, 4 phases, 5 jalons

| Phase | Semaines | Jalon | Statut |
|---|---|---|---|
| Cadrage et gouvernance | S1 à S2 | J1 : gouvernance validée | 🟢 en cours |
| Itérations produit (3 sprints) | S3 à S8 | J2 : reporting en place, J3 : produit prêt | à venir |
| Accompagnement et formation | S6 à S10 | J4 : 100 % des profils formés | à venir |
| Déploiement pilote | S11 à S12 | J5 : bilan et go/no-go | à venir |

**Point clé : les formations se terminent avant le démarrage du pilote.**

<!--
Notes orateur (1 minute 30) :
Le sequencement suit les dependances du backlog : la gouvernance precede l escalade,
la definition des KPI precede le reporting. Les phases produit et accompagnement se
chevauchent volontairement : les agents ont peu de temps, on etale les formations.
-->

---

# 3. Gouvernance : qui décide quoi

- **Méthode : hybride Scrum et Kanban.** Sprints de 2 semaines pour le produit, flux Kanban pour le support et le pilote
- **Comité d'arbitrage hebdomadaire** (PO, Lead Data, référent métier) : les conflits de priorités se règlent chaque semaine, pas en fin de projet
- **Matrice RACI validée : un seul responsable par activité**
  - Priorisation du backlog : le Product Owner
  - Planification, fiabilité des KPI, reporting : le Lead Data
  - Validation accessibilité : le référent accessibilité

**Décision attendue : valider ce mode de gouvernance**

<!--
Notes orateur (1 minute 30) :
Justification de la methode : deux natures de travail differentes. Les evolutions produit
sont planifiables en sprints, lisibles pour la direction. Le flux support est imprevisible,
un Kanban est plus honnete. Le rythme court force les arbitrages, ce qui traite le risque
de conflit IT et metier.
-->

---

# 4. KPI : 4 catégories, des cibles chiffrées

| KPI | Départ | Cible S12 | Catégorie |
|---|---|---|---|
| Taux d'adoption hebdomadaire | 35 % | 75 % | Adoption |
| Délai de compréhension d'une alerte | 5 min | 2 min | Adoption |
| Faux positifs perçus | 28 % | 15 % | Produit |
| Respect des jalons | mesure au fil du projet | 85 % minimum | Projet |
| Empreinte numérique | définie en S4 | suivi mensuel | RSE |

**Chaque KPI a un owner, une formule documentée et une action en cas de dérive.**

<!--
Notes orateur (1 minute 30) :
Tous les chiffres viennent du dossier fourni par la direction, rien n est invente.
En tant que Lead Data, je garantis la fiabilite de ces indicateurs : un glossaire
documente la formule et l owner de chaque KPI. C est la reponse au retour des analystes
sur les definitions imprecises.
-->

---

# 5. Risques : top 3 et décisions associées

| Risque | Niveau | Mitigation |
|---|---|---|
| R01 : non-adoption par les agents | 🟠 élevé | Formations courtes, co-construction, canal de feedback |
| R02 : conflit de priorités IT et métier | 🟠 élevé | Comité d'arbitrage hebdomadaire |
| R04 : accessibilité insuffisante | 🟠 élevé | Validation type RGAA de chaque support |

**Chaque risque a aussi un plan de contingence chiffré** (exemple : adoption sous 50 % en S8, ateliers ciblés et binômes)

<!--
Notes orateur (1 minute) :
Six risques au registre, les trois majeurs sont ici. La mitigation est preventive,
la contingence est le plan B si le signal passe au rouge. Le seuil est defini a l avance :
pas d improvisation en cours de pilote.
-->

---

# 6. Feedbacks utilisateurs : le terrain guide le backlog

Priorisation par impact et fréquence des 6 retours du prototype :

- **Vocabulaire trop technique** (agents) **:** libellés métier et aide contextuelle, sprint 2
- **Aucune procédure d'escalade** (support) **:** procédure et ticketing, sprint 1
- **Définitions des KPI imprécises** (analystes) **:** glossaire KPI, dès la phase 1
- **Graphiques illisibles au lecteur d'écran :** alternatives textuelles, validation RGAA, sprint 3

**L'ordre des sprints reflète directement ces priorités.**

<!--
Notes orateur (1 minute) :
Trois retours combinent impact eleve et frequence elevee : ils passent en premier.
L accessibilite est remontee en priorite malgre sa frequence occasionnelle : c est une
exigence d inclusion du projet, pas une option.
-->

---

# 7. Accompagnement : 4 profils, 4 parcours

- **Ateliers de 45 minutes par profil** : superviseurs, agents, analystes (contrainte : peu de temps disponible)
- **Session dédiée accessibilité** : supports lecteur d'écran, sous-titres, rythme adapté
- **Prise en main en binôme sur poste** pour les agents (S9 à S10)
- **Support post-déploiement en 2 niveaux** avec procédure d'escalade
- Cible : 100 % formés avant le pilote, satisfaction 4/5 minimum

**Décision attendue : valider ce dispositif d'accompagnement**

<!--
Notes orateur (1 minute) :
Le parcours est progressif : informer, former, accompagner sur poste, rendre autonome.
Chaque support est valide type RGAA par le referent accessibilite avant diffusion.
La formation cree l adoption, le support l empeche de retomber.
-->

---

# 8. Décisions demandées au comité

| # | Décision | Échéance |
|---|---|---|
| 1 | Valider le mode de gouvernance | S2 |
| 2 | Valider le calendrier de déploiement (4 phases, 5 jalons) | S2 |
| 3 | Arbitrer les priorités du backlog proposées | S2 |
| 4 | Valider le dispositif d'accompagnement | S4 |

**Prochaines étapes :** lancement de la phase 1, premier reporting hebdomadaire en S3, point de jalon J1 avec la direction en fin de semaine 2.

<!--
Notes orateur (1 minute) :
Je termine par ce que j attends du comite : quatre validations, deux des cette semaine.
Merci de votre attention, je suis pret pour vos questions.
Ensuite : 10 minutes de questions, reponses preparees dans docs/SOUTENANCE_ORALE.md.
-->

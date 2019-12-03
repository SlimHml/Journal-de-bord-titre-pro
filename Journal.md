# Journal de bord Yes-We-Web

## Première partie: Planification

### Chapitre I Définition du role de chef de projet et planification du travail

Définir les outils de communication
Analyser le cahier des charges
Création du backlog => des users stories
Planification des sprints (quelles tâches?) sur quelle durée?
Vérifier la répartition des tâches
=> s'assurer du respect du backlog
Organiser les daily meeting (problèmes rencontrés la veille, qu'est ce que chacun va faire aujourd'hui?)
Recadrer les écarts faits à la planification

##### Lundi 25/11/2019

Apprentissage de l'UML, apprendre les normes prend du temps , mais il est nécessaire d'avoir un UML détaillé pour notre POC, afin que le projet avance le plus vite possible

Nous avons partagé cette tâche avec Amélie, qui elle s'occupe de la branche acheteurs, je m'occupe de la branche producteurs.
Nous avons opté pour Draw.io pour réaliser cette tâche, c'est sommaire, mais gratuit et robuste

##### Mardi 26/11/2019

J'ai terminé la branche producteurs, Amélie doit se pencher sur l'apprentissage des tests, du coup la branche acheteurs prend un peu plus de temps que prévu, de mon côté je me renseigne sur les tokens, avec JWT (à vérifier)

##### Mercredi 27/11/2019

Matin: Nous allons aborder la branche BLOG de l'UML ensemble avec Amélie
Notre objectif et d'arriver à faire cela en plus de la branche inscription

Après-midi: Malheureusement, on n'a pas pu aborder ce thème car il y'a eu des ateliers tout au long de la journée afin de définir exactement les responsabilités / devoirs de chaque rôle dans les équipes, et je me suis porté volontaire pour suivre le cours sur la chaîne prototypale, je m'occuperai de l'UML blog demain

##### Jeudi 28/11/2019

Amélie n'est pas là aujourd'hui dû à deux rendez vous dans sa journée, je m'attaque à l'UML blog, je vais commencer par faire des recherches et un travail de réflexion pour visualiser la structure

Je me suis donné comme piste de reflexion le travail sur l'UML du groupe en charge du blog de la promo, et y adapter les besoins propres à Popfresh

Grâce à celà et à des recherches sur stackOverflow nottament sur la signification et la logique des arrows car il semble que je ne sois pas le seul à qui ça pose des questions, j'ai pu donc avancer sur la branche Blog et y compris Admin

##### Vendredi 29/11/2019

Avec Amélie on s'est penchés sur la fusion de nos deux travaux, mais ma logique ne lui convient pas et a retouché mon travail tout en greffant le sien à tout celà.
De légères tensions qui me confirment que ceci doit être fait par une seule et même personne afin d'éviter ce genre de débat.

##### Lundi 02/12/2019

Après un week-end découverte de typescript, je vais étudier le cahier des charges reformaté afin de créer les premières milestones et issues

Après avoir discuté des priorités avec Hachemi et Amélie, il ressort qu'au niveau du backend nous allons devoir nous atteler d'abord aux **Produits**, point commun entre les **Acheteurs** et les **Producteurs**, j'ai crée une dizaine de milestones, comprenant l'initialisation basique du projet avec **Express**, jusqu'aux premières **Routes** et **Controlleurs**, je ne sais pas si je m'avance un peu trop, mais selon ma logique, nous y viendront tôt ou tard alors j'ai pris l'initiative de les poser sur **Github** d'ores et déjà.

##### Mardi 03/12/2019

Ce matin Céline, qui nous avait initié à la **Méthode agile** il y'a de celà 2 mois est passée pour prendre de nos nouvelles et nous interviewer sur notre ressenti avec la formation, elle était avec sa stagiaire afin de nous poser tout un tas de question, elle nous a aussi parlé de 5 jours de **formation** suivis d'une **certification**, je suis intéressé car l'aspect **tactique / stratégique** me plait beaucoup, malheureusement il faut un compte **CPF** garni, car pour ces 5 jours et la **Certif**, il est nécessaire d'avoir **1750 euros** HT, j'en suis à des années lumière.

J'ai initialisé le projet avec le micro-framework **Express** pour nodeJS qui nous fournira des outils de base afin d'aller plus vite dans la mise en place de notre application. Mais aussi pour nous éviter de manière certaine des bugs que nous aurions eu beaucoup de mal à détecter et fixer plus tard.
Nous serons donc à un niveau un peu moins bas de programmation mais on part plus sereins, Express est une petite révolution pour notre équipe débutante

**Sequelize CLI**, l’ORM le plus adapté dans notre cas est sequelize. Sequelize permet l’utilisation d’une base de données de type Postgres, mais aussi de quelques autres (MySQL, SQLite et Microsoft SQL Server)
Sequelize CLI va générer encore une fois pour nous différents dossiers et fichiers qui vont nous faciliter la vie de manière plus sûre et plus rapide, donc une appli plus robuste à notre niveau de technicité. Nous sommes aussi fortement limités par le temps qu'il nous reste, donc partir sur ce genre d'outil me paraît pertinent.

**Babel** afin que certains éléments de langages soient pris en compte (**Requires remplacés par Imports**),

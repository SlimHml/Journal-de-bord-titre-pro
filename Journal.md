# Journal de bord Yes-We-Web

## Première partie: Planification

### Chapitre I Définition du rôle de chef de projet et planification du travail

**Rôles dans l'équipe**: Définir les outils de communication
Analyser le cahier des charges
Création du backlog => des users stories
Planification des sprints (quelles tâches?) sur quelle durée?
Vérifier la répartition des tâches
=> s'assurer du respect du backlog
Organiser les daily meeting (problèmes rencontrés la veille, qu'est ce que chacun va faire aujourd'hui?)
Recadrer les écarts faits à la planification

**Mise en place du journal** : Je suis encore peu familier avec Markdown, j'utilise un cheatsheet provenant d'un dépôt Github d'un certain "adam-p"
[Source ici !](https://github.com/adam-p/markdown-here)

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

### Chapitre II, Début de la construction du projet

##### Mardi 03/12/2019

Ce matin Céline, qui nous avait initié à la **Méthode agile** il y'a de celà 2 mois est passée pour prendre de nos nouvelles et nous interviewer sur notre ressenti avec la formation, elle était avec sa stagiaire afin de nous poser tout un tas de question, elle nous a aussi parlé de 5 jours de **formation** suivis d'une **certification** à la méthode agile, je suis intéressé car l'aspect **tactique / stratégique** me plait beaucoup, malheureusement il faut un compte **CPF** garni, car pour ces 5 jours et la **Certif**, il est nécessaire d'avoir **1750 euros** HT, j'en suis à des années lumière.

J'ai initialisé le projet avec le micro-framework **Express** pour nodeJS qui nous fournira des outils de base afin d'aller plus vite dans la mise en place de notre application. Mais aussi pour nous éviter de manière certaine des bugs que nous aurions eu beaucoup de mal à détecter et fixer plus tard.
Nous serons donc à un niveau un peu moins bas de programmation mais on part plus sereins, Express est une petite révolution pour notre équipe débutante

**Sequelize CLI**, l’ORM le plus adapté dans notre cas est sequelize. Sequelize permet l’utilisation d’une base de données de type Postgres, mais aussi de quelques autres (MySQL, SQLite et Microsoft SQL Server)
Sequelize CLI va générer encore une fois pour nous différents dossiers et fichiers qui vont nous faciliter la vie de manière plus sûre et plus rapide, donc une appli plus robuste à notre niveau de technicité. Nous sommes aussi fortement limités par le temps qu'il nous reste, donc partir sur ce genre d'outil me paraît pertinent.

**Babel** afin que certains éléments de langages soient pris en compte (**Requires remplacés par Imports**)

J'ai donc refactorisé tous les requires par des imports, toutes les var en const.

J'ai aussi installé, importé et appelé le **Middleware CORS**, qui nous permet de configurer la sécurité de l'API web, il autorise par exemple un domaine à faire des requêtes contre notre API, ça me paraît **extrêmement dangereux** maintenant que je me relit, je me demande si il y'a un moyen de configurer **CORS** afin qu'il n'autorise qu'un seul autre domaine (le notre en l'occurence) à venir se servir dans notre API backend

Le push sur la branche master s'est bien passé, je ne ferme aucune issue dans la section "Done" du **projet backend** sur **Github**, je laisse Amélie, lead Technique, valider mon travail avant de boucler tout ça.

Il ne manque plus qu'à installer Typescript, mais je suis encore un peu frileux à l'idée de me lancer là dedans à à peine 2 mois de l'ultime deadline.

##### Mercredi 04/12/2019

Ce matin nous nous sommes penchés avec Amélie sur les tests unitaires, nous avons insallé Mocha et Chai, et avons run nos premiers tests unitaires dans un dossier factice d'entraînement, il n'y a plus qu'à prendre l'habitude de mettre nos fonctions dans ces fichiers de tests

Cette après-midi, j'ai eu l'agréable surprise de voir que l'on ne pouvait initialiser un projet avec **express** si on compte utiliser **Typescript**, il va falloir partir sur une initialisation du projet fait main

j'ai balancé à la poubelle le dossier **Backend** et je suis reparti sur un bon vieux mkdir, il est temps d'expérimenter jusqu'à trouver la façon la plus propre d'initialiser ce projet.

**npm init -y**, installation de **mocha** et de **chai**, installation de **typescript**, installation npm install @types/node --save-dev), installation de typescript compilator (tsc) à l'aide d'une énorme ligne de commande pour créer notre **tsconfig.json** et y ajouter plusieurs utilités ainsi qu'un dossier build où notre code compilé attérira sous forme de .js

```
npx tsc --init --rootDir src --outDir build \
> --esModuleInterop --resolveJsonModule --lib es6 \
> --module commonjs --allowJs true --noImplicitAny true
message TS6071: Successfully created a tsconfig.json file.
```

Création d'un dossier **src** contenant index.ts
Je pense que rien qu'avec ça, j'ai lancé le plus gros commit que je n'ai jamais vu (petite anecdote)

Installation de **nodemon** et de **ts-node** (npm install --save-dev ts-node nodemon)

Installation de **rimraf**, qui fonctionne comme rm -rf, création d'un script qui supprime build et son contenu et le remplace par un nouveau mais qui ensuite le re-rempli avec la compilation toute fraîche en **.js** de notre **.ts** (le TSC quoi) sur lancement de la commande **npm run build**

Le script dans package.json: **"build": "rimraf ./build && tsc",**

Installation de **babel**, installation des presets d'environnement, création d'un fichier **.babelrc** et ajout d'un **preset**.

Et j'ai l'impression de n'avoir rien fait, il y'a encore énormément de boulot rien que sur l'initialisation, et avec Amélie nous ne savons pas comment partager cette tâche sans se marcher sur les pieds. On va discuter demain matin je pense via **Mattermost**

##### Jeudi 05/12/2019

Suites aux grèves multiples, nous travaillons aujourd'hui à domicile, j'ai trouvé 3 articles ce matin afin d'initialiser un projet avec NodeJS, express et typescript, un article d'un certain [Pierre Paci](https://medium.com/intech-conseil-expertise/d%C3%A9marrer-vite-et-bien-votre-application-node-express-typescript-jest-507bb454147d)
D'un certain [Khalil Stemmler](https://khalilstemmler.com/blogs/typescript/node-starter-project/) et pour finir de [David Neal](https://developer.okta.com/blog/2018/11/15/node-express-typescript)
J'ai su lancer un premier hello world sur un serveur local, mais il reste tout un tas de dossiers et de fichiers à **ajouter** et **modifier**

##### Vendredi 06/12/2019

Journée documentation, tests et modification de mon C.V
J'hésite vraiment à revenir sur une initialisation avec Express, et revenir sur typescript pour le frontend

##### Samedi 07/12/2019

Rendez vous est prit aujourd'hui à l'Adep avec Hachemi et Elias, nous allons nous pencher sur le sujet Deno, le successeur de Node JS

Adios node modules
Adios package json
aucune dépendance externe
basé sur la Go's standard library (librairie indépendante)
Basé sur le langage RUST

(Hors sujet mais pour résoudre l'import des variables d'environnement .env, il faut utiliser env extended)

Il faut que je vois le **destructuring**

##### Dimanche 08/12/2019

Malade, fatigué, je prends clairement cette journée en repos total, demain nous sommes encore en remote suites au mouvement massif de grèves en France

##### Lundi 09/12/2019

J'ai réussi à lancer un helloworld sur le dossier backend, mais je pense essayer de convaincre Amélie de repasser sur une initialisation rapide avec express, nous allons manquer de temps sinon

##### Mardi 10/12/2019

TSLint est un outil d’analyse statique, qui définie des règles permettant d’augmenter la qualité du code TypeScript en termes de lisibilité, maintenabilité et fonctionnalité.

Voici un exemple de règle pour chaque catégorie :

.._ Limiter le nombre maximal de caractères par ligne (max-line-length) permet de rendre le code plus lisible.
.._ Limiter le nombre de if imbriqués dans une fonction (cyclomatic-complexity) permet de rendre le code plus maintenable.
..\* Déclarer des variables uniquement si on les utilise (no-unused-variable) permet d’assurer la bonne fonctionnalité du programme.

Ce sujet est vraiment intéressant et je ressent une vraie plus value tant au niveau professionnel au niveau de la méthode, mais aussi sur le marché du travail

Mais dans un énorme soucis de deadline trop proche, Amélie et moi avons décidés d'abandonner typescript pour la production de ce POC

###### Mercredi 11/12/2019

J'ai recrée les milestones / issues à propos d'express generator dans notre repo github

J'ai ajouté des commentaires pour guider un maximum lors du traitement des issues les plus simples

Amélie s'occupe de la (ré) initialisation du projet avec Express et surtout la correcte façon d'utiliser le système de variables d'environnement.
De mon côté en attendant, je me documente sur [sur JWT (json web token)](https://blog.ippon.fr/2017/10/12/preuve-dauthentification-avec-jwt/) pour l'instant, il semble que celà soit bien pour les SPA (single page application)

###### Mardi 7/01/2020

Je pars sur un projet solo au final, trop de difficultés rencontrées, le groupe s'est dissout, je me lance dans un site d'équitation

Je choisis le modèle MVC sur nodejs, pas de typescript

Initialisation du projet avec Express generator, je pars sur l'article en premier
Même procédure qu'au commencement de pop fresh, sans gitflow, refactorisation, installation de CORS

Je rencontre un gros soucis, pouvoir upload et display des images tout en sauvegardant celles ci dans la base de données
J'ai trouvé un tutoriel assez long, je vais tenter ma chance, installation de Multer

##### Semaine juste avant le début des stages

J'ai décidé de développer directement l'authentification, j'ai crée mon modèle user, le controlleur, la route, j'ai installé Json web token et bcrypt pour l'attribution du token et le cryptage du mot de passe généré lors de l'inscription

Register

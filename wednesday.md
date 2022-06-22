## Conférence d'introduction du deuxième jour
Voxxed Days Luxembourg TEAM

200 talks proposés, 70 sélectionnés

Remerciement des Golden tickets qui facilitent le choix des talks pour les orgas.

## Darwinisme numérique

Cette keynote d'ouverture de ce 2ème jour a été réalisée par Didier GIRARD (Co-CEO SFEIR).

Pour lui, l'informatique, c'est un des métiers les plus "durs" du monde. C'est aussi très souvent un métier "passion" (quand il a posé la question à la salle, 80% des gens ont levé la main).

Son motto : ne jamais confier son avenir à un tier, pour rester maitre de sa vie pro. Ca nécessite de comprendre le futur. D'où la référence à Darwin et la survie du plus apte ;-).

[//]: # "Un des métiers les plus durs au monde. Métier passion 80% des gens on levé la main (pas forcément le meilleur pattern) / Docteur en informatique / apiculteur (allergique à la piqûre des abeilles, running) / Passionné => discuté avec un gars qui a fait 15 ans, sans se renouveler, viré. Je ne confierai pas mon avenir à un tier. Comprendre le futur. Darwin => le plus apte On consomme de plus en plus d'immatériel (musique, livres, apps) / Avant il fallait optimiser la ressource informatique. Maintenant non. Espèce qui a évolué dans un écosystème où la ressource est rare et que la ressource devient abondance. Apprendre à travers un écran. Les jeunes vont vérifier ce que les profs disent sur Internet ! Sauvegarder son document. Une tesla c'est une smart car, pas une voiture électrique. Soft first. Est on à la veille d'une crise ?"

Notre monde est en pleine évolution (pour ne pas dire, en "transformation numérique") et 3 types d'entités doivent évoluer pour ne pas être inapte à ce "nouvel" environnement.

D'abord, les nations (notamment européennes), qui doivent devenir souveraines (attention à la connotation politique du terme). C'est autant vrai sur le software que le hardware. C'est aussi à nous en tant que citoyens d'être exigeants sur les services fournis par son pays.

Ensuite, les entreprises traditionnelles, qui se retrouvent toutes concurrencées par des entreprises "natives" (medtech, agritech, \*\*\*\*tech). Elles doivent d'adapter (dans le mouvement), rester compatibles avec le futur (pas le présent ou le passé), passer plus vite en prod (accept failure as normal, blameless).

Enfin, les individus (notamment dans latech), qui doivent toujours chercher à travailler leur employabilité future.

> On trouve un job sur ses hard skills, on fait carrière avec les softs skills.

[//]: # "Les 3 espèces qui doivent changer Nations => les européens doivent devenir souverains sur le numérique (attention à la connotation politique de ce terme) il faut qu'on soit capable de produire nos propres DCs (avec nos propres composants). Indépendant au niveau du soft. Les citoyens doivent être exigeants. Entreprises => toutes les nouvelles entreprises "tech" (medtech, agritech, fintech etc) qui concurrence les autres. Adaptation (pas une transformation, un mouvement). Rendre l'entreprise compatible avec le futur. Annecdote avec les navigateurs et chrome. Prendre des décisions rapides. Lead time for change (aller le plus vite possible en production). Accept failure as normal. Blameless. Winner takes all. croissance logarithmique en le ratio employés / CA. Gens de la tech au comex. T-shape (base solide et savoirs horizontaux)"

> Le hasard ne favorise que les esprits préparés
> -- Pascal

## REST, gRPC, GraphQL, Webhooks : dans quelles situations ? 

Ce talk de François DELBRAYELLE était un tour d'horizon de toutes les solutions pour faire discuter des composants web entre eux (avantages, inconvénients, patterns).



Communication ipc. Ne pas oublier les contraintes non fonctionnelles

Corba (91)
SOAP xml hyper verbeux

REST : architecture (souvent avec HTTP)
GRaphQL langage (HTTP POST)
Webhook HTTP POST
gRPC HTTP2

REST => souvent des gros payload en JSON
gRCP => requete protobuf ton payload binaires (plus petits)

## 12:45 - 13:00 -  Lead Dev, 3 ans d'xp, et alors ?
Lise QUESNEL

Pas forcément besoin d'avoir 10 ans d'XP, de ne plus coder ou d'être un homme.

Lead dev à Nantes, avec le reste de l'équipe à Paris.

C'est quoi lead dev ?
C'est quoi la diff avec techlead

techlead (expert technique)
lead dev => accompagne l'équipe à la réussite du projet

Référent technique

Rôles partagés dans l'équipe

Le lead dev a plus de réunion

soft skills

## 13:15 - 13:30 -  Améliorer les compétences et les infrastructures avec les katas d'architecture
Alexandre TOURET

Worldline

Software architecture for developers
fundamentals of software architecture

Les katas // coding games pour architectes

Equipes de 6 environs, mixer des juniors, des ops, des seniors

Faire des catas pour s'entrainer 
https://speakerdeck.com/alexandretouret/voxxeddays-lux-22-ameliorer-les-competences-et-les-infrastructures-avec-les-katas-darchitecture

## 13:45 - 14:45 - Performance et prix, comment le hardware influence nos programmes : le journal du hard pour les dev
Quentin ADAM
Main room

Qui connaît la ref des CPU sur ses serveurs
Qui a fait de l'assembleur

> Ah mais vous êtes quand même un peu vieux en fait

C'est intéressant de savoir quel CPU on utilise, car en fonction du CPU on a différent jeux d'instructions

Advanced Matrix Extensions (AMX) / AVX(2,512)

Certains processeurs Intel contient le controler réseau 100 Gbps

Acheter les processeurs avec les jeux d'instructions dont vous avez besoin

Exherbo (source based, great skill builders)

Kernel monolithique 15Mo /ubuntu 100Mo

Rust recompile tout

DPU sur les cartes réseaux et stockage

European Chip Act (vente au détail des IP Intel)
Construire des CPU sur le sol européen va être beaucoup plus simple

Open compute projet

## 14:45 - 15:45 - Faire évoluer ses API HTTP, une approche en plusieurs étapes
Nicolas FRÄNKEL
Main room

## 16:00 - 17:00 - Vertex AI: Pipelines for your MLOps workflows
Marton KODOK
Main room

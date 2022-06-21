## 09:00 - 09:15 - Conference day 1 introduction

Voxxed Days Luxembourg TEAM (Pierre Antoine Grégoire)

Après 2 ans d'annulation cause COVID
Participants et speakers plus d'hommes, peut être encore plus depuis le COVID ? (beaucoup moins d'oratrices et dans les inscrits)

## 09:15 - 10:00 - Pourquoi vous n'attirerez et ne retiendrez pas les femmes dans vos équipes tech !

Marcy CHAROLLOIS

Habitus
Status quo
Resistance au changement
Courbe du deuil
Attraction / Rétention des femmes

On ne va pas vivre la même chose en tant que femme si on est cisgenre blanche ou handicapée voilée trans

We <3 devs
1er année, je ne parle qu'à un groupe identique
Appel à contributeur/trice : ligne édito groupe beaucoup plus hétérogène, reconversion, discrimination, racisme, etc.

Habitus (famille école corps langage) ensemble homogène valeurs vêtements mimiques similaires
Groupe majoritaire / Effet de halo (réassurance de votre première impression)

Biais de sympathie / d'antipathie

What is holding back women in tech

Allié (pas grand monde leve la main dans la salle)

Mettre du sens (acceptation)
Faut encourager quand on est dans le creux de la vague

52% des femmes pensent que leurs genre sera un problème dans leur carrière

90% / 60% pour postuler

Attirer les femmes
Féminiser les titres de postes 
Promettez du concret (accompagner les femmes)

Mettez en avant les femmes (envoyer les femmes en conférence systématiquement)
Mentorat

Sylvia Duckworth, roue des privilèges

Poser des question d'abord, éviter les injonctions

Transparence salariale

Aide à la parentalité / assistance psychologique

67% des femmes pensent que le mentorat interne
Encourager les femmes à prendre la parole
Encourager les femmes à devenir role-model

Entreprise femtech (100% féminines) / cercles de sororités

## 10:15 - 11:15 - Scaling a dormant Java application from 0 to 100 pods in seconds? Quarkus and Knative to the rescue!
Kevin DUBOIS

Solution architect dans devloper advocate

Horizontal scaling
* Use only the ressources that we need
* Rolling deployments (canary A/B, etc)
* Handle loads / HA

But your code needs to be able to handle it

Docker compose => you can scale but not very scalable in prod
Kubernetes => out of the pod autoscaling / Doesn't support scaling to 0 automatically

Serverless  => app that don't require server management / deployment model exact demand

At first => FaaS
Then => containers (Knative, KEDA)
Adds missing parts (enventing)

Build serverless and event driven solutions
Cloud agnostic, can scale to 0 because it listens to event
Event driven architecture

Knative 2 parts :
- serving (deployment)
- eventing (sources, brokers, triggers)

Java high throughput, long running

Quarkus => lightweight, particularly at the start phase
based on java standard
Useful in containers and serverless

Quarkus + GraalVM => 12MB / 0.016s
4.3s with standard JVM

demo 0 to 100+ pods in seconds w/ Quarkus and Knative

Openshift serverless

For test => testcontainer / Quarkus / Dev services ???

## 11:15 - 12:15 - Le GitOps dont vous êtes le héros
Louis TOURNAYRE

Kubernetes + Gitops

Histoire : Le site marche pas (plus d'un jour à déployer, le thème arrive le lendemain)

Table ronde des équipes
* livraison de moins de choses et plus fréquentes
* du temps pour la dette technique

Les déploiements doivent être un non événement

Document word pour les mises en production

La suite est un livre dont on est le héros

Quelques typos à lui remonter

Dhall => 1 fichier 1 objet
Très typé, haskell, fonctionnel
Facilite les tests

ArgoCD ne fait pas du Dhall, mais il y a un plugin pour (sidecar)

kubeseal

## 12:45 - 13:00 - 🏡 Full-remote : comment réussir à travailler en équipe ?
Lise QUESNEL

Pas pu y aller

## 13:15 - 13:30 - L'affordance ou comment l'utilisateur interprète et perçoit une interface
Salvatore BERRITTELLA

Pas pu y aller

## 13:45 - 14:45 - Choreography vs Orchestration in serverless microservices
Guillaume LAFORGE

Orchestration (REST, not loosely coupled)
Choregraphy (event-driven)

Tant que c'est simple, ça va. Si on imagine un problème un peu plus compliqué, il arrive beaucoup de processus métiers qui peuvent devenir compliqué. L'approche événement c'est pas simple à décrire.

Exemple avec une app de partage de photo, développé dans les 2 modes.

## 14:45 - 15:10 - Du code Terraform VRAIMENT factorisé avec Terragrunt
Denis GERMAIN
AmigaOS

## 15:10 - 15:35 - Indexer ses documents bureautique avec la suite Elastic et FSCrawler
David PILATO
AmigaOS

## 16:00 - 17:00 - Comment Doctolib a traversé la crise du COVID : dernier rappel
Nicolas MARTIGNOLE
BSD

## 17:00 - 18:00 - Compose v2 & Compose Specification
Guillaume LOURS
Main room



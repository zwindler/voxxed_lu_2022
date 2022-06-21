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

Ma conférence

## 15:10 - 15:35 - Indexer ses documents bureautique avec la suite Elastic et FSCrawler
David PILATO

Apache Tika pour aller chercher des métadonnées dans les documents open office, pdf, mp3, etc

Pipeline inject dans ES

On peut installer des plugins, notamment celui de tika

Marche avec les images, il faut faire plein de trucs pour extraire les metadata

Ya du texte dans du PDF, on peut ingérer et indexer ce texte

A la place : FSCrawler

Architecture à la logstash

Mount 
JSON / XML / Apache tika
ES 6/7/8

On envoie que les données utiles

OCR avec tesseract, plus de formats dispos

Workplace search => gratuit

WP 7/8

## 16:00 - 17:00 - Comment Doctolib a traversé la crise du COVID : dernier rappel

Nicolas MARTIGNOLE

6 principal engineers

Docto n°1

Quasiment toute la salle est passée par docto 
Boring architecture

La vaccination n'est pas seule responsable de la croissance de docto

La vaccination a bouleverser la roadmap
vaccination en allemange, le ministre de la santé a demandé à docto de le faire du jour au lendemain (coup de téléphone au patron)

Quand ils savent qu'il va y avoir une intervention, ils peuvent gérer (20h non événement)

Ils ont arrêté les tests de charge

Comment gérer l'exceptionnel => n'importe qui peut déclencher une crise (tout le monde est formé)

Service externe inaccessible
Sentries après une mise à jour
Lenteur
...

Cellule de crise (incident manager, communication manager, scribe, ...)

Duty
10h 14h 17h décide si master va en prod ou pas

Datadog / newrelic, santé du logiciel

12 juillet (3h30)
Nicolas était scribe ce jour là
Run => scale
Base => lecture rame
Aurora => 13 readers (max)

Pas de plan B

960k rdv confirmés
1,4M le lendemain

db.r5.24xlarge => 142k$/mois

210k req / secondes

Chiffrement au repos
> Chiffrement de bout en bout pour certaines données médicales. Pas toutes.

Les données ne nous appartiennent pas

1- Soit on passe à 2 bases. 
2- Soit remplacer Aurora pour une base plus élastique

Mais garder "Simplicité du build, simplicité du run".

Données sorties pour le 1.

Tech radar, 2 semaines de discussions

Modular monolith

Les dev se plaignent de la CI (lenteur)
- 40k test
- 11 minutes => 25 minutes

Commit à 22h pour éviter les commits des autres...

Fintech => combien coute un commit 5000 commit 40k pour la CI 8€ par commit

40% des couts d'infra pour du RUN

La CI coute 17% des 60% restant

Revenir sur des choses plus simples

40000 tests sur un cluster à 500 mini machines qui lance les IHM de docto pour voir si on casse des trucs

Arnaud héritier rejoint docto...

## 17:00 - 18:00 - Compose v2 & Compose Specification
Guillaume LOURS
Main room



## Introduction du premier jour de conférence

Pour ce premier talk, Pierre Antoine Grégoire nous a reparlé de ces 2 ans sans VoxxedLu (cause COVID).

Probablement un peu pour embrayer sur la keynote, il a ensuite rappelé qu'il y a encore en conférence beaucoup plus d'hommes que de femmes. Peut être même plus depuis la crise COVID ?

## Pourquoi vous n'attirerez et ne retiendrez pas les femmes dans vos équipes tech !

La keynote du premier jour a été faites pas Marcy CHAROLLOIS.

Marcy a fait ce talk à Devoxx FR en avril dernier. J'avais été le voir et j'étais content de le RE-voir, car il y a beaucoup de messages à assimiler.

* Habitus
* Status quo
* Resistance au changement
* Courbe du deuil
* Attraction / Rétention des femmes

Marcy aborde plein de sujets importants pour comprendre POURQUOI tant de femmes quittent la tech.

Je ne spoil pas plus, **le talk est à voir**.

**Side note personnelle parce que ça shitpost régulièrement sur Twitter contre les speakers qui font un même talk dans plusieurs conf :** ce talk est un excellent exemple de talk qui DOIT être refait dans plusieurs conférences.

[//]: # "On ne va pas vivre la même chose en tant que femme si on est cisgenre blanche ou handicapée voilée trans We <3 devs 1er année, je ne parle qu'à un groupe identique Appel à contributeur/trice : ligne édito groupe beaucoup plus hétérogène, reconversion, discrimination, racisme, etc. Habitus (famille école corps langage) ensemble homogène valeurs vêtements mimiques similaires Groupe majoritaire / Effet de halo (réassurance de votre première impression) Biais de sympathie / d'antipathie What is holding back women in tech Allié (pas grand monde leve la main dans la salle) Mettre du sens (acceptation) Faut encourager quand on est dans le creux de la vague 52% des femmes pensent que leurs genre sera un problème dans leur carrière 90% / 60% pour postuler Attirer les femmes Féminiser les titres de postes Promettez du concret (accompagner les femmes) Mettez en avant les femmes (envoyer les femmes en conférence systématiquement Mentorat Sylvia Duckworth, roue des privilèges Poser des question d'abord, éviter les injonctions Transparence salariale Aide à la parentalité / assistance psychologique 67% des femmes pensent que le mentorat interne Encourager les femmes à prendre la parole Encourager les femmes à devenir role-model Entreprise femtech (100% féminines) / cercles de sororités"

## Scaling a dormant Java application from 0 to 100 pods in seconds? Quarkus and Knative to the rescue!

Kevin DUBOIS, solution architect et developer advocate chez Redhat, nous a fait une présentation suivie d'une démo sur Quarkus et KNative.

Je ne m'étais pas trop intéressé à KNative, mais effectivement, dans le cas d'un microservice "event driven" (en mode serverless), c'est hyper intéressant et Quarkus+GraalVM (avec un démarrage d'une bête API REST en 0.016s) est réellement utile, par rapport à une JVM.

Un point dont n'a pas parlé Kevin est que certes, le couple Quarkus+GraalVM boote très vite, mais qu'on a tout un overhead apporté par Kubernetes pour l'affectation (Scheduling) et l'initialisation des Pods. 

En gros, ça marche, mais pas non plus à 0.016 secondes ;-)

[//]: # "Horizontal scaling * Use only the ressources that we need * Rolling deployments (canary A/B, etc) * Handle loads / HA But your code needs to be able to handle it Docker compose => you can scale but not very scalable in prod Kubernetes => out of the pod autoscaling / Doesn't support scaling to 0 automatically Serverless  => app that don't require server management / deployment model exact demand At first => FaaS Then => containers (Knative, KEDA) Adds missing parts (enventing) Build serverless and event driven solutions Cloud agnostic, can scale to 0 because it listens to event Event driven architecture Knative 2 parts : - serving (deployment) - eventing (sources, brokers, triggers) Java high throughput, long running Quarkus => lightweight, particularly at the start phase based on java standard Useful in containers and serverless Quarkus + GraalVM => 12MB / 0.016s // 4.3s with standard JVM demo 0 to 100+ pods in seconds w/ Quarkus and Knative Openshift serverless For test => testcontainer / Quarkus / Dev services ???"

## Le GitOps dont vous êtes le héros

Je ne vais pas pouvoir vous décrire totalement ce talk de Louis TOURNAYRE puisqu'il s'agit d'un talk "interactif" en mode "livre dont vous êtes le héros".

Ce talk est TRES TRES bien fait, l'expérience est super agréable, mêlant avec brio interactivité, choix multiples et démos lives.

A l'issue de notre "histoire" (puisqu'il y a plusieurs branches possibles), nous avions vu comment déployer une application avec k3d, Gitops et ArgoCD avec en plus des fichiers Dhall et expérimenté les Sealed Secrets avec kubeseal (on a même aussi parlé brièvement de Hashicorp Vault, j'en parle dans [cet article](/2020/08/31/gerez-vos-secrets-kubernetes-dans-vault/)).

A voir absolument si ces technos vous intéressent.

[//]: # "Kubernetes + Gitops / Histoire : Le site marche pas (plus d'un jour à déployer, le thème arrive le lendemain) / Table ronde des équipes / livraison de moins de choses et plus fréquentes / du temps pour la dette technique / Les déploiements doivent être un non événement / Document word pour les mises en production / La suite est un livre dont on est le héros / Quelques typos à lui remonter / Dhall => 1 fichier 1 objet / Très typé, haskell, fonctionnel / Facilite les tests / ArgoCD ne fait pas du Dhall, mais il y a un plugin pour (sidecar) / kubeseal"

## Déjeuner

J'avais prévu d'aller voir "🏡 Full-remote : comment réussir à travailler en équipe ?" de Lise QUESNEL et "L'affordance ou comment l'utilisateur interprète et perçoit une interface" de Salvatore BERRITTELLA, mais je n'ai finalement pas réussi à y aller.

## Choreography vs Orchestration in serverless microservices

Guillaume LAFORGE de chez Google nous a fait un talk pour parler des avantages et des inconvénients de deux patterns :
* Orchestration (REST, not loosely coupled)
* Choregraphy (event-driven)

A première vue, l'approche Choregraphy semble plus efficace (meilleure résilience en cas de coupure d'un de composants de la chaîne métier). Et tant que c'est simple, ça va. 

Sauf que si on imagine un processus métier un peu plus compliqué. L'approche événement n'est pas simple à décrire et peut être difficile à debug, même lors de l'écriture du code.

Guillaume a ensuite montré un exemple des deux approches avec une app de partage de photos, développé dans les 2 modes.

## Du code Terraform VRAIMENT factorisé avec Terragrunt

A 14:45, c'était mon tour avec mon "Tool in action" sur Terragrunt, un wrapper de terraform.

Tout s'est bien passé même si j'étais super stressé et un peu speed (talk calibré pour 25-30 minutes, j'en avais 20). 

> J'adore quand un "plan" se déroule sans accroc

## Indexer ses documents bureautique avec la suite Elastic et FSCrawler

Juste après moi, David PILATO nous a présenté [FSCrawler](https://github.com/dadoonet/fscrawler), un projet open source (qu'il développe en side project)

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

## Comment Doctolib a traversé la crise du COVID : dernier rappel

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

## Compose v2 & Compose Specification

Guillaume LOURS a fait un tour d'horizon de l'évolution de Compose depuis Fig et l'apparition de la spec pour les fichiers de configuration Compose.

C'était intéressant d'avoir l'historique d'avoir plus de détails sur les features qui étaient les plus demandées (qu'ils ont implémenté dans Compose v2), mais n'étant pas utilisateur de Compose je ne suis pas forcément le meilleur public pour juger ;-).

[//]: # "Evolution de compose / format 2 local / format 3 cloud / A cause de l'arrivée de swarm /split sur le format de fichier et le run pour éviter ces problématiques (Compose specification) /Compose v2.0.0-rc1 écrit en Go /Compose v2 GA + EOL v1 / Les nouveautés dans compose (mount de la socket SSH pour l'agent, retrouver automatiquement les fichiers YAML de conf) / dev env"

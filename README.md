# Projet 13 — Passage d’un système RAG du POC au MVP

Projet réalisé dans le cadre du parcours **Data Engineer OpenClassrooms**.

Ce dépôt présente l’étude de gestion de projet permettant de préparer le
passage du chatbot RAG développé lors du Projet 11 vers un Minimum Viable
Product déployable, observable et évolutif.

## Contexte

Le POC initial permet de recommander des événements culturels à partir de
données OpenAgenda en combinant LangChain, FAISS et les modèles Mistral.

Les résultats du POC ont validé la faisabilité technique :

- 1 336 événements culturels préparés ;
- 3 383 chunks documentaires ;
- 3 383 vecteurs indexés dans FAISS ;
- 22 réponses conformes sur 24 ;
- taux de réussite fonctionnelle de 91,7 %.

Le Projet 13 ne consiste pas à développer immédiatement le produit final,
mais à préparer son passage vers un MVP exploitable.

## Présentation

- [Consulter la présentation de soutenance au format PDF](presentation/projet-13-rag-poc-to-mvp-project.pdf)

## Fonctionnalités prioritaires du MVP

Le périmètre étudié comprend notamment :

- une mémoire conversationnelle ;
- la prise en compte du contexte géographique ;
- une recherche web en temps réel ;
- le monitoring technique et fonctionnel ;
- une interface web et une API ;
- l’automatisation de l’ingestion et de l’indexation ;
- la sécurité, la gestion des secrets et la conformité ;
- le déploiement cloud et la chaîne CI/CD.

## Architecture cible

L’architecture proposée repose principalement sur :

- une API Python FastAPI ;
- des conteneurs Docker exécutés sur Amazon ECS Fargate ;
- Amazon RDS PostgreSQL avec l’extension pgvector ;
- Amazon S3 pour les données sources ;
- Amazon EventBridge Scheduler pour les traitements planifiés ;
- Amazon Cognito pour l’authentification ;
- Amazon CloudWatch et AWS X-Ray pour l’observabilité ;
- AWS Secrets Manager pour les secrets ;
- Amazon ECR pour les images Docker ;
- Terraform et GitHub Actions pour l’infrastructure et le déploiement.

## Planification

La réalisation du MVP est organisée sur une durée prévisionnelle de
douze semaines, depuis le cadrage détaillé jusqu’à la décision finale
de Go/No-Go.

Le périmètre Must-Have représente une charge initiale estimée à
58 jours-homme.

## Estimation financière

Les estimations de référence sont :

- coût de construction initial : **29 550 €** ;
- coût d’exploitation mensuel estimé : **2 187 €** pour le scénario
  de 500 utilisateurs actifs.

Ces montants reposent sur les hypothèses détaillées dans le fichier Excel
joint au dépôt.

## Livrables

- [Rapport de gestion au format PDF](rapport/rapport-gestion-projet-13.pdf)
- [Présentation de soutenance au format PDF](presentation/projet-13-rag-poc-to-mvp-project.pdf)
- [Macro backlog des fonctionnalités](livrables/macro-backlog-fonctionnalites.xlsx)
- [Estimation des coûts build et OPEX](livrables/estimation-couts-build-opex.xlsx)

## Projet source

Le POC RAG ayant servi de point de départ est disponible ici :

https://github.com/ericginez/RAG-chatbot

## Portfolio

Le portfolio professionnel présentant les projets du parcours est accessible
à l’adresse suivante :

https://ericginez.github.io/

## Auteur

**Eric Ginez**

Parcours Data Engineer — OpenClassrooms
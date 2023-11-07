## Slide 1 : Qu’est-ce que Camunda ?

- Camunda BPM est un système open source de gestion de processus métier qui facilite l’automatisation et l’optimisation des flux de travail.

## Slide 2 : Architecture de Camunda

- Camunda Engine : Le moteur d’exécution qui gère le cycle de vie des processus.
- Camunda Modeler : Permet de créer, modifier et déployer des modèles de processus BPMN.
- Camunda Tasklist : Interface utilisateur pour les utilisateurs finaux pour accomplir des tâches.
- Camunda Cockpit : Outil de supervision permettant de suivre les instances de processus et d’analyser les performances.
- Camunda Admin : Interface d’administration pour la configuration et la gestion des utilisateurs.

## Slide 3 : Composants de Camunda modeler

1. Tâches : Les tâches représentent les activités ou les étapes spécifiques qui doivent être accomplies dans le processus. Elles sont généralement symbolisées par des rectangles avec des coins arrondis.
2. Événements : Les événements marquent le début, la fin ou les déclencheurs d'actions dans un processus. Ils peuvent être des cercles pour les événements de début, des carrés pour les événements intermédiaires, et des losanges pour les événements de fin.
3. Passerelles : Les passerelles représentent des points de décision dans un processus. Elles déterminent le chemin que suivra le flux du processus en fonction de conditions spécifiques. Il existe des passerelles exclusives, inclusives et parallèles, symbolisées par différentes formes.
4. Flux de séquence : Les flux de séquence sont des flèches qui connectent les éléments du processus pour montrer la direction du flux. Ils indiquent l’ordre des activités et des événements dans le processus.

En combinant ces éléments de manière appropriée dans un diagramme BPMN, les organisations peuvent modéliser, analyser et optimiser leurs processus métier, ce qui facilite la compréhension, la communication et l’automatisation des activités opérationnelles.

## Slide 6 : Intégration de Camunda dans un projet Java

  1. Inclure les dépendances de Camunda dans le fichier `pom.xml`.
  2. Configurer la source de données pour Camunda.
  3. Initialiser le moteur Camunda dans l’application Java.

## Slide 7 :Engine REST API

  1. L'API REST permet de gérer et d'exécuter les processus BPMN.
  2. Pour interagir avec l'API REST de Camunda, vous devez effectuer des requêtes HTTP en utilisant le langage de programmation ou l'outil de votre choix (par exemple, cURL, Postman, Java, Javascript etc.). Les méthodes HTTP courantes que vous utiliserez comprennent GET, POST, PUT et DELETE. Merci de consulter la documentation officielle de Camunda(lien dans Docs sources) pour obtenir des informations détaillées sur les points d'accès de l'API, cependant en voici quelques exemples.
  3. Exemples:
       - Pour démarrer un processus:
           POST /process-definition/{id}/start
           POST /process-definition/key/{key}/start
           POST /process-definition/key/{key}/tenant-id/{tenant-id}/start

           **id** 	 	    L'identifiant de la définition du processus à récupérer.
           **key** 	      La clé de la définition du processus (la dernière version de celle-ci) doit être récupérée.
           **tenant-id** 	L'identifiant du locataire auquel appartient la définition du procédé.

         Le Request Body : Un objet JSON avec les propriétés suivantes: (au moins un objet JSON vide {}ou un payload de demande vide)

         Ex:
         ~~~JSON
            {
              "variables": {
                "nom": {
                  "type": "String",
                  "value": "John"
                },
                "date": {
                  "type": "String",
                  "value": "07/11/23"
                },
               // etc...
               // l'ensembles des variables qu'il faudra renseigner pour démarrer l'instance 
              }
            }
         ~~~

## Slide 8 : External Tasks

  1. Une tache externe (external task) est une étape d'un processus gérée en dehors du moteur de processus, ce qui permet une intégration flexible avec d'autres systèmes et une collaboration avec des acteurs externes pour l'accomplissement de la tâche.
  2. Exemple:
  3. Avantages à utiliser les taches externes:

## Slide 9 : Exemple de Projet - Gestion de Congés

- **Titre :** “Exemple de Projet - Gestion de Congés”
- Présentation détaillée d’un exemple de projet de gestion des demandes de congés :
  - Modélisation d’un processus de demande de congés.
    ![BPMN Modele](/process.png)


## Docs sources

- [Camunda site officiel v07](https://docs.camunda.org/manual/7.20/)
- [Baeldung camunda](https://www.baeldung.com/spring-boot-embedded-camunda)
- [Article sur medium](https://medium.com/nerd-for-tech/bpmn2-0-camunda-workflow-spring-boot-application-2381f3d42e5f)
- [Camunda Engine Rest docs](https://stage.docs.camunda.org/rest/camunda-bpm-platform/7.21-SNAPSHOT/)
- [Camunda BPMN Reference](https://camunda.com/bpmn/reference/)
- [Camunda external tasks article](https://blog.bernd-ruecker.com/how-to-write-glue-code-without-java-delegates-in-camunda-cloud-9ec0495d2ba5)


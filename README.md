## Slide 2 : Qu’est-ce que Camunda ?

- Camunda BPM est un système open source de gestion de processus métier qui facilite l’automatisation et l’optimisation des flux de travail.

## Slide 3 : Architecture de Camunda

- Camunda Engine : Le moteur d’exécution qui gère le cycle de vie des processus.
- Camunda Modeler : Permet de créer, modifier et déployer des modèles de processus BPMN.
- Camunda Tasklist : Interface utilisateur pour les utilisateurs finaux pour accomplir des tâches.
- Camunda Cockpit : Outil de supervision permettant de suivre les instances de processus et d’analyser les performances.
- Camunda Admin : Interface d’administration pour la configuration et la gestion des utilisateurs.

## Slide 4 : Composants de Camunda modeler

1. Tâches : Les tâches représentent les activités ou les étapes spécifiques qui doivent être accomplies dans le processus. Elles sont généralement symbolisées par des rectangles avec des coins arrondis.
2. Événements : Les événements marquent le début, la fin ou les déclencheurs d'actions dans un processus. Ils peuvent être des cercles pour les événements de début, des carrés pour les événements intermédiaires, et des losanges pour les événements de fin.
3. Passerelles : Les passerelles représentent des points de décision dans un processus. Elles déterminent le chemin que suivra le flux du processus en fonction de conditions spécifiques. Il existe des passerelles exclusives, inclusives et parallèles, symbolisées par différentes formes.
4. Flux de séquence : Les flux de séquence sont des flèches qui connectent les éléments du processus pour montrer la direction du flux. Ils indiquent l’ordre des activités et des événements dans le processus.

En combinant ces éléments de manière appropriée dans un diagramme BPMN, les organisations peuvent modéliser, analyser et optimiser leurs processus métier, ce qui facilite la compréhension, la communication et l’automatisation des activités opérationnelles.

## Slide 5 : Intégration de Camunda dans un projet Java

- Étapes détaillées pour l’intégration de Camunda dans un projet Java :
  1. Inclure les dépendances de Camunda dans le fichier `pom.xml`.
  2. Configurer la source de données pour Camunda.
  3. Initialiser le moteur Camunda dans l’application Java.

## Slide 6 : Exemple de Projet - Gestion de Congés

- **Titre :** “Exemple de Projet - Gestion de Congés”
- Présentation détaillée d’un exemple de projet de gestion des demandes de congés :
  - Modélisation d’un processus de demande de congés.
![process model](/process.png?raw=true "Gestion de conges modele")

## Slide 7 : Conclusion

- Encouragement à poser des questions.

## Docs sources

[Camunda site officiel v07](https://docs.camunda.org/manual/7.20/)
[Baeldung camunda](https://www.baeldung.com/spring-boot-embedded-camunda)
[Article sur medium](https://medium.com/nerd-for-tech/bpmn2-0-camunda-workflow-spring-boot-application-2381f3d42e5f)

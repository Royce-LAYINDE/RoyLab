---
title: "Quête I : Mise en place d'une application Web pour la Prédiction d'Éligibilité aux Prêts avec Flask et Machine Learning"
date: 2024-08-20T10:58:08-04:00
description: "Dans cet article, nous vous emmenons dans une aventure captivante autour d'un projet de prédiction d'éligibilité aux prêts bancaires. Grâce à la magie du machine learning (régression logistique et KNN) et à la création d'une plateforme web avec Flask, nous avons pu construire un outil pratique pour les administrateurs de banque. Découvrez comment nous avons intégré des modèles prédictifs, visualisé les données clients, et déployé le tout avec Docker pour une solution complète et accessible."
featured_image: "/images/gest.jpg"
omit_header_text: true
tags: ["Projet","Python", "Machine learning","Flask","Développement web", "Docker"]
disable_share: false   
---
Dans ce chapitre, nous vous dévoilons un projet fascinant : la prédiction d'éligibilité aux prêts à l'aide de deux puissants artefacts du royaume du machine learning, la régression logistique et KNN. Une aventure mêlant données, algorithmes et interface magique, que nous vous invitons à explorer.

## Table des matières
- [Objectif du Projet](#objectif-du-projet)


# Objectif du Projet

Chaque grande aventure commence par un défi. Ici, l'objectif principal était de créer un modèle prédictif qui aide les banques à déterminer si un client potentiel est éligible à un prêt en fonction de ses caractéristiques personnelles et financières comme son revenu, sa situation matrimoniale ou son historique de crédit. Pour ce faire, nous avons mis sur pieds deux modèles de machine learning : la régression logistique et le k-plus proches voisins (KNN), pour analyser et prédire les résultats en fonction des données. Nous avons également créé une plateforme web pour permettre aux banquiers et administrateurs de banque de visualiser et d’interagir facilement avec ces prédictions. Une solution complète, pensée pour rendre le processus décisionnel plus simple et efficace.

# Le grimoire des données

Avant de plonger dans la construction des modèles, il fallait préparer le terrain : le grimoire des données.

***Source des données*** : Ce jeu de données provient de la plateforme [Analytics Vidhya](https://www.analyticsvidhya.com/), un site de référence dans le domaine de la data science. Il contient des informations cruciales sur les candidats aux prêts (revenu, statut marital, historique de crédit, etc.), que nous avons exploitées pour entraîner nos modèles.

![Image d'exemple](/images/dataset.jpg)

Préparation : Les données ont été nettoyées, transformées et explorées, permettant ainsi une intégration fluide dans les modèles et la plateforme.

# Construction des Modèles de Prédiction

Après avoir préparé les données, nous avons entamé la phase de construction des modèles de machine learning afin de prédire l’éligibilité des clients à un prêt. Deux modèles principaux ont été utilisés : la régression logistique et le K-Nearest Neighbors (KNN).

**Régression Logistique** : Nous avons choisi ce modèle pour sa simplicité et son efficacité lorsqu'il s'agit de classification binaire. En utilisant les caractéristiques extraites des données (comme le revenu, le statut professionnel et d'autres variables), nous avons entraîné un modèle de régression logistique pour estimer la probabilité qu’un client soit éligible ou non à un prêt. Ce modèle fournit une interprétation claire des coefficients, nous permettant d'analyser l'impact des différentes variables sur l’éligibilité.

**K-Nearest Neighbors (KNN)** : Ce second modèle a été choisi pour sa capacité à classer de manière non-linéaire, en se basant sur la similarité entre les clients. Avec KNN, le modèle compare un client à ses voisins les plus proches dans l’espace des caractéristiques, et le classe en fonction de la majorité des résultats de ces voisins. Nous avons exploré différentes valeurs de k pour optimiser les performances du modèle.

Nous avons testé et validé ces deux modèles à l’aide de techniques comme la validation croisée et l'évaluation des scores de précision afin de nous assurer que nos prédictions étaient fiables et généralisables à de nouvelles données.

# Développement de la Plateforme Web

Nous ne nous sommes pas arrêtés à la modélisation. Nous avons conçu une plateforme web interactive avec Flask, un micro-framework Python. Cette plateforme était destinée aux banquiers et administrateurs, leur permettant de visualiser et d'interpréter les résultats des prédictions.

***Fonctionnalités Clés***

**Visualisation des Données** : Grâce à cette plateforme, les banquiers peuvent consulter des visualisations telles que la répartition des clients, les trois personnes avec les plus hauts revenus, ou encore les clients ayant la plus longue histoire de crédit.

**Interface Utilisateur** : Nous avons utilisé HTML et CSS pour créer une interface utilisateur simple mais intuitive, agrémentée de quelques éléments en JavaScript pour rendre l’expérience plus dynamique.
Modèles de Machine Learning Intégrés : Les modèles de régression logistique et de KNN, créés en amont, ont été importés dans notre application Flask pour permettre une prédiction en temps réel à partir des données fournies par les utilisateurs.

**Dockerisation** : Pour faciliter le déploiement et l'exécution de l'application sur différentes plateformes, nous avons dockerisé le projet. Grâce à Docker, l'application est encapsulée dans un environnement contrôlé, facilitant la collaboration entre développeurs et l'intégration continue.

# Point sur les Technos Utilisées

-Python 
-pandas, numpy, seaborn, matplotlib
-scikit-learn 
-MySQL
-Flask 
-HTML, CSS, JavaScript 
-Docker 
-Git

# Impact et Utilité

Cette plateforme se veut un outil d’aide à la décision pour les établissements bancaires. En centralisant l'analyse et la visualisation des données client, elle permet aux banquiers d’avoir une vue d’ensemble sur les dossiers et de prendre des décisions plus éclairées concernant l'attribution des prêts.

# Visuels

# Conclusion de la quête

Ce projet a été une belle aventure mêlant data science et développement web, avec la mise en place d'une plateforme pratique pour faciliter l'évaluation de l'éligibilité aux prêts bancaires. De la construction des modèles de prédiction à la création d'une interface utilisateur intuitive avec Flask, nous avons exploré diverses technologies tout en appliquant des méthodes rigoureuses de machine learning.

Si vous souhaitez plonger plus en profondeur dans le projet ou voir son code en action, vous pouvez consulter le dépôt GitHub [ici](https://github.com/Royce-LAYINDE/project_roy_bank_manager). De plus, pour un aperçu plus détaillé des étapes du projet, n'hésitez pas à consulter le rapport complet [ici](/documents/Rapport - Projet Roybank_manager_byRoyce.pdf).

###### Nous espérons que cette quête vous a inspiré et que vous pourrez à votre tour mettre en œuvre des solutions de data science pour résoudre des problèmes réels. 

###### À bientôt pour de nouvelles quêtes numériques !
###### *Magiquement vôtre,*
M.Royce

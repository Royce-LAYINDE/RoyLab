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


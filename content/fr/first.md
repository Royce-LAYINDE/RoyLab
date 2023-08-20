---
title: "Chapitre 1: La Danse Enchantée de la Tortue : Découvrir la Magie de Python avec Turtle"
date: 2023-08-18T10:58:08-04:00
description: "Vous êtes-vous déjà demandé ce que ressent une tortue lorsqu'elle trace son chemin sur le sable? Le module Turtle en Python vous permet d'explorer cette expérience en donnant vie à une tortue numérique. Imaginez que vous la guidez avec des mots, lui demandant d'avancer, de tourner et de créer des dessins fascinants. Découvrez comment importer ce module, créer votre propre tortue virtuelle et la laisser parcourir des chemins enchantés sur votre écran."
featured_image: "/images/python.jpg"
omit_header_text: true
tags: ["python","sql","html"]
type: page
---
L'univers de la programmation peut sembler intimidant pour les débutants, mais il existe des moyens ludiques et créatifs pour introduire les concepts de base. Récemment, j'ai eu le privilège d'être l'un des intervenants lors d'une séance d'initiation à la programmation organisée par le [Dakar Institute of Technology](https://dit.sn/). Parmi toutes les notions abordées au cours de cette semaine passionnante, l'expérience de découvrir le module Turtle en Python a été particulièrement enrichissante. Cette semaine, je t'invite donc à explorer cet outil étonnant, qui ouvre la voie à la création artistique en langage Python. Prépare-toi à embarquer pour un voyage où les figures géométriques prennent vie et où les courbes deviennent des œuvres d'art.   
                        <p align="center">*A vos baguettes, prêts ? Incantations !*</p>

**Le Module Turtle en Python : Une Aventure Graphique**

Imaginez une feuille de papier virtuelle où une tortue numérique peut se déplacer et dessiner en suivant vos commandes. Voilà en quoi consiste le module Turtle en Python. Cette approche graphique permet aux débutants de visualiser en temps réel comment les instructions de programmation se traduisent en mouvements et en dessins.

**La Magie du Démarrage : Importer Turtle**


Comme tout bon enchanteur, notre aventure commence par la préparation. Avant de faire danser notre tortue, il faut invoquer sa présence en important le module Turtle. Voici comment tu peux faire :

```Python
#Importation de turtle
import turtle
```

**Création de l'Environnement : Initialisation de la Fenêtre**

Chaque magicien a besoin de son propre espace pour réaliser ses tours. De même, notre tortue a besoin de sa propre fenêtre pour dessiner. Voici comment créer la fenêtre d'opération :
```Python
#Initialisation de la fenetre
window= turtle.Screen()
```

**Donner un Nom Magique : Titre de la Fenêtre**

Comme tout bon magicien, notre tortue a besoin d'une entrée grandiose. Donnons-lui un titre fascinant pour sa scène de création :
```Python
#Donnons un nom à notre fenetre
window.title("L'Art Enchanté de Tracé avec Turtle")
```

**L'Incantation : Création de l'Instance Turtle**

Avant de faire apparaître notre tortue, nous devons la créer. C'est comme invoquer un familier dans le monde magique. Voici comment créer une instance de tortue avec laquelle nous allons interagir :

```Python
#Creation d'une instance de turtle
t= turtle.Turtle()
```

**Chaque Pas est une Étape : Les Commandes de Base**

Chaque pas de notre tortue est une étape vers la création. Tout comme [Viktor Krum, a utilisé sa baguette pour faire danser Hermione](https://padlet-uploads.storage.googleapis.com/293762411/99453da9e54e6ce8ea76d6dd46671e11/Harry_Potter_et_la_Coupe_de_Feu___J_K_ROWLING.pdf) , nous faisons danser notre tortue avec des commandes simples. Voici quelques-unes des commandes de base pour faire bouger notre tortue :

-Pour faire avancer la tortue sur une certaine distance, on utilise la commande suivante:
```python
#Faire avancer le curseur de 50px
t.forward(50)
```
Une alternative à cette commande est tout simplement:
```python
t.fd(50)
```
-Pour faire reculer la tortue sur une certaine distance, on utilise la commande suivante:
```python
#Faire avancer le curseur de 50px
t.backward(50)
```
De même, on peut aussi ecrire:
```python
t.bk(50)
```

Ainsi donc, pour faire avancer ou reculer notre tortue, il suffit de faire respectivement appel aux méthodes .fd() et .bk() et de mettre en argument, la distance qu'on veut qu'elle parcourt.

*NB: Remarque que la distance sur laquelle on fait bouger le curseur s'exprime en [pixel(px)](https://fr.wikipedia.org/wiki/Pixel)*

-Pour faire tourner la tortue vers la gauche d'un certain angle, on utilise la commande suivante:
```python
#Faire dévier  le curseur à gauche de 60°
t.left(60)
```
Une alternative à cette commande est tout simplement:
```python
t.lt(60)
```
-Pour faire tourner la tortue vers la droite d'un certain angle, on utilise la commande suivante:
```python
#Faire dévier  le curseur à droite de 45°
t.right(45)
```
De même, on peut aussi ecrire:
```python
t.rt(45)
```
Ainsi donc, pour faire tourner notre tortue à gauche ou à droite, il suffit de faire respectivement appel aux méthodes .fd() et .bk() et de mettre en argument la mesure de l'angle(en degré) dont-on veut qu'elle dévie.

En somme, en utilisant ces commandes simples pour faire avancer, reculer, tourner à gauche ou à droite, notre tortue répond à nos instructions pour créer des mouvements enchanteurs.
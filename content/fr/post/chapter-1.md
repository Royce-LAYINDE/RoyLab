---
title: "Chapitre I: La Danse Enchantée de la Tortue : Découvrir la Magie de Python avec Turtle"
date: 2023-08-18T10:58:08-04:00
description: "Vous êtes-vous déjà demandé ce que ressent une tortue lorsqu'elle trace son chemin sur le sable? Le module Turtle en Python vous permet d'explorer cette expérience en donnant vie à une tortue numérique. Imaginez que vous la guidez avec des mots, lui demandant d'avancer, de tourner et de créer des dessins fascinants. Découvrez comment importer ce module, créer votre propre tortue virtuelle et la laisser parcourir des chemins enchantés sur votre écran."
featured_image: "/images/tortue.png"
omit_header_text: true
tags: ["python","turtle","coding"]
disable_share: false   #Pour que les visiteurs puissent partager la page
read_more_copy: En savoir plus sur Turtle #pour personnaliser le message de "Voir plus" ou "lire plus"
# private: true #Pour empecher que les moteurs de recherches indexent la page
---


L'univers de la programmation peut sembler intimidant pour les débutants, mais il existe des moyens ludiques et créatifs pour introduire les concepts de base. Récemment, j'ai eu le privilège d'être l'un des intervenants lors d'une séance d'initiation à la programmation organisée par le [Dakar Institute of Technology](https://dit.sn/). Parmi toutes les notions abordées au cours de cette semaine passionnante, l'expérience de découvrir le module Turtle en Python a été particulièrement enrichissante. Cette semaine, je t'invite donc à explorer cet outil étonnant, qui ouvre la voie à la création artistique en langage Python. Prépare-toi à embarquer pour un voyage où les figures géométriques prennent vie et où les courbes deviennent des œuvres d'art.   
                        <p align="center">*À vos baguettes, prêts ? Incantations !*</p>



## Table des matières
- [La Magie du Démarrage : Importer Turtle](#1)
- [Création de l'Environnement : Initialisation de la Fenêtre](#2)
- [Donner un Nom Magique : Titre de la Fenêtre](#3)
- [L'Incantation : Création de l'Instance Turtle](#4)
- [Chaque Pas est une Étape : Les Commandes de Base](#5)
- [Exploration Créative : Dessiner des Figures Géométriques](#6)
- [Changer d'Encre : Personnaliser les Couleurs et l'Épaisseur](#7)
- [Exploration de l'Apparence : Personnaliser la Tortue](#8)
- [Retour sur Mon Expérience à la Séance d'Initiation ](#9)
- [Conclusion Enchanteur : La Création sans Limites](#10)

# Le Module Turtle en Python : Une Aventure Graphique 

Imaginez une feuille de papier virtuelle où une tortue numérique peut se déplacer et dessiner en suivant vos commandes. Voilà en quoi consiste le module Turtle en Python. Cette approche graphique permet aux débutants de visualiser en temps réel comment les instructions de programmation se traduisent en mouvements et en dessins.

# La Magie du Démarrage : Importer Turtle {#1}


Comme tout bon enchanteur, notre aventure commence par la préparation. Avant de faire danser notre tortue, il faut invoquer sa présence en important le module Turtle. Voici comment tu peux faire :

```Python
#Importation de turtle
import turtle
```

# Création de l'Environnement : Initialisation de la Fenêtre {#2}

Chaque magicien a besoin de son propre espace pour réaliser ses tours. De même, notre tortue a besoin de sa propre fenêtre pour dessiner. Voici comment créer la fenêtre d'opération :
```Python
#Initialisation de la fenetre
window= turtle.Screen()
```

# Donner un Nom Magique : Titre de la Fenêtre {#3}

Comme tout bon magicien, notre tortue a besoin d'une entrée grandiose. Donnons-lui un titre fascinant pour sa scène de création :
```Python
#Donnons un nom à notre fenetre
window.title("L'Art Enchanté de Tracé avec Turtle")
```

# L'Incantation : Création de l'Instance Turtle {#4}

Avant de faire apparaître notre tortue, nous devons la créer. C'est comme invoquer un familier dans le monde magique. Voici comment créer une instance de tortue avec laquelle nous allons interagir :

```Python
#Creation d'une instance de turtle
t= turtle.Turtle()
```

# Chaque Pas est une Étape : Les Commandes de Base {#5}

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
De même, on peut aussi écrire:
```python
t.bk(50)
```

Ainsi , pour faire avancer ou reculer notre tortue, il suffit de faire respectivement appel aux méthodes .fd() et .bk() et de mettre en argument, la distance qu'on veut qu'elle parcoure.

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
De même, on peut aussi écrire:
```python
t.rt(45)
```
Ainsi , pour faire tourner notre tortue à gauche ou à droite, il suffit de faire respectivement appel aux méthodes .lt() et .rt() et de mettre en argument la mesure de l'angle(en degré) dont-on veut qu'elle dévie.

En somme, en utilisant ces commandes simples pour faire avancer, reculer, tourner à gauche ou à droite, notre tortue répond à nos instructions pour créer des mouvements enchanteurs.

# Exploration Créative : Dessiner des Figures Géométriques {#6}

Maintenant que nous maîtrisons les bases, plongeons dans l'art de la création géométrique ! Notre tortue peut dessiner bien plus que des lignes droites. En combinant les mouvements que nous avons appris, nous pouvons créer des figures géométriques fascinantes. Voici quelques exemples pour te donner un aperçu de ce que tu peux accomplir :

## Dessiner un Carré Magique  : 
Utilisons notre tortue pour dessiner un carré. Cela peut sembler simple, mais c'est un premier pas vers des créations plus complexes. Voici comment tu peux faire en tant qu'apprenti mage :
```python
import turtle
window= turtle.Screen()
window.title("Tracé de carré avec turtle")
t= turtle.Turtle()
#--------------------
#Méthode1
t.fd(50)
t.lt(90)
t.fd(50)
t.lt(90)
t.fd(50)
t.lt(90)
t.fd(50)
t.lt(90)
#---------------------
#Ferme la fenetre graphique quand je clique dessus
window.exitonclick()
```
Avec ce code, tu auras assurément un carré à la sortie. En effet, on demande à notre tortue d'avancer de 50 px puis de tourner à gauche d'un angle de 90°. On répète le geste trois autres fois en plus.
Par contre, il existe une autre manière de réécrire ce code. *Attention, voici le moment d'invoquer les boucles temporelles grâce à nos pouvoirs de mage !*

En effet, grâce aux boucles en Python, il nous est possible de répéter une action un certain nombre de fois *(Quelle sorcellerie...)*

On pourrait donc écrire en lieu et place du précédent code;
```python
#--------------------
#Méthode2
for i in range (4):
    t.fd(50)
    t.lt(90)
#---------------------
```
Ou bien;
```python
#--------------------
#Méthode3
a=0
while a<4:
    t.fd(50)
    t.lt(90)
    a+=1
#---------------------
```
Si tu es un jeune *apprenti mage* et que tu n'as pas encore appris le sort d'invocation des boucles , pas de panique, clique [ici](https://courspython.com/boucles.html), pour en apprendre un peu plus en attendant que je publie mon  *grimoire sur la magie des boucles*.

## Créer un Triangle Enchanté :
 Passons au niveau supérieur en dessinant un triangle. En combinant les mouvements de notre tortue, nous pouvons créer une figure à trois côtés. Voici comment procéder :
```python
import turtle
window= turtle.Screen()
window.title("Tracé d'un triangle avec turtle")
t= turtle.Turtle()
#--------------------
#Méthode1
t.fd(80)
t.left(120)
t.fd(80)
t.left(120)
t.fd(80)
t.left(120)
#---------------------
#Ferme la fenetre graphique quand je clique dessus
window.exitonclick()
```
Ou mieux encore;
```python
for i in range(3):
    t.fd(80)
    t.left(120) 
```
NB: Remarque ici qu'on fait tourner notre curseur de 120° vers la gauche. En effet, le triangle ici tracé est un triangle équilatéral et donc ses angles mesurent tous 60°. Cependant, pour obtenir exactement cet angle, il faudrait que l'on tourne notre curseur de 120°(180°-60°), c'est-à-dire de l'angle supplémentaire à notre angle de 60°.

![Image d'exemple](/images/angle.jpg)

Ici alors, il nous faut faire parcourir l'angle en bleu afin de pouvoir obtenir l'angle en jaune dans notre triangle.

Bravo *jeune apprenti(e)* te voilà maintenant capable de Créer des Triangles enchantés à l'infini. Découvrons ensemble d'autres sorts que tu peux apprendre sur Turtle.

# Changer d'Encre : Personnaliser les Couleurs et l'Épaisseur {#7}

La magie opère non seulement dans les formes que nous dessinons, mais aussi dans les couleurs que nous utilisons. Avec Turtle, nous pouvons changer la couleur du tracé en utilisant des noms de couleurs prédéfinis ou des codes hexadécimaux. Voici comment tu peux le faire :

## Invoquer une Couleur Magique :
 Utilisons des couleurs pour donner vie à nos dessins. Voici comment changer la couleur du tracé :
```python
# Changer la couleur du tracé en rouge
t.pencolor("red")
```
Grâce à la méthode .pencolor(), tu pourras donner une couleur à ton tracé
NB: En Python, les incantations sont à prononcer en anglais alors le nom de ta couleur doit être en anglais("blue","red","yellow"...)

## Épaissir le Tracé Enchanté :
 Modifions l'épaisseur du tracé pour donner une nouvelle dimension à nos créations. Voici comment le faire :
```python
# Épaissir le tracé
t.pensize(3)  # Épaisseur de 3 pixels
```

# Exploration de l'Apparence : Personnaliser la Tortue {#8}

Notre tortue numérique peut également subir une métamorphose visuelle. Nous pouvons changer son apparence en modifiant sa forme, sa couleur et bien plus encore. Voici comment rendre notre tortue encore plus captivante :

Changer la Forme Enchantée : Transformons notre tortue en une créature encore plus magique. Utilisons une forme prédéfinie ou même une image personnalisée comme sa nouvelle apparence :
```python
# Changer la forme du curseur en "tortue" 
t.shape("turtle")
```
Avec cette ligne de code, tu pourras voir une vraie *petite tortue magique* comme curseur.

## Un Peu de Remplissage : L'Art du Coloriage
Parfois, un simple contour ne suffit pas. Notre tortue peut également remplir les formes qu'elle crée.Apportons de la couleur à notre tortue pour qu'elle se distingue dans son voyage créatif. Pour définir la couleur de remplissage, utilisez la commande fillcolor suivie du nom de la couleur en anglais.
```python
#Définir la couleur de remplissage en bleu
t.fillcolor("blue")
```
Ensuite, pour commencer à remplir une forme, utilisez la commande begin_fill, et pour arrêter le remplissage, utilisez la commande end_fill :
```python
t.begin_fill()   #Commencer à remplir la forme
#Notre code de tracé ici
#...
t.end_fill()     #Arrêter le remplissage
```

À titre illustratif, l'invocation d'un carré magique coloré devrait ressembler à celui-ci:

```python
import turtle
window= turtle.Screen()
window.title("Tracé d'un triangle avec turtle")
t= turtle.Turtle()
#-------------------- 
t.shape("turtle")    # Changer la forme du curseur en "tortue"
t.fillcolor("blue")   #Définir la couleur de remplissage en bleu
t.begin_fill()  #Commencer à remplir la forme
for i in range (4):
    t.fd(50)
    t.lt(90)
t.end_fill()     #Arrêter le remplissage
#---------------------
#Ferme la fenetre graphique quand je clique dessus
window.exitonclick()
```
# Retour sur Mon Expérience à la Séance d'Initiation {#9}

Lors de la séance d'initiation au DIT, j'ai utilisé le module Turtle pour captiver l'attention des jeunes bacheliers. Les sourires d'émerveillement se dessinaient sur leurs visages lorsqu'ils ont vu la tortue numérique tracer des motifs sous leur contrôle. Nous avons créé des lignes, des triangles et même des étoiles en utilisant des boucles et des commandes Turtle simples.

Parmi les moments mémorables, certains étudiants ont décidé de laisser libre cours à leur créativité en créant des dessins personnalisés avec le module Turtle. Cette expérience a montré que la programmation ne se limite pas à des lignes de code, mais peut être une forme d'expression artistique.


# Conclusion Enchanteur : La Création sans Limites {#10}

Avec ces connaissances, vous avez tout ce dont vous avez besoin pour plonger dans le monde magique du tracé avec Turtle en Python. Chaque ligne de code devient une baguette magique pour votre tortue numérique, donnant vie à des formes et à des couleurs. Que vous créiez des motifs abstraits ou des dessins géométriques, l'art du tracé Turtle n'a pas de limites. Incantez vos idées, laissez votre tortue danser et explorez les infinies possibilités de création artistique offertes par Python et Turtle.

**La Magie Continue**

*Ne laisse pas ta baguette magique rouillée*

[Renforce ton savoir](https://docs.python.org/3/library/turtle.html)

[Découvre](https://www.frederic-junier.org/PythonSeconde/Python_Seconde_Parc/tortue/tortue2.html)

Consulte les tutoriels en ligne pour des idées de projets amusants.

🧙‍♂️🔮🌐📜

###### *Que chaque ligne de code devienne une baguette magique, et que chaque projet soit une œuvre enchanteresse.*
###### À bientôt pour plus de découvertes et de créations magiques !
###### *Votre enchanteur,*

 M.Royce

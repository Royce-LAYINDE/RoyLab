---
date: 2023-11-26T11:14:48-04:00
description: "Plongez dans le royaume fascinant du développement web avec cet article explorant les fondations magiques du HTML et du CSS. Découvrez l'art enchanteur derrière la création de sites web et apprenez les secrets du langage de balisage HTML et du langage de style CSS. De la structuration des pages à l'esthétique captivante, cette aventure vous guidera à travers les éléments essentiels du développement web. Préparez-vous à embrasser le pouvoir magique du code et à ouvrir la porte à des créations web extraordinaires."
featured_image: "/images/web1.jpg"
omit_header_text: true
tags: ["développement web", "HTML", "CSS", "coding"]
disable_share: false
title: "Chapitre IV: Les Fondations Magiques du Web : Explorez l'Art Enchanté du HTML et du CSS"

---
Mis à jour le 02/12/2023

*Temps de Lecture Estimé: Environ 15 à 20 minutes*
## Table des matières
- [Le Langage des Structurations: HTML](#1)
- [Création de la structure d'une page HTML](#2)
- [Utilisation des balises essentielles (head, body, div, etc.)](#3)
- [Création de la structure d'une page HTML : Façonnez votre univers en lignes de code](#4)


Bienvenue dans le royaume fascinant du développement web, où chaque ligne de code tisse la toile magique qui donne vie à l'univers en ligne. Dans cette quête, nous plongerons au cœur des fondations mystiques du HTML et du CSS, les deux langages qui servent d'alchimie pour transformer des lignes de code en sites web éblouissants.

Le HTML, langage de balisage, sera notre première étoile à explorer. Il forme la structure fondamentale de chaque page web, chaque balise jouant un rôle crucial dans la construction de cet édifice numérique. Ensuite, nous nous immergerons dans l'esthétique ensorcelante du CSS, le langage qui donne vie aux couleurs, aux polices, et qui modèle l'apparence de nos créations.

Attachez vos ceintures, car cette aventure promet non seulement de vous familiariser avec ces langages, mais aussi de vous armer d'astuces pratiques pour résoudre les énigmes les plus complexes du développement web. Préparez-vous à découvrir l'art et la magie qui se cachent derrière chaque site web que vous visitez.

# Le Langage des Structurations: HTML {#1}

Le HTML, acronyme de HyperText Markup Language, n'est pas simplement une suite de lettres et de symboles, mais plutôt une baguette magique numérique qui donne forme et structure à l'univers virtuel que nous connaissons. Imaginez-le comme le maçon virtuel qui assemble les blocs fondamentaux, érigeant ainsi la toile sur laquelle l'art du web se déploie.

En tant que langage de balisage, le HTML joue un rôle central en permettant aux créateurs web de définir la structure de leurs pages. Chaque balise HTML agit comme une incantation, attribuant un sens spécifique à chaque élément de contenu. Ainsi, il ne s'agit pas simplement d'une suite de lignes de code, mais d'une partition magique qui orchestre la disposition, l'organisation et la hiérarchie de chaque élément sur une page web. Sans le HTML, l'architecture même du web perdrait sa structure essentielle.

# Création de la structure d'une page HTML {#2}

La création d'une page web commence par ériger les piliers fondamentaux à l'aide du langage HTML, le langage de balisage qui donne forme à l'invisible. Suivez le guide étape par étape pour maîtriser cette première incantation.

## Étape 1 : Déclaration HTML

Chaque sort nécessite une incantation, et pour une page web, c'est la déclaration HTML qui amorce le rituel. Utilisez le code sacré suivant au sommet de votre parchemin web :

```htm
<!DOCTYPE html>
<html lang="fr">
```
Cette invocation indique au navigateur qu'une incroyable expérience web est sur le point de se dérouler. La langue utilisée (dans cet exemple, le français) sert à harmoniser les vibrations linguistiques de votre création.

## Étape 2 : En-tête de la page

Le mage prudent prépare son équipement avant de se lancer dans une quête. L'en-tête de la page, défini par la balise <head>, est l'endroit où vous placez vos outils magiques :

```htm
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titre de votre page</title>
</head>
```
- Encodage des caractères (meta charset) : Cette rune assure que votre texte s'affiche correctement, sans distorsion linguistique.
- Vision initiale (meta viewport) : Cette incantation garantit une expérience visuelle optimale, quel que soit l'appareil utilisé.
- Titre (title) : Le titre est la bannière qui flotte dans les vents mystiques des onglets du navigateur. Choisissez-la donc judicieusement.

## Étape 3 : Corps de la page

Le cœur de votre création réside dans le corps de la page, délimité par la balise <body> :

```htm
<body>
     Votre contenu va ici 
</body>
```

À l'intérieur de ce sanctuaire, vous insérerez les éléments qui donneront vie à votre page : texte, images, liens et autres artefacts magiques. Préparez-vous, car c'est ici que l'histoire commence à prendre forme.

## Étape 4 : Fermeture HTML

Enfin, ne pas oublier de refermer tout ça pour faire comprendre au navigateur que l'expérience web se termine là

```htm
</head>
```

Maintenant que les fondations mystiques de votre page sont établies, il est temps de plonger plus profondément dans le grimoire du HTML.

# Utilisation des balises essentielles (head, body, div, etc.) {#3}

Le HTML, langage de balisage fondamental pour la création de pages web, repose sur l'utilisation judicieuse de balises. Ces balises, délimitées par des chevrons(sorte de guillemets), sont les éléments de base qui structurent votre contenu. Avant de plonger dans les spécificités de chaque balise, familiarisons-nous avec leur syntaxe et leur rôle essentiel.

## Syntaxe de base d'une balise HTML :
Une balise HTML se compose généralement de deux parties :

- **Balise d'ouverture** : Débute avec le nom de la balise enveloppé entre des chevrons. Exemple : <nom_de_balise>

A titre illustratif, on retrouve: \<html>,\<head>,\<body>,\<title>
- **Balise de fermeture** : Similaire à la balise d'ouverture mais comporte une barre oblique avant le nom. Exemple : </nom_de_balise>

A titre illustratif, on retrouve: \</html>,\</head>,\</body>,\</title>

## Structure générale d'une balise :

```htm
<nom_de_balise> Contenu de la balise </nom_de_balise>
```

## Balises nécessaires

### Balise \<head> : La porte des mystères

La balise \<head> n'est pas seulement une cachette pour les outils, elle ouvre également une porte vers des dimensions cachées. Utilisez cette balise pour connecter votre page au monde extérieur sans perturber le récit principal et pour insérer des éléments cruciaux tels que  des informations [méta](https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta), des liens vers des [feuilles de style](), des [scripts](https://www.w3schools.com/html/html_scripts.asp#:~:text=The%20HTML%20%3Cscript%3E%20tag%20is%20used%20to%20define,manipulation%2C%20form%20validation%2C%20and%20dynamic%20changes%20of%20content.), et d'autres éléments qui ne sont pas directement affichés sur la page..

```htm
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="article.css"> <!--  ne fait pas attention à celui-ci pour le moment -->
    <title>Le titre ensorcelant de votre page</title>

    <!-- Autres éléments magiques vont ici -->
</head>

```


### \<html> : Racine de votre document HTML

La balise \<html> englobe l'ensemble du document HTML. C'est le point de départ de tout contenu de la page web.

```htm
<html>
   Le reste de votre contenu HTML va ici
</html>
```

### \<body> : Le corps de la magie
Tout le contenu visible de votre page, des paragraphes aux images, réside entre les balises \<body>.

```htm
<body>
  Hello, je suis le contenu de la page. Je peux être de tout genre, du simple texte aux images, en passant par des vidéos, des liens ou tout élément que vous voyez d'habitude sur une page d'un site web.
</body>
```
Comprendre ces balises essentielles est comme déchiffrer les runes d'un grimoire. Maintenant que nous avons dévoilé ces mystères, préparez-vous à forger votre propre sortilège en partant à la découverte d'autres balises à utiliser dans votre body.

## Création de la structure d'une page HTML : Façonnez votre univers en lignes de code {#4}

Maintenant que nous avons exploré les bases du HTML et des balises essentielles, plongeons dans la création concrète de la structure d'une page HTML. C'est ici que la magie opère vraiment, donnant vie à votre vision à travers des lignes de code.

### Les Titres Enchantés : \<h1>, \<h2>, \<h3>, ...

Les balises de titre \<h1>, \<h2>, \<h3>, etc., définissent la hiérarchie des titres sur votre page. \<h1> est généralement utilisé pour le titre principal, suivi de \<h2> pour les sections, et ainsi de suite.

```htm
<h1>Titre Principal</h1>
<h2>Sous-Section Enchantée</h2>
<h3>Exploration Magique</h3>
<h4>Exemples Magiques</h4>
```

### \<p> : Le paragraphe ensorcelant
Utilisée cette balise pour définir des paragraphes de texte.

```htm
<p>Ceci est un paragraphe de texte.</p>
<p>Ceci est un autre paragraphe de texte.</p>
<p>Ceci est encore un autre paragraphe de texte.</p>
```
### \<div> : La division magique
La balise \<div> est un puissant outil de structuration, permettant de regrouper des éléments et de les styliser ensemble à l'aide de CSS.

```htm
<div>
  <h2>Section 1</h2>
  <p>Contenu de la section 1.</p>
</div>

<div>
  <h2>Section 2</h2>
  <p>Contenu de la section 2.</p>
</div>
```
### \<a> : Le lien mystique
La balise <a> est utilisée pour créer des liens, que ce soit vers d'autres pages, des ressources externes, ou même des sections de la même page. 

```htm
<a href="https://www.roylab.xyz">Explorez davantage la magie du web</a>
```
Ici, href spécifie l'URL de la destination. C'est ce qu'on appelle un **[attribut](https://w3tutoriels.com/html/html-attributs/)**. En effet,les attributs sont comme des runes magiques que vous attribuez aux balises pour leur conférer des pouvoirs spécifiques. Ils sont les incantations secrètes qui intensifient le pouvoir des balises. 

### Les Images Envoûtantes : \<img> et les attributs src et alt
La balise \<img> est utilisée pour incorporer des images dans votre page. L'attribut src indique l'emplacement de l'image, tandis que l'attribut alt fournit un texte descriptif, important pour l'accessibilité et pour décrire l'image si elle ne peut pas être affichée.

```htm
<img src="image-magique.jpg" alt="Une illustration magique">
```

### La Magie des Listes : \<ul>, \<ol>, \<li>
Les balises \<ul> (liste non ordonnée) et \<ol> (liste ordonnée) vous permettent de créer des listes, tandis que \<li> définit chaque élément de la liste.

```htm
<ul>
  <li>Potion de CSS</li>
  <li>Sortilège de Flexbox</li>
  <li>Enchantement de Grid</li>
</ul>

<ol>
  <li>Introduction à HTML</li>
  <li>Exploration des balises</li>
  <li>Création de la structure</li>
</ol>
```
### Balises autofermantes 
Certaines balises n'ont pas de balise de fermeture distincte et sont autofermantes. En effet, les balises autofermantes, également appelées balises void, sont des balises HTML qui ne nécessitent pas de balise de fermeture. Elles sont utilisées pour insérer des contenus sans texte entre les balises d'ouverture et de fermeture. Voici quelques exemples courants de balises autofermantes avec leurs utilisations typiques :

\<img> : Image magique

 ```htm
<img src="image.jpg" alt="Description ensorcelante de l'image">
```
Utilisation : Sert à insérer une image enchanteresse dans votre royaume web.

\<br> : Saut de ligne ensorcelant

```htm
<p>Première incantation. <br> Deuxième incantation.</p>
```
Utilisation : Sert à tisser un sort pour créer un saut de ligne mystique à l'intérieur d'un paragraphe.

\<input> : Champ de saisie enchanté

```htm
<input type="text" name="nom" id="nom" placeholder="Votre nom enchanté">

```
Utilisation : Sert à forger un champ de saisie magique au sein d'un formulaire.

\<hr> : Ligne horizontale enchantée

```htm
<hr>
```
Utilisation : Sert à insuffler de la magie avec une ligne horizontale séparatrice.

\<meta> : Métadonnées magiques

```htm
<meta charset="UTF-8">
```

Utilisation : Sert à spécifier les métadonnées de votre page avec cette incantation, comme l'encodage des caractères.

Ces balises autofermantes, par leur nature magique, simplifient la structure du code sans avoir besoin de balises de fermeture. N'oubliez pas le trait final, symbolisé par le slash ("/"), pour compléter l'incantation.









Et voilà, en comprenant le rôle de toutes ces balises, vous êtes prêt à donner vie à votre page en créant une structure HTML solide.

Avec ces connaissances, vous avez désormais les outils nécessaires pour façonner votre univers en ligne. Dans la prochaine section, plongeons dans l'art de l'esthétique avec le CSS.

**La Magie Continue**
###### À bientôt pour de nouvelles découvertes enchanteresses !
###### *Magiquement vôtre,*
M.Royce
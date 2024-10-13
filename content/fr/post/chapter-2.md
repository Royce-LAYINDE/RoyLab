---
title: "Chapitre II: Exploration Enchantée du Web Scraping : L'Art Mystique de Collecter les Trésors Cachés du Monde Virtuel"
date: 2023-08-24T10:58:08-04:00
description: "
Explorez les mystères du Web Scraping et apprenez à collecter des données précieuses en ligne. Plongez dans l'art de l'exploration web automatisée et découvrez comment transformer votre navigateur en une baguette magique pour extraire des informations cachées. Découvrez les rituels du Web Scraping avec Python, et devenez un apprenti mage capable d'explorer les profondeurs du cyberespace pour des trésors d'informations. "
featured_image: "/images/web.jpg"
omit_header_text: true
tags: ["python","web scraping","coding"]
disable_share: false   #Pour que les visiteurs puissent partager la page
---
Mis à jour le 01/09/2023

*Temps de Lecture Estimé: Environ 7 à 11 minutes*


Bienvenue, cher apprenti mage du numérique, dans une nouvelle aventure au cœur du monde virtuel où les données se cachent tels des trésors dissimulés, attendant d'être découverts par des esprits curieux comme le vôtre. Dans ce récit, nous allons plonger dans l'art mystérieux du Web Scraping, une magie qui nous permet de collecter des données précieuses à partir du tissu même du web.

## Table des matières
- [La Baguette Magique du Web Scraping](#1)
- [Les Formules Enchanteresses : Bibliothèques Python et Outils de Scraping](#2)
- [Les Sorts de Sélection : Cibler les Trésors Cachés](#3)
- [La Transmutation des Données : De l'Invisible au Visible](#4)
- [Les Limites Éthiques : Un Code de Conduite Magique](#5)
- [Importer les Bibliothèques Magiques](#6)
- [Préparer la Potion Magique (URL)](#7)
- [Lancer le Sort d'urllib.request](#8)
- [Utiliser Beautiful Soup pour Lire les Runes](#9)
- [Explorer les Mystères du Code HTML](#10)
- [Manipuler les Résultats](#11)
- [Conclusion : Révéler les Mystères Cachés](#12)

# La Baguette Magique du Web Scraping {#1}

Imaginez-vous tenant entre vos mains une baguette magique virtuelle, une baguette capable de parcourir les recoins du monde virtuel, d'extraire des informations cachées dans les pages web et de les assembler pour créer une vision plus riche et informée de notre univers en ligne. C'est exactement ce que le Web Scraping nous permet de faire. Telle une incantation, cette technique nous ouvre les portes des trésors de données en ligne, nous permettant de les collecter et de les transformer en une forme que nous pouvons explorer et analyser.

# Les Formules Enchanteresses : Bibliothèques Python et Outils de Scraping {#2}

Pour maîtriser l'art du Web Scraping, nous devons d'abord invoquer nos outils magiques. Dans notre quête de révéler les trésors enfouis au cœur des pages web, nous faisons appel à des bibliothèques Python spéciales, qui sont nos alliées pour décrypter les arcanes du code source et extraire des données précieuses. Tout comme un grimoire ancien renferme des sorts puissants, ces bibliothèques tels que [Beautiful Soup](https://wiki.python.org/moin/beautiful%20soup) et [Requests](https://docs.python.org/3/library/urllib.request.html) nous confèrent le pouvoir de déchiffrer le langage cryptique du HTML et de révéler les secrets cachés dans chaque balise.

Imaginez ces bibliothèques comme des baguettes magiques, prêtes à exécuter vos commandes avec précision. Beautiful Soup, par exemple, agit comme un enchantement de compréhension, permettant de parcourir les éléments HTML avec aisance et d'extraire les informations qui nous intéressent. Quant à Requests, c'est un sort d'invocation de pages web, nous permettant d'accéder à leur contenu pour le manipuler selon notre désir.

Comme des mages anciens qui étudient et maîtrisent les formules de la magie, nous explorons ces bibliothèques, apprenons leurs incantations et les intégrons dans nos rituels de Web Scraping. Avec ces outils à notre disposition, nous sommes prêts à entrer dans l'arène numérique, où les pages web se transforment en scènes de nos exploits magiques.

# Les Sorts de Sélection : Cibler les Trésors Cachés {#3}
Chaque apprenti mage doit apprendre les formules de base, et dans le Web Scraping, les sélecteurs CSS sont nos sorts. Ils agissent comme des incantations ciblées, nous permettant de localiser et d'extraire précisément les éléments qui nous intéressent sur une page web. Grâce à ces sorts, nous pouvons identifier et extraire des images, des textes, des liens et même des données structurées, tout comme un alchimiste transformant des ingrédients bruts en potions magiques.

Imaginez que vous vous tenez devant une page web, votre baguette magique du Web Scraping prête à être utilisée. Vous prononcez le sélecteur CSS approprié, et soudain, les éléments que vous recherchez se révèlent à vous. Que ce soit un titre accrocheur, une liste d'articles, des images éblouissantes ou même des données de tableaux, les sélecteurs CSS sont vos sorts pour cibler ces trésors cachés.

Par exemple, si vous explorez un site d'actualités, vous pourriez utiliser un sélecteur CSS pour extraire les titres des articles. Si vous vous trouvez sur une page de recettes de cuisine, vous pourriez utiliser un autre sort pour saisir les listes d'ingrédients et les étapes de préparation. Même les images peuvent être révélées grâce à ces sorts magiques. Vous pouvez extraire des images pour les afficher dans votre propre grimoire numérique ou pour créer des illustrations dans vos propres créations.

Les sélecteurs CSS sont puissants, mais ils nécessitent de la précision. Comme un enchanteur minutieux, vous devez choisir le bon sort pour chaque trésor que vous recherchez. Cela signifie comprendre la structure de la page, identifier les balises et les classes appropriées, et formuler vos sorts avec soin. Mais une fois que vous maîtrisez ces sorts de sélection, vous avez le pouvoir de révéler et de collecter les éléments précieux qui vous permettront d'enrichir vos propres créations.

Maintenant que nous avons appris à cibler et à extraire des éléments spécifiques, il est temps de révéler le véritable secret de l'art du Web Scraping:  la transmutation des données. Dans le monde de la magie du Web Scraping, nous ne nous contentons pas de collecter des données, nous les transformons et les transmutons en informations précieuses. Rejoignez-moi dans la prochaine section pour découvrir comment nous pouvons utiliser notre magie pour changer l'invisible en visible, le brut en raffiné, et le chaos en clarté.


# La Transmutation des Données : De l'Invisible au Visible {#4}
Tout comme un alchimiste transmute des métaux en or, nous transformons les données brutes en informations précieuses grâce à notre magie du Web Scraping. Nous collectons des fragments d'informations éparpillés sur plusieurs pages web et les transmutons en données structurées que nous pouvons analyser et exploiter. C'est ainsi que nous révélons la vraie puissance de notre art, en transformant le chaos en clarté.

Imaginez que vous ayez collecté des données à partir de différentes sources, comme un alchimiste rassemblant des ingrédients rares et précieux. Ces données peuvent être dans des formats variés, parfois désorganisées et difficiles à comprendre. Cependant, avec nos sorts de transmutation, nous pouvons les purifier et les transformer en quelque chose de significatif.

Par exemple, supposons que vous ayez collecté des informations sur les préférences musicales de différentes personnes à partir de différents sites web. Ces données pourraient être dans des formats différents, tels que des listes, des paragraphes ou même des tableaux. À l'aide de nos sorts de transmutation, nous pouvons harmoniser ces données, les organiser en une structure cohérente et les présenter de manière lisible.

Les sorts de transmutation peuvent également nous permettre de convertir les données brutes en formats plus utiles. Par exemple, nous pourrions transformer des dates en formats standard, convertir des mesures en unités familières ou même traduire du texte dans différentes langues. Tout comme un alchimiste qui maîtrise l'art de la transformation des substances, nous maîtrisons l'art de la transformation des données.

Mais attention, tout comme les alchimistes doivent connaître les propriétés des substances qu'ils transmutent, nous devons avoir une compréhension solide des données que nous manipulons. Cela nous permet de choisir les sorts de transmutation appropriés et d'éviter de fausser les informations. En respectant ces règles, nous pouvons transformer des données brutes en connaissances précieuses, prêtes à être utilisées pour prendre des décisions éclairées.

Ainsi, grâce à notre magie du Web Scraping, nous ne sommes plus limités à simplement collecter des données. Nous sommes des alchimistes numériques, capables de transmuter ces données en informations utiles et significatives. Avec chaque incantation de transmutation, nous apportons de la clarté à l'obscurité, de l'ordre au chaos et de la signification à la confusion. 

# Les Limites Éthiques : Un Code de Conduite Magique {#5}

Comme tout praticien de la magie, nous devons suivre un code de conduite éthique. Dans le monde du Web Scraping, cela signifie respecter les règles établies par les propriétaires des sites web que nous explorons. Notre magie doit être utilisée avec responsabilité et prudence, en évitant de perturber ou d'endommager les sites que nous visitons.

# Expérimentation du sort

Maintenant que nous avons exploré les mystères de la transmutation des données, il est temps de jeter un pont entre ces concepts abstraits et la réalité concrète du Web Scraping. Pour éclairer notre chemin, plongeons dans un exemple pratique qui mettra en lumière les sorts que nous avons appris jusqu'à présent. Rejoignez-moi dans la section suivante pour découvrir comment nous pouvons appliquer notre magie du Web Scraping pour extraire des informations spécifiques d'une page web réelle.

## Préparation : Importer les Bibliothèques Magiques {#6}

Tout comme un magicien a besoin de sa baguette pour lancer des sorts, nous avons besoin de nos bibliothèques Python pour scraper des pages web. Pour cette quête, nous allons utiliser deux puissantes bibliothèques : Beautiful Soup et urllib.request.
```python
import urllib.request
from bs4 import BeautifulSoup
```
Beautiful Soup agira comme notre œil magique, analysant et naviguant à travers le code source de la page web. Urllib.request, quant à lui, sera notre invocation pour accéder à la page et obtenir son contenu.

## Préparer la Potion Magique (URL) {#7}

Tout commence par l'URL de la page que nous voulons scraper. C'est comme choisir une destination pour notre voyage. Par exemple, si nous voulons extraire des informations sur un article d'un blog, nous utilisons l'URL de la page menant à cet article. 
```python
# L'URL de la page à explorer
url = "https://roylab.netlify.app/fr/first"
```
## Lancer le Sort d'urllib.request {#8}
Notre première formule magique consiste à invoquer urllib.request pour obtenir le contenu de la page. Nous utilisons le sort urllib.request.urlopen() pour ouvrir la porte virtuelle vers la page et obtenir sa réponse.
```python
doc = urllib.request.urlopen(url)  # Invoquer la page avec notre sort d'invocation (urllib)
```
## Utiliser Beautiful Soup pour Lire les Runes {#9}
Une fois que nous avons obtenu la réponse de la page, nous devons la passer à notre œil magique, Beautiful Soup. Il l'analysera et créera une structure d'objet que nous pouvons interroger pour obtenir les informations que nous cherchons.
```python
contenu = BeautifulSoup(doc, "html.parser")   # Utilisation de Beautiful Soup pour analyser le contenu HTML de la page
```
Ici, BeautifulSoup() prend en argument la réponse de la page (doc) et ce qu'on appelle un parseur html. Un [Parseur HTML](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#parser-installation) est  un programme qui analyse un code HTML et le transforme en une structure de données que nous pouvons manipuler en Python. Dans ce cas, "html.parser" est un parseur intégré à la bibliothèque standard de Python, et il est utilisé pour analyser le contenu HTML de la page web. 

On pourrait s'en arrêter là et continuer notre expérimentation mais il y a bien longtemps, [*mon mentor des arcanes Python*](https://nskm.xyz/about/) me révéla qu'il était sage d'enregistrer les traces magiques d'une page ensorcelée, car cette page pourrait disparaître comme par enchantement ou changer telle une métamorphose.
Alors, nous allons donc suivre son conseil et ajouter à notre programme, un code qui se chargera de sauvegarder le contenu html de notre page dans le cas où nous en aurions besoin plus tard. 
```python
contenu_html = contenu.prettify()   # Obtenir le contenu HTML formaté

# Sauvegarder le contenu HTML dans un fichier
nom_du_fichier = "page.html"
with open(nom_du_fichier, "w", encoding="utf-8") as file:
    file.write(contenu_html)

print(f"✨ Le contenu HTML de la page a été sauvegardé dans '{nom_du_fichier}'")
```
Ici, la méthode .prettify() est utilisée pour formater joliment le contenu HTML en ajoutant des indentations et des sauts de ligne pour une lecture humaine plus facile. Ensuite, nous utilisons simplement la méthode open() pour créer et écrire dans un fichier.

## Explorer les Mystères du Code HTML {#10}
Maintenant que nous avons invoqué Beautiful Soup, nous pouvons plonger dans le code HTML de la page. Comme un aventurier explorant une caverne mystérieuse, nous utilisons les compétences de Beautiful Soup pour trouver les éléments et les données qui nous intéressent.
```python
links = contenu.find_all("a")  # Trouver tous les éléments <a> qui contiennent des liens
title = contenu.find("h1").text    # Trouver le titre de l'article avec notre sort de divination 
```
Pour cette étape nous aurions pu aussi faire appel aux [regex](https://docs.python.org/3/library/re.html), cette magie incantatoire dont nous parlerons certainement dans un autre grimoire.

# Manipuler les Résultats {#11}
Une fois que nous avons trouvé les informations, nous pouvons les manipuler à notre guise. Nous pouvons les afficher à l'écran, les enregistrer dans un fichier ou les utiliser pour créer quelque chose de nouveau.
```python
# Ici, on souhaite afficher l'intégralité des liens sécurisés trouvés sur notre page avec un geste d'enchantement
print("🔮 Voici la liste des liens sécurisés trouvés sur cette page:")
for link in links:
    href = link.get("href")     # Extraire l'attribut "href" de la balise <a> pour obtenir le lien
    if href and href.startswith("https"):   # Filtrer les liens pour ne prendre en compte que ceux commençant par "https"
        print(href)

# Afficher le titre de l'article pour captiver l'attention
print(f"📜 Titre de l'article : {title}")
```
# Conclusion : Révéler les Mystères Cachés {#12}

Voilà, nous avons accompli notre quête et révélé les mystères cachés derrière une page web en utilisant Python et les pouvoirs de Beautiful Soup et urllib.request. Comme des apprentis sorciers découvrant les secrets d'un sortilège, nous avons appris à naviguer dans le code HTML et à extraire des informations précieuses.

Maintenant, c'est à vous de devenir l'explorateur intrépide du monde en ligne. Utilisez vos compétences nouvellement acquises en Web Scraping pour découvrir les trésors cachés du Web et explorer les connaissances enfouies derrière chaque URL. Que chaque ligne de code que vous écrivez soit une incantation puissante pour dévoiler les mystères du numérique. À vous de jouer, jeune apprenti mage !

**La Magie Continue**

*Ne laisse pas ta baguette magique rouillée*

Renforce ton savoir [ici](https://docs.python.org/3/library/urllib.request.html) et [ici](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

Découvre [ici](https://github.com/Royce-LAYINDE/Royce-s-Programs/blob/master/Python/scrapping%20d'un%20site%20de%20vente%20de%20livres.py), [ici aussi](https://github.com/Royce-LAYINDE/Royce-s-Programs/blob/master/Python/scraping%20de%20la%20page%20d'article.py)

🧙‍♂️🔮🌐📜

###### Dans cette quête de connaissances cachées, que chaque ligne de code soit pour vous une incantation, chaque page web un grimoire et chaque donnée collectée un trésor précieux. Que votre curiosité vous guide alors que nous levons le voile sur les mystères du Web Scraping, une magie qui nous permet de découvrir le monde numérique sous un nouvel éclairage. *À vous de jouer, jeune apprenti mage !*

###### À bientôt pour de nouvelles découvertes enchanteresses !

###### *Magiquement vôtre,*

M.Royce
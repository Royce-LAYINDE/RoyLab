---
title: "Chapitre III: Décoder et Encoder des QR Codes en Python : L'Art des Apprentis Enchanteurs"
date: 2023-09-06T10:58:08-04:00
description: "Explorez les secrets de l'encodage et du décodage de QR codes grâce à la magie de Python. Plongez dans l'art fascinant de la création et de la lecture de ces parchemins numériques et découvrez comment faire de votre ordinateur une baguette magique capable de générer des codes mystérieux et de révéler les messages cachés en un instant. Plongez dans les rituels de codage et de décodage des QR codes avec Python, et devenez un apprenti enchanteur capable de manipuler ces symboles numériques pour communiquer des informations secrètes ou créer des portails interactifs vers le monde numérique. Votre aventure dans l'univers des QR codes commence ici, alors préparez-vous à explorer un nouveau monde de possibilités magiques."
featured_image: "/images/qrcode1.png"
omit_header_text: true
tags: ["python","qr code","coding"]
disable_share: false   #Pour que les visiteurs puissent partager la page

---
Bienvenue, chers apprentis enchanteurs, dans une nouvelle aventure au cœur du monde numérique, où les QR codes se présentent comme de mystérieux parchemins. 

Mis à jour le 07/09/2023

*Temps de Lecture Estimé: Environ 6 à 10 minutes*

## Table des matières
- [QR Codes : Porteurs de Mystères Numériques](#1)
- [L'Encodage des QR Codes : Tisser la Toile Magique](#2)
- [L'Encodage Simple : Un Premier Pas](#3)
- [Un QR Code en Couleur : Une Touche d'Éclat](#4)
- [Le Décodage des QR Codes : L'Art de la Divination](#5)
- [Le Décodage Simple : Révéler les Secrets](#6)
- [Le Décodage Simple : Déchiffrer les Secrets](#7)
- [Conclure notre Aventure Magique](#8)

# QR Codes : Porteurs de Mystères Numériques {#1}
Les QR codes, abrégés de l'anglais "Quick Response" (Réponse Rapide), sont comme des parchemins magiques du monde numérique. Ce sont des images bidimensionnelles qui renferme un pouvoir énigmatique : la capacité de stocker et de transmettre des informations secrètes. Leur apparence, telles des caractères d'un vieux grimoire, forment un code qui peut être décrypté par des apprentis mages numériques. Dans cet univers de "techno magie", les QR codes servent de portails vers un monde de données et d'informations cachées.

Ces codes numériques ont une utilité versatile. Ils peuvent contenir des liens vers des sites web, des informations de contact, des messages, ou même des données structurées telles que des numéros d'identification. Tout comme un sac magique, les QR codes peuvent transporter une variété infinie d'informations dans un espace restreint. C'est pourquoi ils sont devenus des alliés précieux dans le monde numérique, servant à des fins aussi variées que la publicité, la gestion de l'inventaire, la billetterie, et bien plus encore.

En somme, les QR codes sont comme des sortilèges numériques, capables de révéler des connaissances cachées d'un simple coup d'œil. À travers leur mystérieuse structure, ils renferment des trésors d'informations, prêts à être découverts par ceux qui possèdent la clé de leur déchiffrement.

Dans notre quête, nous allons explorer l'art de l'encodage et du décodage de ces codes magiques en utilisant Python.

# L'Encodage des QR Codes : Tisser la Toile Magique {#2}

Notre première étape consiste à apprendre l'art de l'encodage, qui nous permet de créer nos propres QR codes. Pour ce faire, nous allons invoquer la bibliothèque qrcode. Assurez-vous de la préparer en utilisant le sortilège suivant :
```python
pip install qrcode
```
## L'Encodage Simple : Un Premier Pas {#3}

Pour créer un QR code simple, récitons cette formule magique :
```python
#Après son installation nous allons maintenant procéder à l'importation de notre bibliothèque
import qrcode   
# On stocke ensuite dans une variable le message à inscrire dans le QR code
message = "Mon premier QR code en tant qu'apprenti mage sur @RoyLab "   
# On va maintenant générer notre QR code grâce à la méthode .make()
img = qrcode.make(message)
# On enregistre enfin le QR code en tant qu'image grâce à la méthode .save() qui prendra en argument le nom de notre QR code suivi de l'extension de l'image
img.save('myfirst_qrcode.png')
```
Ce sort générera un QR code avec le message désiré et le sauvegardera sous forme d'image nommée myfirst_qrcode. 
![myfirst_qrcode](/images/myfirst_qrcode.png)

Vous pouvez ensuite partager cette image avec d'autres aventuriers pour qu'ils la scannent avec leur téléphone par exemple.

NB: L'image sera sauvegarder dans le dossier courant, c'est-à-dire celui dans lequel vous exécutez votre script. Pour l'enregistrer ailleurs, vous devez renseigner le chemin d'accès du dossier. Exemple: 
```python
img.save('/home/nomutilisateur/myfirst_qrcode.png') #Pour les mages de la maison Linux
img.save('C:/Users/Me/Images/myfirst_qrcode.png')   #Pour les mages de la maison Windows
```
## Un QR Code en Couleur : Une Touche d'Éclat {#4}

Si vous souhaitez ajouter une touche de couleur à vos QR codes, nous pouvons utiliser la magie supplémentaire de qrcode[pil]. Assurez-vous de l'installer en utilisant cette formule :
```python
pip install qrcode[pil]
```
Voici comment créer un QR code coloré :
```python
import qrcode
message = "Mon premier QR code coloré en tant qu'apprenti mage sur @RoyLab "   
# On "peut" décider de créer un parchemin QR code personnalisé en modifiant certaines de ses caractéristiques
qr = qrcode.QRCode(
    version=2,  # La version du QR code
    box_size=10,  # La taille des cases
    border=5  # La taille de la bordure
)
# On ajoute ensuite le message à inscrire dans le QR code
qr.add_data(message)
# On enchante le parchemin pour qu'il prenne vie
qr.make(fit=True)
# On va créer maintenant une image en couleur
img = qr.make_image(fill_color='black', back_color='green')
# On enregistre enfin l'image colorée
img.save('qrcodecolore.png')

```
![myfirst_qrcode](/images/qrcodecolore.png)

NB:
- L'argument **fit=True** dans la méthode "qr.make(fit=True)" est utilisé pour indiquer à la bibliothèque qrcode de faire en sorte que le QR code s'adapte automatiquement à la quantité de données que vous avez ajoutées. En d'autres termes, si vos données sont trop longues pour tenir dans un QR code de taille standard, cette option permettra au QR code d'augmenter sa taille pour accommoder toutes les données, sans dépasser les limites autorisées pour un QR code de cette [version](https://fr.wikipedia.org/wiki/Code_QR#Versions).
- **fill_color**: C'est la couleur de remplissage des parties actives du QR code, c'est-à-dire des parties qui portent l'information. Dans l'exemple, la couleur de remplissage est définie sur 'black', ce qui signifie que les parties actives du QR code seront de couleur noire.
- **back_color**: C'est la couleur de fond du QR code, c'est-à-dire la couleur de l'arrière-plan qui entoure les parties actives. Dans l'exemple, la couleur de fond est définie sur 'green', ce qui signifie que l'arrière-plan du QR code sera de couleur verte.

**Attention**: Bien que l'envie de jouer avec les couleurs peut sembler très forte par souci de personnalisation du QR code, il est primordial de ne pas être extravaguant dans le choix des couleurs et dans leur association. Mieux vaut partir sur des couleurs contrastées ou préférer le traditionnel Black & White. Plus de conseils [ici](#0)

# Le Décodage des QR Codes : L'Art de la Divination {#5}

Maintenant que nous maîtrisons l'encodage, passons à l'art fascinant du décryptage. Pour cela, nous utiliserons les sorts pyzbar et Pillow. Avant de poursuivre votre quête, assurez-vous de les avoir invoqués en utilisant les sorts suivants :
```python
pip install pyzbar
pip install pillow
```
## Le Décodage Simple : Révéler les Secrets {#6}
Voici comment vous pouvez décoder un QR code à partir d'une image simple :
```python
from pyzbar.pyzbar import decode
from PIL import Image
# Ouvrir l'image contenant le QR code
img = Image.open('myfirst_qrcode.png')
# Utiliser la divination pour extraire les secrets
resultat = decode(img)
# Révéler les découvertes
print(resultat)
```
Ce sortilège ouvrira l'image du QR code que vous avez spécifiée, extraira les données qu'elle contient, et vous révèlera les secrets à l'écran. On aura alors un résultat semblable à celui-ci:
> [Decoded(data=b"Mon premier QR code en tant qu'apprenti mage sur @RoyLab ", type='QRCODE', rect=Rect(left=40, top=40, width=330, height=330), polygon=[Point(x=40, y=40), Point(x=40, y=369), Point(x=370, y=370), Point(x=369, y=40)], quality=1, orientation='UP')]



Il convient de dire que ce résultat n'est pas très évocatoire. Rendons le plus compréhensible.
## Le Décodage Simple : Déchiffrer les Secrets {#7}
Pour ce faire, il suffit de parcourir le résultat obtenu afin d'y extraire les caractéristiques du QR code:

```python
for information in resultat:
    # Extraire et afficher le type du code (généralement 'QRCODE')
    code_type = information.type
    print(f"Type de code : {code_type}")
    # Extraire et afficher les données du code
    data = information.data.decode('utf-8')  # Décode les données du code QR
    print(f"Données du code : {data}")
    # Extraire et afficher la taille du QR code (en pixels)
    rect = information.rect  # Récupérer les coordonnées du rectangle du code QR
    width = rect.width  # Largeur du rectangle
    height = rect.height  # Hauteur du rectangle
    print(f"Taille du code (en pixels) - Largeur : {width}, Hauteur : {height}")
    # Extraire et afficher la qualité du décodage
    qualite_decodage = information.quality
    print(f"Qualité de décodage : {qualite_decodage}")
    # Extraire et afficher l'orientation du QR code'
    code_orientation = information.orientation
    print(f"Orientation du qr code : {code_orientation}")
```
En ajoutant ce bout de code au code précédent, nous allons pouvoir révéler les mystères qui se cachaient dans le QR code qu'on cherchait à décoder.
> Type de code : QRCODE

> Données du code : Mon premier QR code en tant qu'apprenti mage sur @RoyLab

> Taille du code (en pixels) - Largeur : 330, Hauteur : 330

> Qualité de décodage : 1

> Orientation du qr code : UP

NB: 
- **quality** : Cet attribut représente la qualité du décodage du QR code. Il peut avoir différentes valeurs numériques qui indiquent à quel point le décodage a été réussi. Les valeurs possibles incluent généralement 0, 1, 2, etc., où 0 représente une qualité de décodage faible et une valeur plus élevée  indique une meilleure qualité de décodage.
- **orientation** : Cet attribut indique l'orientation du QR code. Dans notre exemple, il est défini sur 'UP', ce qui signifie que le QR code est orienté vers le haut, c'est-à-dire qu'il est dans la position standard sans rotation. Cependant, il existe d'autres valeurs possibles, telles que 'RIGHT', 'DOWN', 'LEFT', qui indiqueraient si le QR code a été détecté dans une orientation différente, comme tourné vers la droite, vers le bas ou vers la gauche.

# Conclure notre Aventure Magique {#8}
Comme tout bon apprenti enchanteur, vous avez désormais en votre possession les connaissances essentielles pour créer et décoder des QR codes en Python. L'art de l'encodage et du décodage de ces mystérieux parchemins numériques n'aura bientôt plus de secrets pour vous.

Toutefois, n'oubliez jamais que la magie doit être utilisée avec responsabilité et prudence. Assurez-vous de respecter les lois et les règles concernant l'utilisation des QR codes, notamment en matière de protection de la vie privée et de sécurité des données.

L'aventure continue, jeunes enchanteurs ! Vous pouvez maintenant personnaliser vos QR codes, les intégrer dans vos projets magiques, ou même les utiliser pour créer des liens interactifs vers des informations en ligne. Le monde numérique est vaste et rempli de possibilités, alors n'ayez pas peur d'explorer et d'expérimenter de nouvelles incantations.


Restez à l'écoute pour de nouvelles incantations technologiques et des découvertes captivantes ! 📚🔮🌐

**La Magie Continue**
### Conseils sur la personnalisation de QR code {#0}
- Contraste: Assurez-vous qu'il y a un bon contraste entre la couleur de l'arrière-plan (back_color) et la couleur de remplissage (fill_color) pour que le QR code soit facilement lisible. Par exemple, le noir sur le blanc ou le blanc sur le noir fonctionnent bien en termes de contraste.

- Couleurs vives: Les couleurs vives, comme le rouge, le bleu, le vert ou le jaune, sont souvent un bon choix pour attirer l'attention. Cependant, elles doivent être utilisées avec parcimonie pour ne pas rendre le QR code illisible.

- Évitez les couleurs similaires: Évitez d'utiliser des couleurs qui se ressemblent trop pour l'arrière-plan et le remplissage, car cela peut rendre le QR code difficile à décoder.

- Testez votre QR code: Avant de publier ou d'imprimer un QR code, assurez-vous de le tester avec différents lecteurs de QR code et sur différents appareils pour vous assurer qu'il est bien lisible.

- Adaptez au contexte: Choisissez des couleurs qui s'intègrent bien dans le contexte de votre utilisation du QR code. Par exemple, si vous l'intégrez sur une affiche ou un document, assurez-vous qu'il s'harmonise visuellement.

*Ne laisse pas ta baguette magique rouillée*

Explorez [ici](https://pypi.org/project/qrcode/) pour en savoir plus sur la bibliothèque qrcode, et [ici](https://pypi.org/project/pyzbar/) pour explorer pyzbar.

Découvrez les pouvoirs [ici](https://github.com/lincolnloop/python-qrcode) et [ici](https://github.com/NaturalHistoryMuseum/pyzbar) pour les incantations plus avancées.

🧙‍♂️🔮🌐📜

###### Dans cette aventure enchantée, que chaque QR code que vous créez soit une invitation à la découverte, un lien vers des connaissances cachées, ou un moyen de partager votre magie avec le monde. À vous de jouer, jeunes enchanteurs !

###### À bientôt pour de nouvelles découvertes enchanteresses !
###### *Magiquement vôtre,*
M.Royce
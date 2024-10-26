---
title: "Trucs & Astuces 1 : Enregistrer des contacts à partir d'un fichier Excel sur votre téléphone"
date: 2024-10-26T10:58:08-04:00
description: "Dans cet article, plongez dans une situation courante où des contacts d'entreprise, éparpillés dans un fichier Excel, doivent être transférés rapidement vers un téléphone. Avec un peu de magie Python, découvrez comment transformer un fichier de contacts en un format VCF prêt à l’emploi. Vous y trouverez une solution simple et rapide qui vous épargne les saisies manuelles et facilite la gestion de vos contacts."
featured_image: "/images/contact.jpg"
omit_header_text: true
tags: ["Trucs & Astuces","Python","automatisation","VCF","vCard","contacts",]
disable_share: false 
---

Imaginez la scène : vous êtes en entreprise, et votre patron vous demande de transférer tous les contacts de clients, qui se trouvent dans un fichier Excel (ou CSV, ou même TXT), vers son téléphone. C'est une demande qui semble simple, mais qui peut rapidement devenir une corvée, surtout si le fichier contient des dizaines, voire des centaines de noms et numéros à saisir un par un. Pas de panique ! Cet article vous dévoile une méthode magique pour accomplir cette tâche facilement grâce à Python et au format VCF, la clé pour importer vos contacts dans votre téléphone en un rien de temps.

## Table des matières
- [Problématique](#problématique)
- [Solution proposée](#solution-proposée)
  - [Étape 1 : Convertir le fichier Excel en fichier CSV](#étape-1--convertir-le-fichier-excel-en-fichier-csv)
  - [Étape 2 : Comprendre les fichiers VCF et vCard](#étape-2--comprendre-les-fichiers-vcf-et-vcard)
  - [Étape 3 : Créer un fichier VCF à partir du fichier CSV](#étape-3--créer-un-fichier-vcf-à-partir-du-fichier-csv)
  - [Étape 4 : Importer le fichier VCF sur votre téléphone](#étape-4--importer-le-fichier-vcf-sur-votre-téléphone)
- [Résultats obtenus](#résultats-obtenus)
- [Conclusion](#conclusion)


# Problématique

Transférer des informations de contact peut sembler être un véritable casse-tête, surtout lorsque vous devez le faire rapidement. Comment extraire efficacement des données d'un fichier Excel ? Quel format choisir pour assurer une importation sans faille sur un smartphone ? Et surtout, comment éviter de perdre un temps précieux à saisir chaque contact manuellement ?

# Solution proposée

Pour résoudre ce problème, nous allons transformer votre fichier contenant les contacts en un fichier VCF, un format standard qui permet aux applications de gestion de contacts de lire et d'importer facilement les informations. Si votre fichier est déjà en format CSV, parfait ! Sinon, pas de souci, nous allons le convertir. Dans tous les cas, notre solution s'appuie sur le format CSV, que ce soit pour extraire des données d'un fichier Excel ou pour créer le fichier final.

## Étape 1 : Convertir le fichier Excel en fichier CSV

Si vous avez votre fichier Excel prêt, voici comment procéder pour le convertir en CSV :

Ouvrez le fichier Excel.
Cliquez sur "Fichier" > "Enregistrer sous".
Choisissez "CSV (Comma delimited) (*.csv)" comme format de fichier.
Si vous avez déjà un fichier CSV, vous pouvez passer directement à la suite. Voilà, c'est simple comme bonjour !

## Étape 2 : Comprendre les fichiers VCF et vCard

Le format VCF (Virtual Contact File) est le champion des informations de contact. C'est un fichier contient des vCards, qui sont de véritables cartes de visite numériques. Avec ce format, votre téléphone pourra reconnaître et importer les contacts sans aucun souci.

***Qu’est-ce qu’une vCard ?***

Une vCard (ou Virtual Card) est une carte de visite virtuelle qui contient les informations de base d'un contact : nom, numéro de téléphone, adresse, email et bien plus encore. Les vCards sont stockées dans des fichiers avec l'extension <mark>.vcf</mark>, ce qui leur permet d’être facilement partagées et reconnues par de nombreux appareils et applications.

**Structure d’une vCard**

Chaque vCard dans un fichier VCF est structurée en plusieurs lignes, chacune contenant une information spécifique du contact, avec des balises prédéfinies. Voici un exemple de vCard simple pour mieux comprendre la structure :

```console
BEGIN:VCARD
VERSION:3.0
N:M;Royce;;;
TEL:000000
EMAIL:royce@roylab.xyz
END:VCARD
```
- **BEGIN et END** : Délimitent le début et la fin de chaque carte de contact.

- **VERSION** : Indique la version de la vCard, ici 3.0, compatible avec la plupart des appareils modernes.

- **N** : Contient le nom du contact. La structure suit le format Nom;Prénom.

- **TEL** : Contient le numéro de téléphone du contact.
  
- **EMAIL (facultatif)** : Enregistre l'email du contact si besoin.

Ces éléments peuvent varier et inclure des informations supplémentaires (comme l'adresse, le nom de l'entreprise, etc.), mais les éléments de base que nous utiliserons pour notre cas sont le nom et le numéro de téléphone.

En utilisant cette structure, notre script Python va parcourir chaque contact dans le fichier CSV et générer une vCard pour chacun, en respectant ce format.

## Étape 3 : Créer un fichier VCF à partir du fichier CSV

Maintenant, place au cœur de la magie : créer un fichier VCF à partir de votre fichier CSV à l'aide d'un petit script Python. Voici comment cela fonctionne :

- ***Ouvrir le fichier CSV*** : Nous allons lire le fichier contenant nos contacts. Chaque ligne correspond à un contact.

- **Extraire les données** : On va séparer chaque ligne pour obtenir le nom, le prénom et le numéro de téléphone.
  
- **Construire la vCard** : Pour chaque contact, on crée une vCard, qui est un simple ensemble de lignes décrivant les informations de contact.
Écrire dans un fichier VCF : Enfin, on regroupe toutes les vCards et on les écrit dans un fichier VCF.

Voici le code correspondant :

```python
# -*- coding: utf-8 -*-
"""
author: M.Royce
"""
# On stocke le chemin du fichier CSV contenant les contacts
fichier_contacts = "contacts.csv" 
#Ici notre fichier se nomme contacts.csv et se trouve dans le répertoire courant
#On pouvait aussi mettre le chemin complet (Ex: C:/Mypc/Documents/contacts.csv)

# Initialisation de la variable qui contiendra toutes les vCards
listes_de_tous_les_contacts = ""

# Ouverture du fichier CSV en mode lecture
with open(fichier_contacts, "r") as contacts_file:
    for ligne in contacts_file:
        # Séparation de la ligne en prénom, nom et numéro en utilisant la virgule comme séparateur
        nom, prenom, numero = ligne.strip().split(",")
        
        # Création du contenu d'une vCard pour le contact actuel
        contenu_d_un_contact = f"BEGIN:VCARD\nVERSION:3.0\nN:{prenom};{nom};;;\nTEL:{numero}\nEND:VCARD\n"
        
        # Ajout du contenu de la vCard au contenu global
        listes_de_tous_les_contacts += contenu_d_un_contact

# Chemin du fichier où nous allons écrire les vCards
filename = "all_contacts.vcf"

# Ouverture du fichier en mode écriture et écriture du contenu des vCards
with open(filename, "w") as vcf_file:
    vcf_file.write(listes_de_tous_les_contacts)  # Écriture des vCards dans le fichier

```

## Étape 4 : Importer le fichier VCF sur votre téléphone

Une fois que vous avez créé votre fichier VCF, il est temps de l'importer sur votre téléphone. Pas de panique, il existe plusieurs moyens pour cela :

- Câble USB : Connectez votre téléphone à votre ordinateur et transférez le fichier directement.
  
- Bluetooth : Envoyez le fichier via Bluetooth si vous êtes dans un rayon de proximité.
  
- Email : Envoyez-vous le fichier par email et ouvrez-le sur votre téléphone.
  
- Services Cloud : Utilisez Google Drive, Dropbox ou tout autre service de cloud pour accéder facilement au fichier.
  
Après avoir transféré le fichier, il vous suffit de l'ouvrir sur votre téléphone :

- Sur Android : Accédez à l'application Contacts, allez dans les paramètres et choisissez **"Importer/Exporter"**, puis **"Importer à partir du fichier .vcf"**.

- Sur iPhone : Ouvrez le fichier VCF depuis l'application Mail et choisissez **"Ajouter tous les contacts"**.

# Résultats obtenus

Grâce à ce processus, vous avez réussi à enregistrer vos contacts sans effort. Fini les corvées à entrer chaque contact manuellement, vous pouvez désormais le faire en quelques clics.

# Conclusion

En résumé, il n’est pas nécessaire de se laisser submerger par des tâches répétitives. Vous voilà armé d'une méthode efficace pour gérer vos contacts comme un pro ! En automatisant cette tâche, vous gagnez un temps précieux que vous pouvez consacrer à d'autres activités (comme siroter un café tranquillement, par exemple). Alors, n'hésitez pas à essayer cette astuce, à la partager avec vos amis et n’oubliez pas de revenir pour d'autres "Trucs & Astuces" à venir !

###### Dans cette aventure codée, que chaque ligne de script soit un sortilège ouvrant un univers de possibilités, une solution transformant l'ordinaire en extraordinaire. Désormais, plus besoin de sacrifier du temps précieux pour entrer manuellement chaque contact : laissez la magie des scripts faire le travail à votre place !

###### À très bientôt pour de nouvelles explorations et toujours plus de Trucs & Astuces !

###### *Magiquement vôtre,*
M.Royce
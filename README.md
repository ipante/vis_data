# Projet de visualisation de données

## Introduction

Ce projet a été développé dans le cadre du cours Visualisation de données dispensé par Isaac Pante (SLI, Lettres, UNIL).
L'idée de ce projet est de réaliser une visualisation web basée sur des données géographiques, qui permettent de visualiser et d'interagir avec les différents type de limites
admnistratives de la Suisse, à savoir les limites (i) nationales (ii) cantonales, (ii) de districts et (iv) communales.

## Librairies Utilisées

-  d3.js
-  Leaflet
-  Jquery

## Installation

A COMPLETER

## Détail du processus de création

### Fond de carte:

Leaflet est une bibliothèque libre de cartographie en ligne développée par _Vladimir Agafonkin_ de CloudMade et de nombreux autres contributeurs. Elle donne accès à des fonds de carte et autorise l'ajout d'éléments interactifs. Cette librairie a permis de créer le fond de carte sur lequel sont projetées nos limites administratives.

![ch_esri](https://user-images.githubusercontent.com/81638170/148357329-06e40d3d-6615-4fc8-ad14-881efc3f9b9e.JPG)

### Recherche de données topographiques & habillage de la carte

Une fois le fond de carte créé, nous pouvons ajouter nos éléments d'habillage à la carte, dont les données des différentes limites administratives de la Suisse. Nous avons décidé de travailler à partir d'un jeu de donnée gratuit rendu disponible par _Swisstopo_. Ce jeu de donnée [swissBOUNDARIES3D](https://www.swisstopo.admin.ch/fr/geodata/landscape/boundaries3d.html) contient des fichiers Shapefile correspondant au différentes limites administrative de la Suisse. En transformant ces fichiers Shapefile en fichier Geojson au travers d'un logiciel SIG (ici [QGIS](https://www.qgis.org/fr/site/)), il est ensuite possible d'exploiter ces données dans notre pojet.
![Capture](https://user-images.githubusercontent.com/81638170/148370274-8191f090-0941-41e3-8424-cbe41a640f4b.JPG)

## Création de l'interface

Une fois les éléments de fond de carte et d'habillages définis. nous avons créé une interface d'interaction avec la carte et les données Geojson. Cette interface se décompose en trois parties :

-  une carte interactive qui permet de visualiser nos limites administratives de la Suisse,
-  une liste de boutons permettant de sélectionner les limites à afficher,
-  une zone textuelle où s'inscriront les informations.
   ![projet_vis_data](https://user-images.githubusercontent.com/81638170/148364214-4c2a3c3d-bceb-47ba-adf3-a30cdc6fbd8f.JPG)

### Interactivité

Il est dès lors possible de sélectionner un type de limite administrative à visualiser en cliquant sur l'élément souhaité en dessous de la carte. Cette fonction permet d'afficher les limites sur la carte, mises en évidence au survol de la souris. Un clic sur une zone affiche le nombre d'habitants figurant dans cette zone administrative.
![exempe](https://user-images.githubusercontent.com/81638170/148365150-1a70f6ec-9fb6-4a8b-981a-9e145db0e475.JPG)

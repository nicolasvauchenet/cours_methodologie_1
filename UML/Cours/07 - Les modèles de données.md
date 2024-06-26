# 07. Les modèles de données

## 07a. Modèle Hiérarchique

![07a-example.png](../images/07a-example.png)

### Présentation

Le modèle de données hiérarchique organise les données en une structure en arbre où chaque enregistrement a un seul
parent, mais peut avoir plusieurs enfants. Initialement utilisé dans les premiers systèmes de gestion de bases de
données, ce modèle est simple et permet une navigation rapide à travers les structures.

### Utilité dans le Développement Logiciel

#### Organisation des Données :

Les données sont structurées de manière hiérarchique, ce qui est particulièrement utile pour représenter des
informations organisées naturellement sous cette forme, comme les structures d'entreprise, les catégories de produits,
ou les dossiers et sous-dossiers sur un système de fichiers.

#### Requêtes Rapides :

La navigation et les requêtes peuvent être très rapides si les relations parent-enfant sont clairement définies, car le
chemin d'accès à chaque noeud est unique.

### Symboles

Les symboles utilisés dans le modèle hiérarchique incluent principalement les noeuds et les liens qui les connectent.
Chaque noeud représente un enregistrement ou un objet, et les liens représentent les relations de parenté à enfant.

## 07b. Modèle Relationnel

![07b-example.png](../images/07b-example.png)

### Présentation

Le modèle relationnel, proposé par Edgar F. Codd, organise les données en tables (ou relations) composées de lignes et
de colonnes. Chaque table représente un type d'entité, et chaque ligne (ou tuple) une instance de cette entité. Les
relations entre les tables sont gérées par des clés étrangères.

### Utilité dans le Développement Logiciel

#### Flexibilité des Requêtes :

Grâce à l'algèbre relationnelle et au SQL, ce modèle offre une grande flexibilité pour écrire des requêtes complexes et
réaliser des jointures entre tables.

#### Intégrité des Données :

Le modèle relationnel permet une gestion efficace de l'intégrité des données à travers des contraintes de clés primaires
et étrangères.

### Symboles

Les symboles principaux incluent les rectangles représentant les tables, et les lignes qui relient ces tables pour
indiquer les relations. Les clés primaires et étrangères sont souvent mises en évidence dans les schémas.

## 07c. Modèle Réseau

![07c-example.png](../images/07c-example.png)

### Présentation

Le modèle de données réseau est une extension du modèle hiérarchique où chaque enregistrement peut avoir plusieurs
parents. Ce modèle permet une plus grande flexibilité par rapport au modèle strictement hiérarchique.

### Utilité dans le Développement Logiciel

#### Flexibilité des Relations :

Les relations complexes entre enregistrements peuvent être plus naturellement modélisées, ce qui est utile pour des
applications nécessitant de multiples relations entre les données, comme les systèmes de réservation ou les réseaux
sociaux.

### Symboles

Comme pour le modèle hiérarchique, les symboles comprennent des noeuds et des connexions, mais avec la possibilité de
multiples connexions entrantes pour chaque noeud, reflétant la structure de réseau.

## 07d. Modèle Document

![07d-example.png](../images/07d-example.png)

### Présentation

Le modèle de données basé sur des documents stocke les informations sous forme de documents (souvent formatés en JSON ou
XML). Chaque document peut contenir une structure de données complexe avec des champs imbriqués.

### Utilité dans le Développement Logiciel

#### Souplesse de Schéma :

Le modèle document est très flexible, permettant des modifications de schéma sans interruption de service, idéal pour
les applications nécessitant une évolution rapide et des structures de données variées.

### Symboles

Les documents sont souvent représentés par des icônes ressemblant à des documents ou des fichiers, avec des liaisons
entre eux pour montrer les relations imbriquées ou les références.

## 07e. Modèle Entité / Association

![07e-example.png](../images/07e-example.png)

## Présentation

- **Origine :** Le modèle EA, souvent utilisé dans la méthode MERISE, a été développé en France dans les années 1970.
  MERISE est une méthode d'analyse et de conception des systèmes d'information qui utilise le modèle EA pour représenter
  les données.
- **Objectif :** Le modèle EA vise à fournir une représentation claire et simple des données et des relations dans un
  système d'information, en se concentrant sur les entités et leurs associations.

### Symboles

Les entités sont représentées par des rectangles, et les associations par des lignes les reliant, souvent avec des
labels pour décrire la nature de la relation. Les attributs peuvent être listés dans ou autour des rectangles d'entité.
Ce modèle utilise des bulles pour représenter les associations entre entités. Les cardinalités sont souvent notées sous
la forme "1,n".

## 07f. Modèle Entité / Relation

![07f-example2.png](../images/07f-example.png)

## Présentation

- **Origine :** Le modèle ER a été introduit par Peter Chen en 1976 dans son article "The Entity-Relationship Model -
  Toward a Unified View of Data". Ce modèle est devenu largement adopté dans le monde entier pour la modélisation des
  bases de données relationnelles.
- **Objectif :** Le modèle ER vise à fournir une représentation graphique plus structurée et formelle des entités, des
  attributs et des relations dans une base de données.

### Symboles

![07f-symbols.png](../images/07f-symbols.png)

Le modèle ER utilise des traits verticaux, des pattes d'oie, et des ronds pour indiquer les cardinalités des relations
entre les entités.

## Exercices pratiques

### [Système de Gestion Universitaire](..%2FExercices%2F%C3%89nonc%C3%A9%2F07a%20-%20Mod%C3%A8le%20Entit%C3%A9-Relation%20-%20Exercice.md)

### [Plateforme de Gestion d'Événements](..%2FExercices%2F%C3%89nonc%C3%A9%2F07b%20-%20Mod%C3%A8le%20Entit%C3%A9-Relation%20-%20Exercice.md)

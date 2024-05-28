# 05. Le diagramme de Classes

![05-example.png](../images/05-example.png)

## Présentation

Le diagramme de classes est un élément central de la modélisation UML, fournissant une vue structurée du système. Il
définit la structure des classes du logiciel, leurs attributs, leurs méthodes, ainsi que les relations qu'elles
entretiennent entre elles. Ce diagramme joue un rôle crucial dans la conception orientée objet, permettant aux
architectes logiciels de planifier la manière dont le système est organisé.

## Utilité dans le Développement Logiciel

### Conception Orientée Objet :

Les diagrammes de classes facilitent la modélisation des concepts réels sous forme de classes, aidant les développeurs à
visualiser les objets du système et leurs relations. Ils constituent une base solide pour l'implémentation des principes
SOLID.

### Documentation :

Ils fournissent une documentation visuelle des classes, des attributs, et des méthodes, ce qui simplifie la
compréhension du code par les développeurs qui rejoignent le projet ou qui en prennent la maintenance.

### Optimisation et Refactorisation :

Le diagramme aide les développeurs à identifier les duplications ou les dépendances excessives entre les classes, ce qui
facilite la refactorisation et l'amélioration continue du design.

### Collaboration d'Équipe :

Le diagramme de classes sert de langage commun entre les architectes, les développeurs et les autres parties prenantes,
en alignant les attentes et les objectifs dès la phase de conception.

## Symboles et Éléments

![05-symbols-class.png](../images/05-symbols-class.png)

![05-symbols-relations.png](../images/05-symbols-relations.png)

### Classe :

Une classe est représentée par un rectangle à trois compartiments. Le compartiment supérieur affiche le nom de la
classe. Le compartiment central contient les attributs (propriétés). Le compartiment inférieur liste les méthodes (
opérations).

### Attribut :

Un attribut est un champ dans une classe, typiquement sous la forme : visibilité nom: type. Par exemple, +nom: String
représente un attribut public nommé "nom" de type chaîne de caractères.

### Méthode :

Les méthodes (opérations) sont définies de la même manière : visibilité nom(paramètres): type. Par exemple,
+calculerSalaire(): double représente une méthode publique sans paramètres, qui retourne un double.

### Visibilité :

Les symboles précédant les attributs et méthodes indiquent la visibilité :

- `+` **Public :** Accessible depuis n'importe quelle autre classe ou composant du programme. Cela signifie qu'aucune
  restriction n'est imposée à l'accès ou à l'utilisation de l'élément.
- `#` **Protégé :** Accessible uniquement par les classes qui sont des descendants (sous-classes) de la classe où
  l'élément protégé est déclaré. Cela permet un accès plus restreint que le public, protégeant l'élément des accès
  extérieurs tout en permettant son utilisation par les classes dérivées.
- `-` **Privé :** L'accès est strictement limité à la classe dans laquelle l'élément est déclaré. Aucune autre classe,
  même une sous-classe, ne peut accéder à cet élément directement. Cela est utilisé pour cacher les détails
  d'implémentation de la classe et encourager l'encapsulation.
- `~` **Package :** Accessible uniquement par les classes qui sont dans le même paquet. Ce niveau de visibilité est
  utilisé pour contrôler l'accès au sein d'un même regroupement logique de classes qui travaillent ensemble de manière
  interne, sans exposer l'élément au-delà des frontières du paquet.
- `/` **Dérivé :** Indique que l'attribut n'est pas stocké directement mais calculé ou dérivé d'autres attributs ou
  relations. Les attributs dérivés sont souvent marqués par une barre oblique pour indiquer qu'ils sont le résultat d'
  une opération ou d'une méthode spécifique. Par exemple, un attribut âge pourrait être dérivé de la date de naissance.
- `souligné` **Statique :** Indique que l'élément (attribut ou méthode) appartient à la classe elle-même plutôt qu'à une
  instance spécifique de la classe. Cela signifie que l'élément est partagé entre toutes les instances de la classe. En
  UML, un nom souligné signifie que l'élément est statique.

### Relation :

- **Association :**  
  Une connexion générale entre deux classes, indiquant une relation bidirectionnelle ou unidirectionnelle.  
  Exemple : Une Personne peut avoir une association avec Voiture, indiquant qu'une personne possède une voiture.

- **Agrégation :**  
  Une forme spéciale d'association qui représente une relation "tout-partie" où la partie peut exister indépendamment du
  tout.  
  Exemple : Entreprise et Employé, où les employés peuvent exister séparément de l'entreprise.

- **Composition :**  
  Une forme plus forte d'agrégation où la partie ne peut pas exister sans le tout.   
  Exemple : Moteur est une partie essentielle de Voiture.

- **Héritage :**  
  Une relation où une classe (sous-classe ou classe dérivée) hérite des caractéristiques d'une autre classe (
  super-classe
  ou classe parente).  
  Exemple : VoitureElectrique héritant de Voiture, reprenant ses attributs et méthodes tout en ajoutant les siens.

- **Réalisation :**  
  La réalisation ou mise en œuvre spécifie qu'une classe réalise l'ensemble des méthodes définies dans une interface. La
  notion de mise en œuvre dans le contexte d'un diagramme de classes UML fait référence à la façon dont une classe
  concrétise ou réalise la fonctionnalité définie dans une autre classe ou une interface : une classe peut mettre en
  œuvre les méthodes et les comportements définis dans une autre classe. Cela signifie qu'elle fournit une
  implémentation pratique pour ces fonctionnalités.  
  Exemple : La classe Voiture peut réaliser une interface IVehicule qui définit des méthodes comme conduire() et
  stationner(). Les méthodes seront simplement définies dans l'interface, tandis que le code exécutant les actions sera
  écrit dans la classe qui l'implémente.

- **Implémentation :**  
  Se réfère souvent à l'action d'une classe concrète exécutant les méthodes d'une interface. Lorsque l'on parle de mise
  en œuvre dans un diagramme de classes UML, cela fait généralement référence à l'implémentation d'interfaces ou de
  contrats définis dans une classe par une autre classe. Les interfaces sont des contrats abstraits qui spécifient les
  méthodes que les classes concrètes doivent implémenter. Dans ce contexte, une classe qui implémente une interface
  s'engage à fournir une implémentation concrète pour les méthodes déclarées dans cette interface.  
  Exemple : Voiture implémentant l'interface IVehicule.

- **Dépendance :**  
  Une dépendance est une relation où une classe dépend d'une autre pour fonctionner, mais cette dépendance est
  généralement de courte durée ou moins formelle.  
  Exemple : La classe Conducteur peut avoir une dépendance à la classe Voiture pour sa méthode conduire().

## Notions avancées en POO

### Le polymorphisme

Le polymorphisme est un principe clé de la programmation orientée objet (POO) qui permet aux objets de différentes
classes de répondre à la même action, chaque objet traitant l'action d'une manière appropriée à son type. Ce concept
repose sur trois aspects fondamentaux : les interfaces, l'abstraction, et la concrétisation.

- **Interfaces :**
  En POO, une interface est une déclaration de méthodes sans implémentations, agissant comme un contrat que les classes
  implémentantes doivent respecter. Les interfaces permettent à des classes de types très différents de s'interfacer de
  manière uniforme avec le reste du système.
- **Abstraction :**  
  Le polymorphisme favorise l'abstraction en permettant l'utilisation de types plus généraux (comme les types de base
  dans une hiérarchie de classes ou les interfaces) pour manipuler des objets. Cela permet aux développeurs de
  programmer en termes d'interfaces ou de classes abstraites tout en laissant le système décider de l'objet spécifique à
  créer et à utiliser en fonction du contexte.
- **Concrétisation :**  
  Cela se produit lorsque des classes concrètes implémentent les méthodes définies par leurs interfaces ou classes
  abstraites. La concrétisation est l'acte de définir le comportement spécifique des méthodes abstraites ou des
  interfaces, fournissant ainsi une implémentation réelle aux opérations abstraites.

### L'encapsulation

L'encapsulation est un mécanisme de restriction de l'accès direct aux composants d'un objet, ce qui protège l'intégrité
des données de l'objet en empêchant des interférences extérieures ou une utilisation incorrecte.

- **Protection des données :**  
  Les attributs d'un objet sont cachés et seulement accessibles via des méthodes définies dans la classe (souvent
  appelées getters et setters). Cela assure que les données internes ne peuvent pas être changées arbitrairement,
  imposant un contrôle strict sur la manière dont les données essentielles sont modifiées et consultées.
- **Contrôle de l'accès :**  
  L'encapsulation utilise des modificateurs d'accès tels que public, private, et protected pour contrôler comment les
  membres de données sont visibles à l'extérieur de la classe. Les méthodes publiques fournissent une interface avec
  l'extérieur, tandis que les détails internes restent privés, permettant à la classe de garantir qu'aucun comportement
  erroné ne soit induit par des changements inattendus dans son état interne.
- **Cohérence et validation :**  
  En encapsulant les données, les classes peuvent forcer des règles de validation sur les données entrantes,
  garantissant que l'objet reste dans un état valide. Par exemple, si une classe CompteBancaire a un attribut solde, le
  setter pour ce solde peut vérifier que les fonds ne sont pas définis à une valeur négative.

L'encapsulation et le polymorphisme sont des piliers de la POO qui permettent de construire des systèmes plus fiables,
modulaires et évolutifs. Ces mécanismes aident à gérer la complexité et à augmenter la réutilisabilité du code, tout en
améliorant la maintenance et la flexibilité des logiciels.

## Exercices pratiques

### [Système de réservation de bibliothèque en ligne](..%2FExercices%2F%C3%89nonc%C3%A9%2F05a%20-%20Diagramme%20de%20Classes%20-%20Exercice.md)

### [Plateforme de Gestion d'Événements](..%2FExercices%2F%C3%89nonc%C3%A9%2F05b%20-%20Diagramme%20de%20Classes%20-%20Exercice.md)

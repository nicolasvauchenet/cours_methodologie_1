# Cas d'utilisation - Correction : Système de réservation de bibliothèque en ligne

## Définition des acteurs

### Acteur interne :
- Bibliothécaire : Gère les livres et les transactions de prêt au sein de la bibliothèque. Peut également être responsable de la mise à jour de l'inventaire des livres et de l'envoi des rappels aux emprunteurs.

### Acteur externe :
- Lecteur (utilisateur de la bibliothèque) : Utilise le système pour rechercher et emprunter des livres. Reçoit des rappels du système pour rendre les livres.

### Acteur système :
- Système de réservation : Automatise le processus de recherche, d'emprunt et de rappel de livres. Assure la mise à jour des statuts des livres et l'envoi des notifications.

## Définition des fonctionnalités clés et regroupement par domaine

### Gestion des livres :
- Ajouter/Retirer des livres à l'inventaire : Permet au bibliothécaire de mettre à jour l'inventaire des livres.
- Mettre à jour les informations des livres : Modifier les détails des livres comme le titre, l'auteur, l'année de publication, etc.

### Emprunt de livres :
- Rechercher des livres : Permet aux lecteurs de trouver des livres disponibles dans la bibliothèque.
- Réserver un livre : Permet aux lecteurs de réserver des livres disponibles et de les emprunter.
- Gestion des prêts : Suivi des livres empruntés par chaque lecteur et gestion de la durée du prêt.

### Rappels :
- Envoyer des rappels : Le système envoie automatiquement des rappels aux lecteurs pour la restitution des livres en retard.
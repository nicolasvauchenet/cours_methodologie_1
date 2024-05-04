# Diagrammes de Séquence

1. Programmation et horaires des artistes

- Diagramme de séquence : Notifier un changement de planning
- Acteurs : Régisseur Artistique, Artiste
- Description :
    - Le Régisseur Artistique identifie un changement de planning
    - Le système affiche le nouveau planning à l'écran
    - Le Régisseur Artistique valide le nouveau planning
    - Le système envoie une notification à l'Artiste concerné par le changement
    - L'Artiste reçoit la notification et consulte le nouveau planning

2. Accueil et services aux artistes

- Diagramme de séquence : Réserver un hébergement pour un artiste
- Acteurs : Personnel d'Accueil, Gestionnaire des Logements, Artiste
- Description :
    - Le Personnel d'Accueil reçoit les préférences d'hébergement de l'Artiste
    - Le Personnel d'Accueil saisit les préférences dans le système
    - Le système vérifie les disponibilités auprès du Gestionnaire des Logements
    - Le Gestionnaire des Logements confirme la disponibilité d'un hébergement
    - Le système réserve l'hébergement pour l'Artiste
    - Le Personnel d'Accueil informe l'Artiste de la réservation

3. Logistique du festival

- Diagramme de séquence : Gérer un incident technique sur scène
- Acteurs : Technicien de Scène, Régisseur Technique
- Description :
    - Le Technicien de Scène détecte un incident technique sur scène
    - Le Technicien de Scène informe le Régisseur Technique de l'incident
    - Le Régisseur Technique évalue la gravité de l'incident
    - Le système affiche les procédures d'intervention d'urgence à suivre
    - Le Régisseur Technique coordonne les actions des Techniciens de Scène pour résoudre l'incident
    - Le Technicien de Scène résout l'incident et informe le Régisseur Technique
    - Le Régisseur Technique valide la résolution de l'incident dans le système

4. Communication et publicité

- Diagramme de séquence : Publier une annonce sur les réseaux sociaux
- Acteurs : Chargé de Communication, Équipe Marketing, Système de gestion des réseaux sociaux
- Description :
    - Le Chargé de Communication crée une annonce pour le festival
    - Le Chargé de Communication soumet l'annonce à l'Équipe Marketing pour approbation
    - L'Équipe Marketing approuve l'annonce
    - Le Chargé de Communication programme la publication de l'annonce dans le système de gestion des réseaux sociaux
    - Le système publie l'annonce sur les réseaux sociaux aux heures programmées

5. Gestion de la billetterie et services sur site

- Diagramme de séquence : Valider un billet d'entrée
- Acteurs : Agent de billetterie, Spectateur, Système de billetterie
- Description :
    - Le Spectateur présente son billet à l'Agent de billetterie
    - L'Agent de billetterie scanne le billet à l'aide du système de billetterie
    - Le système vérifie la validité du billet
    - Le système valide le billet et enregistre l'entrée du Spectateur
    - L'Agent de billetterie autorise l'accès au site du festival au Spectateur

6. Budgétisation du festival

- Diagramme de séquence : Approuver une dépense
- Acteurs : Chef de département, Directeur Financier, Système de gestion financière
- Description :
    - Le Chef de département soumet une demande de dépense dans le système de gestion financière
    - Le système notifie le Directeur Financier de la demande de dépense
    - Le Directeur Financier vérifie la conformité de la demande avec le budget alloué
    - Le Directeur Financier approuve ou rejette la demande de dépense dans le système
    - Le système notifie le Chef de département de la décision du Directeur Financier
    - Le Chef de département procède à la dépense approuvée ou ajuste sa demande en cas de rejet

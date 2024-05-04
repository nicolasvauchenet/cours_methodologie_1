# Diagrammes de Classes

1. Programmation et horaires des artistes

- Classes :
    - Artiste
        - idArtiste : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - genreMusical : String (visibilité : privée)
        - popularité : int (visibilité : privée)
    - Scène
        - idScène : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - capacité : int (visibilité : privée)
    - Performance
        - idPerformance : int (visibilité : privée)
        - idArtiste : int (visibilité : privée)
        - idScène : int (visibilité : privée)
        - date : Date (visibilité : privée)
        - heureDébut : Time (visibilité : privée)
        - heureFin : Time (visibilité : privée)
        - AjouterArtiste(artiste : Artiste) : void
        - SupprimerArtiste() : void
        - AjouterScène(scène : Scène) : void
        - SupprimerScène() : void
    - Planning
        - idPlanning : int (visibilité : privée)
        - date : Date (visibilité : privée)
        - listePerformances : List<Performance> (visibilité : privée)
        - ajouterPerformance(performance : Performance) : void (visibilité : publique)
        - supprimerPerformance(performance : Performance) : void (visibilité : publique)
- Relations :
    - Association : Artiste - Performance, Scène - Performance
    - Agrégation : Planning - Performance (un planning est composé de plusieurs performances, mais une performance peut
      exister sans le planning)

2. Accueil et services aux artistes

- Classes :
    - Artiste
        - idArtiste : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - préférencesHébergement : String (visibilité : privée)
        - régimeAlimentaire : String (visibilité : privée)
        - AjouterPréférenceHébergement(préférence : PréférenceHébergement) : void
        - SupprimerPréférenceHébergement(préférence : PréférenceHébergement) : void
    - Hébergement
        - idHébergement : int (visibilité : privée)
        - type : String (visibilité : privée)
        - adresse : String (visibilité : privée)
        - capacité : int (visibilité : privée)
    - Restauration
        - idRestauration : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - typeCuisine : String (visibilité : privée)
        - menu : String (visibilité : privée)
    - Service
        - idService : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - description : String (visibilité : privée)
- Relations :
    - Association : Artiste - Hébergement, Artiste - Restauration, Artiste - Service
    - Agrégation : Artiste - PréférencesHébergement (un artiste peut avoir plusieurs préférences d'hébergement, mais une
      préférence d'hébergement peut exister sans l'artiste)

3. Logistique du festival

- Classes :
    - Équipement
        - idÉquipement : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - type : String (visibilité : privée)
        - quantité : int (visibilité : privée)
    - Scène
        - idScène : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - capacité : int (visibilité : privée)
        - listeÉquipements : List<Équipement> (visibilité : privée)
        - ajouterÉquipement(équipement : Équipement) : void (visibilité : publique)
        - supprimerÉquipement(équipement : Équipement) : void (visibilité : publique)
    - Technicien
        - idTechnicien : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - compétences : List<String> (visibilité : privée)
        - ajouterCompétence(compétence : String) : void (visibilité : publique)
        - supprimerCompétence(compétence : String) : void (visibilité : publique)
    - Intervention
        - idIntervention : int (visibilité : privée)
        - idTechnicien : int (visibilité : privée)
        - idÉquipement : int (visibilité : privée)
        - date : Date (visibilité : privée)
        - heureDébut : Time (visibilité : privée)
        - heureFin : Time (visibilité : privée)
        - AjouterTechnicien(technicien : Technicien) : void
        - SupprimerTechnicien() : void
        - AjouterÉquipement(équipement : Équipement) : void
        - SupprimerÉquipement() : void
- Relations :
    - Association : Scène - Équipement, Technicien - Intervention, Équipement - Intervention
    - Composition : Scène - ListeÉquipements (une scène est composée d'une liste d'équipements, et un équipement ne peut
      exister sans la scène)

4. Communication et publicité

- Classes :
    - Annonce
        - idAnnonce : int (visibilité : privée)
        - titre : String (visibilité : privée)
        - contenu : String (visibilité : privée)
        - datePublication : Date (visibilité : privée)
        - AjouterRéseauSocial(réseauSocial : RéseauSocial) : void
        - SupprimerRéseauSocial(réseauSocial : RéseauSocial) : void
    - RéseauSocial
        - idRéseauSocial : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - url : String (visibilité : privée)
    - Campagne
        - idCampagne : int (visibilité : privée)
        - budget : float (visibilité : privée)
        - dateDébut : Date (visibilité : privée)
        - dateFin : Date (visibilité : privée)
        - listeAnnonces : List<Annonce> (visibilité : privée)
        - ajouterAnnonce(annonce : Annonce) : void (visibilité : publique)
        - supprimerAnnonce(annonce : Annonce) : void (visibilité : publique)
    - Public
        - idPublic : int (visibilité : privée)
        - trancheAge : String (visibilité : privée)
        - centresIntérêt : List<String> (visibilité : privée)
        - ajouterCentreIntérêt(centreIntérêt : String) : void (visibilité : publique)
        - supprimerCentreIntérêt(centreIntérêt : String) : void (visibilité : publique)
- Relations :
    - Association : CampagnePublicitaire - Annonce, Annonce - RéseauSocial, CampagnePublicitaire - Public
    - Agrégation : Public - CentresIntérêt (un public peut avoir plusieurs centres d'intérêt, mais un centre d'intérêt
      peut exister sans le public)

5. Gestion de la billetterie et services sur site

- Classes :
    - Billet
        - idBillet : int (visibilité : privée)
        - type : String (visibilité : privée)
        - prix : float (visibilité : privée)
        - statut : String (visibilité : privée)
    - Spectateur
        - idSpectateur : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - prénom : String (visibilité : privée)
        - email : String (visibilité : privée)
        - AcheterBillet(billet : Billet) : void
        - AnnulerBillet(billet : Billet) : void
    - Entrée
        - idEntrée : int (visibilité : privée)
        - idBillet : int (visibilité : privée)
        - idSpectateur : int (visibilité : privée)
        - date : Date (visibilité : privée)
        - heure : Time (visibilité : privée)
        - AjouterSpectateur(spectateur : Spectateur) : void
        - SupprimerSpectateur() : void
    - ServiceSurSite
        - idServiceSurSite : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - description : String (visibilité : privée)
        - tarif : float (visibilité : privée)
- Relations :
    - Association : Billet - Entrée, Spectateur - Entrée, Spectateur - ServiceSurSite
    - Composition : Spectateur - ListeBillets (un spectateur peut avoir plusieurs billets, mais un billet ne peut
      exister sans le spectateur)

6. Budgétisation du festival

- Classes :
    - Dépense
        - idDépense : int (visibilité : privée)
        - montant : float (visibilité : privée)
        - date : Date (visibilité : privée)
        - catégorie : String (visibilité : privée)
    - Budget
        - idBudget : int (visibilité : privée)
        - montantTotal : float (visibilité : privée)
        - listeDépenses : List<Dépense> (visibilité : privée)
        - ajouterDépense(dépense : Dépense) : void (visibilité : publique)
        - supprimerDépense(dépense : Dépense) : void (visibilité : publique)
    - Catégorie
        - idCatégorie : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - montantAlloué : float (visibilité : privée)
    - Département
        - idDépartement : int (visibilité : privée)
        - nom : String (visibilité : privée)
        - responsable : String (visibilité : privée)
        - AjouterDépense(dépense : Dépense) : void
        - SupprimerDépense(dépense : Dépense) : void
- Relations :
    - Association : Budget - Dépense, Catégorie - Dépense, Département - Dépense, Catégorie - Département
    - Composition : Budget - ListeDépenses (un budget est composé d'une liste de dépenses, et une dépense ne peut
      exister sans le budget)

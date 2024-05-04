# Modèle Entité-Association

1. Entités :

- Artiste
    - ID (clé primaire)
    - Nom
    - PréférencesHébergement
- Scène
    - ID (clé primaire)
    - Nom
    - Capacité
- Performance
    - ID (clé primaire)
    - Date
    - HeureDébut
    - HeureFin
- Planning
    - ID (clé primaire)
    - Date
- Hébergement
    - ID (clé primaire)
    - Nom
    - Type
    - Adresse
- Restauration
    - ID (clé primaire)
    - Nom
    - TypeCuisine
- Service
    - ID (clé primaire)
    - Nom
    - Description
- Équipement
    - ID (clé primaire)
    - Nom
    - Quantité
- Technicien
    - ID (clé primaire)
    - Nom
    - Prénom
- Intervention
    - ID (clé primaire)
    - Date
    - HeureDébut
    - HeureFin
- CampagnePublicitaire
    - ID (clé primaire)
    - Nom
    - Budget
    - DateDébut
    - DateFin
- Annonce
    - ID (clé primaire)
    - Titre
    - Contenu
    - DatePublication
- RéseauSocial
    - ID (clé primaire)
    - Nom
- Public
    - ID (clé primaire)
    - TrancheAge
    - CentresIntérêt
- Billet
    - ID (clé primaire)
    - Type
    - Prix
    - Statut
- Spectateur
    - ID (clé primaire)
    - Nom
    - Prénom
    - Email
- Entrée
    - ID (clé primaire)
    - Date
    - Heure
- ServiceSurSite
    - ID (clé primaire)
    - Nom
    - Description
    - Tarif
- Dépense
    - ID (clé primaire)
    - Montant
    - Date
    - Catégorie
- Catégorie
    - ID (clé primaire)
    - Nom
- Département
    - ID (clé primaire)
    - Nom

2. Associations :

- Un Artiste peut avoir plusieurs Performances, et une Performance est associée à un Artiste. (1 Artiste - *
  Performance)
- Une Scène peut accueillir plusieurs Performances, et une Performance est associée à une Scène. (1 Scène - *
  Performance)
- Un Planning contient plusieurs Performances, et une Performance est associée à un Planning. (1 Planning - *
  Performance)
- Un Artiste peut avoir plusieurs préférences d'Hébergement, et un Hébergement peut être préféré par plusieurs
  Artistes. (* Artiste - * Hébergement)
- Un Artiste peut apprécier plusieurs Restauration, et une Restauration peut être appréciée par plusieurs Artistes. (*
  Artiste - * Restauration)
- Un Artiste peut bénéficier de plusieurs Services, et un Service peut être utilisé par plusieurs Artistes. (*
  Artiste - * Service)
- Une Scène possède plusieurs Équipements, et un Équipement est associé à une Scène. (1 Scène - * Équipement)
- Un Technicien peut avoir plusieurs Compétences, et une Compétence peut être possédée par plusieurs Techniciens. (*
  Technicien - * Compétence)
- Un Technicien peut effectuer plusieurs Interventions, et une Intervention est associée à un Technicien. (1
  Technicien - * Intervention)
- Un Équipement peut faire l'objet de plusieurs Interventions, et une Intervention est associée à un Équipement. (1
  Équipement - * Intervention)
- Une CampagnePublicitaire contient plusieurs Annonces, et une Annonce est associée à une CampagnePublicitaire. (1
  CampagnePublicitaire - * Annonce)
- Une Annonce peut être diffusée sur plusieurs RéseauxSociaux, et un RéseauSocial peut diffuser plusieurs Annonces. (*
  Annonce - * RéseauSocial)
- Une CampagnePublicitaire cible plusieurs Publics, et un Public peut être ciblé par plusieurs
  CampagnesPublicitaires. (* CampagnePublicitaire - * Public)
- Un Public peut avoir plusieurs CentresIntérêt, et un CentreIntérêt peut être partagé par plusieurs Publics. (*
  Public - * CentreIntérêt)
- Un Spectateur peut acheter plusieurs Billets, et un Billet est associé à un Spectateur. (1 Spectateur - * Billet)
- Une Entrée est associée à un Spectateur et un Billet. (1 Entrée - 1 Spectateur, 1 Entrée - 1 Billet)
- Un Spectateur peut bénéficier de plusieurs ServicesSurSite, et un ServiceSurSite peut être utilisé par plusieurs
  Spectateurs. (* Spectateur - * ServiceSurSite)
- Une Dépense est associée à une Catégorie et un Département. (1 Dépense - 1 Catégorie, 1 Dépense - 1 Département)
- Une Catégorie peut regrouper plusieurs Dépenses, et une Dépense est associée à une Catégorie. (1 Catégorie - *
  Dépense)
- Un Département peut avoir plusieurs Dépenses, et une Dépense est associée à un Département. (1 Département - *
  Dépense)

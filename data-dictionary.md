# Data dictionary

## Candidat (`candidate`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du candidat|
|lasttname|VARCHAR(64)|NOT NULL|Le nom du candidat|
|firstname|VARCHAR(64)|NULL|Le prénom du candidat|
|birthday|TEXT|NULL|La description du personnage|
|genre|TINYINT|NOT NULL|Le sexe du candidat (0 pour inconnu, 1 pour masculin, 2 pour féminin)|
|phone_number|VARCHAR(10)|NULL|Le numéro de téléphone du candidat|
|picture|VARCHAR(2083)|NULL|L'URL de la photo du candidat|
|resume|VARCHAR(2083)|NULL|L'URL du CV du candidat|
|description|LONGTEXT|NULL|La description du candidat|
|position_held|VARCHAR(128)|NULL|L'intitulé du poste souhaité|
|portfolio|VARCHAR(2083)|NULL|L'URL du portfolio du candidat|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création du candidat|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du candidat|
|adress_id|entity|NULL|L'adresse (autre entité) du candidat|
|experience_id|entity|NULL|Le niveau d'expérience (autre entité) du candidat|
|salary_id|entity|NULL|La tranche de salaire (autre entité) du candidat|
|user_id|entity|NOT NULL|L'utilisateur (autre entité) associé au candidat|

## Utilisateur (`user`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant de l'utilisateur|
|email|VARCHAR(180)|NOT NULL|L'adresse mail de l'utilisateur|
|password|VARCHAR(255)|NOT NULL|le mot de passe de l'utilisateur|
|roles|LONGTEXT|NOT NULL|le role de l'utilisateur|
|created_at|TIMESTAMP|DEFAULT CURRENT_TIMESTAMP|La date de création de l'utilisateur|
|updated_at|TIMESTAMP|NULL|La date de la dernière mise à jour de l'utilisateur|

## Recruteur (`recruiter`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du recruteur|
|lasttname|VARCHAR(64)|NOT NULL|Le nom du recruteur|
|firstname|VARCHAR(64)|NULL|Le prénom du recruteur|
|phone_number|VARCHAR(10)|NULL|Le numéro de téléphone du recruteur|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création du recruteur|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du recruteur|
|adress_id|entity|NULL|L'adresse (autre entité) du candidat|
|company_id|entity|NULL|L'entreprise (autre entité) du recruteur|

## Entreprise (`company`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant de l'entreprise|
|company_name|VARCHAR(64)|NOT NULL|Le nom de l'entreprise|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création de l'entreprise|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour de l'entreprise|
|sector_id|entity|NULL|Le secteur d'activité (autre entité) de l'entreprise|

## Offre d'emploi (`job`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant de l'offre|
|job_name|VARCHAR(128)|NOT NULL|Le nom de l'offre|
|description|LONGTEXT|NOT NULL|La description de l'offre|
|statut|TINYINT|NOT NULL|Le statut de l'offre (0 pour active, 1 pour inactive/archivée)|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création de l'offre|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour de l'offre|
|experience_id|entity|NULL|Le niveau d'expérience (autre entité) pour l'offre|
|contract_id|entity|NULL|Le type de contract (autre entité) pour l'offre|
|salary_id|entity|NULL|La tranche de salaire (autre entité) pour l'offre|

## Type de contrat (`contract`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du type de contrat|
|type|VARCHAR(64)|NOT NULL|Le nom du type de contrat|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création du type de contrat|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du type de contrat|

## Titre de l'emploi (`jobtitle`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du titre de l'emploi|
|title|VARCHAR(64)|NOT NULL|L'intitulé du titre de l'emploi|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création de la technologie|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour de la technologie|

## Type de technologie (`technology`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant de la technologie|
|technology_name|VARCHAR(64)|NOT NULL|Le nom de la technologie|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création de la technologie|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour de la technologie|

## Tranche de salaire (`salary`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant de la tranche de salaire|
|slice|VARCHAR(64)|NOT NULL|Le nom de la tranche de salaire|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création de la tranche de salaire|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour de la tranche de salaire|

## Niveau d'expérience (`experience`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du niveau d'expérience|
|years_number|TINYINT|NOT NULL|Le nombre d'années du niveau d'expérience|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date du niveau d'expérience|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du niveau d'expérience|

## Secteur d'activité (`sector`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du secteur d'activité|
|sector_name|VARCHAR(64)|NOT NULL|Le nom du secteur d'activité|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date du secteur d'activité|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du secteur d'activité|

## Match (`match`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant de match|
|candidate_status|TINYINT|NULL, UNSIGNED|Le status du candidat (0 si pas de like 1 si like)|
|recruiter_status|TINYINT|NULL, UNSIGNED|Le statut du recruiter (0 si pas de like 1 si like)|
|match_status|TINYINT|NULL, UNSIGNED|Le statut du match (0 si pas de match 1 si match)|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date du secteur d'activité|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du secteur d'activité|
|job_id|entity|NULL|L'id du job (autre entité) pour le match|
|candidate_id|entity|NULL|L'id du candidat (autre entité) pour le match|
|recruiter_id|entity|NULL|L'id du recruteur (autre entité) pour le match|

# Data dictionary

## Candidat (`candidate`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|id|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|L'identifiant du candidat|
|firstname|VARCHAR(64)|NOT NULL|Le prénom du candidat|
|lasttname|VARCHAR(64)|NOT NULL|Le nom du candidat|
|birthday|TEXT|NULL|La description du personnage|
|genre|TINYINT|NOT NULL|Le sexe du candidat (0 pour inconnu, 1 pour masculin, 2 pour féminin|
|phone_number|VARCHAR(10)|NULL|Le numéro de téléphone du candidat|
|picture|VARCHAR(2083)|NULL|L'URL de la photo du candidat|
|resume|VARCHAR(2083)|NULL|L'URL du CV du candidat|
|description|LONGTEXT|NULL|La description du candidat|
|position_held|VARCHAR(128)|NULL|L'intitulé du poste souhaité|
|portfolio|VARCHAR(2083)|NULL|L'URL du portfolio du candidat|
|created_at|DATETIME|NOT NULL, DEFAULT CURRENT_TIMESTAMP|La date de création du personnage|
|updated_at|DATETIME|NULL|La date de la dernière mise à jour du personnage|
|adress_id|entity|NULL|L'adresse (autre entité) du candidat|
|experience_id|entity|NULL|Le niveau d'expérience (autre entité) du candidat|

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

## Entreprise (`company`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

## Offre d'emploi (`job`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

## Type de contrat (`contract`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

## Type de technologie (`technology`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

## Tranche de salaire (`salary`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

## Niveau d'expérience (`experience`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

## Secteur d'activité (`sector`)

|Champ|Type|Spécificités|Description|
|-|-|-|-|

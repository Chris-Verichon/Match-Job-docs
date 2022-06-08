# Liste des routes

## Routes de l'application

| URL                 | Méthode HTTP | Titre                  | Contenu                   |
| ------------------- | ------------ | ---------------------- | ------------------------- |
| `/`                 | `GET`        | `Match-job Accueil`    |                           |
| `/`                 | `Post`       | `connexion`            | ------------------------- |
| `/`                 | `Post`       | `subscribe`            | ------------------------- |
| `/mentions-legales` | `GET`        | `Mentions-legals`      | legal mention             |
| `/a-propos`         | `GET`        | `A propos`             | read-more                 |
| `/retours`          | `feedback`   | `Retour d'expériences` | share your feedback       |
| `/fil`              | `GET`        | `feed`                 |                           |
| `/profil`           | `GET`        | `profile`              | personal area             |
| `/profil/edition`   | `POST`       | `edit`                 | change your profile       |

## Routes BackOffice

| URL                            | Méthode HTTP | Titre                                   | Contenu                                  |
| ------------------------------ | ------------ | --------------------------------------- | ---------------------------------------- |
| `/back`                        | `GET`        | `Backoffice Match Job`                  | `Backoffice dashboard`                   |
| `/back/users`                  | `GET`        | `Liste des utilisateurs`                | `Users list`                             |
| `/back/users/add`              | `POST`       | `Ajout d'un utilisateur`                | `Form to add a user`                     |
| `/back/users/update`           | `POST`       | `Modification d'un utilisateur`         | `Form to update a user`                  |
| `/back/users/delete`           | `DELETE`     | `Suppression d'un utilisateur`          | `message before remove a user`           |
| `/back/contracts`              | `GET`        | `Liste des types de contrats`           | `Contracts list`                         |
| `/back/contracts/add`          | `POST`       | `Ajout d'un type de contrat`            | `Form to add a contract`                 |
| `/back/contracts/update`       | `POST`       | `Modification d'un type de contrat`     | `Form to update a contract`              |
| `/back/contracts/delete`       | `DELETE`     | `Suppression d'un type de contrat`      | `message before remove a contract`       |
| `/back/technologies`           | `GET`        | `Liste des technologies`                | `Technologies list`                      |
| `/back/technologies/add`       | `POST`       | `Ajout d'une technologie`               | `Form to add a technology`               |
| `/back/technologies/update`    | `POST`       | `Modification d'une technologie`        | `Form to update a technology`            |
| `/back/technologies/delete`    | `DELETE`     | `Suppression d'une technologie`         | `message before remove a technology`     |
| `/back/salary-brackets`        | `GET`        | `Liste des tranches de salaires`        | `Salary-brackets list`                   |
| `/back/salary-brackets/add`    | `POST`       | `Ajout d'une tranche de salaire`        | `Form to add a salary-bracket`           |
| `/back/salary-brackets/update` | `POST`       | `Modification d'une tranche de salaire` | `Form to update a salary-bracket`        |
| `/back/salary-brackets/delete` | `DELETE`     | `Suppression d'une tranche de salaire`  | `message before remove a salary-bracket` |
| `/back/sectors`                | `GET`        | `liste des secteurs d'activités`        | `Sectors list`                           |
| `/back/sectors/add`            | `POST`       | `Ajout d'un secteur d'activité`         | `Form to add a sector`                   |
| `/back/sectors/update`         | `POST`       | `Modification d'un secteur d'activité`  | `Form to update a sector`                |
| `/back/sectors/delete`         | `DELETE`     | `Suppression d'un secteur d'activité`   | `message before remove a sector`         |

## Endpoints API

| Endpoint                             | Méthode HTTP | Description                          | Retour               |
| ------------------------------------ | ------------ | ------------------------------------ | -------------------- |
| `/api/v1/feedbacks`                  | `GET`        | get all the feedbacks                | 200                  |
| `/api/v1/feedbacks`                  | `POST`       | add a feedback                       | 201 + created object |
| `/api/v1/subscribe`                  | `POST`       | add new user                         | 201 + created object |
| `/api/v1/connexion`                  | `POST`       | connect user                         | 200 or 401           |
| `/api/v1/connection`                 | `GET`        | get user to connect and all card     | 200                  |
| `/api/v1/users/{id}/profil`          | `GET`        | get user profil                      | 200 or 404           |
| `/api/v1/users`                      | `POST`       | add a user                           | 201 + created object |
| `/api/v1/users/{id}`                 | `PUT`        | update a user                        | 200, 204 or 404      |
| `/api/v1/users/{id}`                 | `DELETE`     | delete a user                        | 200, 204 or 404      |
| `/api/v1/companies`                  | `GET`        | get all companies                    | 200                  |
| `/api/v1/companies`                  | `POST`       | add a company                        | 201 + created object |
| `/api/v1/companies/{id}`             | `GET`        | get informations of a companies      | 200 or 404           |
| `/api/v1/companies/{id}`             | `PUT`        | update a company                     | 200, 204 or 404      |
| `/api/v1/companies/{id}`             | `DELETE`     | delete a company                     | 200, 204 or 404      |
| `/api/v1/addresses`                  | `GET`        | get all a addresses                  | 200                  |
| `/api/v1/addresses/{id}`             | `POST`       | add a address                        | 201 + created object |
| `/api/v1/addresses`                  | `GET`        | get informations of a address        | 200 or 404           |
| `/api/v1/addresses/{id}`             | `PUT`        | update a address                     | 200, 204 or 404      |
| `/api/v1/addresses/{id}`             | `DELETE`     | delete a address                     | 200, 204 or 404      |
| `/api/v1/experiences`                | `GET`        | get all experiences                  | 200                  |
| `/api/v1/experiences`                | `POST`       | add a experiences                    | 201 + created object |
| `/api/v1/experiences/{id}`           | `GET`        | get informations of a experience     | 200 or 404           |
| `/api/v1/experiences/{id}`           | `PUT`        | update a experience                  | 200, 204 or 404      |
| `/api/v1/experiences/{id}`           | `DELETE`     | delete informations of a experience  | 200, 204 or 404      |
| `/api/v1/jobs`                       | `GET`        | get all jobs                         | 200                  |
| `/api/v1/jobs`                       | `POST`       | add a job                            | 201 + created object |
| `/api/v1/jobs/{id}`                  | `GET`        | get informations of a job            | 200 or 404           |
| `/api/v1/jobs/{id}`                  | `PUT`        | update a job                         | 200, 204 or 404      |
| `/api/v1/jobs/{id}`                  | `DELETE`     | delete a job                         | 200, 204 or 404      |
| `/api/v1/jobs/recruiters/{id}`       | `GET`        | get all jobs of a recruiter          | 200 or 404           |
| `/api/v1/jobs/candidate/{id}`        | `GET`        | get all jobs of a candidate          | 200 or 404           |
| `/api/v1/recruiters`                 | `GET`        | Get all recruiters                   | 200                  |
| `/api/v1/recruiters/{id}`            | `POST`       | add a recruiter                      | 201 + created object |
| `/api/v1/recruiters/{id}`            | `GET`        | get informations of a recruiter      | 200                  |
| `/api/v1/recruiters/{id}`            | `PUT`        | update a recruiter                   | 200, 204 or 404      |
| `/api/v1/recruiters/{id}`            | `DELETE`     | delete a recruiter                   | 200, 204 or 404      |
| `/api/v1/sectors`                    | `GET`        | get all sectors                      | 200                  |
| `/api/v1/sectors/{id}`               | `POST`       | add a sector                         | 201 + created object |
| `/api/v1/sectors/{id}`               | `GET`        | get informations of a sector         | 200 or 404           |
| `/api/v1/sectors/{id}`               | `PUT`        | update informations of a sector      | 200, 204 or 404      |
| `/api/v1/sectors/{id}`               | `DELETE`     | delete a sector                      | 200, 204 or 404      |
| `/api/v1/salary-brackets`            | `GET`        | get all salary-brackets              | 200                  |
| `/api/v1/salary-brackets/{id}`       | `POST`       | add a salary-bracket                 | 201 + created object |
| `/api/v1/salary-brackets/{id}`       | `GET`        | get informations of a salary-bracket | 200 or 404           |
| `/api/v1/salary-brackets/{id}`       | `PUT`        | update a salary-bracket              | 200, 204 or 404      |
| `/api/v1/salary-brackets/{id}`       | `DELETE`     | delete a salary-bracket              | 200, 204 or 404      |
| `/api/v1/technologies`               | `GET`        | get all technologies                 | 200                  |
| `/api/v1/technologies/{id}`          | `POST`       | add a technology                     | 201 + created object |
| `/api/v1/technologies/{id}`          | `GET`        | get informations of a technology     | 200 or 404           |
| `/api/v1/technologies/{id}`          | `PUT`        | update a technology                  | 200, 204 or 404      |
| `/api/v1/technologies/{id}`          | `DELETE`     | get informations of a technology     | 200, 204 or 404      |
| `/api/v1/contracts`                  | `GET`        | get all contracts                    | 200                  |
| `/api/v1/contracts/{id}`             | `POST`       | add a contract                       | 201 + created object |
| `/api/v1/contracts/{id}`             | `GET`        | get informations of a contract       | 200 or 404           |
| `/api/v1/contracts/{id}`             | `PUT`        | update a contract                    | 200, 204 or 404      |
| `/api/v1/contracts/{id}`             | `DELETE`     | delete a contract                    | 200, 204 or 404      |
| `/api/v1/candidates`                 | `GET`        | get all candidates                   | 200                  |
| `/api/v1/candidates`                 | `POST`       | add a candidate                      | 201 + created object |
| `/api/v1/candidates/{id}`            | `GET`        | get informations of a candidate      | 200 or 404           |
| `/api/v1/candidates/{id}`            | `PUT`        | update a candidate                   | 200, 204 or 404      |
| `/api/v1/candidates/{id}`            | `DELETE`     | delete a candidate                   | 201 + created object |
| `/api/v1/candidates/{id}/jobs/match` | `GET`        | get all jobs matched for a candidate | 200 or 404           |
| `/api/v1/candidates/{id}/jobs/like`  | `GET`        | get all jobs liked for a candidate   | 200 or 404           |

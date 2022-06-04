# Liste des routes

## Routes de l'application

| URL              | Méthode HTTP | Titre                  | Contenu                   |
| ---------------- | ------------ | ---------------------- | ------------------------- |
| `/`              | `GET`        | `Match-job Accueil`    |                           |
| `/`              | `Post`       | `connexion`            | ------------------------- |
| `/`              | `Post`       | `subscribe`            | ------------------------- |
| `/legal-mention` | `GET`        | `Mentions-legals`      | legal mention             |
| `/about`         | `GET`        | `A propos`             | read-more                 |
| `/feedback`      | `feedback`   | `Retour d'expériences` | share your feedback       |
| `/feed`          | `GET`        | `feed`                 |                           |
| `/profile`       | `GET`        | `profile`              | personal area             |
| `/profile/edit`  | `POST`       | `edit`                 | change your profile       |

## Routes BackOffice

| URL                | Méthode HTTP | Titre                            | Contenu                        |
| ------------------ | ------------ | -------------------------------- | ------------------------------ |
| `/back`            | `GET`        | `Backoffice Match Job`           | `Backoffice dashboard`         |
| `/users`           | `GET`        | `Liste des utilisateurs`         | `Users list`                   |
| `/users/add`       | `POST`       | `Ajout d'un utilisateur`         | `Form to add a user`           |
| `/users/update`    | `POST`       | `Modification d'un utilisateur`  | `Form to update a user`        |
| `/users/delete`    | `POST`       | `Suppression d'un utilisateur`   | `message before remove a user` |
| `/contracts`       | `GET`        | `Liste des types de contrats`    | `Contracts list`               |
| `/contracts/add`       | `POST`       | `Ajout d'un type de contrat`         | `Form to add a contract`           |
| `/contracts/update`    | `POST`       | `Modification d'un type de contrat`  | `Form to update a contract`        |
| `/contracts/delete`    | `POST`       | `Suppression d'un type de contrat`   | `message before remove a contract` |
| `/technologies`    | `GET`        | `Liste des technologies`         | `Technologies list`            |
| `/technologies/add`       | `POST`       | `Ajout d'une technologie`         | `Form to add a technology`           |
| `/technologies/update`    | `POST`       | `Modification d'une technologie`  | `Form to update a technology`        |
| `/technologies/delete`    | `POST`       | `Suppression d'une technologie`   | `message before remove a technology` |
| `/salary-brackets` | `GET`        | `Liste des tranches de salaires` | `Salary-brackets list`         |
| `/salary-brackets/add`       | `POST`       | `Ajout d'une tranche de salaire`         | `Form to add a salary-bracket`           |
| `/salary-brackets/update`    | `POST`       | `Modification d'une tranche de salaire`  | `Form to update a salary-bracket`        |
| `/salary-brackets/delete`    | `POST`       | `Suppression d'une tranche de salaire`   | `message before remove a salary-bracket` |
| `/sectors`         | `GET`        | `liste des secteurs d'activités` | `Sectors list`                 |
| `/sectors/add`       | `POST`       | `Ajout d'un secteur d'activité`         | `Form to add a sector`           |
| `/sectors/update`    | `POST`       | `Modification d'un secteur d'activité`  | `Form to update a sector`        |
| `/sectors/delete`    | `POST`       | `Suppression d'un secteur d'activité`   | `message before remove a sector` |

## Endpoints API

| Endpoint             | Méthode HTTP | Description                      | Retour |
| -------------------- | ------------ | -------------------------------- | ------ |
| `/api/v1/feedbacks`  | `GET`        | Get all the feedbacks            | 200    |
| `/api/v1/feedbacks`  | `POST`       | Add a feedback                   | 201 + created Object  |
| `/api/v1/subscribe`  | `POST`       | add new user                     | 201 + created Object |
| `/api/v1/connexion`  | `POST`       | connect user                     | 200 or 401 |
| `/api/v1/connection` | `GET`        | get user to connect and all card | 200    |
| `/api/v1/users/{id}/profil` | `GET`        | get user profil | 200    |
| `/api/v1/users` | `POST`        | add a user | 201 + created object    |
| `/api/v1/users/{id}` | `PUT`        | update a user | 200, 204 or 404    |
| `/api/v1/companies` | `GET`        | get all companies | 200    |
| `/api/v1/companies` | `POST`        | add a company | 201 + created object    |
| `/api/v1/companies/{id}` | `GET`        | get informations of a companies | 200    |
| `/api/v1/companies/{id}` | `PUT`        | update a company | 200, 204 or 404    |
| `/api/v1/addresses/{id}` | `GET`        | get informations of a adress | 200    |
| `/api/v1/addresses` | `POST`        | add a adress | 201 + created object    |
| `/api/v1/addresses/{id}` | `PUT`        | update a address | 200, 204 or 404    |
| `/api/v1/experiences`  | `GET`        | Get all experiences            | 200    |
| `/api/v1/experiences/{id}` | `GET`        | get informations of a experience | 200    |
| `/api/v1/jobs`  | `GET`        | Get all jobs            | 200    |
| `/api/v1/jobs` | `POST`        | add a job | 201 + created object    |
| `/api/v1/jobs/{id}` | `PUT`        | update a job | 200, 204 or 404    |
| `/api/v1/jobs/{id}` | `GET`        | get informations of a job | 200    |
| `/api/v1/jobs/recruiters/{id}` | `GET`        | get all jobs of a recruiter | 200    |
| `/api/v1/jobs/candidate/{id}` | `GET`        | get all jobs of a candidate | 200    |
| `/api/v1/recruiters`  | `GET`        | Get all recruiters            | 200    |
| `/api/v1/recruiters` | `POST`        | add a recruiter | 201 + created object    |
| `/api/v1/recruiters/{id}` | `PUT`        | update a recruiter | 200, 204 or 404    |
| `/api/v1/recruiters/{id}` | `GET`        | get informations of a recruiter | 200    |
| `/api/v1/sectors`  | `GET`        | Get all sectors            | 200    |
| `/api/v1/sectors/{id}` | `GET`        | get informations of a sector | 200    |
| `/api/v1/salary-brackets`  | `GET`        | Get all salary-brackets            | 200    |
| `/api/v1/salary-brackets/{id}` | `GET`        | get informations of a salary-bracket | 200    |
| `/api/v1/technologies`  | `GET`        | Get all technologies            | 200    |
| `/api/v1/technologies/{id}` | `GET`        | get informations of a technology | 200    |
| `/api/v1/contracts`  | `GET`        | Get all contracts            | 200    |
| `/api/v1/contracts/{id}` | `GET`        | get informations of a contract | 200    |
| `/api/v1/candidates`  | `GET`        | Get all candidates            | 200    |
| `/api/v1/candidates` | `POST`        | add a candidate | 201 + created object    |
| `/api/v1/candidates/{id}` | `PUT`        | update a candidate | 200, 204 or 404    |
| `/api/v1/candidates/{id}` | `GET`        | get informations of a candidate | 200    |
| `/api/v1/candidates/{id}/jobs/match`  | `GET`        | Get all jobs matched for a candidate         | 200    |
| `/api/v1/candidates/{id}/jobs/like`  | `GET`        | Get all jobs liked for a candidate         | 200    |

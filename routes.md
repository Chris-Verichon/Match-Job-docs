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
| `/users`           | `GET`        | `Liste des utilisateurs`         | `Users list`                   |
| `/contracts`       | `GET`        | `Liste des types de contrats`    | `Contracts list`               |
| `/technologies`    | `GET`        | `Liste des technologies`         | `Technologies list`            |
| `/salary-brackets` | `GET`        | `Liste des tranches de salaires` | `Salary-brackets list`         |
| `/sectors`         | `GET`        | `liste des secteurs d'activités` | `Sectors list`                 |

## Endpoints API

| Endpoint             | Méthode HTTP | Description                      | Retour |
| -------------------- | ------------ | -------------------------------- | ------ |
| `/api/v1/feedbacks`  | `GET`        | Get all the feedbacks            | 200    |
| `/api/v1/feedbacks`  | `POST`       | Add a feedback                   | 201 + created Object  |
| `/api/v1/subscribe`  | `POST`       | add new user                     | 201 + created Object |
| `/api/v1/connexion`  | `POST`       | connect user                     | 200 or 401 |
| `/api/v1/connection` | `GET`        | get user to connect and all card | 200    |

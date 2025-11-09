# Marmiton

This is a recipe application with a frontend, a backend, and a database.

## Les installations nécessaire

- Docker and Docker Compose

## Lancer le projet

Le gide d'instalation pour lancer les parties de l'application sont dans les readme de ces derniers.

### Avant de lancer le projet

Créer et remplire le .env à partir du message moodle. (Ils ont été enlevé du .gitignore, donc pas besoin, mais je le remets la au cas où)

```bash
DATABASE_USER = "marmitax"
DATABASE_NAME = "marmitax"
DATABASE_PASSWORD = "marmitax"
```

### Build l'application

Open a terminal at the root of the project and run the following command:

```bash
docker compose up -d --build
```

This will build the Docker images for the frontend and backend services and start all the containers in detached mode.

### Acceder à l'application


#### Frontend

 Le front est sur `http://localhost:4173`

#### Backend (Swagger UI)

 Le swagger du back est sur `http://localhost:3000/swagger-ui/index.html`

## Connexion

### Guest

On peut consulter les recettes.

### User

On peut consulter et créer des recettes.
On peut modifier et supprimer ses recettes.

### Admnin

On peut consulter, créer et supprimer des recettes
On a accès à la page admin où on peut valider les recettes en attente
Pour se connecter en tant que Admin, utilisez :

```
email : arthur@arthur
mdp   : arthur
```

## Arreter le projet

Pour areter le projet et supprimer containers, images et volumes (supprimer les images ralentie grandement le temps de lancement, ne pas mettre les flags --rmi all si vous compter relancer) :

```bash
docker compose down -v --rmi 'all'
```

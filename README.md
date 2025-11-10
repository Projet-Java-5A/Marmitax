# Marmiton

This is a recipe application with a frontend, a backend, and a database.

## Les installations nécessaire

- Docker and Docker Compose

## Lancer le projet

Le guide d'installation pour lancer les parties de l'application sont dans les readme de ces derniers.

### Avant de lancer le projet

Créer et remplire le .env à partir du message moodle.

```bash
DATABASE_USER = "marmitax"
DATABASE_NAME = "marmitax"
DATABASE_PASSWORD = "marmitax"
```

### Build l'application

Ouvrir un terminal à la racine du projet et run la commande suivante :

```bash
docker compose up -d --build
```

Cela va créer les images Docker pour le front et le back et démarrer les containers en mode détaché.

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

### Admin

On peut consulter, créer et supprimer des recettes
On a accès à la page admin où on peut valider les recettes en attente
Pour se connecter en tant que Admin, utilisez :

```
email : arthur@arthur
mdp   : arthur
```

## Arreter le projet

Pour arrêter le projet et supprimer containers, images et volumes (supprimer les images ralentie grandement le temps de lancement, ne pas mettre les flags --rmi all si vous compter relancer) :

```bash
docker compose down -v --rmi 'all'
```

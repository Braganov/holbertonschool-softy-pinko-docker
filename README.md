# Projet Softy Pinko Docker

Ce projet se concentre sur l'apprentissage des concepts Docker à travers une série de tâches progressives pour déployer une application web complète avec un front-end, une API et un proxy inverse.

## Structure du Projet

Le projet est organisé en plusieurs tâches, chacune construisant sur la précédente:

- **Tâche 0**: Création d'une image Docker simple basée sur Ubuntu
- **Tâche 1**: Configuration d'une API Flask dans un conteneur
- **Tâche 2**: Configuration séparée des conteneurs front-end et back-end
- **Tâche 3**: Configuration avancée des conteneurs
- **Tâche 4**: Utilisation de docker-compose pour orchestrer les conteneurs
- **Tâche 5**: Ajout d'un proxy inverse pour gérer les requêtes
- **Tâche 6**: Mise en place d'un équilibrage de charge entre plusieurs serveurs API

## Technologies Utilisées

- Docker
- Ubuntu
- Python/Flask pour l'API
- Nginx pour le front-end et le proxy inverse
- Docker Compose pour l'orchestration

## Comment Exécuter le Projet

Chaque tâche peut être exécutée individuellement. Pour la tâche finale avec l'ensemble complet:

```bash
cd task6
docker-compose up --build
```

Accédez à l'application via: http://localhost:8080

## Auteur

[Votre nom]

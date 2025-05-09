# Tâche 4: Orchestration avec Docker Compose

## Description
Cette tâche utilise Docker Compose pour orchestrer les conteneurs front-end et back-end, simplifiant la gestion et le déploiement des services.

## Structure
- **docker-compose.yml**: Fichier de configuration pour Docker Compose

## Fonctionnalités
- Définition des services front-end et back-end dans un seul fichier
- Gestion des dépendances entre services
- Configuration des ports
- Construction automatique des images Docker

## Comment construire et exécuter
```bash
# Construire et démarrer tous les services
docker-compose up --build

# Arrêter tous les services
docker-compose down
```

## Accès aux services
Une fois les conteneurs en cours d'exécution:
- API Back-end: http://localhost:5252
- Front-end: http://localhost:9000

# Tâche 5: Mise en place d'un proxy inverse

## Description
Cette tâche utilise Docker Compose pour orchestrer trois services: le back-end, le front-end et un proxy inverse qui gère les requêtes entrantes et les distribue aux services appropriés.

## Structure
- **docker-compose.yml**: Configuration pour orchestrer les trois services
- **proxy/**: Dossier contenant la configuration du proxy
  - **Dockerfile**: Configuration pour construire l'image du proxy
  - **proxy.conf**: Configuration Nginx pour le proxy inverse

## Fonctionnalités
- Accès unifié à l'application via le proxy (port 80)
- Redirection des requêtes API vers le back-end
- Redirection des requêtes générales vers le front-end
- Isolation des services internes (seul le proxy est exposé)

## Comment construire et exécuter
```bash
# Construire et démarrer tous les services
docker-compose up --build

# Arrêter tous les services
docker-compose down
```

## Accès à l'application
Une fois les conteneurs en cours d'exécution:
- Application complète: http://localhost
- API: http://localhost/api

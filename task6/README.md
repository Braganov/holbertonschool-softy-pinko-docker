# Tâche 6: Équilibrage de charge avec plusieurs serveurs API

## Description
Cette tâche étend la tâche 5 en ajoutant l'équilibrage de charge pour les serveurs API. La configuration permet de démarrer plusieurs instances du service back-end et utilise l'algorithme Round Robin pour distribuer les requêtes entre elles.

## Structure
- **docker-compose.yml**: Configuration pour orchestrer les services avec possibilité de scaling
- **2-api-servers.txt**: Commande pour démarrer les services avec 2 instances du back-end
- **proxy/**: Dossier contenant la configuration du proxy avec équilibrage de charge
  - **Dockerfile**: Configuration pour construire l'image du proxy
  - **proxy.conf**: Configuration Nginx pour le proxy inverse et l'équilibrage de charge

## Fonctionnalités
- Accès unifié à l'application via le proxy (port 80)
- Équilibrage de charge entre plusieurs instances du service back-end
- Utilisation de l'algorithme Round Robin pour la distribution des requêtes
- Isolation des services internes (seul le proxy est exposé)

## Comment construire et exécuter
```bash
# Construire et démarrer avec 2 instances du back-end
docker-compose up --build --scale back-end=2

# Arrêter tous les services
docker-compose down
```

## Accès à l'application
Une fois les conteneurs en cours d'exécution:
- Application complète: http://localhost
- API: http://localhost/api (répartie entre les instances API)

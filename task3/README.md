# Tâche 3: Configuration avancée des conteneurs

## Description
Cette tâche étend la tâche 2 avec des configurations plus avancées pour les conteneurs du front-end et du back-end.

## Structure
Identique à la tâche 2, avec des optimisations dans les Dockerfiles.

### Back-end
- **Dockerfile**: Configuration optimisée pour le serveur API
- **api.py**: Script Python de l'API Flask

### Front-end
- **Dockerfile**: Configuration optimisée pour le serveur web
- **softy-pinko-front-end.conf**: Configuration Nginx avancée

## Comment construire et exécuter
```bash
# Back-end
cd back-end
docker build -f ./Dockerfile -t softy-pinko-back-end:task3 .
docker run -p 5252:5252 --rm --name softy-pinko-be-task3 softy-pinko-back-end:task3

# Front-end
cd ../front-end
docker build -f ./Dockerfile -t softy-pinko-front-end:task3 .
docker run -p 9000:9000 --rm --name softy-pinko-fe-task3 softy-pinko-front-end:task3
```

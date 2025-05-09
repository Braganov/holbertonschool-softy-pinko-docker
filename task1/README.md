# Tâche 1: API Flask dans un conteneur Docker

## Description
Cette tâche consiste à créer une image Docker qui exécute une API Flask simple.

## Structure
- **Dockerfile**: Fichier de configuration pour construire l'image Docker
- **api.py**: Script Python contenant le code de l'API Flask

## Fonctionnalités
- Basé sur la dernière version d'Ubuntu
- Installation de Python 3 et pip
- Installation de Flask
- Configuration et exécution de l'API Flask

## Comment construire et exécuter
```bash
# Construire l'image
docker build -f ./Dockerfile -t softy-pinko:task1 .

# Exécuter le conteneur
docker run -p 5252:5252 --rm --name softy-pinko-task1 softy-pinko:task1
```

## Accès à l'API
Une fois le conteneur en cours d'exécution, l'API sera accessible à l'adresse:
```
http://localhost:5252
```

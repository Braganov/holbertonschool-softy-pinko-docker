# Tâche 2: Conteneurs séparés pour le front-end et le back-end

## Description
Cette tâche consiste à créer deux images Docker distinctes:
1. Une pour le serveur back-end (API Flask)
2. Une pour le serveur front-end (Nginx servant des fichiers statiques)

## Structure
### Back-end
- **Dockerfile**: Fichier de configuration pour construire l'image du back-end
- **api.py**: Script Python contenant le code de l'API Flask

### Front-end
- **Dockerfile**: Fichier de configuration pour construire l'image du front-end
- **softy-pinko-front-end.conf**: Configuration Nginx pour servir le front-end

## Fonctionnalités
- **Back-end**: API Flask s'exécutant sur le port 5252
- **Front-end**: Serveur Nginx s'exécutant sur le port 9000 et servant du contenu statique

## Comment construire et exécuter
```bash
# Back-end
cd back-end
docker build -f ./Dockerfile -t softy-pinko-back-end:task2 .
docker run -p 5252:5252 --rm --name softy-pinko-be-task2 softy-pinko-back-end:task2

# Front-end
cd ../front-end
docker build -f ./Dockerfile -t softy-pinko-front-end:task2 .
docker run -p 9000:9000 --rm --name softy-pinko-fe-task2 softy-pinko-front-end:task2
```

## Accès aux services
Une fois les conteneurs en cours d'exécution:
- API Back-end: http://localhost:5252
- Front-end: http://localhost:9000

# Tâche 0: Création de la première image Docker

## Description
Cette tâche consiste à créer une image Docker de base utilisant Ubuntu, qui affiche simplement "Hello, World!" lorsqu'elle est exécutée.

## Structure
- **Dockerfile**: Fichier de configuration pour construire l'image Docker

## Fonctionnalités
- Basé sur la dernière version d'Ubuntu
- Met à jour les paquets via APT
- Met à niveau les logiciels installés
- Affiche "Hello, World!" lors de l'exécution

## Comment construire et exécuter
```bash
# Construire l'image
docker build -f ./Dockerfile -t softy-pinko:task0 .

# Exécuter le conteneur
docker run -it --rm --name softy-pinko-task0 softy-pinko:task0
```

## Résultat attendu
```
Hello, World!
```

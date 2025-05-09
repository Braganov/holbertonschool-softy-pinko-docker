# Utilise l'image Ubuntu la plus récente comme base
FROM ubuntu:latest

# Met à jour la liste des paquets disponibles
RUN apt-get update
# Met à niveau tous les paquets installés
RUN apt-get upgrade -y

# Commande exécutée au démarrage du conteneur pour afficher "Hello, World!"
CMD ["echo", "Hello, World!"]
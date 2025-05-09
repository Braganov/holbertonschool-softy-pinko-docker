# Utilise l'image Ubuntu la plus récente comme base
FROM ubuntu:latest

# Met à jour la liste des paquets disponibles
RUN apt-get update
# Met à niveau tous les paquets installés
RUN apt-get upgrade -y
# Installe Python3 et pip pour exécuter l'API Flask
RUN apt-get install -y python3 python3-pip

# Supprime le fichier EXTERNALLY-MANAGED pour permettre l'installation de packages via pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
# Installe le framework Flask pour l'API
RUN pip3 install flask

# Définit le répertoire de travail pour l'application
WORKDIR /app
# Copie le fichier d'API Python dans le conteneur
COPY ./api.py /app/api.py

# Commande pour démarrer le serveur API Flask
CMD ["python3", "api.py"]
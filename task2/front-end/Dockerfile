# Utilise l'image Nginx Alpine comme serveur web (plus légère et sécurisée)
FROM nginx:alpine

# Copie les fichiers statiques du front-end dans le répertoire de serveur web Nginx
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end
# Copie le fichier de configuration Nginx pour le front-end
COPY ./softy-pinko-front-end.conf  /etc/nginx/conf.d/default.conf
# Angularimage

#Creer un projet angular nommé angularimage avec la commande:

 ng new angularimage

# On crée un nouveau dossier appelé dist/angularimage dans lequel 
les fichiers compilés sont placé:

ng build 

#Créer un fichier Dockerfile dans la racine du projet
-premier à obtenir uneimage Docker nginx de Docker Hubétiquetée 
avec alpine (c’est comme un numéro de version),
-et enfin copier-coller l’application compilée
(nous l’avons fait à l’étape précédente) dans le conteneur.

FROM nginx:alpine
COPY /dist/angularimage /usr/share/nginx/html

# Créer l' image nommée imageanguler:

docker build -t imageanguler

# Executerr l' image nommée imageanguler:

docker run --name container_angular -d -p 8080:80 imageanguler

C'est OK

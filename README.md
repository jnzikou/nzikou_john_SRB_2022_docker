# nzikou_john_SRB_2022_docker
# Déploiement via Docker-compose
Ce projet à pour objectif de déployer des services sous 3 parties frontend (react.js), backend (node.js) et la base de donnée Mongo DB. Cela nous permet de mettre en conteneur les services.

## Dockerfiles
Dans ce projet, le dockerfile va être unique pour les dépots frontend et backend.
```Javascript
FROM node:lts-alpine
WORKDIR /usr/src/server
ADD . .

RUN yarn install

EXPOSE 8080

CMD [ "node", "server.js" ]
```
Le dockerfile ci-dessus permet de copier les fichiers dans l'image. Toute les dépendances sont aussi installées.
## Docker-Compose
Il se trouve à la racine du du projet. Il va permettre de mettre en relation les 3 services afin de les démarrer correctement. De lancer les conteneurs correctement.

### A retenir
Se projet nous permet de voir comment est construit un conteneur, ainsi comment nous pouvons le structurer.

## ♥ Lister les conteneurs en cours d’exécution :
docker ps

## ♥ Télécharger et lancer un conteneur Nginx :
docker run -d -p 8080:80 nginx

## ♥ Arrêter un conteneur :
docker stop [container_id]

## ♥ Redémarrer le conteneur :
docker start [container_id]

## ♥ Lister les conteneurs arrêtés (tous les conteneurs y compris ceux qui sont arrêtés) :
docker ps -a

## ♥ Supprimer le conteneur (si plus besoin) :
docker rm [container_id]

## ♥ Construit une image Docker à partir d’un Dockerfile :
docker build

## ♥ Lister les images existantes :
 docker image ls 

## ♥ Lister les conteneurs :
 docker container ls -a
 
## ♥ Lancer ou créer le conteneur alpine :
 docker run alpine:latest 

## ♥ Lancer ou créer le conteneur alpine, le nommer alpinetestet le laisser fonctionner (mode DetachInteractive) :
 docker run -di --name alpinetest alpine:latest 
 
## ♥ Comme au dessus mais en plus on conserve un process qui tourne sur le conteneur :
docker run -di --name alpinetest alpine:latest sleep infinity 

## ♥ Lancer le conteneur nginx, le nommer monnginx, le laisser fonctionner. Rediriger son port 80 sur le 8080 de notre machine locale :
docker run -tid -p 8080:80 --name monnginx nginx:latest  

## ♥ Lancer un conteneur alpine que l'on nomme conteneur2, le linker avec conteneur1 (conteneur2 pourra pinguer conteneur1) :
docker run -tid --name conteneur2 --link conteneur1 alpine

## ♥ Redémarrer un conteneur arrêté :
docker start monconteneur 

## ♥ Accéder à un conteneur en cours d'exécution pour exécuter des commandes directement à l'intérieur (comme si tu te connectais à une machine virtuelle) :
docker exec -it [nom_du_conteneur] bash

## ♥ Se connecter au conteneur nommé monnginx avec le shell et le bach :
docker exec -ti monnginx sh 

## ♥ Arrêter un conteneur :
docker stop <nom du conteneur> 

## ♥ Tuer tous les conteneurs :
docker container kill $(docker ps -q)

## ♥ Supprimer un conteneur (-f permet de forcer, même si le conteneur tourne) :
docker rm -f <nom du conteneur> 

## ♥ Supprimer tous les conteneurs :
docker rm $(docker ps -a -q) 

## ♥ Obtenir les infos sur un conteneur :
docker inspect <nom du conteneur> 

## ♥ Obtenir l'ip d'un conteneur :
docker inspect-f "{{.NetworkSettings.IPAddress}}" <nom du conteneur> 

## ♥ Démarre les conteneurs définis dans docker-compose.yml. S'ils n'existent pas encore, Docker les créera :
docker compose up

## ♥ Arrête et supprime les conteneurs :
docker compose down

## ♥ Accéder aux logs d'un conteneur :
docker compose logs <nom_du_conteneur>

## ♥ Accéder aux logs d'un conteneur et suivre en temps réel :
docker compose logs -f <nom_du_conteneur>

## ♥ Envoyer une requête à l'API pour tester la connexion avec utilisateurs fournis :
-Ouvre Postman.
-Clique sur "New" pour créer une nouvelle requête.
-Méthode HTTP : Sélectionne "POST".
-URL : Entre https://localhost/api/authentication.
-Headers : Ajoute un header "Content-Type": "application/json".
-Body : Sélectionne "raw" et choisis "JSON", puis entre :
json
-Copier le code
{
  "username": "user1@local.host",
  "password": "my_password"
}
-Clique sur Send.

## ♥ Me connecter au terminal d'une VM via mon PowerShell Windows :
ssh -p 2222 root@127.0.0.1
ps aux | grep python

♥ Voir les jobs en arrière-plan :
jobs -l



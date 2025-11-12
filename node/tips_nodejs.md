/!\ Un fichier "app.js" est nécessaire pour démarrer un projet Node js 
## ♥ Installer bibliothèques Node.js et npm (terminal):
npm init -y  
npm install express jsonwebtoken body-parser cors  

## ♥ Initialiser un projet Node.js (va créer mon package.json) :
npm init -y  

## ♥ Exécuter le serveur (dans le terminal) :
node app.js  

## ♥ Importer un module Node.js :
const http = require('http');// Module http pour créer un serveur  
const fs = require('fs'); // Module pour interagir avec le système de fichiers (file system)  
const url = require('url');// Module pour analyser l'URL des requêtes  
const crypto = require('crypto');// Module pour générer des identifiants uniques (comme pour les sessions)  

## ♥ Créer un serveur HTTP :

## ♥ Démarrer le serveur sur le port 3000 :
server.listen(3000, () => {  
  console.log('Serveur démarré sur http://localhost:3000');  
});

## ♥ Vérifier que Node js est bien installé :
Node --version  
ET  
npm --version

## ♥ Mettre à jour la version de npm :
npm install -g npm@lates  

## ♥ Installer une bibliothèque (ici les bibliothèques express, jsonwebtoken et body-parser):
npm install express jsonwebtoken body-parser  


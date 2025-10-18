## ♥ Commencer mon fichier:
body {
	margin: 0px 50px
}

a {
	text-decoration: none;
}

## ♥ Mettre une ombre sur une image PNG:
-webkit-filter: drop-shadow(

 50% {
 
 }

 To {
 
 }
}

## ♥ Faire du responsive design:
• Ajouter en <head> du HTML (Pour que les media queries fonctionnent correctement sur les appareils mobiles): 
<meta name="viewport" content="width=device-width, initial-scale=1.0">

• Ajouter en CSS: 
@media (max-width: 767px) {/*Mobile (paysage)*/
    /*CONTENU CSS*/
}

@media (max-width: 480px) {/*Mobile (portrait)*/
    /*CONTENU CSS*/
}

@media (min-width: 768px) and (max-width: 1024px) {/*Tablettes*/
    /*CONTENU CSS*/
}

@media (min-width: 1025px) {/*Desktop standard*/
    /*CONTENU CSS*/
}

@media (min-width: 1440px) {/*Grands écrans*/
    /*CONTENU CSS*/
}

• Ajuster la taille d'un élément dans un media queries :
.item {
    flex: 1 1 calc(50% - 20px); /* Ajuste automatiquement la taille */
}

## ♥ Ombre dedans et diffusée:
box-shadow: inset 0 0 1em gold, 0 0 2em red;

## ♥ Flouter le background:
backdrop-filter: blur(2px)

## ♥ Pour enlever les puces des li :
list-style-type: none;
2px 1px 10px #ff49cb);
filter: drop-shadow(2px 1px 10px #ff49cb);

♥ Importer une font (police d'écriture):
@font-face {
    font-family: "Vintage King";
    src: url("/font/VintageKing.ttf") format("

## ♥ Commencer une page HTML :
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8"> <!-- Définit le jeu de caractères -->
    <meta name="description" content="Description de la page"/>
    <meta name="viewport" content="width=device-width, initial-scale=1"> <!-- Assure la compatibilité avec les écrans de différentes tailles -->
    
    <title>Titre de la page</title>
    <link rel="stylesheet" href="votre-fichier.css" type="text/css">
    <link rel="shortcut icon" href="lien-vers-image.png" type="image/png"> <!-- Icône de la page -->
    
    <meta name="robots" content="index,follow"> <!-- Indique aux robots d'indexer et de suivre les liens -->
</head>
<body>
    <!-- Contenu de la page -->

    <noscript>
        Message qui apparait si JavaScript est désactivé sur le navigateur de l'utilisateur
    </noscript>

    <script src="votre-script.js" defer></script> <!-- Charger le script JavaScript avec defer -->
</body>
</html>


## ♥ Point d'ancrage:
Mettre dans la balise concernée par l'ancrage : name="NOMDELANCRE"
Mettre dans le lien vers l'ancre: <a href="Page1.html#NOMDELANCRE">

## ♥ La création de tableaux:
On ouvre la balise <table> qui nous permet de coder le tableau à l'intérieur.
<caption> : l'élément de légende d'un tableau (toujours premier descendant de <table>)
<tr> : l'élément de ligne d'un tableau
<th> : l'élément d'en-tête de tableau (dans l'élément <tr>)
<td> : l'élément de cellule de tableau (dans l'élément <tr>)

## ♥ Faire des listes:
<ul> : Insérer la liste (porte <li> et <ol> à l'intérieur)

## ♥ Faire une sélection:
<label for="pet-select">Choose a pet:</label>

<select name="pets" id="pet-select">
    <option value="">--Please choose an option--</option>
    <option value="dog">Dog</option>
    <option value="cat">Cat</option>
</select>

## ♥ Faire un formulaire:
<form action="" method="get" class="form-example">
    <label for="name">Enter your name: </label>
    <input type="text" name="name" id="name" required />
    <label for="email">Enter your email: </label>
    <input type="email" name="email" id="email" required />
    <input type="submit" value="Subscribe!" />
    <input type="checkbox" id="scales" name="scales" checked />
    <label for="scales">Scales</label>
  <label for="story">Tell us your story:</label>
  <textarea id="story" name="story" rows="5" cols="33">
  It was a dark and stormy night...
  </textarea>
</form>

## ♥ Boutons radio:
<input type="radio" id="huey" name="drone" value="huey" checked />
<label for="huey">Huey</label>



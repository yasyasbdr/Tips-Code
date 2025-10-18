## ♥ Déclarer une variable: 
maVariable;
var maVariable;
let maVariable;
const maVariable;

## ♥ Créer une fonction: 
function carré(nombre) {
  return nombre * nombre;
}

## ♥ les incrémentations:
Ecrire "i++" c'est ajouter 1 à la variable i.
Ecrite "i+=1" c'est ajouté 1 à ce que i est déjà (i = i + 1)

## ♥ Les signes:
Ecrire "=" assigne une valeur.
Ecrire "==" vérifie l'égalité même si le type est différent.
Ecrire "===" Teste si les valeurs de droite et de gauche sont identiques.
Ecrire "!==" Non-égalité stricte
Ecrire "&&" Renvoie vrai si et uniquement si ses deux opérandes sont true ou équivalents à true.
Ecrire "||" Renvoie vrai si et seulement si au moins un de ses opérandes est vrai.

## ♥ Changer le style d'un élément HTML:
document.getElementById("monID").style.backgroundColor = "blue";
document.getElementById("monID").style.width = "blue";

## ♥ Retirer une classe:
document.getElementById("my-div").classList.remove("fade");
document.getElementById("monID").classList.toggle('maClass');

## ♥ Ajouter une classe :
document.getElementById("my-div").classList.add("fade");
document.getElementById("monID").classList.toggle('maClass');

## ♥ Effectuer une fontion au bout d'un certain temps:
setTimeout(() => {
 document.getElementById("my-div").classList.remove("fade");
 }, 1000);

## ♥ Changer contenu d'un élément HTML:
document.getElementById("monSpan").innerText = "texte";
document.getElementById("monSpan").innerHTML ="<span>Hello!</span>";

## ♥ Prendre l'entrée d'un champ formulaire:
const val = document.querySelector('input').value;
console.log(val);

## ♥ Condition if:
if(maVariable){
 console.log("le IF");
}
else if (maVariable === 2){
 console.log("le ELSE IF");
}
else {
 console.log("le ELSE");
}

## ♥ Condition switch:
const expr = 'Papayas';
switch (expr) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    // Expected output: "Mangoes and papayas are $2.79 a pound."
    break;
  default:
    console.log(`Sorry, we are out of ${expr}.`);
}

## ♥ Additioner les valeurs de variables sans concaténation:
${nomvariable1 + nomvariable2 + nomvariable3}

## ♥ Désactiver une checkbox:
getElementById("myCheck").disabled = true;

## ♥ Boucle for:
for (let i = 0; i< array.length; i++) {
 const element = array[i];
 console.log("Le for");
}

## ♥ Désactiver ou activer un bouton:
document.querySelector('#button').disabled = true;
//ou
document.querySelector('#button').disabled = false;

## ♥ Retirer un attribut:
document.getElementById("boutonRechercher").removeAttribute("title");

## ♥ Prendre une date depuis un calendrier input:
//Ici l'id de l'input est dateDeDebut
dateDeDebut= new Date(document.getElementById("dateDeDebut").value);//Récupération de la valeur de l'input
console.log("Date de début: ",dateDeDebut);

## ♥ Mettre une date au format français:
//D'abord créer une date, ici ma date est dateDeDebut
let dateDeDebutLocale = dateDeDebut.toLocaleString('fr-FR',{weekday:'long',year:'numeric',month:'long',day:'numeric'});


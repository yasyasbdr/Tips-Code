## ♥ Créer un nouveau projet (ouvrir terminal dans fichier du nouveau projet):
Taper dans l'ordre:
- initialiser un nouveau projet : npm init -y
- Installer TypeScript : npm install typescript --save-dev

## ♥ Créer une variable:
const age: number = 10;

## ♥ Compiler un projet (avec le terminal):
tsc -p [chemin dossier]/tsconfig.json (Le résultat se retrouve dans out/.)

## ♥ Compiler un fichier ts:
npx tsc nomdufichier.ts

## ♥ Contenu du tsconfig.json à mettre dans le dossier du projet:
{
    "compilerOptions": {
      "target": "ES5",
      "module": "commonjs",
      "sourceMap": true,
      "outDir":"out",
      /*Si besoin:*/"strict": true
    }
}


## ♥ Créer une classe:
class Voiture {
	public position: number = 0;
	private vitesse: number = 42;

	seDeplacer() {
		this.position += this.vitesse;
	}
}

/*(Ici on déclare la classe simple Voiture. La classe a trois membres: vitesse propriété privée, une position propriété publique et un seDeplacer() méthode publique. Chaque membre est public par défaut. )*/


## ♥ Utilisation d'une classe (ici Voiture):
// Création d'une instance de la classe Voiture
var auto1 = new Car();
// Appel de la méthode
auto1.seDeplacer(); 
// Accès aux members public
console.log(auto1.position); 


## ♥ Créer une sous-classe (ici Taxi):
class Taxi extends Vehicule {
private numLicence: string;
seDeplacer() {
super.seDeplacer;
super.seDeplacer
}
}
/*(La sous-classe Taxi spécialise la classe Vehicule, en ajoutant un attribut privé (numLicence) et en surchargeant la méthode seDeplacer(). Pour que la sous-classe accède aux membres (Attributs et méthodes) de la classe, il faut qu'ils soient public ou protected.)*/


## ♥ Créer un constructeur (ici dans notre classe Voiture):
class Voiture {
public position: number = 0;
protected vitesse: number = 42;

constructor(position: number, vitesse: number) {
this.position = position;
this.vitesse = vitesse;
}

seDeplacer() {
this.position += this.vitesse;
}
}
/*(Le constructeur d'une classe est la méthode qui permet de créer les objets d'une classe. La méthode se nomme constructor et possède propriétés, appelés des paramètres.)*/
//ou
class Voiture {
constructor(public position: number, protected Vitesse : number) {}

seDeplacer() {
this.position += this.vitesse;
}
}


## ♥ Créer une fonction:
function damage(characterToDamage, amount: number): number {
    characterToDamage.life -= amount;
    return characterToDamage.life;
}
const result = damage({ life: 100 }, 12);
console.log(result);


## ♥ Créer un type (alias):
// On définit deux alias Money et Age, pour qu’ils soient identiques à 'number'
type Money = number;
type Age = number;
type CodeSecret = string | number; // le type CodeSecret peut contenir du texte ou des nombres


## ♥ Déclarer un objet:
{ nomobjet: typeobjet/*(number, string, etc)*/; };
//Exemple de déclaration d'objet dans des types:
type Character = {
    name: string;
    life: number;
    attack: number;
    defense: number;
};

type Pet = Character;

type Hero = Character & {
    pet?: Pet;
};//?  sur la dernière propriété de Hero: indique que pet est optionnelle. Un objet Hero  sera ainsi valide, qu’il ait ou non un animal de compagnie.
};

type Hero = Character & {
    pet?: Pet;
};
//Pour rendre ce code moins répétitif, nous pouvons créer un type intermédiaire contenant toutes les propriétés en commun, que nous appellerons dans cet exemple Character:
interface Character {
    name: string;
    life: number;
    attack: number;
    defense: number;
};
type Pet = Character;
interface Hero extends Character {
    pet?: Pet;
};


## ♥ Créer un tableau avec type:
type MyArrayOfNumbers = number[]; // Définition d'un tableau de nombres
// Que des nombres, c'est OK !
const arrayOk: MyArrayOfNumbers = [1, 2, 3]; //ou type MyArrayOfNumbers = Array<number>;
// Autre chose que des nombres : erreur TypeScript !
const arrayNotOk: MyArrayOfNumbers = [1, 'two', false];


## ♥ Transformer un type en générique:
type Shop<ItemType> = { /* … */  };

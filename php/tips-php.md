<!DOCTYPE html>
♥ Commencer mon fichier:
<html>
<head>
	<title>Ma page PHP</title>
</head>

<body>
<?php echo'voici ma partie en php'; ?>
</body>
</html>

♥ Aller à la ligne:
echo '\n';
ou
echo '<br/>';

♥ Afficher des guillemets (ou tout autre signe/symbole) dans un texte:
<?php echo "Cette ligne a été écrite \"uniquement\" en PHP."; ?>


♥ Les variables:
string, pour le texte (ex:"Mathieu", avec guillemets)
int, pour les nombres entiers sans virgule (ex:-3)
float, pour les nombres à virgule (ex:14.738, attention, les nombres doivent être écrits avec un point au lieu de la virgule)
bool, pour vrai ou faux (ex:true, sans guillemets !!)
null, quand pas de type de donnée, absence de type (NULL)


♥ Créer une variable:
$userAge = 17;


♥ Incrémentation d'une variable:
$nomvariable++


♥ Avoir le résultat au carré (²):
$variable = 10;
$variable ** 2

SORTIE -> 100


♥ Avoir le résultat absolu:
$variable = null;
$variable = abs(10);
echo $variable;

SORTIE -> 10


♥ Avoir le résultat arrondi:
$variable = null;
$variable = round(4.99);
echo $variable;
SORTIE -> 5

//OU arrondir à 2 chiffres après la virgule
$variable = 50.25689;
$variable = round($variable,2);
SORTIE -> 50.25

♥ Avoir le résultat arrondi à l'inférieur:
$variable = null;
$variable = round(4.99);
echo $variable;

SORTIE -> 4


♥ Avoir le résultat arrondi au supérieur:
$variable = null;
$variable = ceil(4.49);
echo $variable;

SORTIE -> 5


♥ Avoir la plus grande valeur entre 3 variables/valeurs:
$x = 30;
$y = 60;
$z = 10;
$total = max($x, $y, $z);

echo $total;

SORTIE -> 60


♥ Avoir la plus petite valeur entre 3 variables/valeurs:
$x = 30;
$y = 60;
$z = 10;
$total = min($x, $y, $z);

echo $total;

SORTIE -> 10


♥ Avoir une valeur au hasard (aléatoire):
$total = rand();
echo $total;
SORTIE -> un nombre aléatoire jusqu'à 2 million

//OU

$total = rand(90, 100);
echo $total;
SORTIE -> un nombre aléatoire entre 90 et 100.


♥ Enregistrer infos formulaire dans une page de traitement:
<?php
    // Récupère les valeurs du formulaire dans des variables (on prend ce qu'on a mis comme name !)
    $nom = $_POST["Nom"];
    $email = $_POST["Email"];
    $numero = $_POST["Message"];

    // Redirige vers la page de confirmation
    header("Location: confirmation.php");
    exit();
?>

♥ Afficher des données issues d'un formulaire:
Bonjour, <?php echo htmlspecialchars($_POST['nom']); ?>.
Tu as <?php echo (int)$_POST['age']; ?> ans.


♥ Afficher la date:
echo date('l d/m/Y h:i:s');


♥ Imprimer contenu d'une variable:
$fullname = 'Yasmine Badarou';
echo 'Bonjour ' . $fullname . ', bienvenue sur le site.';


♥ Symboles à connaître:
== : Est égal à
> : Est supérieur à
< : Est inférieur à
>= : Est supérieur ou égal à
<= : Est inférieur ou égal à
!= : Est différent de
AND: &&
OR: ||
!: inverse le résultat d'une opération booléenne ('true' devient 'false' et inversement)


♥ Faire une 
    else {
        echo "You must be 18+ to enter this site";
    }


♥ Condition avec une variable booléenne:
$isAllowedToEnter = true;

if ($isAllowedToEnter) {//vérifier si true
    echo "Bienvenue petit nouveau. :o)";
}

//OU

if (! $isAllowedToEnter) {//vérifier si false

}


♥ Condition avec && (Les deux conditions sont vraies):
$isEnabled = true;
$isOwner = false;

if ($isEnabled && $isOwner) {
    echo 'Accès à la recette validé ✅';
} else {
    echo 'Accès à la recette interdit ! ❌';


♥ Condition avec || (Au moins une des condition est vraie):
$isEnabled = true;
$isOwner = false;
$isAdmin = true;

if (($isEnabled && $isOwner) || $isAdmin) {
    echo 'Accès à la recette validé ✅';
} else {
    echo 'Accès à la recette interdit ! ❌';
}
//soit la première condition s'applique, soit l'utilisateur concerné est un administrateur


♥ Condition avec Switch (remplace l'utilisation de plein de elseif):
$yasmine = 20;

switch ($yasmine) {// indiquer variable, le switch teste l'égalité
    case "20":
        echo"tu viens d'avoir la vingtaine";
        break;
    case "15":
        echo"dans 5 ans tu dépassera la vingtaine";
        break;
    case "10":
        echo"il te reste un bon bout de temps pour atteindre la vingtaine.";
        break;
        case "1":
            echo"Tu as {$yasmine} an. Je ne te donne de réponse qu'à tes 10, 15 ou 20 ans";
            break;
    default://équivalent de else
        echo"Tu as {$yasmine} ans. Je ne te donne de réponse qu'à tes 10, 15 ou 20 ans";
}


♥ Boucle While ("tant que"):
$lines = 3; // lire les 3 premières lignes du tableau
$counter = 0;

while ($counter < $lines) {//TANT QUE $counter < $lines est vrai, exécuter les instructions
    echo $users[$counter][0] . ' ' . $users[$counter][1] . '<br />';
    $counter++; // Counter augmente à chaque fois

//AUTRE EXEMPLE

$lines = 1;

while ($lines <= 100) {//TANT QUE $lines est inférieur ou égal à 100
    echo 'Je ne dois pas regarder les mouches voler quand j\'apprends le PHP.<br />';
    $lines++; // $lines = $lines + 1 (incrémentation)
}


//AUTRE EXEMPLE

$lines = 1;

while ($lines <= 100)
{
    echo 'Ceci est la ligne n°' . $lines . '<br />';
    $lines++;
}


♥ Boucle For:
$i=0;

for($i=0/*la variable $lines par de 0 pour exécuter le code*/; $i < 5/*condition pour exécuter le code. Dès qu'on sort de cette condition le code ne s'exécute plus.*/; $i++/*Ajoute +1 à la variable à chaque exécution de la boucle.*/) {
    echo "<div style=\"width:10px; height:10px; background-color:red; margin: 10px;\"></div>";
}

//OU ON PEUT MÊME AFFICHER CERTAINES VALEURS D'UN TABLEAU

<?php
$recipes = [
    ['Cassoulet','[...]','mickael.andrieu@exemple.com',true,],
    ['Couscous','[...]','mickael.andrieu@exemple.com',false,],
];?>

<?php for ($lines = 0; $lines <= 1; $lines++): ?>
<li><?php echo $recipes[$lines][0] . ' (' . $recipes[$lines][2] . ')'; ?></li>
<?php endfor; ?>


♥ Boucle For ou boucle While ?
while  est plus simple et plus flexible : on peut faire tous les types de boucles avec, mais on peut oublier de faire certaines étapes, comme l'incrémentation de la variable.

for  est bien adapté quand on doit compter le nombre de fois que l'on répète les instructions, et il permet de ne pas oublier de faire l'incrémentation pour augmenter la valeur de la variable !

Il suffit simplement de vous poser la question suivante : « Est-ce que je sais d'avance combien de fois je veux que mes instructions soient répétées ? ».

Si la réponse est oui, alors la boucle for  est tout indiquée.

Sinon, alors il vaut mieux utiliser la boucle while .


♥ Afficher le contenu d'un tableau à l'aide de la boucle For:
//Chaque élément du tableau est un tableau numéroté
$recipes = [
    ['Cassoulet','[...]','mickael.andrieu@exemple.com',true,],
    ['Couscous','[...]','mickael.andrieu@exemple.com',false,],
];

for ($lines = 0; $lines <= 1; $lines++) {//Si $lines vaut 1, cela signifie qu'on cherche ce que contient $recipes[1][0] , c'est-à-dire : Couscous
    echo $recipes[$lines][0];
}


♥ Afficher le contenu d'un tableau à l'aide de la boucle Foreach:
$recipes = [
    ['Cassoulet','[...]','mickael.andrieu@exemple.com',true,],
    ['Couscous','[...]','mickael.andrieu@exemple.com',false,],
];

foreach ($recipes as $recipe) {
    echo $recipe[0]; // Affichera Cassoulet, puis Couscous
}

//OU AVEC UN TABLEAU ASSOCIATIF

$recipe = [
    'title' => 'Cassoulet',
    'recipe' => 'Etape 1 : des flageolets, Etape 2 : ...',
    'author' => 'mickael.andrieu@exemple.com',
    'enabled' => true,
];

foreach ($recipe as $value) {
    echo $value;
}/*nom du tableau ici $recipe, mot-clé as (= "en tant que"), nom d'une variable au choix contenant tour à tour chaque valeur du tableau, ici $value.*/


♥ Créer un tableau :
$recipes = ['Cassoulet', 'Couscous', 'Escalope Milanaise', 'Salade César',];

// La fonction array permet aussi de créer un tableau
$recipes = array('Cassoulet', 'Couscous', 'Escalope Milanaise');


♥Afficher le contenu d'un array :
$foods = array("apple", "orange","banana", "coconut"); 

foreach($foods as $food) {
echo $food;
}


♥Ajouter (push) des cases à la fin du tableau :
array_push($nomdutableau, "pineapple", "mango");


♥Supprimer la dernière case du tableau :
array_pop($nomdutableau);


♥Supprimer la première case du tableau :
array_shift($nomdutableau);


♥Inverser le sens d'un tableau :
$nomvariablereverse = array_reverse($foods);

//pour l'afficher :
foreach($nomvariablereverse as $food) {
echo $food . "<br>";
}


♥Afficher le nombre de cases dans un tableau :
echo count($nomdutableau);


♥ Créer un tableau de tableau :
//Tableaux de base :
$mickael = ['Mickaël Andrieu', 'mickael.andrieu@exemple.com', 'S3cr3t', 34];
$mathieu = ['Mathieu Nebra', 'mathieu.nebra@exemple.com', 'devine', 33];
$laurene = ['Laurène Castor', 'laurene.castor@exemple.com', 'P4ssw0rD', 28];

//Tableau users de tableaux mickael, mathieu et laurene
$users = [$mickael, $mathieu, $laurene];

echo $users[1][1]; // "mathieu.nebra@exemple.com"


♥ Créer manuellement un tableau, case par case:
$recipes[0] = 'Cassoulet';
$recipes[1] = 'Couscous';
$recipes[2] = 'Escalope Milanaise';
//OU
$recipes[] = 'Cassoulet'; // Créera $recipes[0]
$recipes[] = 'Couscous'; // Créera $recipes[1]
$recipes[] = 'Escalope Milanaise'; // Créera $recipes[2]
//OU ASSOCIATIF
<?php
$recipe['title'] = 'Cassoulet';
$recipe['recipe'] = 'Etape 1';
$recipe['author'] = 'john.doe@exemple.com';
$recipe['enable'] = true;
?>


♥ Créer un tableau associatif:
$recipe = [
    'title' => 'Cassoulet',
    'recipe' => 'Etape 1',
    'author' => 'john.doe@exemple.com',
    'enabled' => true,
];
//OU :
$capitals = array(


♥ Calcul des valeurs d'un tableau:
function calcul($x) { //On crée fonction calcul ayant paramètre $x
    $x=$x*2;//$x multiplié /2 lorsque fonction utilisée
    return($x);//renvoyer valeur, pour pouvoir la récupérer ensuite et stocker dans variable par exemple
};

foreach ($montableau as $valeur) {//On crée la boucle foreach où ttes les valeurs du tableau prennent la variable $valeur
    $valeur=calcul($valeur);//On assigne que la variable $variable (qui correspond à toutes les cases du tableau) est égale à son résultat une fois passée dans la fonction calcul
    echo $valeur."\n";//on imprime les valeurs du tableau sur la page
}


♥Afficher le contenu d'un tableau:
//Le tableau :
$user1 = ['Mickaël Andrieu', 'email', 'S3cr3t', 34];
//Affichage de son contenu:
echo $user1[0]; // "Mickaël Andrieu"
echo $user1[1]; // "email"
echo $user1[3]; // 34


♥ Afficher le contenu d'un tableau associatif:
echo $nomdutableauassociatif['title'];

//ou afficher les valeurs avec leur clé :
foreach($nomdutableauassociatif as $elements => $value){
 echo"{$elements} = {$value} <br>";
}


♥$value} <br>";
}


♥Afficher le nombre de paires d'un tableau associatif :
echo count($nomdutableauassociatif);


♥ Récupérer la clé de l'élément d'un tableau :
//Le tableau :
$recipe = [
    'title' => 'Salade Romaine',
    'recipe' => 'Etape 1 : Lavez la salade ; Etape 2 : euh ...',
    'author' => 'laurene.castor@exemple.com',
];

//Récupération des clés des éléments du tableau
foreach($recipe as $property => $propertyValue){
    echo '[' . $property . '] = ' . $propertyValue . PHP_EOL;
}


♥ Visualiser simplement ce que contient un tableau pour savoir:
echo '<pre>';//<pre> permet d'avoir les retours à la ligne
print_r($nomdutableau);
echo '</pre>';


♥ Recherchez dans un tableau:
//"array_key_exists" pour vérifier si une clé existe dans le tableau
//"in_array" pour vérifier si une valeur existe dans le tableau
//"array_search" pour récupérer la clé d'une valeur dans le tableau

//AVEC "array_key_exists":
$recipe = [
    'title' => 'Salade Romaine',
    'recipe' => 'Etape 1 : Lavez la salade ; Etape 2 : euh ...',
    'author' => 'laurene.castor@exemple.com',
];

if (array_key_exists('title', $recipe))
{
    echo 'La clé "title" se trouve dans la recette !';
}

if (array_key_exists('commentaires', $recipe))
{
    echo 'La clé "commentaires" se trouve dans la recette !';
}

//AVEC "in_array":
$users = [
    'Mathieu Nebra',
    'Mickaël Andrieu',
    'Laurène Castor',
];

if (in_array('Mathieu Nebra'/*nom de la clé à rechercher*/, $users/*nom du tableau dans lequel on fait la recherche*/))
{
    echo 'Mathieu fait bien partie des utilisateurs enregistrés !';
}//La fonction renverra un booléen true car la clé est dans le tableau

if (in_array('Arlette Chabot', $users))
{
    echo 'Arlette fait bien partie des utilisateurs enregistrés !';
}//La fonction renverra un booléen false car la clé n'est pas dans le tableau. On ne voit que le message pour Mathieu, car Arlette ne fait pas partie des utilisateurs enregistrés

//AVEC "array_search":
$users = [
    'Mathieu Nebra',
    'Mickaël Andrieu',
    'Laurène Castor',
];

$positionMathieu = array_search('Mathieu Nebra', $users);
echo '"Mathieu" se trouve en position ' . $positionMathieu . PHP_EOL;//Elle a trouvé la valeur, elle renvoie la clé correspondante (dans le cas d'un tableau numéroté, la clé sera un numéro ; dans le cas d'un tableau associatif, la clé sera un nom)

$positionLaurène = array_search('Laurène Castor', $users);
echo '"Laurène" se trouve en position ' . $positionLaurène . PHP_EOL;//Elle a trouvé la valeur, elle renvoie la clé correspondante (dans le cas d'un tableau numéroté, la clé sera un numéro ; dans le cas d'un tableau associatif, la clé sera un nom)
// Si elle n'a pas trouvé la valeur, elle renvoie false


♥ Créer une instance d’une classe:
//exemple 1
<?php
$objet = new nomdelaclasse(paramètres);
?>
//exemple 2
<?php
$user1 = new Utilisateur("Roger","Toto","21/09/1972");
?>
//exemple 3
<?php
$user = array(
new Utilisateur("Roger","Toto","21/09/2002"),
new Utilisateur("Foo","Foo","11/10/2005"));
?>


♥ Exemple de calcul de variables d'un tableau:
$montableau = [2, 4, 6, 8];
function calcul($x) { //On crée la fonction calcul qui a pour paramètre $x
    $x=$x*2;//On fait en sorte que $x soit multiplié /2 lorsque fonction utilisée
    return($x);//signifie qu'on va renvoyer la valeur, pour pouvoir la récupérer ensuite et la stocker dans une variable par exemple
};

foreach ($montableau as $valeur) {//On crée la boucle foreach où ttes les valeurs du tableau prennent la variable $valeur
    $valeur=calcul($valeur);//On assigne que la variable $variable est égal à son résultat une fois passée dans la fonction calcul
    echo $valeur."\n";//on imprime les valeurs du tableau sur la page
}


♥ Connexion à sa base de données PHPMYADMIN (dans un fichier de connexion à la bdd):
<?php
$host = 'localhost';//nom du serveur
$username = 'root';//nom de l'utilisateur
$password = ''; // Par défaut pas de mdp sur WAMP/XAMPP pour utilisateur root
$dbname = 'authentification';//nom de la bdd


try {
    $pdo = new PDO("mysql:host=$host;dbname=$dbname", $username, $password);
    // Activer le mode exception pour PDO
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
} catch (PDOException $e) {
    die("Erreur de connexion à la base de données : " . $e->getMessage());
}
?>


♥ Connexion du formulaire d'inscription à la bdd (dans un fichier d'inscription):
<!DOCTYPE html>
<html>
<head>
	<title>Exercice d'authentification</title>
</head>

<body>
<h2>Formulaire d'inscription</h2>
    <form method="post" action="inscription.php">
        <label for="nom">Nom :</label><br>
        <input type="text" id="nom" name="nom" required><br>
        <label for="email">Email :</label><br>
        <input type="email" id="email" name="email" required><br>
        <label for="mot_de_passe">Mot de passe :</label><br>
        <input type="password" id="mot_de_passe" name="mot_de_passe" required><br>
        <button type="submit" name="inscrire">Je m'inscris</button>
    </form>

<?php
if ($_SERVER['REQUEST_METHOD'] == 'POST' && isset($_POST['inscrire'])) {
    // Inclusion de la connexion à la base de données
    require_once 'db.php';
    
    // Récupérer les données du formulaire
    $nom = $_POST['nom'];
    $email = $_POST['email'];
    $mot_de_passe = password_hash($_POST['mot_de_passe'], PASSWORD_DEFAULT); // Hacher le mot de passe
    
    // Vérification si l'email existe déjà
    $stmt = $pdo->prepare("SELECT * FROM utilisateurs WHERE email = ?");
    $stmt->execute([$email]);
    
    if ($stmt->rowCount() > 0) {
        echo "Cet email est déjà utilisé.";
    } else {
        // Insertion des données dans la base
        $stmt = $pdo->prepare("INSERT INTO utilisateurs (nom, email, mot_de_passe) VALUES (?, ?, ?)");
        if ($stmt->execute([$nom, $email, $mot_de_passe])) {
            echo "Inscription réussie !";
        } else {
            echo "Erreur lors de l'inscription.";
        }
    }
}
?>
</body>
</html>


♥ Formulaire de connexion (dans une page pour la connexion) :
<!DOCTYPE html>
<html>
<head>
    <title>Connexion</title>
</head>
<body>
    <h2>Formulaire de connexion</h2>
    <form method="post" action="connexion.php">
        <label for="email">Email :</label><br>
        <input type="email" id="email" name="email" required><br>
        <label for="mot_de_passe">Mot de passe :</label><br>
        <input type="password" id="mot_de_passe" name="mot_de_passe" required><br>
        <button type="submit" name="connexion">Se connecter</button>
    </form>

<?php
if ($_SERVER['REQUEST_METHOD'] == 'POST' && isset($_POST['connexion'])) {
    // Inclusion de la connexion à la base de données
    require_once 'db.php';
    
    // Récupérer les données du formulaire
    $email = $_POST['email'];
    $mot_de_passe = $_POST['mot_de_passe'];
    
    // Vérification des informations d'identification
    $stmt = $pdo->prepare("SELECT * FROM utilisateurs WHERE email = ?");
    $stmt->execute([$email]);
    $utilisateur = $stmt->fetch();
    
    if ($utilisateur && password_verify($mot_de_passe, $utilisateur['mot_de_passe'])) {
        // Démarrer la session et stocker les informations de l'utilisateur
        session_start();
        $_SESSION['utilisateur_id'] = $utilisateur['id'];
        $_SESSION['nom'] = $utilisateur['nom'];
        echo "Connexion réussie ! Bienvenue, " . $_SESSION['nom'];
    } else {
        echo "Email ou mot de passe incorrect.";
    }
}
?>
</body>
</html>

♥ Page qui accueille l'utilisateur connecté :
<?php
session_start();

if (!isset($_SESSION['utilisateur_id'])) {
    // Rediriger vers la page de connexion si l'utilisateur n'est pas connecté
    header("Location: connexion.php");
    exit;
}
?>

<!DOCTYPE html>
<html>
<head>
    <title>Accueil</title>
</head>
<body>
    <h1>Bienvenue, <?php echo $_SESSION['nom']; ?> !</h1>
    <a href="deconnexion.php">Se déconnecter</a>
</body>
</html>

♥ Page de déconnexion :
<?php
session_start();
session_destroy();
header("Location: connexion.php");
exit;

♥ Vérifier qu'une variable contient du contenu (retourne TRUE(1) si variable déclarée) :
$yasbadass = "je suis la plus belle";

if(isset($yasbadass)) {
   echo "La variable contient bien du contenu";
}

//Ou même vérifier qu'un champ de formaulaire est rempli :
if(isset($_POST['champprenom'])){
   $champprenom = $_POST['champprenom'];
   echo "Le prénom de l'utilisateur est {$champprenom}";
}


♥ Vérifier qu'une variable contient aucun contenu (retourne TRUE(1) si variable pas déclarée/null/false) :
$yasbadass = null;

if(empty($yasbadass)) {
   echo "La variable ne contient aucun contenu";
}


♥ Vérifier qu'un bouton radio a été sélectionné :
<form action="index.php" method="post">
   <input type="radio" name="credit_card"/*le name est la clé*/ value="Visa"/*value est la valeur*/>
   Visa <br>
   <input type="radio" name="credit_card" value="Mastercard">
   Mastercard <br>
   <input type="radio" name="credit_card" value="American Express">
   American Express <br>
   <input type="submit" name="Soumettre" value="Soumettre">
</form>

<?php
 if(isset($_POST["Soumettre"])){
     $credit_card = $_POST["credit_card"];
     echo "Votre carte de crédit est une " . "{$credit_card}.";
 }
?>


♥ Vérifier qu'une checkbox a été sélectionnée :
<form action="index.php" method="post">
<input type="checkbox" name="pizza" value="Pizza">
Pizza <br>
<input type="submit" value="Submit" name="submit">
</form>

<?php
if(isset($_POST['submit'])) {
    if(isset($_POST['pizza'])){
        echo "Tu aimes les pizzas" . "<br>";
    }
    
    if(empty($_POST['pizza'])){
        echo "Tu n'aimes pas les pizzas" . "<br>";
    }
}
?>


♥ Créer une fonction :
function nomdelafonction(){
    echo "CONGRATS ! Fasting is OVER ♥";
}


♥ Appeler une fonction :
nomdelafonction();


♥ Créer une fonction avec paramètre(s) :
function nomdelafonction($prenom){
    echo "CONGRATS ! Fasting is OVER dear {$prenom} ♥" . "<br>";
}

function nomdelafonctiondeux($prenom, $age){
    echo "HEY {$prenom} ♥! You are {$age} years old today !" . "<br>";
}

//Pour appeler la fonction :
nomdelafonction("Yasmine");
nomdelafonctiondeux("Yasmine", 22);

♥ différentes fonction string :
$username = "badyass";

//►mettre chaîne de caractères en minuscule
$username = strtolower($username);
echo $username;
//►mettre chaîne de caractères en capitales
$username = strtoupper($username);
echo $username;
//►supprimer espace présent avant après chaîne de caractères
$username = trim($username);
echo $username;
//►remplir la chaîne de caractères d'un certain nombre de caractères définis
$username = str_pad($username, 20, "?");
echo $username;
//►remplacer des caractères dans la chaîne de caractères
$username = "pseudo?badyass";
$username = str_replace("?", "->", $username);
echo $username;
//►écrire la chaîne de caractères à l'envers
$username = strrev($username);
echo $username;
//►compte le nombre de caractères dans la chaîne de caractères
$count = strlen($username);
echo $count;
//►trouve la position du caractère (premier de son genre) dans la chaîne de caractères (commence à 0)
$index = strlen($username, "y");
echo $index;
//►tirer une variable à partir de la chaîne de caractères
$username = "Yasmine Badarou";
$lastname = substr($username, 8/*début*/, 15/*fin*/);
echo $lastname;
//►Insérer du caractère dans les espaces la chaîne de caractères
$username = array("Yasmine", "Badarou", "la", "meilleure");
$lastname = implode("/", $username);
echo $lastname;

♥ Sécuriser les entrées dans un input (POST et GET):
$username = filter_input(INPUT_POST/*Ou INPUT_GET*/, "username",
FILTER_SANITIZE_SPECIAL_CHARS);//enlève les caractères spéciaux

$age = filter_input(INPUT_POST, "age",
FILTER_SANITIZE_NUMBER_INT);//enlève les caractères lettres

$email = filter_input(INPUT_POST, "email",
FILTER_SANITIZE_EMAIL);//enlève les caractères non autorisés format email

♥ Valider les entrées d'un input (POST et GET):
$age = filter_input(INPUT_POST/*Ou INPUT_GET*/ , "age",
FILTER_VALIDATE_INT);//vérifie qu'il n'y a que des chiffres

$email = filter_input(INPUT_POST, "email",
FILTER_VALIDATE_EMAIL);//vérifie que le format d'email est valide

♥ Inclure le contenu d'un autre fichier dans la page courante :
include("header.html");//J'appelle le contenu de la page  header.html

♥ Créer un cookie :
setcookie("cookie_key", "cookie_value", /*expiration*/time() + (86400 * 2), /*path du cookie*/"/")

♥ Accéder aux infos du cookie :
foreach($_COOKIE as $key => $value){
 echo"{$key} = {$value} <br>";
}

if(isset($_COOKIE["fav_"password"] = "monmdp123";

//Mettre cela dans une autre page contenant "session_start()" au début pour afficher ces infos
echo $_SESSION["username"] . "<br>";
echo $_SESSION["password"] . "<br>";

♥ Rediriger vers une autre page :
header("Location: page.php");

♥ Fermer une session (se déconnecter) :
//Créer un bouton de déconnexion
<form action="home.php" method="post">
    <input type="submit" value="Log Out" name="logout">
</form>

//Créer une fonction de déconnexion
if(isset($_POST["logout"])){
    session_unset();
    session_destroy();//détruit la session
    header("Location: index.php");//redirige vers autre page
}

♥ Afficher les données de serveur de l'environnement de la page (on peut les utiliser dans la Superglobals "$_SERVER") :
foreach($_SERVER as $key => $value){
	echo"{$key} = {$value} <br>";
}

♥ Effectuer une action dans le fichier courant sans avoir à préciser son nom (utile si il viendrait à changer + tard, exemple d'utilisation avec la Superglobals $_SERVER):
<form action="<?php $_SERVER["PHP_SELF"]?>/*va appliquer l'action à la page courante*/" method="post">
	username:<br>
	<input type="text" name="username">
	<input type="submit">
</form>

♥ Hasher un mot de passe :
$password = "code123";
$hash = password_hash($password/*le mdp*/, PASSWORD_DEFAULT/*le bcrypt algorithm*/);
echo $hash;

♥ Vérifier qu'un mot de passe est correct :
$password = "code1243";
$hash = password_hash($password, PASSWORD_DEFAULT);

if(password_verify("code123", $hash)){
	echo "You are logged in!";
}
else{
	echo "Incorrect password!";
}

♥ Connexion à une base de données (dans un fichier database.php):
$db_server = "localhost";//nom du serveur
$db_username = "root";//nom d'utilisateur de la bdd
$db_password = "";//mot de passe de la bdd
$db_name = "businessdb";//nom de la bdd
$conn = "";//variable de connexion à la bdd

$conn = mysqli_connect($db_server, $db_username, $db_password, $db_name);//connexion à la bdd

♥ Tester si on est connecté à la bdd :
include('database.php');

if($conn){
	echo "You are connected";
}
else {
	echo "Could not connect";
}

♥ Modifier un message d'erreur avec try et catch :
include('database.php');

try{
	$conn = mysqli_connect($db_server, $db_username, $db_password, $db_name);//connexion à la bdd
}
catch(mysqli_sql_exception){
	echo "Could not connect";
}

♥ Fermer la connexion à la bdd (pour des raisons de sécurité):
mysqli_close($conn);//normal si ça fait une erreur à cause d'Intelephense

♥ Insérer une ligne dans un tableau de la bdd :
include('database.php');

$sql = "INSERT INTO users (user, password)
	VALUES	 ('Spongebob','pineapple1')";

mysqli_query($conn, $sql);//pour soumettre la requête sql dans la bdd

mysqli_close($conn);

//OU AVEC DES VARIABLES + HASH :
include('database.php');

$username = "yamani";
$password = "mimi123";
$hash = password_hash($password, PASSWORD_DEFAULT);

$sql = "INSERT INTO users (user, password)
	VALUES	 ('$username','$hash')";

mysqli_query($conn, $sql);//pour soumettre la requête sql dans la bdd

mysqli_close($conn);

♥ Afficher les données d'un tableau d'une bdd :
include('database.php');

$sql = "SELECT * FROM users";
$result = mysqli_query($conn, $sql);

if(mysqli_num_rows($result) > 0){//pour chaque ligne de la table
    while($row = mysqli_fetch_assoc($result)){//récupérer les données de la table
        echo $row["id"] . "<br>";
        echo $row["user"] . "<br>";
        echo $row["reg_date"] . "<br>";
    };
}
else{
    echo "0 results";//sinon si la table est vide
}
mysqli_close($conn);
food"])){
 echo "BUY SOME {$_COOKIE["fav_food"]} !!!";
}
else {
 echo"I don't know your favorite food";
}

♥ Afficher seulement les clés d'un tableau associatif :
$keys = array_keys($nomdutableauassociatif);

foreach($keys as $key){
  echo "{$key} <br>";
}


♥Afficher seulement les valeurs d'un tableau associatif :
$values = array_values($nomdutableauassociatif);

foreach($values as $value){
  echo "{$value} <br>";
}


♥Invecondition if:
$age = 15;

    if ($age >= 18) {
        echo "You may enter this site";
    }
    elseif ($age == 15) {
 

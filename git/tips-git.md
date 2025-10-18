## ♥ Mettre à jour mon dépôt GitHub :
git pull origin main
git add .
git commit -m "premier commit"
git push origin main
//Remarque : Remplace main par master ou tout autre nom de branche si ton dépôt utilise un autre nom pour la branche principale.

git pull origin brancheprincipale
git add .
git commit -m "ajout des fichiers Controller (vides pour l'instant) + tri dossiers Twig"
git push origin brancheprincipale https://github.com/yasyasbdr/streemi_yasmine_badarou
//Remarque : Remplace main par master ou tout autre nom de branche si ton dépôt utilise un autre nom pour la branche principale.

## ♥ Effectuer un commit (enregistre l'état du projet) :
git commit -m "Description du commit"

## ♥ Établir un nom d'utilisateur Git + mail :
POUR LES PROJETS GLOBAUX ->
git config --global user.name "Yasmine"
git config --global user.email "yasminebadarou.yb@gmail.com"
POUR DES PROJETS SPÉCIFIQUES (si besoin) ->
git config user.name "Yasmine"
git config user.email "yasminebadarou.yb@gmail.com"

## ♥ Cloner un repository GitHub sur mon PC (se mettre dans le répertoire où executer la commande) :
git clone https://github.com/yasyasbdr/lien_du_repository.git
git clone https://github.com/mathadata/entretien

## ♥ Créer un fichier txt avec du contenu dedans :
echo "This is file1.txt" > file1.txt

## ♥ Voir le contenu d'un fichier :
cat file1.txt

## ♥ Faire suivre l'état d'un fichier par Git (garder un oeil sur tous les changements apportés à ce fichier) :
git add file1.txt

## ♥ Faire en sorte que Git ne suive pas l'état d'un fichier (comme un fichier contenant des infos confidentielles par exemple) :
nano .gitignore
PUIS AJOUTER LE NOM DES FICHIERS À IGNORER

## ♥ Créer un fichier et l'ouvrir :
nano file2.txt

## ♥ Commande raccourcie qui permet de commit les fichiers déjà suivis par git (donc déjà add à git) :
git commit -a -m "description du commit"

## ♥ Connaître les fichiers qui sont add/commit ou pas et sur quelle branche :
git status

## ♥ Publier en ligne mon dépôt local :
git push

## ♥ Créer une nouvelle branche :
git checkout -b nom-de-ta-branche

git log -- .\ressources\Animation_Bras_Articulé-Yasmine_Badarou.zip

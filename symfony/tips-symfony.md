## ♥ Créer un nouveau projet (dans le terminal) :
symfony new --webapp my_project

## ♥ Construire microservice, console application or API (dans le terminal):
symfony new my_project

## ♥ Lancer mon serveur :
symfony server:start

## ♥ Créer une entity (dans le terminal) :
php bin/console make:entity


## ♥ Importer Fixtures :
php bin/console make:fixtures

https://www.doctrine-project.org/projects/doctrine-orm/en/3.3/reference/inheritance-mapping.html

supp les id, getter et setter en php, ajouter extends nomclasse

POUR LES MIGRATIONS :
1 - Créer fichier ".env.local" dans mm répertoire que .env
2 - Enlever la valeur de DATABASE_URL dans fichier .env
3 - Mettre valeur de DATABASE_URL = "lien de ma base de données"

4- Supprimer les commentaires dans le fichier version20250131...php
5- maj bdd dans le terminal -> php bin/console doctrine:migrations:migrate (après migration tjr ouvrir fichier et supp coms: permet de savoir qu'on a lu la migration)
6- Installer via terminal le -> composer require alice. On fait nos fixtures en IML dans Resources/fixtures. Si ne marche pas, taper -> composer require 

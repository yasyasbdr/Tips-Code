♥ Sélectionner toutes les valeurs (colonnes) de la table students :
SELECT * FROM students;

♥ Sélectionner les colonnes firstname et lastname de la table students :
 SELECT firstname, lastname FROM students;

♥ Compter le nombre d'étudiants en AL par promotion jusqu'en 2019 inclus :
SELECT count(*) FROM students
WHERE specialty = 'AL'
GROUP BY promotion_year
HAVING promotion_year < 2020;

♥ Afficher uniquement les 12 premiers étudiants, en commençant par le 5ème :
SELECT * FROM students
LIMIT 12 OFFSET 4;

♥ Calculer le chiffre d'affaires pour la vente de jeux vidéo en Europe en 2015 :
SELECT sum(eu_sales) FROM video_game_sales
WHERE year = 2015

♥ Afficher tous les étudiants par nom de famille puis prénom, dans l'ordre alphabétique :
SELECT * FROM students
ORDER BY lastname ASC, firstname ASC;
ASC = ascendant
DESC = descendant

♥ Arrondir à 2 chiffres après la virgules :
SELECT id, utilisateur, algorithme, ROUND(algorithme, 2)
FROM `resultat`

♥ Afficher le genre qui s'est le plus vendu en 2016 et son montant :
SELECT year, genre, ROUND(SUM(na_sales + eu_sales + jp_sales + other_sales), 2) AS ventesTotalesGenrePlusVendu
FROM video_game_sales
WHERE year = 2016
GROUP BY genre, year
ORDER BY ventesTotalesGenrePlusVendu DESC
LIMIT 1;

♥ Rendre un nombre plus visible (ici un chiffre d'affaires) :
to_char(148556989, '999L999L999€')
Affichera -> 148 556 989€

♥ Calculer une moyenne :
AVG(na_sales + eu_sales + jp_sales + other_sales)


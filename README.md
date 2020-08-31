# DB_sql

Bonjour , ma mission consiste à créer une base de données qui s' appelle World.

Voici les actions que je fais sur cette table :

    1 - Creation d'une basse de donnée : "World".

        SCRIPT : CREATE DATABASE world;

    2 - Creation d'une table : "personnes".

        SCRIPT : CREATE TABLE `world`.`personnes` ( `id` INT NOT NULL AUTO_INCREMENT , `nom` VARCHAR(50) NOT NULL , `prenom` VARCHAR(50) NOT NULL , `age` INT NOT NULL , `taille` FLOAT NOT NULL , `poids` FLOAT NOT NULL , PRIMARY KEY (`id`)) ENGINE = InnoDB;

    3 - Insertion de données dans la table personnes.

        SCRIPT : INSERT INTO `personnes` (`id`, `nom`, `prenom`, `age`, `taille`, `poids`)
        VALUES 
        (NULL, 'Rakoto', 'Be Nify', '10', '1.50', '70.0'),
        (NULL, 'Lava', 'Rapeto', '25', '2.0', '30.0'),
        (NULL, 'Ba', 'Lita', '7', '1.0', '20.5'),
        (NULL, 'Kiala', 'Manjakely','100','1.68' , '45.7'),
        (NULL , 'Kiala' , 'Pota' , '37', '0.8' , '50.0')

    4 - Modifivation de la table personnes

        4-1 Ajout d'une colonne "couleur_preferee" après la colonne poids

        SCRIPT : ALTER TABLE `personnes` ADD `couleur_preferee` VARCHAR(20) NOT NULL AFTER `poids`;

        4-2 AJouter les données dans la colonne c'est à dire modifier la table personnes

            SCRIPT : 
        UPDATE `personnes` SET `couleur_preferee` = 'rouge' WHERE `personnes`.`id` = 1
        UPDATE `personnes` SET `couleur_preferee` = 'vert' WHERE `personnes`.`id` = 2
        UPDATE `personnes` SET `couleur_preferee` = 'jaune' WHERE `personnes`.`id` = 3
        UPDATE `personnes` SET `couleur_preferee` = 'violet' WHERE `personnes`.`id` = 4
        UPDATE `personnes` SET `couleur_preferee` = 'grise' WHERE `personnes`.`id` = 5

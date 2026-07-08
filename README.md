# TP 3 Linux : Environnement WSL, Docker et Services

Ce dépôt regroupe les 4 exercices du TP3 : WSL2, Docker, Docker Compose et MySQL CRUD.

## Structure
- exercice1/ : Installation WSL2
- exercice2/ : Installation Docker
- exercice3/ : Orchestration Docker Compose (6 conteneurs)
- exercice4/ : Gestion CRUD MySQL

## Exercice 4 : CRUD MySQL
docker exec -it exercice3_mysql_1 mysql -u root -p

CREATE DATABASE ecole;
USE ecole;
CREATE TABLE Etudiants (id INT AUTO_INCREMENT PRIMARY KEY, nom VARCHAR(50), prenom VARCHAR(50));
INSERT INTO Etudiants (nom, prenom) VALUES ('Diallo','Moussa'), ('Fall','Fatou');
SELECT * FROM Etudiants;
UPDATE Etudiants SET nom='Traoré' WHERE id=1;
DELETE FROM Etudiants WHERE id=2;
SELECT * FROM Etudiants;

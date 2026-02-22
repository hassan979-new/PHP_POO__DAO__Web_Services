# 🧮 Gestion des étudiants avec DAO, Service et Web Interface
## Description
Ce projet PHP met en place une application complète de gestion des étudiants avec une architecture en couches :

- Classe Etudiant représentant l’entité métier.

- Connexion PDO pour interagir avec une base MySQL.

- DAO générique (IDao) définissant les opérations CRUD.

- Service EtudiantService implémentant les méthodes CRUD et fournissant une API JSON.

- Contrôleurs pour gérer l’ajout et la suppression via formulaire.

- Interface web (index.php) avec formulaire d’ajout et tableau listant les étudiants.

- Web services (ws) pour insertion et récupération des étudiants en JSON.
## Project Structure
```
projet/
├── index.php
├── racine.php
├── classes/
│   └── Etudiant.php
├── connexion/
│   └── Connexion.php
├── controller/
│   ├── addEtudiant.php
│   └── deleteEtudiant.php
├── dao/
│   └── IDao.php
├── service/
│   └── EtudiantService.php
├── ws/
│   ├── insertEtudiant.php
│   └── listEtudiants.php
└── README.md
```
# ⚙️ Features
## 1. Fichier index.php

- Formulaire HTML pour ajouter un étudiant (nom, prénom, ville, sexe).

- Affichage de la liste des étudiants dans un tableau.

- Bouton de suppression avec confirmation.

## 2. Fichier racine.php

- Définit la constante Racine pour gérer les chemins d’inclusion.

## 3. Classe Etudiant

- Attributs : id, nom, prenom, ville, sexe.

- Getters et setters pour chaque attribut.

- Méthode __toString() pour afficher nom et prénom.

## 4. Classe Connexion

- Gère la connexion PDO à la base MySQL school1.

- Active les options de gestion des erreurs et encodage UTF-8.

## 5. Interface IDao

- Définit les méthodes génériques : create, delete, update, findAll, findById.

## 6. Service EtudiantService

- Implémente IDao.

- Méthodes CRUD avec requêtes préparées PDO.

- Méthode findAllApi() pour retourner les étudiants en JSON.

## 7. Contrôleurs

- addEtudiant.php : vérifie les champs, crée un étudiant et l’insère.

- deleteEtudiant.php : supprime un étudiant par son identifiant.

## 8. Web Services (ws)

- Insertion JSON : ajoute un étudiant via POST et retourne un message JSON.

- Liste JSON : retourne tous les étudiants au format JSON.

## 🖥️ Example Execution
- <img width="960" height="504" alt="Capture d’écran 2026-02-19 144500" src="https://github.com/user-attachments/assets/cb746dc7-7cd4-47d6-807c-5ba81800ffdf" />
- <img width="960" height="504" alt="Capture d’écran 2026-02-19 144851" src="https://github.com/user-attachments/assets/8d2636c8-4b05-4cc4-83e3-cc12f396e67c" />
- <img width="960" height="504" alt="image" src="https://github.com/user-attachments/assets/bcc9e5ea-38f9-4953-8e0b-e8e0816452c9" />
- <img width="960" height="504" alt="image" src="https://github.com/user-attachments/assets/7da21175-7fbc-4cd9-b363-8cee9f28a64d" />
## 💡 Concepts Practiced

- Architecture en couches (Entity, DAO, Service, Controller, View).

- Utilisation de PDO avec requêtes préparées.

- Gestion des formulaires HTML et validation côté serveur.

- Implémentation CRUD complet.

- Développement d’API JSON pour intégration externe.
## 🧑‍💻 Author

- 👤 Agouram Hassan
- 🏫 Programmation orientée objet : PHP
- 🎓 Instructor	Mr.LACHGAR
- 📅 19 février 2026

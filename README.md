# BookStack - Répertoire de Livres

Application de répertoire de livres construite avec **Node.js**, **Express**, et **MongoDB**.
Elle permet de gérer une collection de livres via une API RESTful et inclut des fonctionnalités comme la recherche et le regroupement par genres.

## 🛠️ Technologies Utilisées
- **Node.js** : Environnement d'exécution JavaScript.
- **Express.js** : Framework web pour Node.js.
- **MongoDB** : Base de données NoSQL.
- **Mongoose** : ORM pour MongoDB.
- **Postman** : Pour tester les points de terminaisons API.

## 🎯 Fonctionnalités
- **CRUD complet** : Créer, Lire, Mettre à jour, Supprimer des livres.
- **Recherche** : Rechercher des livres par titre.
- **Regroupement** : Regrouper les livres par genres.

## 🚀 Installation et Configuration

### 1. Pré-requis
- [Node.js](https://nodejs.org/) installé.
- [MongoDB](https://www.mongodb.com/) installé ou compte MongoDB Atlas.
- [Postman](https://www.postman.com/) pour tester l'API.

### 2. Installation du Projet

Pour cloner le projet :

```bash
git clone git@github.com:Doruo/BookStack.git
cd BookStack
```

## 📖 Routes de l'API

#### - **URL par défaut :** http://localhost:3000

### 1. Obtenir tous les livres
```bash
GET /books
```
### 2. Ajouter un livre
```bash
POST /books
```
#### Résultat :
``` JSON
{
  "title": "Les Misérables",
  "author": "Victor Hugo",
  "genre": "Roman",
  "publishedYear": 1862
}
```

### 3. Mettre à jour un livre
```bash
PUT /books/:id
```
#### Résultat :
```JSON
{
  "title": "Les Misérables (Édition révisée)"
}
```

### 4. Supprimer un livre
```bash
DELETE /books/:id
```

### 5. Rechercher un livre
```bash
GET /books/search?title=<recherche> 
```
Exemple : /books/search?title=Misérables

### 6. Regrouper par genres

```bash
GET /books/genres
```

Exemple : /books/fantaisie

## 📂 Structure du Projet
```graphql
BookStack/
│
├── models/
│   └── Book.js         # Modèle Mongoose pour les livres
│
├── routes/
│   └── books.js        # Routes API pour la gestion des livres
│
├── index.js            # Fichier principal du serveur
├── package.json        # Gestionnaire de dépendances
```
## 🔗 Ressources
- [Documentation Node.js](https://nodejs.org/en/docs/) 
- [Documentation Express](https://expressjs.com/) 
- [Documentation Mongoose](https://mongoosejs.com/)

## ✨ Réalisé par Marc Haye dans le cadre de l'apprentissage de Node.js, des API RESTfull et MongoDB.
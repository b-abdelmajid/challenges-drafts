# 📘 Challenge PFE — Mini Application "Task Manager"

Bienvenue dans ce challenge technique destiné aux stagiaires PFE ou profils juniors.  

L'objectif est d'évaluer votre capacité à **apprendre rapidement**, **coder proprement**, et **concevoir une petite application complète** (frontend + backend + base de données + Docker).

---

## 🎯 Objectifs du challenge

Vous devez développer une application "Task Manager" permettant de gérer des tâches (CRUD).

Le challenge inclut :

- **Frontend** en **React** ou **Next.js**
- **Backend** en **Node.js** (Express ou Next.js API Routes)
- **Base SQL** (SQLite, PostgreSQL ou MySQL)
- **Containerisation Docker** (frontend + backend + DB)
- Documentation écrite dans ce fichier

---

## 📌 Fonctionnalités à implémenter

### ✔️ Fonctionnalités obligatoires

#### 1. Affichage de la liste des tâches

Chaque tâche contient :

- `id`
- `title`
- `description` (optionnel)
- `status`: `todo`, `in-progress`, `done`
- `created_at`

#### 2. Création d'une tâche

#### 3. Mise à jour d'une tâche

#### 4. Suppression d'une tâche

---

## 🔧 Contraintes techniques

### 🖥️ Frontend (React ou Next.js)

- Interface simple (libre)
- Appels API fonctionnels
- Liste des tâches + formulaire(s)
- Composants organisés proprement

### 🛠️ Backend (Node.js)

Vous pouvez utiliser soit :

- **Express.js**
- **ou Next.js API routes**

Endpoints requis :

| Méthode | Endpoint | Description |
|---------|----------|-------------|
| GET | `/api/tasks` | Récupérer toutes les tâches |
| POST | `/api/tasks` | Créer une nouvelle tâche |
| PUT | `/api/tasks/:id` | Modifier une tâche |
| DELETE | `/api/tasks/:id` | Supprimer une tâche |

---

## 🗄️ Base de données (SQL)

### Votre base doit contenir une table `tasks` :

```sql
CREATE TABLE tasks (
    id INTEGER PRIMARY KEY,
    title VARCHAR(255),
    description TEXT,
    status VARCHAR(20),
    created_at DATETIME
);
```

---

## 🐳 Containerisation (Docker)

Vous devez fournir :

- un `Dockerfile` pour le backend
- un `Dockerfile` ou configuration Docker pour le frontend
- un `docker-compose.yml` permettant de lancer :
  - la base SQL
  - le backend
  - le frontend

---

## 📦 Installation & lancement

Ajoutez ici les commandes propres à votre projet, par exemple :

```bash
git clone <URL_DU_REPO>
cd challenge-task-manager
docker-compose up --build
```

Puis accéder à :

- **Frontend** : http://localhost:3000
- **Backend** : http://localhost:3001/api/tasks
- **Base PostgreSQL** : localhost:5432

---

## 🧪 Bonus (Optionnel mais recommandé)

Si vous souhaitez aller plus loin :

- Filtrage / tri des tâches
- Interface Kanban (drag & drop)
- Authentification simple (JWT)
- Tests unitaires (Jest / RTL)
- Documentation API (Swagger)
- UI améliorée (Tailwind, MUI…)

---

## 📁 Ce que vous devez rendre

- Code source complet (frontend + backend), et à déposer sur Github
- `Dockerfile(s)` + `docker-compose.yml`
- Script SQL d'initialisation ou migration
- Ce fichier `README.md` complété :
  - décisions techniques
  - instructions de lancement
  - améliorations possibles


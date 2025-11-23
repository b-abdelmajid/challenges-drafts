# 📘 Challenge PFE — Mini Application "Movie Explorer App"

Bienvenue dans ce challenge technique destiné aux stagiaires PFE ou profils juniors.  

L'objectif est d'évaluer votre capacité à **apprendre rapidement**, **coder proprement**, et **concevoir une petite application complète** (frontend + backend + base de données + Docker).

---

## 🎯 Objectif général

Générer la structure complète d'un challenge technique (frontend + backend API) pour des Stagiaires ou Juniors.  

L'application s'appelle **Movie Explorer App** et doit permettre de chercher des films et gérer une liste de favoris.

Ce challenge doit tester :

- compétences front (React ou Next.js)
- compétences backend (Node.js + API REST)
- logique et organisation du code
- capacité à consommer une API externe
- capacité à concevoir une API interne (favorites)
- Docker
- autonomie et bonnes pratiques

---

## 🧱 Architecture à produire

### 📌 1. Frontend (React ou Next.js)

#### Fonctionnalités :

- Page permettant de rechercher des films via une API externe (ex: OMDB API)
- Afficher résultats : titre, affiche, année
- Bouton "Ajouter aux favoris"
- Page "Mes favoris" (stockés via backend)
- Appels fetch à une API interne

#### Tech requirements :

- Next.js 14 ou React 18 + Vite
- Appels API via fetch
- Composants propres, dossier `/components`, `/pages` ou `/app`

---

### 📌 2. Backend API (Node.js + Express ou Next.js API routes)

#### Endpoints à implémenter :

##### Films (proxy API externe)

| Méthode | Endpoint | Description |
|---------|----------|-------------|
| GET | `/api/search?query=...` | Appeler OMDB API ou autre API publique cinéma. Retourner une liste simple : `{ title, year, poster, imdbID }` |

##### Favoris (gérés dans une DB interne)

| Méthode | Endpoint | Description |
|---------|----------|-------------|
| GET | `/api/favorites` | Récupérer tous les favoris |
| POST | `/api/favorites` | Ajouter un film aux favoris |
| DELETE | `/api/favorites/:id` | Supprimer un favori |

La base peut être en :

- SQLite (recommandé)
- PostgreSQL
- ou simple JSON file (pour une version simplifiée)

---

## 🗄️ Base de données

### Table `favorites` :

```sql
CREATE TABLE favorites (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    imdbID VARCHAR(20) UNIQUE NOT NULL,
    title VARCHAR(255) NOT NULL,
    year VARCHAR(10),
    poster TEXT,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

---

## 🐳 Containerisation (Docker)

Vous devez fournir :

- un `Dockerfile` pour le backend
- un `Dockerfile` ou configuration Docker pour le frontend
- un `docker-compose.yml` permettant de lancer :
  - la base SQL (si applicable)
  - le backend
  - le frontend

---

## 📦 Installation & lancement

Ajoutez ici les commandes propres à votre projet, par exemple :

```bash
git clone <URL_DU_REPO>
cd movie-explorer-app
docker-compose up --build
```

Puis accéder à :

- **Frontend** : http://localhost:3000
- **Backend** : http://localhost:3001/api
- **Base SQLite/PostgreSQL** : selon votre configuration

### Configuration API externe

Pour utiliser l'API OMDB, vous devrez :

1. Obtenir une clé API gratuite sur [OMDB API](http://www.omdbapi.com/apikey.aspx)
2. Configurer la variable d'environnement `OMDB_API_KEY` dans votre backend

---

## 🧪 Bonus (Optionnel mais recommandé)

Si vous souhaitez aller plus loin :

- Pagination des résultats de recherche
- Détails d'un film (page dédiée)
- Filtrage des favoris (par année, genre)
- Recherche locale dans les favoris
- Gestion des erreurs API (retry, fallback)
- Tests unitaires (Jest / RTL)
- Documentation API (Swagger)
- UI améliorée (Tailwind, MUI…)
- Cache des résultats de recherche
- Notifications (toast) pour les actions

---

## 📁 Ce que vous devez rendre

- Code source complet (frontend + backend), et à déposer sur Github
- `Dockerfile(s)` + `docker-compose.yml`
- Script SQL d'initialisation ou migration
- Fichier `.env.example` avec les variables d'environnement nécessaires
- Ce fichier `README.md` complété :
  - décisions techniques
  - instructions de lancement
  - améliorations possibles
  - choix de l'API externe utilisée

---

## 🔑 Points d'attention

- **Gestion des erreurs** : Que faire si l'API externe est indisponible ?
- **Performance** : Éviter les appels API redondants
- **UX** : Loading states, messages d'erreur clairs
- **Sécurité** : Ne pas exposer la clé API côté frontend
- **Validation** : Valider les données avant insertion en base


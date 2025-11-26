# 🎓 Challenge Technique
## Mini-Plateforme de Gestion de Tâches  
**Technologies : PHP (Laravel) – React – MySQL – Docker**

---

## 🎯 1. Objectif du Challenge

Ce challenge a pour objectif d’évaluer votre capacité à analyser un problème, le découper, proposer une solution cohérente et développer une mini-application full-stack.

Les compétences évaluées sont :

- Conception d’une API simple  
- Développement backend avec Laravel  
- Développement frontend avec React  
- Communication Front ↔ API  
- Manipulation MySQL  
- Utilisation de Docker pour orchestrer l’environnement  
- Logique, autonomie, organisation  

---

## 📘 2. Description du Projet

Vous devez développer une **mini plateforme de gestion de tâches**, composée :

- d’un backend Laravel exposant une API REST,  
- d’un frontend React affichant et manipulant les données,  
- d’une base de données MySQL,  
- d’un environnement Docker permettant de lancer le tout.

Le but : une application **fonctionnelle**, **simple**, et **bien structurée**.

---

## 🧩 3. Fonctionnalités à Implémenter

### 🔹 Backend (Laravel)

Créer une API REST permettant :

| Action | Méthode | Route | Description |
|--------|---------|--------|-------------|
| Lister les tâches | GET | `/api/tasks` | Retourner toutes les tâches |
| Ajouter une tâche | POST | `/api/tasks` | Ajouter une nouvelle tâche |
| Marquer comme faite | PATCH | `/api/tasks/{id}/complete` | Modifier l'état `is_completed` |
| Statistiques | GET | `/api/tasks/stats` | { total, completed, pending } |

#### Modèle `Task`
- `id`  
- `title` *(string)*  
- `is_completed` *(boolean, default false)*  
- `created_at` / `updated_at`

---

### 🔹 Frontend (React)

Créer une interface simple comprenant :

1. Un **formulaire d’ajout de tâche**
2. Une **liste des tâches**
3. Un **bouton pour marquer chaque tâche comme complétée**
4. Un encart de **statistiques** affichant :
   - nombre total  
   - nombre complétées  
   - nombre en attente  

L’interface doit interagir avec l’API via fetch ou Axios.

---

### 🔹 Base de données (MySQL)

Base composée d’une seule table :

tasks
├─ id
├─ title
├─ is_completed
├─ created_at
└─ updated_at


---

### 🔹 Docker

Créer un environnement `docker-compose` incluant :

- un conteneur Laravel (PHP + serveur web),
- un conteneur MySQL,
- un conteneur Node/React.

Le projet doit pouvoir être lancé en une commande.

---

## ⭐ 4. Livrables Attendus

À rendre sous forme de **repository GitHub** contenant :

1. Backend Laravel  
2. Frontend React  
3. `docker-compose.yml`  
4. Fichier `README.md` contenant :  
   - Description du projet  
   - Instructions d’installation et lancement  
   - Problèmes rencontrés et solutions  
5. (Optionnel) Captures d’écran du résultat des différents écrans

---

## 🏅 5. Bonus Facultatifs

Non obligatoires mais valorisés :

- Suppression d’une tâche  
- Filtre (tâches faites / en attente)  
- Pagination simple  
- Design simple (ex : TailwindCSS)  
- Tests unitaires Laravel  
- Tests React (Jest)  

---

## 🧠 6. Points Évalués

- Compréhension du sujet  
- Clarté et cohérence du code  
- Organisation du projet  
- Qualité de l’API et du frontend  
- Gestion d’erreurs  
- Qualité des explications dans le README  
- Réflexion et logique  
- Capacité à surmonter des obstacles techniques  

---

## ⏱️ 7. Durée Recommandée

- **Format court : 4 à 6 heures**  
- **Format long : 10 à 12 heures**

---

Bonne chance et bon challenge !  

# 📚 Schoola-Taawon - Livrable Objectif 3

## Groupe : [Votre Groupe]

## Membres de l'équipe :
- [Nom Prénom] - [Rôle]
- [Nom Prénom] - [Rôle]
- [Nom Prénom] - [Rôle]

---

## 🎯 Objectif 3 : Développement Concret

### Contexte
Suite à la définition de la structure (sitemap), à la conception des prototypes et à la validation du design (Objectif 2), nous avons passé à la phase de développement concret. Cette étape consiste à traduire nos maquettes en un site fonctionnel à l'aide du framework choisi et à implémenter les fonctionnalités essentielles répondant aux besoins définis lors de l'Objectif 1.

---

## 🏗️ Choix du Framework

### Framework Frontend : React + TypeScript
**Raisons du choix :**
- **Composants réutilisables** : Architecture modulaire facilitant la maintenance
- **TypeScript** : Sécurité des types et meilleure expérience développeur
- **Écosystème riche** : Nombreuses bibliothèques (Material-UI, React Router, Axios)
- **Performance** : Virtual DOM et optimisation automatique
- **Communauté active** : Support et ressources abondantes

### Framework Backend : Node.js + Express
**Raisons du choix :**
- **JavaScript full-stack** : Même langage pour front et back
- **Express.js** : Framework léger et flexible
- **NPM** : Gestionnaire de paquets robuste
- **Socket.IO** : Support natif du temps réel
- **MongoDB** : Base de données NoSQL adaptée aux données flexibles

---

## 📋 Fonctionnalités Développées

### ✅ 1. Authentification et Gestion des Utilisateurs
- **Inscription** : Formulaire complet avec validation (username, email, password, ville, photo de profil)
- **Connexion** : Authentification JWT avec session persistante
- **Profil utilisateur** : Modification des informations personnelles
- **Sécurité** : Hashage des mots de passe (bcrypt), validation des données

### ✅ 2. Gestion des Annonces
- **Consultation** : Affichage de toutes les annonces avec filtrage (catégorie, niveau, ville, recherche)
- **Publication** : Formulaire complet avec upload de photos (max 5 images, 5MB chacune)
- **Modification/Suppression** : Uniquement pour le propriétaire (vérification côté client et serveur)
- **Détails** : Page dédiée avec informations complètes et contact vendeur

### ✅ 3. Messagerie en Temps Réel
- **Socket.IO** : Communication temps réel entre utilisateurs
- **Conversations privées** : Démarrage depuis les annonces
- **Interface moderne** : Type Messenger avec distinction visuelle envoi/réception
- **Indicateurs** : Messages non lus en gras, badge avec compteur
- **Notifications** : Mises à jour automatiques

### ✅ 4. Système de Favoris
- **Icône cœur** : Ajout/retrait en un clic
- **Stockage local** : Persistance des favoris (localStorage)
- **Page dédiée** : "Mes Favoris" avec compteur précis
- **Synchronisation** : Mise à jour temps réel du compteur

### ✅ 5. Fonctionnalités Supplémentaires
- **Système de likes** : Bouton "J'aime" avec compteur
- **Navigation responsive** : Menu adaptatif mobile/desktop
- **Recherche avancée** : Filtres multiples
- **Upload sécurisé** : Gestion des images avec validation

---

## 🗂️ Structure du Projet

```
schoola-taawon/
├── client/                          # Frontend React
│   ├── public/                      # Assets statiques
│   ├── src/
│   │   ├── components/              # Composants réutilisables
│   │   │   ├── Navbar.tsx          # Navigation principale
│   │   │   ├── ListingCard.tsx     # Carte d'annonce
│   │   │   ├── Layout.tsx          # Layout de base
│   │   │   └── ...
│   │   ├── pages/                  # Pages principales
│   │   │   ├── Home.tsx            # Page d'accueil
│   │   │   ├── Listings.tsx        # Liste des annonces
│   │   │   ├── CreateListing.tsx   # Création d'annonce
│   │   │   ├── ListingDetail.tsx   # Détail d'annonce
│   │   │   ├── Messages.tsx        # Messagerie
│   │   │   ├── Favorites.tsx       # Favoris
│   │   │   ├── Login.tsx           # Connexion
│   │   │   ├── Register.tsx        # Inscription
│   │   │   ├── Profile.tsx         # Profil utilisateur
│   │   │   └── EditListing.tsx     # Modification annonce
│   │   ├── context/                # Context React
│   │   │   ├── AuthContext.tsx     # Gestion authentification
│   │   │   └── ListingsContext.tsx # Gestion annonces
│   │   ├── services/               # Services API
│   │   │   ├── auth.service.ts
│   │   │   ├── listing.service.ts
│   │   │   └── message.service.ts
│   │   ├── types/                  # Types TypeScript
│   │   └── App.tsx                 # Application principale
│   ├── package.json
│   └── tsconfig.json
├── server/                          # Backend Node.js
│   ├── controllers/                 # Logique métier
│   │   ├── auth.controller.js
│   │   ├── listing.controller.js
│   │   ├── message.controller.js
│   │   └── user.controller.js
│   ├── models/                     # Modèles MongoDB
│   │   ├── User.js
│   │   ├── Listing.js
│   │   ├── Message.js
│   │   └── Conversation.js
│   ├── routes/                     # Routes API
│   │   ├── auth.js
│   │   ├── listings.js
│   │   ├── messages.js
│   │   └── user.routes.js
│   ├── middleware/                 # Middleware
│   │   ├── auth.js                 # Authentification
│   │   ├── upload.js               # Upload fichiers
│   │   ├── validation.js           # Validation données
│   │   └── security.js             # Sécurité
│   ├── scripts/                    # Scripts utilitaires
│   ├── config/                     # Configuration
│   ├── uploads/                    # Fichiers uploadés
│   ├── package.json
│   └── index.js                    # Point d'entrée
├── livrable/
│   └── README.md                   # Ce fichier
├── README.md                       # Documentation générale
├── start-app.bat                   # Script démarrage
├── ecosystem.config.json           # Configuration PM2
└── TODO.md                         # Tâches restantes
```

---

## 🚀 Étapes de Lancement du Projet

### Prérequis
- **Node.js** (version 16+) : [Télécharger](https://nodejs.org/)
- **MongoDB** : Base de données (local ou MongoDB Atlas)
- **Git** : Pour le versioning
- **Navigateur moderne** : Chrome, Firefox, Edge, Safari

### Installation

#### 1. Clonage du repository
```bash
git clone [URL_DU_REPOSITORY]
cd schoola-taawon
```

#### 2. Installation des dépendances Backend
```bash
cd server
npm install
```

#### 3. Installation des dépendances Frontend
```bash
cd ../client
npm install
```

#### 4. Configuration de l'environnement
```bash
# Dans le dossier server/
cp .env.example .env
# Éditer .env avec vos configurations (MongoDB, JWT_SECRET, etc.)
```

#### 5. Démarrage de MongoDB
```bash
# Si MongoDB local
./start-mongodb.bat
# Ou utiliser MongoDB Atlas pour le cloud
```

#### 6. Démarrage du Backend
```bash
cd server
npm run dev  # Développement
# ou
npm start    # Production
```

#### 7. Démarrage du Frontend
```bash
cd client
npm start
```

### Accès à l'application
- **Frontend** : http://localhost:3000
- **Backend API** : http://localhost:5001

---

## 🧪 Tests et Validation

### Tests Fonctionnels
1. **Inscription/Connexion**
   - Créer un compte avec photo de profil
   - Se connecter avec les identifiants
   - Vérifier la persistance de la session

2. **Gestion des Annonces**
   - Publier une annonce avec photos
   - Modifier sa propre annonce
   - Supprimer une annonce
   - Vérifier que les boutons modif/suppr n'apparaissent que sur ses annonces

3. **Messagerie**
   - Démarrer une conversation depuis une annonce
   - Envoyer des messages
   - Vérifier les indicateurs de messages non lus
   - Tester la distinction visuelle envoi/réception

4. **Favoris**
   - Ajouter des annonces aux favoris (cœur rouge)
   - Consulter la page "Mes Favoris"
   - Vérifier le compteur

### Tests Techniques
- **Responsivité** : Tester sur mobile, tablette, desktop
- **Navigateurs** : Chrome, Firefox, Edge, Safari
- **Performance** : Temps de chargement, optimisation images
- **Sécurité** : Tentatives d'accès non autorisé, validation des données

---

## 🔒 Sécurité Implémentée

### Côté Serveur
- **Authentification JWT** : Tokens sécurisés avec expiration
- **Hashage des mots de passe** : bcrypt avec salt
- **Validation des données** : express-validator
- **Protection XSS** : xss-clean
- **Rate limiting** : express-rate-limit
- **CORS** : Configuration sécurisée
- **Helmet** : Headers de sécurité HTTP

### Côté Client
- **Validation des formulaires** : Messages d'erreur en temps réel
- **Protection des routes** : Guards d'authentification
- **Sanitisation** : Nettoyage des entrées utilisateur

---

## 📱 Fonctionnalités Responsive

### Breakpoints
- **Mobile** : < 768px
- **Tablette** : 768px - 1024px
- **Desktop** : > 1024px

### Adaptations
- **Navigation** : Menu hamburger sur mobile
- **Grille d'annonces** : 1 colonne mobile, 2 tablette, 3 desktop
- **Formulaires** : Champs adaptés à la taille d'écran
- **Images** : Optimisation automatique

---

## 🎨 Design et UX

### Framework UI : Material-UI (MUI)
- **Composants cohérents** : Design system Google Material Design
- **Thème personnalisé** : Couleurs adaptées à l'éducation
- **Accessibilité** : Conformité WCAG
- **Internationalisation** : Support multilingue (arabe/français)

### Palette de Couleurs
- **Primaire** : Bleu éducatif (#1976d2)
- **Secondaire** : Vert réussite (#388e3c)
- **Accent** : Orange motivation (#ff9800)

---

## 📊 Base de Données

### MongoDB Collections
- **users** : Informations utilisateurs
- **listings** : Annonces avec photos
- **conversations** : Conversations messagerie
- **messages** : Messages individuels
- **notifications** : Système de notifications

### Index et Performance
- Index sur les champs fréquemment recherchés
- Agrégations pour les statistiques
- Optimisation des requêtes

---

## 🚀 Déploiement

### Environnement de Production
```bash
# Build du frontend
cd client
npm run build

# Configuration PM2
cd ..
pm2 start ecosystem.config.json --env production

# Configuration Nginx (optionnel)
# Copier server/config/nginx.conf
```

### Variables d'Environnement
- **MONGODB_URI** : Connexion base de données
- **JWT_SECRET** : Clé secrète JWT
- **PORT** : Port du serveur (5001)
- **NODE_ENV** : production/development

---

## 👥 Collaboration et Méthodologie

### Outils Utilisés
- **Git/GitHub** : Versioning et collaboration
- **Trello/Notion** : Gestion des tâches
- **Discord/Slack** : Communication équipe
- **VS Code** : Éditeur de code
- **Postman** : Test des API

### Méthodologie Agile
- **Sprints hebdomadaires** : Planification, développement, revue
- **Code review** : Validation collective des modifications
- **Documentation** : Mise à jour continue de la documentation
- **Tests continus** : Validation à chaque modification

---

## 🔧 Maintenance et Évolutions

### Scripts Disponibles
- **Sauvegarde** : `server/scripts/backup.js`
- **Initialisation DB** : `server/scripts/init-database.js`
- **Tests de charge** : Utilisation d'autocannon
- **Monitoring** : PM2 monit

### Améliorations Futures
- **Notifications push** : Service workers
- **Paiement intégré** : Stripe/PayPal
- **Géolocalisation** : Cartes interactives
- **IA** : Recommandations personnalisées

---

## 📈 Métriques et Performances

### KPIs
- **Temps de chargement** : < 3 secondes
- **Taux de conversion** : Inscription → Publication d'annonce
- **Engagement** : Messages échangés, favoris ajoutés
- **Satisfaction** : Feedback utilisateurs

### Optimisations
- **Images** : Compression automatique, formats WebP
- **Bundle** : Code splitting, lazy loading
- **Cache** : Headers appropriés, service worker
- **CDN** : Distribution des assets statiques

---

## 📞 Support et Contact

### Équipe Technique
- **Lead Developer** : [Nom] - [Email]
- **Backend Developer** : [Nom] - [Email]
- **Frontend Developer** : [Nom] - [Email]
- **UI/UX Designer** : [Nom] - [Email]

### Documentation Complète
- **Guide d'utilisation** : `GUIDE_UTILISATION.md`
- **Guide d'implémentation** : `GUIDE_IMPLEMENTATION_PRIORITAIRE.md`
- **API Documentation** : Disponible via Swagger (futur)

---

## 🎯 Conclusion

Ce livrable présente un site web fonctionnel complet répondant aux exigences de l'Objectif 3. L'application **Schoola-Taawon** offre une plateforme moderne et sécurisée d'échange de fournitures scolaires pour les étudiants tunisiens.

### Points Forts
- ✅ **5+ pages dynamiques** : Home, Listings, Détails, Messagerie, Profil
- ✅ **Frontend complet** : React + TypeScript + Material-UI
- ✅ **Backend robuste** : Node.js + Express + MongoDB
- ✅ **Fonctionnalités avancées** : Temps réel, upload, sécurité
- ✅ **Responsive design** : Adapté tous supports

---

## 🧩 Cas particulier : Présence d’un backend (instructions d’évaluation)

L’application comprend un backend Node.js/Express connecté à MongoDB (Atlas). Cette section fournit tout le nécessaire pour l’exécuter et le tester rapidement, en particulier avec MongoDB Atlas qui requiert une configuration réseau spécifique.

### 🔧 Prérequis backend
- Node.js 16+ et npm
- Compte MongoDB Atlas (ou instance MongoDB locale)
- Navigateur moderne (Chrome, Firefox, Edge)

### ⚙️ Configuration de l’environnement (server/.env)
Créer ou vérifier le fichier `server/.env` avec les variables suivantes (exemple de format, sans secret) :

```
PORT=5001
# URI Atlas — remplacez <USER>, <PASSWORD>, <HOST>
MONGODB_URI=mongodb+srv://<USER>:<PASSWORD>@<HOST>/schoola-taawon?retryWrites=true&w=majority&appName=Cluster0

# Clé JWT arbitraire pour tests
JWT_SECRET=schoola-taawon-secret-key-2025

# Optionnel: origine autorisée côté client
CLIENT_URL=http://localhost:3000
```

Notes:
- Le nom de base utilisé est `schoola-taawon` (inclus dans l’URI).
- Le paramètre `appName=Cluster0` est recommandé pour Atlas.
- Ne pas commiter de mots de passe en clair dans un dépôt public.

### 🌐 Autoriser l’IP sur MongoDB Atlas
1) Atlas > Network Access > Add IP Address > Add Current IP Address
2) Attendre 1–2 minutes que la règle s’applique
3) Option de dev (temporaire): `0.0.0.0/0` (à retirer ensuite)

### ▶️ Démarrer le backend (développement)
Dans le dossier `server/` :

```
npm install
npm run dev   # lance nodemon sur http://localhost:5001
```

Production (optionnel) :
```
npm start
```

PM2 (optionnel) :
```
pm2 start ecosystem.config.json --env production
```

### 🔌 Ports utilisés
- Backend API: http://localhost:5001
- Frontend: http://localhost:3000 (npm start)

### 🧪 Endpoints/API rapides pour tests
- Annonces (public): `GET http://localhost:5001/api/listings`
- Auth:
  - `POST http://localhost:5001/api/auth/register`
  - `POST http://localhost:5001/api/auth/login`
- Messagerie:
  - `GET http://localhost:5001/api/messages/conversations`
  - `GET http://localhost:5001/api/messages/unread-count`

### 🖼️ Uploads de fichiers
- Upload via `multer` (diskStorage)
- Stockage local: `server/uploads/`
- Exposition statique: `http://localhost:5001/uploads/<fichier>`

### 🧵 Socket.IO (temps réel)
- Servi sur le même host/port que l’API
- Le client s’y connecte automatiquement (auth: `user.id`)

### 🛠️ Dépannage Atlas (erreurs fréquentes)
- « Could not connect to any servers in your MongoDB Atlas cluster »
  - Vérifier l’IP whitelist
  - Vérifier `MONGODB_URI` (USER/PASSWORD/HOST corrects et base présente)
- « querySrv ENOTFOUND _mongodb._tcp.<host> »
  - Hôte Atlas incorrect (copier-coller l’URI depuis Atlas)
- Erreur 500 `/api/messages/unread-count`
  - Géré dans ce projet (normalisation d’IDs peuplés vs strings)

### ✅ Procédure de test (recommandée)
1) Configurer `server/.env` avec votre URI Atlas et `JWT_SECRET`
2) Autoriser votre IP sur Atlas
3) Démarrer backend: `cd server && npm install && npm run dev`
4) Démarrer frontend: `cd client && npm install && npm start`
5) Ouvrir `http://localhost:3000`
6) Créer 2 comptes et tester: Auth, CRUD annonces (avec images), Favoris, Messagerie (A→B, B→A), Notifications
- ✅ **Code qualité** : Structure organisée, bonnes pratiques

### Technologies Maîtrisées
- Frameworks modernes (React, Node.js)
- Base de données NoSQL (MongoDB)
- Communication temps réel (Socket.IO)
- Sécurité web (JWT, validation, CORS)
- Déploiement production (PM2, Nginx)

---

**Date de soumission :** [Date]
**Version :** 1.0.0
**Statut :** ✅ Prêt pour production



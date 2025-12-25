# Schoola-Taawon 📚

## Description
Plateforme d'échange de fournitures scolaires pour les étudiants tunisiens. Cette application permet aux étudiants de publier, rechercher et échanger des fournitures scolaires de manière simple et sécurisée.

## Fonctionnalités principales
- 👥 **Authentification** : Inscription et connexion sécurisées
- 📝 **Annonces** : Publication, consultation et gestion des annonces
- 🔍 **Recherche avancée** : Filtrage par catégorie, ville, état, etc.
- 💬 **Messagerie** : Communication en temps réel entre utilisateurs
- 📸 **Gestion des médias** : Téléchargement et affichage d'images
- ⭐ **Favoris** : Sauvegarde des annonces préférées

## 🚀 Démarrage rapide

### Prérequis
- Node.js v16 ou supérieur
- MongoDB (local ou Atlas)
- npm ou yarn

### Installation

1. **Cloner le dépôt**
   ```bash
   git clone https://github.com/votre-utilisateur/schoola-taawon.git
   cd schoola-taawon
   ```

2. **Backend**
   ```bash
   cd server
   npm install
   cp .env.example .env
   # Configurer les variables d'environnement dans .env
   npm run dev  # Mode développement
   # OU
   npm start    # Mode production
   ```

3. **Frontend**
   ```bash
   cd ../client
   npm install
   npm start    # Démarre sur http://localhost:3000
   ```

## 🏗 Structure du projet

```
schoola-taawon/
├── client/                 # Application React (Frontend)
│   ├── public/            # Fichiers statiques
│   └── src/
│       ├── components/    # Composants réutilisables
│       ├── pages/         # Pages de l'application
│       ├── context/       # Contextes React
│       ├── services/      # Appels API
│       └── types/         # Types TypeScript
│
├── server/                # API Node.js (Backend)
│   ├── controllers/       # Logique métier
│   ├── models/            # Modèles MongoDB
│   ├── routes/            # Routes API
│   ├── middleware/        # Middleware (auth, upload, etc.)
│   └── uploads/           # Fichiers uploadés (images)
│
└── README.md             # Cette documentation
```

## 🧪 Tests

### Backend
```bash
cd server
npm test
```

### Frontend
```bash
cd client
npm test
```

## 🚀 Déploiement

### Préparation
1. Configurer les variables d'environnement de production
2. Installer PM2 globalement : `npm install -g pm2`

### Frontend
```bash
cd client
npm run build
# Le dossier build/ contient les fichiers à déployer
```

### Backend
```bash
cd server
npm install --production
pm2 start ecosystem.config.json --env production
```

## 🔒 Sécurité
- Authentification par JWT
- Validation des données côté serveur
- Protection contre les attaques XSS et CSRF
- Gestion sécurisée des uploads de fichiers
- Rate limiting pour prévenir les abus

## 🛠 Maintenance
- **Logs** : `/var/log/schoola-taawon/`
- **Monitoring** : `pm2 monit`
- **Sauvegarde** : Configuration MongoDB Atlas ou script de sauvegarde

## 🤝 Contribution
1. Forkez le projet
2. Créez une branche : `git checkout -b feature/ma-fonctionnalite`
3. Committez vos changements : `git commit -am 'Ajout d\'une fonctionnalité'`
4. Poussez la branche : `git push origin feature/ma-fonctionnalite`
5. Créez une Pull Request

## 📄 Licence
Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 📞 Support
Pour toute question ou problème, veuillez ouvrir une issue sur GitHub ou nous contacter à support@schoola-taawon.tn
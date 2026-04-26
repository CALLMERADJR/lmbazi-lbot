# Instructions de Déploiement sur Render

Ce bot a été configuré pour être déployé sur Render. Voici les étapes à suivre :

## 1. Prérequis
- Un compte [Render](https://render.com) (gratuit).
- Un compte [GitHub](https://github.com).

## 2. Étapes de déploiement
1. **Forkez** ce dépôt sur votre propre compte GitHub.
2. Sur Render, créez un nouveau **Web Service**.
3. Connectez votre compte GitHub et sélectionnez le dépôt forké.
4. Configurez les paramètres suivants :
   - **Runtime** : `Node`
   - **Build Command** : `npm install`
   - **Start Command** : `node index.js`
5. Ajoutez les **Environment Variables** suivantes dans l'onglet "Environment" :
   - `TOKEN` : Votre token Discord (déjà inclus dans le code, mais conseillé ici).
   - `MONGODB_URI` : Votre URI MongoDB.
   - `SPOTIFY_CLIENT_ID` : Votre ID client Spotify.
   - `SPOTIFY_CLIENT_SECRET` : Votre Secret client Spotify.
6. Cliquez sur **Create Web Service**.

## 3. Garder le bot en ligne 24/7
Comme Render met les services gratuits en veille après 15 minutes d'inactivité, utilisez un service comme [BetterStack](https://betterstack.com/) ou [Cron-job.org](https://cron-job.org/) pour appeler l'URL de votre service Render toutes les 5 à 10 minutes.

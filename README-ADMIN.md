# YOUTUBE BUSINESS 360° — Administration et accès protégés

## Ce que cette version ajoute
- panneau administrateur sur `/admin`
- connexion administrateur protégée par identifiants stockés dans les variables d'environnement
- ajout / activation / blocage / suppression d'utilisateurs
- base locale JSON dans `data/users.json`
- page `/connexion` pour les clients
- protection serveur des pages de formation : elles ne sont servies qu'à un utilisateur autorisé et connecté

## Installation Windows
1. Installer Node.js 18 ou plus récent.
2. Ouvrir PowerShell dans le dossier du projet.
3. Copier `.env.example` en `.env`.
4. Modifier `.env` et choisir votre email admin, un mot de passe fort et une longue valeur `SESSION_SECRET`.
5. Lancer : `npm start`
6. Ouvrir : `http://127.0.0.1:3000/admin`

## Important
Cette version constitue la base technique de l'accès protégé. Le paiement automatique de 1 $ et l'envoi de liens de connexion par email nécessitent ensuite un prestataire de paiement et un service d'envoi d'emails côté serveur. Ne mettez jamais une clé secrète de paiement ou une clé serveur dans les fichiers HTML/JavaScript publics.

Pour une mise en ligne publique, déployer ce serveur sur un hébergement backend HTTPS (et non uniquement GitHub Pages). La base locale JSON convient pour une petite installation/test ; pour une exploitation commerciale avec plusieurs connexions simultanées, migrer vers SQLite/PostgreSQL.


## Gaston N3 — présentation du fondateur
La page d’accueil présente désormais le fondateur Gaston N3 avec sa photo, son profil professionnel, son contact WhatsApp et ses réseaux sociaux (YouTube, Facebook, TikTok). Les liens sociaux utilisent des recherches de nom tant que les URLs officielles de profils n’ont pas été fournies.

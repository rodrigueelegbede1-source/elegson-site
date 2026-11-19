# Site Elegson

Landing page statique d'Elegson, dans `index.html`. Elle charge React et
Tailwind CSS depuis des CDN publics et ne nécessite aucune variable
d'environnement ni commande de build.

Le projet Vercel `elegson/elegson-site` est relié à ce dépôt et utilise la
branche `main` pour la production. `vercel.json` définit les en-têtes HTTP
appliqués par Vercel. GitHub Pages sert également la page depuis `main`.

Le formulaire prépare un message dans l'application e-mail ou WhatsApp du
visiteur ; il n'envoie pas de données à un serveur.

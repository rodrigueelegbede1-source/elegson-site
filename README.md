# Site Elegson

Landing page statique d'Elegson, dans `index.html` et `app.js`. React est
chargé depuis un CDN public, en différé. Le CSS Tailwind est précompilé et
versionné ; aucune commande de build n'est nécessaire au déploiement.
Après modification des classes utilitaires, régénérer le fichier :

```bash
npx --yes tailwindcss@3.4.17 -c tailwind.config.cjs -o tailwind.css --minify
```

Le projet Vercel `elegson/elegson-site` est relié à ce dépôt et utilise la
branche `main` pour la production. `vercel.json` définit les en-têtes HTTP
appliqués par Vercel. GitHub Pages sert également la page depuis `main`.

Le formulaire prépare un message dans l'application e-mail ou WhatsApp du
visiteur ; il ne soumet rien au site. La validation et le champ piège
freinent les robots simples mais ne filtrent pas l'e-mail ou WhatsApp.

Le bandeau ne charge aucun outil d'audience actuellement. Pour activer GA4,
mettre à jour la politique de confidentialité et la CSP Vercel (script depuis
`www.googletagmanager.com`, connexions et images vers les points de collecte
GA4 utilisés), renseigner l'identifiant **public** `G-…` dans `consent.js`,
puis vérifier en préproduction les parcours refuser, accepter et retirer.
Aucune clé secrète ne doit être placée dans le site statique.

Avant publication, faire valider les pages légales : identité juridique de
l'éditeur, modalités d'exercice des droits et règles de conservation.

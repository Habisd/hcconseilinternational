# H&C Conseil International - GitHub Pages

Site vitrine statique pret pour GitHub Pages.

## Publication recommandee

1. Creer un depot GitHub, par exemple `Habisd/hc-conseil-international`.
2. Ajouter tout le contenu de ce dossier a la racine du depot.
3. Dans GitHub : `Settings` -> `Pages`.
4. Source : `Deploy from a branch`.
5. Branch : `main`, folder : `/root`.
6. Custom domain : `hcconseilinternational.com`.
7. Activer `Enforce HTTPS` quand GitHub le permet.

## DNS GitHub Pages

Pour le domaine racine :

```text
A @ 185.199.108.153
A @ 185.199.109.153
A @ 185.199.110.153
A @ 185.199.111.153
```

Pour `www`, si l'enregistrement peut etre modifie :

```text
CNAME www Habisd.github.io
```

GitHub indique que la propagation DNS peut prendre jusqu'a 24 heures.

## Formulaire de contact

Le site contient maintenant :

- un formulaire de contact complet ;
- une fenetre `Appeler` avec lien telephonique, WhatsApp et demande de rappel ;
- un fichier `app.js` pret a envoyer les messages vers un Cloudflare Worker.

Avant publication finale, remplacer dans `app.js` :

```js
const CONTACT_ENDPOINT = "https://hc-conseil-contact.YOUR_SUBDOMAIN.workers.dev";
```

par l'URL reelle du Worker Cloudflare.

Le Worker pret a utiliser est dans le dossier voisin `hc-conseil-contact-worker`.
La cle Resend doit etre ajoutee dans Cloudflare comme secret `RESEND_API_KEY`, jamais dans ce dossier GitHub Pages.

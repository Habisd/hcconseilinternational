# H&C Conseil International - GitHub Pages

Site vitrine statique prêt pour GitHub Pages.

## Publication recommandée

1. Créer un dépôt GitHub, par exemple `Habisd/hc-conseil-international`.
2. Ajouter tout le contenu de ce dossier à la racine du dépôt.
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

Pour `www`, si l'enregistrement peut être modifié :

```text
CNAME www Habisd.github.io
```

GitHub indique que la propagation DNS peut prendre jusqu'à 24 heures.

## Formulaire de contact

GitHub Pages héberge seulement des fichiers statiques. Pour un formulaire connecté à Resend, il faudra ajouter un petit endpoint serveur séparé, par exemple Cloudflare Worker, Vercel Function ou Netlify Function, afin de garder la clé API Resend secrète.

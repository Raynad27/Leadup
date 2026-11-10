# Site web Leadup

Site vitrine en HTML + CSS (aucun JavaScript), en arabe de droite à gauche.

```
leadup-site/
├── index.html          la page
├── css/style.css       la mise en forme
└── images/             logo, favicon, capture d'écran
```

## 1. À compléter avant la mise en ligne

Ouvrez `index.html` avec VS Code et cherchez (Ctrl+F) :

| Chercher | Remplacer par |
|---|---|
| `ID_SURVEILLANT_64` | l'identifiant Google Drive de l'installeur Surveillant 64 bits |
| `ID_SURVEILLANT_32` | … Surveillant 32 bits |
| `ID_DIRECTEUR_64` | … Directeur 64 bits |
| `ID_DIRECTEUR_32` | … Directeur 32 bits |
| `VOTRE_EMAIL` | votre adresse e-mail |
| `212XXXXXXXXX` | votre numéro WhatsApp au format international, sans + ni 0 (ex. 2126XXXXXXXX) |
| `1.0.0` | le numéro de version, à chaque nouvelle version |

## 2. Récupérer l'identifiant Google Drive d'un installeur

1. Déposez `Setup_Leadup_Surveillant_1.0.0.exe` (etc.) dans Google Drive.
2. Clic droit → **Partager** → Accès général : **Tous les utilisateurs disposant du lien**.
3. **Copier le lien**. Il ressemble à :
   `https://drive.google.com/file/d/1AbCdEfGhIjKlMnOp/view?usp=sharing`
4. L'identifiant est la partie entre `/d/` et `/view` : `1AbCdEfGhIjKlMnOp`.
5. Dans `index.html`, remplacez `ID_SURVEILLANT_64` par cet identifiant.

Le bouton téléchargera alors directement le fichier. Pour un fichier volumineux,
Google Drive affiche d'abord « Impossible de rechercher des virus » : l'utilisateur
clique sur **Télécharger quand même** (c'est expliqué sur le site, étape 1).

**Mise à jour d'une version :** dans Drive, clic droit sur le fichier → **Gérer les
versions** → **Importer une nouvelle version**. L'identifiant ne change pas, le site
n'a pas besoin d'être modifié (sauf le numéro de version affiché).

## 3. Mettre le site en ligne avec GitHub Pages

1. Créez un compte sur https://github.com (gratuit).
2. **New repository** → nom : `leadup` (ou `votre-nom.github.io` pour avoir une adresse sans sous-dossier) → **Public** → **Create repository**.
3. **Add file → Upload files** → glissez le **contenu** du dossier `leadup-site`
   (`index.html`, le dossier `css`, le dossier `images`) → **Commit changes**.
   `index.html` doit être à la racine du dépôt, pas dans un sous-dossier.
4. **Settings → Pages** → Source : **Deploy from a branch** → Branch : `main` / `(root)` → **Save**.
5. Après 1 à 2 minutes, le site est en ligne à :
   `https://votre-nom.github.io/leadup/`

Pour modifier le site plus tard : éditez le fichier sur GitHub (icône crayon) ou
ré-importez-le ; la mise en ligne se refait automatiquement.

**Nom de domaine (facultatif)** : achetez par exemple `leadup.ma` ou `leadup-app.com`,
puis Settings → Pages → **Custom domain**, et suivez les instructions DNS de GitHub.

## 4. Ajouter de vraies captures d'écran

La capture actuelle (`images/apercu-examens.jpg`) est une maquette.
Pour la remplacer : faites une capture du programme (touche Windows + Maj + S),
enregistrez-la en JPG dans `images/` sous le même nom, ou ajoutez d'autres
`<figure class="shot">` dans la section « لقطات » de `index.html`.

## 5. Tester sur votre PC avant la mise en ligne

Double-cliquez sur `index.html` : le site s'ouvre dans le navigateur.
Rétrécissez la fenêtre pour voir la version téléphone (menu ☰).

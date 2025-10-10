# QCMWebsite

Site statique pour des QCM et cours (HTML + JSON).

## Description

Projet simple contenant une page d'accueil `index.html` et plusieurs pages de cours et QCM dans le dossier `public/`.

Les questions des QCM sont stockées en JSON (par exemple `public/questionsPOO1.json`, `public/questionsOSINT1.json`, `public/questionsWindows1.json`, ...).

## Structure

- `index.html` : page d'accueil
- `app.css` / `public/output.css` : styles
- `public/` : pages de cours, fichiers JSON de questions et autres ressources

Exemples:
- `public/Java.html`
- `public/WindowsCours1.html`
- `public/questionsOSINT1.json`

## Lancer le site en local

Comme il s'agit d'un site statique, vous avez deux options simples :

1) Ouvrir `index.html` directement dans votre navigateur (double-clic) — fonctionne pour la plupart des usages mais peut restreindre certaines requêtes locales liées à `fetch`.

2) Servir le dossier via un serveur HTTP local (recommandé) :

En utilisant Python 3 :

```bash
# depuis la racine du projet
python3 -m http.server 8000
# puis ouvrez http://localhost:8000
```

En utilisant `npm` (si vous avez `live-server` installé globalement) :

```bash
# installer live-server si nécessaire
# npm install -g live-server
live-server --port=8000
```

## Modifier / ajouter des questions

Les QCM sont définis dans des fichiers JSON dans `public/`. Chaque fichier contient un tableau d'objets question. Pour ajouter un QCM :

1. Créez un nouveau fichier `public/questionsNOM.json` en suivant le même format que les fichiers existants.
2. Ajoutez une nouvelle page HTML ou modifiez une page existante pour charger ce JSON via `fetch`.

## Contribuer

- Faites une branche et ouvrez une pull request. Gardez les changements concentrés (nouvelle page, nouveau QCM, corrections de style).

## Licence

Ce projet est distribué sous la licence MIT. Voir le fichier `LICENSE` à la racine pour le texte complet.


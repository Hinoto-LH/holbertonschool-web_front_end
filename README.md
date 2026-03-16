# holbertonschool-web_front_end

Guide des bases HTML

Ce document explique les principales bonnes pratiques et concepts nécessaires pour structurer correctement une page web en HTML.

## Quelles bonnes pratiques suivre en HTML

Lorsque vous écrivez du HTML, il est important de suivre certaines règles :

Utiliser HTML5

- Respecter une structure sémantique
- Garder un code propre et lisible
- Utiliser une indentation claire
- Toujours ajouter l'attribut alt aux images
- Respecter les standards d’accessibilité
- Utiliser des balises HTML appropriées au lieu de conteneurs inutiles
- Respecter une structure de titres logique pour le SEO

## Comment créer le squelette d'une page HTML5

Chaque page HTML commence par une structure de base :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ma page web</title>
</head>

<body>

  <header>
    <h1>Titre du site</h1>
  </header>

  <main>
    <p>Le contenu principal va ici.</p>
  </main>

  <footer>
    <p>© 2026</p>
  </footer>

</body>
</html>
```

## Comment utiliser les balises HTML sémantiques pour structurer une page

Les balises sémantiques donnent du sens au contenu, ce qui aide :

les navigateurs

les moteurs de recherche

les technologies d’assistance

Exemples :

Balise	Utilité
header	Contenu d’introduction
nav	Navigation
main	Contenu principal
section	Groupe de contenu
article	Contenu indépendant
aside	Contenu secondaire
footer	Informations en bas de page

Exemple :

```html
<main>
  <section>
    <article>
      <h2>Article de blog</h2>
      <p>Contenu de l'article</p>
    </article>
  </section>
</main>
```

## Quand utiliser div et span
div

- Élément block
- Sert à regrouper de grandes sections
- Souvent utilisé pour la mise en page

Exemple :

```html
<div class="container">
  <p>Contenu</p>
</div>
span
```

- Élément inline
- Sert à modifier ou styliser une partie du texte

Exemple :

```html
<p>Ceci est un mot <span class="highlight">important</span>.</p>
```

## Valeur sémantique des principales balises
header

Contient généralement :

- le logo
- le titre
- la navigation

#### nav

Utilisé pour les menus de navigation.

#### main

Contient le contenu principal de la page.

#### article

Représente un contenu autonome (article, publication, news).

#### section

Permet de regrouper un ensemble de contenu lié.

#### aside

Contient des informations secondaires ou complémentaires (sidebar).

#### footer

Contient souvent :

- copyright
- liens
- informations de contact

## Comment utiliser les titres (et pourquoi la hiérarchie est importante)

Les titres HTML vont de h1 à h6.

Une bonne hiérarchie améliore :

- l’accessibilité
- le référencement (SEO)
- la lisibilité

Exemple :

```html
<h1>Titre principal</h1>
<h2>Titre de section</h2>
<h3>Sous-section</h3>
```

Règles :

utiliser un seul h1 par page (recommandé)

ne pas sauter de niveaux (éviter h1 → h4)

## Comment créer des listes en HTML
Liste non ordonnée

```html
<ul>
  <li>Pomme</li>
  <li>Banane</li>
  <li>Orange</li>
</ul>
```
Liste ordonnée
```html
<ol>
  <li>Étape 1</li>
  <li>Étape 2</li>
</ol>
```
Liste de description
```html
<dl>
  <dt>HTML</dt>
  <dd>Langage de balisage pour créer des pages web</dd>
</dl>
```

## Différences entre les formats d’image

Format|	Utilisation
------|----------------------
SVG	  |Graphiques vectoriels, logos, icônes
GIF.  |	Animations simples
PNG	  |Images de haute qualité avec transparence
JPG / JPEG|	Photographies compressées

Résumé :

- SVG → graphique vectoriel redimensionnable
- PNG → images nettes avec transparence
- JPG → photos
- GIF → animations

## Comment structurer des données dans un tableau

Exemple :

```html
<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Âge</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Alice</td>
      <td>25</td>
    </tr>
  </tbody>
</table>
```

Balises importantes :

Balise|	Rôle
------|--------------------
table |Conteneur du tableau
thead |	En-tête du tableau
tbody |	Corps du tableau
tr.   |	Ligne
th	  |Cellule d'en-tête
td	  |Cellule de données

## Comment intégrer une vidéo dans une page web

Utilisation de la balise video :

```html
<video controls width="600">
  <source src="video.mp4" type="video/mp4">
  Votre navigateur ne supporte pas la vidéo.
</video>
```

Attributs utiles :

- controls
- autoplay
- loop
- muted

## Comment intégrer un fichier audio dans une page web

Utilisation de la balise audio :

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Votre navigateur ne supporte pas l'audio.
</audio>
```

## Comment intégrer du contenu externe

On utilise la balise iframe.

Exemple :

```html
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  width="560"
  height="315"
  frameborder="0"
  allowfullscreen>
</iframe>
```

Cela permet d’intégrer :

- vidéos YouTube
- cartes Google Maps
- pages externes

## Comment bien structurer une page HTML

Structure recommandée :

```html
<body>

<header>
  <nav></nav>
</header>

<main>

  <section>
    <article></article>
  </section>

  <aside></aside>

</main>

<footer></footer>

</body>
```

Bonne organisation :

header → introduction et navigation

main → contenu principal

sections / articles → organisation du contenu

aside → contenu secondaire

footer → informations finales

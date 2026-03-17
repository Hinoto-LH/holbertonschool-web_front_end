# Maîtrise du CSS : Fondamentaux et Concepts Avancés

Ce guide regroupe les concepts essentiels pour passer de "je change la couleur d'un texte" à une compréhension réelle de l'architecture CSS.

## Syntaxe et Structure
Le CSS fonctionne sur un système simple de Sélecteur, Propriété et Valeur.

- Sélecteur : Cible l'élément HTML (ex: ```h1```, ```.ma-classe```, ```#mon-id```).
- Propriété : Ce que l'on veut changer (ex: ```color```, ```margin```).
- Valeur : Le réglage appliqué (ex: ```red```, ```20px```).

Méthodes d'intégration

1. Inline (En ligne) : Directement dans la balise HTML via l'attribut ```style```. (À éviter).

2. Embedded (Interne) : Dans une balise ```<style>``` au sein du ```<head>```.

3. External (Externe) : Dans un fichier ```.css``` séparé, lié via une balise ```<link>```. C'est la méthode standard pour la maintenance.

## Le Modèle de Boîte (Box Model)

Il est crucial de différencier le comportement des éléments :

- Block : L'élément prend toute la largeur disponible et commence sur une nouvelle ligne (ex: ```<div>```, ```<h1>```, ```<p>```).

- Inline : L'élément ne prend que la largeur nécessaire et ne force pas de retour à la ligne (ex: ```<span>```, ```<a>```).

## Architecture et Consistance

### CSS Reset
Les navigateurs (Chrome, Firefox, Safari) appliquent des styles par défaut différents. Un CSS Reset (ou une Normalize) est un morceau de code qui remet ces compteurs à zéro pour garantir que votre site ressemble à la même chose partout.

### Variables CSS (Custom Properties)
Pour maintenir un code propre, on utilise des variables :

```CSS
:root {
  --primary-color: #3498db;
  --main-padding: 15px;
}

.button {
  background-color: var(--primary-color);
}
```
## Mise en page : Le système de Grille (via Floats)
Avant Flexbox et Grid Layout, on utilisait les floats. Bien que moins commun aujourd'hui, comprendre ce système est vital pour la maintenance de vieux projets :

- On utilise ```float: left;``` ou ```right;```.

- Il faut impérativement "nettoyer" le flux après des éléments flottants avec un ```clear:``` ```both;``` ou un "clearfix" sur le parent pour éviter que le container ne s'effondre.

## Sélecteurs Avancés

Pseudo-classes : Ciblent l'état d'un élément (ex: ```:hover``` au survol, ```:nth-child(2)``` pour le deuxième enfant).

Pseudo-éléments : Ciblent une partie spécifique d'un élément (ex: ```::before``` ou ```::after``` pour insérer du contenu cosmétique, ```::first-letter```).

## Graphisme et Assets

### Gradients (Dégradés)
On utilise ```linear-gradient``` ou ```radial-gradient``` sur la propriété ```background```.

Exemple : ```background: linear-gradient(to right, red, blue);```

### Icônes : Webfonts vs SVG

- Webfonts (ex: FontAwesome) : Faciles à utiliser comme du texte, mais moins flexibles et plus lourdes.
- SVG : Vecteurs nets à toutes les résolutions, manipulables par CSS (couleurs, animations), plus performants.

## Animations et Transformations

### Transformations (2D & 3D)
La propriété ```transform``` permet de modifier la géométrie :

- translate(x, y) : Déplacement.
- rotate(deg) : Rotation.
- scale(n) : Redimensionnement.
- L'ajout d'une perspective permet de manipuler l'axe Z (3D).

### Animations
On définit des étapes avec @keyframes et on les applique avec la propriété animation.

```CSS
@keyframes slide {
  from { left: 0; }
  to { left: 100px; }
}
```

## Compatibilité : Vendor Prefixes

Certaines fonctionnalités récentes ne sont pas standardisées immédiatement. On ajoute des préfixes pour que les moteurs de rendu les comprennent :

- -webkit- (Chrome, Safari, versions récentes d'Edge)
- -moz- (Firefox)
- -ms- (Internet Explorer / Old Edge)

Note : Maîtriser ces points, c'est posséder les fondations nécessaires pour apprendre n'importe quel framework moderne (Tailwind, Bootstrap).

# Synthèse : Texte et couleurs

## 1. Définir une couleur en CSS

Pour définir une couleur pour du texte en CSS on utilise la propriété `color`ou pour définir la couleur d'un fond la propriété `background-color`suivie d'une valeur qui peut être dans différent formats : 

- un nom : `red`
- l'hexadécimal : `#ff0000`
- `rgb(255, 0, 0)`
- `hsl(0, 100%, 50%)`

Ces 4 formats permettent de donnée du rouge mais certain comme HSL permet de nuancé et de choisir la couler exact voulue et pas la couleur par default du `red`.

## 2. Différence entre  `px`, `em` et `rem` 

Ce sont toutes les trois des unités permettant de définir une taille en CSS :

- `px`(pixel) est une unité absolue, quel que soit le contexte elle vaudra la même chose, par exemple si elle vaut `16px`ce sera la même taille sur un ordinateur que sur un telephone.
- `em`est une unité relative, `1em` correspond à la taille de police de l'élément parent, elle sert a faire des tailles qui suivent le texte, si le parent fait `20px`, alors `1.5em` fait `30px`.
- `rem`(root em) est aussi une unité relative mais ele prendre toujours comme réference la taille de la police racine de la page, la balise `<html>`, elle sert a sert à définir des tailles de police et des espacements cohérents sur tout le site.

## 3. Choisir une police de caractères

Pour choisir une police de caractère on utilise la propriété `font-family`, à laquelle on donne une liste de polices par ordre de préference et on termine par une famille générique, par exemple:

```css
font-family: "Segoe UI", Arial, sans-serif;
```

Le navigateur prend la première police disponible sur l'ordinateur de l'utilisateur, sinon la suivante, et à défaut une police de la famille générique.

## 4. Différence entre `font-weight` et `font-style` 

Ce sont deux propriétés qui permette de changer l'epaisseur ou l'inclinaison d'un texte .

- `font-weight` règle l'épaisseur des traits : `normal` (400), `bold` (700), ou une valeur de 100 à 900.
- `font-style` règle l'inclinaison : `normal`, `italic` ou `oblique`.

Elles sont toutes les deux indépendantes, un texte peut être en gras seul, en italique seul, ou les deux.

## 5. Importance du contraste pour l'accessibilité

Le contraste est la différence de luminosité entre le texte et son fond. Un contraste faible rend la lecture difficile, voire impossible, pour les personnes malvoyantes, daltoniennes ou âgées. Il pénalise aussi tout le monde dans de mauvaises conditions : écran en plein soleil, petit écran, fatigue.
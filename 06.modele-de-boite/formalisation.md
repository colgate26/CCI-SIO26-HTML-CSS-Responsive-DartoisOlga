# 06 Le modèle de boîte CSS

## Fonctionnement du modèle de boîte 

Chaque élément HTML est une boîte rectangulaire.

Cette boîte a quatre couches. De l'intérieur vers l'extérieur :

1. Contenu : le texte, l'image, etc.
2. Padding : l'espace autour du contenu, à l'intérieur de la bordure.
3. Bordure (`border`) : le trait autour du padding.
4. Marge (`margin`) : l'espace autour de la bordure, à l'extérieur.

Le navigateur utilise ces couches pour calculer la taille et la position de chaque élément.

## Différence entre `margin` et `padding` 

- `padding` est l'espace à l'intérieur de la boîte. Il est dans la couleur de fond.
- `margin` est l'espace à l'extérieur de la boîte. Il est toujours transparent.

Le padding éloigne le contenu de la bordure.
La marge éloigne la boîte de ses voisines.

```css
.carte {
  padding: 16px; /* espace dans la carte */
  margin: 24px;  /* espace autour de la carte */
}
```

## Calculer la largeur totale avec `content-box` 

C'est le comportement par défaut.

Avec `content-box`, `width` ne mesure que le contenu.
Le padding et la bordure s'ajoutent.

Formule :

```
largeur totale = width + padding gauche + padding droit + bordure gauche + bordure droite
```

Exemple :

```css
.boite {
  box-sizing: content-box;
  width: 200px;
  padding: 20px;
  border: 5px solid black;
}
```

Calcul : 200 + 20 + 20 + 5 + 5 = 250 px.

La marge n'est pas comptée dans la largeur totale. Elle ajoute juste de l'espace autour.

## L'effet de `box-sizing: border-box` 

Avec `border-box`, `width` inclut le contenu, le padding et la bordure.

La boîte garde la largeur qu'on lui donne.
Le contenu se réduit pour faire de la place au padding et à la bordure.

Formule :

```
largeur totale = width
```

Exemple :

```css
.boite {
  box-sizing: border-box;
  width: 200px;
  padding: 20px;
  border: 5px solid black;
}
```

Largeur totale : 200 px.
Largeur du contenu : 200 − 20 − 20 − 5 − 5 = 150 px.

C'est plus facile à prévoir. Beaucoup de développeurs l'appliquent partout :

```css
*, *::before, *::after {
  box-sizing: border-box;
}
```

## Utiliser l'inspecteur du navigateur pour analyser les espacements 

1. Faire un clic droit sur l'élément.
2. Choisir Inspecter (ou appuie sur `F12`).
3. Sélectionner l'élément dans le panneau Éléments.
4. Ouvrir l'onglet Calculé (ou Computed).
5. Regarder le schéma du modèle de boîte.

Le schéma montre :

- le contenu au centre, avec ses dimensions ;
- le padding, souvent en vert ;
- la bordure, souvent en jaune ;
- la marge, souvent en orange.

En survolant un élément, le navigateur le colore sur la page. On voit ainsi ses marges et son padding.

On peut aussi modifier les valeurs dans le panneau Styles. Le résultat s'affiche tout de suite.


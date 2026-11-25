# Exercice 2

## Prévisions

2)Boite A : content-box

Largeur du contenu : 200 px

Largeur total visible : 200 + 20 + 20 + 10 + 10 = 260 px

Boite B : border-box

Largeur du contenu : 200 - 20 - 20 - 10 - 10 = 140 px

Largeur total visible : 200 px

4)

- `width: 200px` inclut maintenant le padding et la bordure.
- La largeur visible de A passe de 260 px à 200 px.
- Le contenu passe de 200 px à 140 px.
- A et B deviennent identiques.

Pour garder la même largeur il faut augmenter la `width` de la valeur du padding et de la bordure.

5)Avec `border-box`, la `width` est la largeur finale de la boîte. On n'a plus besoin de calculer. On peut changer le padding ou la bordure sans que la boîte change de taille. Les pourcentages sont aussi plus simples : deux boîtes à `width: 50%` tiennent côte à côte, même avec du padding.


Question n°1 : Quelle est la différence entre `color` et `background-color` ? Donne une règle CSS qui met le texte d'un paragraphe en gris foncé sur un fond jaune pâle.
Réponse (avant correction) : color c'est pour la couleur du texte et background-color pour le fond, `p { color:  #444444; background-color: #e6eeb2;}`
Correction de l'IA : Correct. `color` règle la couleur du texte, `background-color` celle du fond, et ta règle fait bien ce qui était demandé. Ton jaune `#e6eeb2` est pâle, et le contraste avec `#444444` est d'environ 8:1, donc largement lisible.
Réponse initiale : juste
À retenir :

Question n°2 : Voici une règle :

css

```css
body {
    font-family: Papyrus;
}
```

Quel problème pose-t-elle, et comment la corriges-tu ?

Réponse (avant correction) : il manque d'autres possibilité de police et une famille generique, `font-family: Papyrus, Arial, sans-serif;`
Correction de l'IA : Correct. Une seule police sans repli est risquée : si Papyrus n'est pas installée sur l'ordinateur de l'utilisateur, le navigateur choisit une police par défaut que tu ne contrôles pas. Il faut d'autres polices en solution de rechange, puis une famille générique en dernier.
Réponse initiale : juste 
À retenir : Papyrus est de plus une police décorative, peu lisible pour du texte courant, ce qui n'était pas demandé mais vaut la peine d'être noté.

Question n°3 : Dans ce code :

css

```css
html { font-size: 16px; }
.parent { font-size: 20px; }
.enfant { font-size: 1.5em; }
.autre  { font-size: 1.5rem; }
```

Si `.enfant` et `.autre` sont à l'intérieur de `.parent`, quelle taille réelle (en px) obtient chacun ? Justifie en une phrase.

Réponse (avant correction) :  `.enfant` sera de 30 px et `.autre` de 24 px car `em` se calcule à partir du parent, `rem` à partir de `<html>`.
Correction de l'IA : Correct. `.enfant` en `1.5em` est relatif à la taille du parent (1,5 × 20 = 30px), et `.autre` en `1.5rem` est relatif à la racine (1,5 × 16 = 24px).
Réponse initiale : juste
À retenir :

Question n°4 : Tu as `font-weight: 100` sur un paragraphe, mais le texte s'affiche en graisse normale. Donne une raison possible pour laquelle la graisse fine n'apparaît pas.
Réponse (avant correction) : il y avait peut être une autre regle plus tard avec un poid superieur qui change ce parametre
Correction de l'IA : Partiellement correct. Ta piste est valable : une autre règle peut écraser `font-weight: 100`. Mais attention au vocabulaire. Une règle écrite plus tard l'emporte seulement à spécificité égale. Si une règle précédente est plus spécifique, elle gagne même si elle est écrite avant. Retiens donc « une autre règle plus spécifique, ou de même spécificité mais écrite après ».

Tu n'as en revanche pas donné la raison qui était visée ici, plus propre à `font-weight` : la police elle-même. Le navigateur ne peut afficher que les graisses que la police contient. Si elle n'existe qu'en normal et en gras, la valeur `100` s'affiche comme `400`, sans aucune erreur.

Réponse initiale : partiellement juste 
À retenir :

Question n°5 : Voici deux déclarations :

css

```css
.a { font-weight: bold; }
.b { font-style: italic; }
```

Quelle différence y a-t-il entre `font-weight` et `font-style` ? Donne aussi un exemple de texte qui combine les deux.

Réponse (avant correction) :  `font-weight` c'est pour épaisseur et `font-style` c'est pour l'inclinaison, `p {font-weight: bold; font-style: italic; }`
Correction de l'IA : Correct. `font-weight` règle l'épaisseur, `font-style` l'inclinaison, et ta règle `p` combine bien les deux : le paragraphe est en gras et en italique.
Réponse initiale : juste 
À retenir :

Question n°6 : Un site affiche son texte en `#999999` sur fond blanc. Le texte courant doit respecter le niveau AA des WCAG.

1. Quel rapport de contraste minimum est exigé ?
2. Penses-tu que cette combinaison le respecte ? Dis oui ou non, et propose une couleur de texte plus sûre.

Réponse (avant correction) : 1) le rapport de contraste minimum exigé est de 4,5:1 2) je pense pas car elle sont toutes les deux clair et dans les meme tons, je pense qu'un gris foncé #444444 en revanche le respect.
Correction de l'IA :Correct.

1. Le minimum est bien de 4,5:1 pour un texte normal (3:1 pour un grand texte).
2. Ta réponse est juste : `#999999` sur blanc donne environ 2,8:1, donc la combinaison échoue. Ton raisonnement (deux couleurs claires, peu de différence de luminosité) est le bon réflexe. Et `#444444` sur blanc donne environ 9,7:1, donc il respecte largement le seuil.

Réponse initiale : juste 
À retenir :

Question n°7 : Voici une feuille de style et son HTML :

html

```html
<p id="note" class="texte">Bonjour</p>
```

css

```css
.texte { color: green; }
p { color: blue; }
#note { color: orange; }
p.texte { color: purple; }
```

Quelle couleur obtient le paragraphe ?

Réponse (avant correction) : orange 
Correction de l'IA : Correct : orange.

`#note` est la seule règle avec une valeur dans la première colonne : (1, 0, 0) contre (0, x, x) pour les trois autres. La comparaison s'arrête dès cette colonne, donc `#note` gagne.

Réponse initiale : juste 
À retenir :

Question n°8 : Dans ce code :

css

```css
.alerte {
    color: red;
}
```

Pourquoi ne suffit-il pas de colorer le message d'alerte en rouge pour que l'information soit accessible à tout le monde ? Propose une amélioration.

Réponse (avant correction) : il faudrait la mettre en font-weight: bold pour le mettre en gras si jamais on ne distingue pas le changement de couleur
Correction de l'IA : Correct. `font-weight: bold` rend l'alerte reconnaissable par sa forme et pas seulement par sa couleur : même sans percevoir le rouge, le texte ressort parce qu'il est en gras.

css

```css
.alerte {
    color: #b40b0b;
    font-weight: bold;
}
```

Tu aurais pu aussi citer `font-size` ou, côté contenu, un mot (« Attention : ») ou une icône. La règle à retenir : ne jamais transmettre une information par la couleur seule.

Réponse initiale : juste 
À retenir : La règle à retenir : ne jamais transmettre une information par la couleur seule.

Question n°9 : Pour chacune de ces trois unités, dis dans quel cas tu la choisirais : `px`, `em`, `rem`. Une phrase par unité suffit.
Réponse (avant correction) : px : si je veux mettre quelque chose dans une taille précise indépendamment du reste
em : si je veux une taille qui s'adapte a don "parents"
rem : si je veux une taille qui s'adapte a la taille de base
Correction de l'IA : Correct pour les trois. Tes formulations sont justes :

- `px` donne une taille fixe, indépendante du contexte. On l'utilise pour les détails fins (bordure de 1px, ombre).
- `em` suit le parent pour `font-size`, ou la taille de police de l'élément lui-même pour les autres propriétés (marges, espacements d'un bouton). Attention au cumul dans les éléments imbriqués.
- `rem` suit la taille de base de `<html>`, sans cumul.

Il manque une nuance pour `px`. Une taille fixe est utile pour les détails, mais en `font-size` elle ignore le réglage de taille de texte du navigateur, donc on préfère `rem` pour les polices.

Réponse initiale : juste
À retenir :

Question n°10 : Voici un extrait d'une feuille de style :

css

```css
body {
    background-color: #ffffff;
    color: #bbbbbb;
    font-family: "Brush Script MT";
    font-size: 11px;
    line-height: 1;
    text-align: justify;
}
```

Trouve au moins trois défauts (lisibilité, accessibilité ou bonnes pratiques) et propose une correction pour chacun.

Réponse (avant correction) : la taille 11 px c'est petit il faudrait plus grand, il faut ajouter d'autres police ou au moins une famille générique, les deux couleur sont trop clair, gris clair et blanc il faudrait mettre du gris foncé
Correction de l'IA : Bien joué, avec quelques précisions.

Tu as trouvé trois défauts réels :

- Taille de 11px : trop petite. Il fallait préciser une valeur : vise au moins 16px, par exemple `font-size: 1rem` (avec une base à 16px ou 18px).
- Pas de repli de police : correct. Par exemple `font-family: "Segoe UI", Arial, sans-serif;`.
- Contraste : correct. `#bbbbbb` sur blanc donne environ 1,9:1, très loin des 4,5:1. Un gris foncé comme `#444444` (environ 9,7:1) convient.

Tu n'as pas relevé trois autres défauts :

- `line-height: 1` : les lignes se touchent. Corrige avec `line-height: 1.5`.
- `text-align: justify` : espaces irréguliers entre les mots sur colonne étroite. Préfère `left` pour un long texte.
- Brush Script MT : police décorative, peu lisible pour du texte courant. Une police sans empattement convient mieux.

Réponse initiale : juste 
À retenir :
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

Question n°6 : 

Réponse (avant correction) :
Correction de l'IA :
Réponse initiale : juste / partiellement juste / fausse
À retenir :

Question n°7 : 
Réponse (avant correction) :
Correction de l'IA :
Réponse initiale : juste / partiellement juste / fausse
À retenir :

Question n°8 : 
Réponse (avant correction) :
Correction de l'IA :
Réponse initiale : juste / partiellement juste / fausse
À retenir :

Question n°9 : 
Réponse (avant correction) :
Correction de l'IA :
Réponse initiale : juste / partiellement juste / fausse
À retenir :

Question n°10 : 
Réponse (avant correction) :
Correction de l'IA :
Réponse initiale : juste / partiellement juste / fausse
À retenir :
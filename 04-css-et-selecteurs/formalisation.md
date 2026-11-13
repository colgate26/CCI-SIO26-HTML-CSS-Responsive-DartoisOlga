# Synthèse : les bases du CSS

Le CSS est un langage qui gère l'apparence d'un site web (couleurs, tailles, positions…).

## 1. Anatomie d'une règle

```css
p {
  color: blue;
  font-size: 18px;
}
```

- Sélecteur (`p`) : quels éléments sont concernés
- Propriété (`color`) : ce qu'on modifie
- Valeur (`blue`) : comment on le modifie
- Déclaration : `propriété: valeur;`, entre accolades `{ }`

Le fonctionnement d'une règle commence par le navigateur qui trouve tous les éléments qui correspondent au sélecteur et leur applique chaque déclaration.

## 2. Trois façons d'appliquer du CSS

| Méthode          | Exemple                                    | Usage                           |
| ---------------- | ------------------------------------------ | ------------------------------- |
| Fichier externe  | `<link rel="stylesheet" href="style.css">` | Recommandée, réutilisable       |
| Balise `<style>` | `<style> p { color: blue; } </style>`      | Tests rapides                   |
| Style en ligne   | `<p style="color: blue;">`                 | À éviter, mais très prioritaire |

On peut donc relier un fichier CSS externe avec `<link rel="stylesheet" href="chemin/vers/style.css">` dans le `<head>` de la page.

## 3. Types de sélecteurs

| Sélecteur             | Cible                                                    |
| --------------------- | -------------------------------------------------------- |
| `p` (balise)          | Tous les `<p>`                                           |
| `.important` (classe) | Tous les éléments avec `class="important"`, réutilisable |
| `#titre` (id)         | Un seul élément avec `id="titre"`, unique dans la page   |
| `div p`               | Les `<p>` à l'intérieur d'un `<div>`                     |
| `h1, h2`              | Plusieurs sélecteurs à la fois                           |
| `a:hover`             | Un élément dans un état (ici, survolé)                   |

Les différence entre `p`, `.important` et `#titre` sont que `p` est un type de balise, `.important` est un groupe d'éléments choisis et `#titre` est un élément unique. Leur poids augmente dans cet ordre : balise < classe < id.

## 4. Priorité des règles

Une cascade c'est quand plusieurs règles se contredisent, la cascade est l'algorithme qui permet au navigateur de choisir la valeur appliquée.

Le navigateur tranche propriété par propriété, dans cet ordre :

1. `!important` l'emporte (à utiliser avec parcimonie).
2. Spécificité : style en ligne > `#id` > `.classe` > `balise`.
3. Ordre : à spécificité égale, la règle écrite en dernier gagne.

```css
p          { color: blue; }   /* faible */
.important { color: green; }  /* moyen */
#titre     { color: red; }    /* fort : gagne sur <p id="titre" class="important"> */
```

On utilise l'héritage si aucune règle ne définit une propriété, certaines (`color`, `font-family`, `line-height`…) sont transmises du parent à l'enfant. D'autres (`margin`, `border`, `background`) ne le sont pas. Une règle directe bat toujours une valeur héritée.


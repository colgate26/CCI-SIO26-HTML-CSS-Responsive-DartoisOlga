# Exercice 1

## Différentes méthodes

**1ere** : Dans un fichier externe : 

ligne 6 dans `<head>` :  `<link rel="stylesheet" href="css/style.css">` 

Permet de modifier toutes les pages du site sur un seul fichier, c'est la manière recommandé.

**2eme** : CSS interne :

ligne 7 à 9 dans `<head>` : 

```css
<style>
        h1 { color: darkblue; }
    </style>
```

Permet de modifier page par page du site donc avoir des différences entre le style de chaque page, a utiliser de préférence pour des testes ou des pages uniques.

**3eme** : CSS en ligne :

ligne 13 : directement dans la balise `<h1 style="color: darkblue;">Bienvenue</h1>`

Permet d'apporter une modification directe à un endroit précis et ne modifie rien d'autres que la balise concerné. Elle a aussi une forte priorité par rapport aux deux autre méthode, a utiliser exceptionnellement.
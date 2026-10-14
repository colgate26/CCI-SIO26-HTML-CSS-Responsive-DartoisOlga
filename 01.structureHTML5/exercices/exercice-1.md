# Exercice 1

## Support - doc a

1) A première vu quand on ouvre le document dans le navigateur il semble ne pas y avoir d'erreur, l'affichage et correct, pareil pour le titre de l'onglet et les accents, or il y a bien des erreurs dans le script

2) - ligne 10 : `<!DOCTYPE html>` , cette commande ce trouve a la ligne 10 or elle doit se trouver a la ligne 1
   - ligne 1 : manque l'attribut langue
   - ligne 2 : `<body>` cette commande se trouve autour de la commande `<head>` or elle est sensé être placé après 
   - ligne 8 : à la fin de cette ligne la deuxième commande `<p>` est écrite `<p>` alors qu'elle devrait être `</p>`

3) Correction proposé (document-a-corrige.html)

   ```html
   <!DOCTYPE html>
   <html>
   <head>
     <meta charset="UTF-8">
     <title>Réseau du BTS SIO</title>
   </head>
   <body>  
     <h1>Bienvenue sur ma page</h1>
     <p>Je prépare un BTS SIO option SISR.</p>
   </body>
   </html>
   ```

   

## Support - doc b

1) Tout comme le doc a, à première vu tout semble correct.
2) - ligne 5 : manque titre de l'onglet qui est obligatoire
   - ligne 9 et 10 : `</html>` est avant `<body>` alors qu'il devrait être après
   - ligne 4 : UFT au lieu de UTF
3) Correction proposé (document-b-corrige.html)

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>BTS SIO</title>
</head>
<body>
  <h1>Ma page</h1>
  <p>Élève de première année</p>
</body>
</html>

```


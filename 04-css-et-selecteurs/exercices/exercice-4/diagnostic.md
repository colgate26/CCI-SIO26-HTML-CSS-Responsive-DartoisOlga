# Exercice 4

Cause 1 : le fichier CSS n'est pas chargé (chemin et nom)

Pas le bon chemin pour le fichier `style.css` , `<link href="styles.css">`. Le fichier est dans `css/` et s'appelle `style.css` (sans « s ») correction :  `href="css/style.css"`

Cause 2 : sélecteur de classe pour un id

Le titre n'est pas agrandi.

Le HTML a `id="titre-page"`, le CSS cible `.titre-page` (classe), correction : `#titre-page`

Cause 3 : point-virgule manquant

L'alerte n'est ni rouge ni en gras, `color: red` sans `;`. Le navigateur lit `color: red font-weight: bold`, valeur invalide, et ignore les deux déclarations, correction : `color: red;`

Cause 4 : propriété mal orthographiée

L'info n'est pas verte,  `colour`  n'existe pas en CSS, correction : `color: green;`

Cause 5 : problème de spécificité sur DHCP

DHCP reste gris malgré `.actif`, `.liste-services li` = (0,1,1) bat `.actif` = (0,1,0). L'ordre ne compte pas, la spécificité passe avant, correction :  `.liste-services .actif` (0,2,0), sans `!important`.

Cause 6 : espace dans la valeur

Le lien « Aide » n'est pas agrandi, `1.2 rem` avec un espace est invalide, l'unité doit être collée au nombre. Le navigateur ignore la déclaration, correction :  `1.2rem`


```html
<!DOCTYPE html>
<html lang="fr">
   <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>La commande ping</title>
    </head>
    <body> <!--Dartois-Stojadinovic Olga-->
        <h1>La commande ping</h1>
        <h2>Introduction</h2>
        <p> intro expliquant a quoi elle sert</p>
        <h2>Syntaxe</h2>
        <p>texte</p>
        <h2>Option courantes</h2>
        <ul>
            <li>texte</li>
            <li>texte</li>
        </ul>
        <h2>Utilisation pas à pas</h2>
        <p><strong>Attention :</strong> texte</p>
        <ol>
            <li>texte</li>
            <li>texte</li>
        </ol>
        <h3>Tester le reseau local</h3>
        <p>texte</p>
        <h3>Tester Internet</h3>
        <p>texte</p>
    </body>
```

Rédaction : la page « La commande ping »

1. Le `<h1>` est le titre principal de la page. Les `<h2>` sont les grandes parties. Les `<h3>` sont les sous-parties d'« Utilisation pas à pas ». Le `<ul>` liste les options, dans n'importe quel ordre. Le `<ol>` liste les étapes, dans un ordre précis.

2. Le `<title>` s'affiche dans l'onglet du navigateur. Il est dans le `<head>`. Le `<h1>` s'affiche dans la page. Il est dans le `<body>`.

3. HTML écrit le contenu de la page. CSS choisit l'apparence. JavaScript rend la page interactive.

4. Le navigateur reçoit le fichier HTML et lit `<!DOCTYPE html>` : il sait que c’est du HTML5. Il lit `charset="UTF-8"` pour afficher correctement les accents, comme dans « Utilisation pas à pas » et `<meta name="viewport" content="width=device-width, initial-scale=1.0">`pour que l'affichage sur téléphone soit bien. Il lit `<title>` et écrit « La commande ping » dans l’onglet. Il construit le DOM : `html` contient `head` et `body`, et `body` contient le `h1`, les `h2`, les `h3`, les `p`, le `ul` et le `ol`. Il applique ses styles par défaut : titres en gras, points pour le `ul`, numéros pour le `ol`. Il affiche ensuite la page à l’écran.
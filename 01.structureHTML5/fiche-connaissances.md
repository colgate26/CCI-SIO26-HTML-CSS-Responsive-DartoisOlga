# Fiche de connaissances HTML5

### Qu'est ce qu'HTML5 ?

HTML5 est la 5eme version de HTML (HyperText Markup Language) c'est un langage qui sert a structurer le contenu d'une page web et décrit ce qu'est chaque élément à partir de balises sémantiques qui sont des balises qui décrivent le rôle de son contenu.

Ce langage de balisage est une langage qui sert à annoter un texte avec des marqueurs pour indiquer sa structure ou sa mise en forme sans en changer le contenue

**Exemples de balises**  :

```html
<header>	#En-tête de la page ou d’une section (logo, titre, menu)
<nav> 		#Bloc de liens de navigation
<main>		#Contenu principal, un seul par page
<article>	#Contenu autonome (article de blog, actualité)
<section>	#Regroupement thématique de contenu, généralement avec un titre
<aside>		#Contenu annexe (encadré, publicité, liens connexes)
<footer>	#Pied de page (mentions légales, contact)
```

### Autres commandes

```html
<!DOCTYPE html> 
```

Cette commande sert à indiquer au navigateur qu'il doit interpréter la page en HTML5, ce n'est pas vraiment une balise HTML et elle n'a pas de balise fermante.

```html
<head>
```

Cette commande contient les métadonnées c'est à dire des infos sur la page qui ne s'affiche pas dans la zone de contenu.

```html
<body>
```

Cette commande contient tout ce que l'utilisateur voit.

```html
<title>
```

Cette commande indique le titre affiché dans l'onglet du navigateur, il est obligatoire, se place dans <head>.

```html
<h1> #jusqu'à
<h6>
```

Ces commandes décrivent les titre hiérarchisés et se placent dans <body>.

```html
<p> 
```

Cette commande définit un paragraphe.

Les commandes suivantes sont des sont des attributs. Ils se placent à l’intérieur d’une balise ouvrante pour la préciser :

**lang="fr"**

**charset="UTF-8"**

**name="viewport"**

**content="..."**

**href**

**src**

**Exemple:**

```html
<html lang="fr">			#Élément racine qui contient tout le document. lang précise la langue (accessibilité, référencement, traduction).
<meta charset="UTF-8">		#Encodage des caractères (évite les accents mal affichés)
<meta name="viewport" ...>	#Adapte l’affichage aux écrans mobiles.
```



### Différence HTML/CSS/JavaScript

HTML et CSS sont des langages déclaratifs (ils décrivent, ils n’exécutent pas d’instructions). HTML est un langage de balisage, CSS un langage de style. JavaScript est un langage de programmation : il réagit aux actions de l’utilisateur, modifie la page, valide un formulaire, etc.

### Interprétation d'un document HTML par un navigateur

1) Réception et décodage : le navigateur réception et décode le fichier
2) Analyse et création du DOM : le texte est découper en balises puis organisé en un arbre d'objets, DOM (Document Object Model)
3) Chargement des ressources : il télécharge les fichiers liés 
4) Analyse et création du CSSOM : le CSS est analysé et organisé en arbre de style, CSSOM (CSS Object Model)
5) Arbre de rendu : il combine le DOM et le CSSOM, seul les élément visibles sont conservés
6) Mise en page : Le navigateur calcule la taille et la position de chaque élément en fonction de la taille de la fenêtre
7) Affichage : il dessine les éléments en différentes couches, puis les assemble à l’écran



### Exemple de document minimal

```html
<!DOCTYPE html>			   	#document en HTML5
<html lang="fr"> 		  	#langue francais
  <head> 				   	#métadonnées
    <meta charset="UTF-8"> 	#affiche correctement les accents
    <title>Ma page</title> 	#titre dans l'onglet du nav
  </head>
  <body> 					#corps, visible par l'utilisateur
    <p>Bonjour !</p> 		#paragraphe de texte
  </body>
</html>
```


# Exercice 1

A) content-box

largeur total visble :  `width + padding x2 + border x2` = 300 + (20+20) +(5+5) = 350 px

largeur du contenu : `width` = 300 px

largeur occupé dans la page : largeur totale visible + `margin x2` = 350 + (10+10) = 370 px

hauteur visible : `height + padding x2 + border x2`  = 120 + (20+20) + (5+5) = 170 px



B) content-box

largeur total visible : 600 + 30 + 30 + 2 + 2 = 664 px

largeur du contenu : 600 px

largeur occupé dans la page : 644 + 0 + 20 = 704 px 



C) border-box

largeur total visible : 400 px

largeur du contenu : `width - padding x2 - border x2`  = 400 - 25 - 25 - 10 -10 = 330 px

largeur occupé dans la page : 400 + 15 + 15 = 430 px



D) content-box

largeur total visible : 280 + 10 + 10 + 1 + 1 = 302 px

largeur du contenu : 280 px

largeur occupé dans la page : 1 boite : 302 + 5 + 5 = 312 px / 3 boite : 3 x 312 = 936 px

conteneur = 900 px et 3 boites 936 px donc elles ne tiennent pas sur une même ligne
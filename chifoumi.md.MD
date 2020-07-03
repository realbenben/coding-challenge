ENNONCE
L'objectif de ce projet est de créer un chifoumi (le jeu pierre, feuille, ciseaux).

Vous devez pour cela travailler uniquement sur la partie javascript (dans le fichier script.js).

Pour la première partie vous devez déclarer 3 variables :

 variable pour le choix de l'utilisateur (nommée player)

1 variable qui contiendra le choix de l'IA (nommée computer)

1 variable qui contiendra le calcul aléatoire (nommée random)

une fois ces variables déclarées, affecter la réponse de l'utilisateur à la variable player, l'utilisateur donne sa réponse grâce à un window.prompt.

Pour éviter tout malentendu, modifier la casse de la réponse en la mettant en minuscule.

##########################################################################################

mon code

'use strict';
var player = window.prompt();
var computer = Math.random();
var random = "pierre,feuille,ciseaux";
// Vous devez déclarer 3 variables,

// demandez à l'utilisateur son choix (pierre, feuille ou ciseaux)
player = window.prompt("Que choisissez vous ? pierre,feuille,ciseaux");
// modifier la casse en minusule
var answer = player.toLowerCase();

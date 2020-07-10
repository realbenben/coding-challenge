Cours-js-vol-2
#
les opérateurs de comparaison et notamment les opérateurs d'égalité :

var test1 = 1 == "1";
var test2 = 1 === "1";

Dans le code ci-dessus, test1 vaut true et test2 vaut false.
Dans le premier cas == permet de vérifier si la valeur est la même, ce qui est vrai.
Dans le second cas === permet de vérifier si la valeur et le type sont identiques, ce qui est faux car il y a un nombre et une chaîne de caractère.
Le second opérateur est donc plus restrictif.

Remarque :

Dans la plupart des cas, utiliser l'égalité stricte === est plus sûre et aussi plus rapide pour Javascript. Avec == Javascript va d'abord essayer de convertir le type des variables avant de comparer leur valeur, comme avec 1 == "1".

index.html
script.js

Activer JavaScript
http://localhost:8080
#############################################################################
 les opérateurs permettant de comparer des inégalités.

Exemple :

var test1 = 1 != 2;
var test2 = 1 !== "1";

Dans le code ci-dessus, test1 vaut true car 1 est bien différent de 2. Et test2 vaut true car même si le contenu est identique, le type de variable est différent.
Dans le premier cas, l'opérateur compare juste si la valeur est différente, dans le second cas l'opérateur compare si la valeur ou le type est différent (et le type est bien différent car on compare un nombre avec du texte).
#############################################################################

 les opérateurs permettant de comparer des supériorités et infériorités.

Exemple :

var test1 = 1 > 2; // False
var test2 = 1 >= 1; // True
var test3 = 1 < 2; // True
var test4 = 1 <= 1; // True
#############################################################################

Les opérateurs logiques. Ils sont au nombre de trois :
Opérateur   Sens logique  Exemple
&&  ET  var1 && var2
||  OU  var1 || var2
!   NON   !var

Dans cet exercice vous allez voir l'opérateur &&. Cet opérateur permet de vérifier que toutes les expressions sont vraies (true) et pas seulement l'une d'entre elles.

Exemple :

var expression1 = 1 < 2; // True
var expression2 = 1 > 2; // False
var test =  expression1 && expression2;

Ici, test vaut false car toutes les expressions testées ne sont pas vraies (true).


L'opérateur ! est une négation car il inverse la valeur ou expression qui lui est donnée.

Exemple :

var expression = true; // True
var test = !expression; // False

Ici, test vaut false car l'opérateur à inversé la valeur d'origine.

Exemple :

var expression1 = 1 < 2; // True
var expression2 = 1 > 2; // False
var test =  expression1 || expression2;

Ici, test vaut true car une des expressions testées est vraie (true).

Remarque :

L'opérateur || (OU) sert aussi à retourner le contenu d'une variable évaluée à true.

Dans cet exercice vous allez voir l'opérateur !.
Attention, cet opérateur ne s'utilise qu'avec une seule expression et pas deux comme les opérateurs logiques précédents.

L'opérateur ! est une négation car il inverse la valeur ou expression qui lui est donnée.

Exemple :

var expression = true; // True
var test = !expression; // False

Ici, test vaut false car l'opérateur à inversé la valeur d'origine.

##########################################################################################################################################################
faire le point sur ce qui est considéré comme vrai et comme faux en Javascript. Il y a quelques subtilités à connaître.

Ce qui est considéré comme faux :

    le booléen false;
    une chaîne vide "";
    le nombre zéro 0
    undefined;

Ce qui est considéré comme vrai :

    le booleéen true;
    une chaîne contenant zéro "0";
    une chaîne contenant false "false";

Il existe d'autres subtilités similaires mais celles-ci sont les plus évidentes.
#############################################################################

les structures conditionnelles, qu'on appellera simplement "conditions". Il existe trois types de conditions :

    la stucture if else;
    les switchs;
    les ternaires;

Commençons par la première qui est aussi la plus utilisée.
Dans les exercices précédents vous avez vu comment récupérer un booléen (true,false en testant des variables avec les opérateurs de comparaison et les opérateurs logiques.

Avec les conditions; le résultat (booléen) d'un test permettra de modifier le flux d'exécution de votre code et donc de donner une certaine intelligence à votre script.

La structure if (si)

Elle est composée :

    du mot-clé if;
    suivi de parenthèses () contenant l'expression à tester, et donc le booléen qui est retourné en résultat;
    des accolades &#123;} contenant le code à exécuter si la condition entre les parenthèses est vérifiée, résultat true.

Exemple :

if (1 == 1)
&#123;
    // La condition est vérifiée (true), on exécute le code qui est ici.
}

if (1 === "1")
&#123;
    // La condition n'est pas vérifiée (false) car les variables n'ont pas le même type, donc tout le code ici ne sera pas exécuté.
}

Une structure conditionnelle doit rester lisible, surtout quand elle devient complexe, aussi il est fortement conseillé de l'écrire comme ceci :

if ()
&#123;
    // Votre code ici
}

    un espace entre le if et les parenthèses ();
    allez à la ligne pour ouvrir les accolades &#123;;
    indentez le code entre les accolades avec une tabulation pour bien voir la hiérarchie;
    allez à la ligne pour fermer les accolades;
    les 2 accolades doivent être alignées, ainsi vous verrez plus facilement si il y a un oubli et à quel niveau;

Cet exemple est une très bonne façon d'écrire des conditions et dans cet exercice vous devez utiliser ce modèle.";
Il est possible d'utiliser plusieurs if :

var var1 = true;
if (var1)
&#123;
    // Code exécuté si var1 est vrai;
}
if (!var1)
&#123;
    // Code exécuté si var1 est faux;
    // En effet, ici on teste l'inverse de var1 avec !, donc on teste si c'est faux;
}

Mais il y a plus simple avec l'utilisation de la structure else.

La structure else (sinon)

Si un if peut s'utiliser seul, un else va de paire avec un if et ne peut pas être utilisé seul, ce qui donne :

if ()
&#123;
}
else
&#123;
}

L'autre différence est qu'il n'est pas nécessaire d'indiquer quelle expression il faut vérifier entre parenthèses. En fait on le sait déjà puisque c'est l'inverse de l'expression testée dans le if qui précède.
Ainsi l'exemple ci-dessus devient :

var var1 = true;
if (var1) // Si var1 est vrai
&#123;
    // Code exécuté si var1 est vrai;
}
else // Sinon, var1 est forcément faux
&#123;
    // Code exécuté si var1 est faux;
    // En effet, ici on teste l'inverse de var1 avec !, donc on teste si c'est faux;
}

#############################################################################


    la première condition est testée avec if;
    une deuxième condition est testée si la précédente n'est pas vérifiée avec else if;
    d'autres conditions peuvent être testées en ajoutant autant de else if;
    enfin, si aucune des conditions précédentes n'est vérifiée, la structure else exécute le code souhaité;

La structure elseif (sinon si)

Avec else if il est donc possible de tester plusieurs conditions à la fois:

if (condition1)
&#123;
    // Code exécuté si "condition1" est vérifié
}
else if (condition2)
&#123;
    // Code exécuté si "condition1" n'est pas vérifié...
    // ... et si "condition2" est vérifiée
}
else if (condition3)
&#123;
    // Code exécuté si "condition2" n'est pas vérifée...
    // ... et si "condition3" est vérifiée
}
... // Ainsi de suite
else
&#123;
    // Si aucune des conditions n'est vérifiée alors le code ici est exécuté
}

#############################################################################

Dans l'exercice précédent vous avez testé si number était positif, négatif ou égale à zéro. Imaginez une situation dans laquelle vous devez tester toutes les possibilités pour cette même variable number.

Il va falloir vérifier si number est égale à -10, -9, -8 ... jusqu'à 10. Avec une structure de type if elseif else, le code devient vite lourd et pas forcément lisible.

C'est là qu'intervient la structure switch :

switch (maVariable)
&#123;
    case valeur1:instruction1;
    break;
    case valeur2:instruction2;
    break;
    case valeur3:instruction3;
    break;
    default:instruction4;
}

Comment ça marche ?

    il faut le mot-clé switch suivi de la variable à tester entre parenthèses ();
    ensuite tout se passe entre une seule paire d'accolades &#123;};
    chaque possibilité est testée avec le mot-clé case suivi de la valeur à laquelle doit être comparée maVariable;
    attention, case vérifie uniquement si maVariable est égale à la valeur spécifiée (ici valeur1, valeur2, valeur3) et rien d'autre;
    si l'égalité est vérifiée, alors l'instruction qui suit le double-point : est exécutée;
    pour chaque case il faut un break qui permet d'arrêter le switch si l'égalité est vérifiée car pas besoin d'aller plus loin;
    si aucun des case n'est vérifié, alors on exécute l'instruction par défaut avec le mot-clé default;

Remarque :

Avec case c'est une égalité stricte === qui est testée, c'est-à-dire que le contenu et le type de maVariable doivent être identique soit à valeur1 ou valeur2 ou valeur3.

##########################################################################################################################################################

les ternaires. Leur avantage est d'être simple à écrire mais c'est au détriment de la lisibilité.

Une structure ternaire est comme une structure if else mais écrite sur une seule ligne.

Exemple :

var permis = confirm("Avez-vous le permis de conduire ?");
var resultat;
if (permis) // confirm() renvoi un booléen, donc on peut directement tester "permis", pas besoin de mettre "permis == true"
&#123;
    resultat = "Vous pouvez conduire";
}
else
&#123;
    resultat = "Vous ne pouvez pas conduire";
}

Equivalent ternaire :

var permis = confirm("Avez-vous le permis de conduire ?");
var resultat = permis ? "Vous pouvez conduire" : "Vous ne pouvez pas conduire";

Comment ça marche ?

    la variable resultat récupère le résultat de la ternaire;
    la variable permis est testée par la ternaire;
    suivie par ?;
    suivi par une première valeur puis : et une seconde valeur;

Si permis est vérifiée (évaluée à true) alors la première valeur sera retournée.
Si permis n'est pas vérifiée (évaluée à false) alors la seconde valeur sera retournée.

##########################################################################################################################################################

Du coup, en utilisant une condition if il est tout à fait possible de tester si une variable est true ou false de façon très simple :

Méthode standard :

var test = "Je suis une chaîne de caractères";
if (test == true)
&#123;
    alert("La variable test est vraie");
}

Méthode simple :

var test = "Je suis une chaîne de caractères";
if (test)
&#123;
    alert("La variable test est vraie");
}

##########################################################################################################################################################

Cet exercice est un rappel sur l'opérateur logique OU qui possède une fonctionnalité particulière (retournez voir la description de l'exercice en question si nécessaire).

Exemple :

var var1 = "";
var var2 = 1;
var var3 = "Je suis une chaîne de caractères";
var resultat = var1 || var2 || var3;

Dans cet exemple, resultat contient la valeur de la première variable évaluée à true.


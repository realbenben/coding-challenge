Il existe deux façons d'insérer des commentaires dans un code Javascript :
/*     */
//

Vous avez déjà vu trois types de variables :

    la chaîne de caractères (type "string");
    la valeur numérique (type "number");
    la valeur booléenne (type "boolean");
    Il existe aussi le type undefined. Une variable est considérée comme "undefined" (indéfinie) dans trois cas:

    elle n'a pas été déclarée (avec var) donc elle n'existe pas;
    elle existe mais ne contient aucune valeur;
    elle existe et on lui affecte la valeur undefined;


var var_1 = uneValeur; // Déclaration d'une variable
/* var var_2 = uneValeur;
var var_3 = uneValeur;
var var_4 = uneValeur; */

Un commentaire sur une seule ligne qui commence par //.

Quand vous avez plusieurs variables à déclarer, il y a plusieurs façon de faire :

// Méthode 1
var var1;
var var2;
var var3;
// Méthode 2
var var1, var2, var3;

type de variabe numérique
var nombreEntier = 10;
var nombreNegatif = -10;
var nombreDecimal = 1.1;
var nombreHexa = 1e240;

Il existe aussi le type booléen. Une variable de ce type peut prendre deux valeurs uniquement :

    true;
    false;

typeof retourne une chaîne de caractères contenant le type de la variable testée. Elle peut s'utiliser comme cela :

var maVariable = 10;
alert(typeof maVariable); // Affiche "number"

n fichier javascript .js et de faire le lien vers le fichier simplement en mettant le code suivant entre les balises <head><\head> de votre page .html.

<script src="script.js"></script>

ous avez vu les opérateurs arithmétiques + et -. Voyons maintenant l'opérateur * qui sert à faire des multiplications.

Comme en mathématiques, la multiplication est prioritaire sur l'addition et la soustraction. Par exemple :

var result = 7 + 2 * 5; // = 17

Ici, result vaut 17 car Javascript multiplie 2 par 5 puis additionne 7. Pour changer la priorité d'exécution des calculs il faut utiliser les parenthèses () comme en mathématiques. Ainsi :

var result = (7 + 2) * 5; // = 45

l'opérateur / qui sert à faire des divisions.

Comme en mathématiques, la division est prioritaire sur l'addition et la soustraction. Par exemple :

var result = 7 + 4 / 2; // = 9

Ici, result vaut 9 car Javascript divise 4 par 2 puis additionne 7. Pour changer la priorité d'exécution des calculs il faut utiliser les parenthèses () comme en mathématiques. Ainsi :

var result = (7 + 4) / 2; // = 5.5

 le modulo %.
Le modulo correspond au reste entier d'une division. Il prend automatiquement le signe du numérateur. Par exemple :

var result1 = 12 / 5; // = 2.4
var modulo1 = 12 % 5; // = 2

var result2 = -12 / 5; // = -2.4
var modulo2 = -12 % 5; // = -2

Notation raccourcie   Exemple   Equivalent standard
=   a = b   a = b
+=  a += b  a = a + b
-=  a -= b  a = a - b
*=  a *= b  a = a * b
/=  a /= b  a = a / b
%=  a %= b  a = a % b

 les opérateurs d'incrémentation et de décrémentation.
Leur fonction est simple, ajouter ou soustraire 1 à une valeur. vous savez déjà le faire avec les opérateurs arithmétiques :

var init = 0;
init = init + 1; // init = 1
init = init - 1;  // init = 0

C'est là qu'interviennent les opérateurs d'incrémentation et de décrémentation. L'exemple ci-dessus devient donc :

var init = 0;
init++; // init = 1
init--; // init = 0

Il existe en fait deux façons d'utiliser les opérateurs pour incrémenter et décrémenter.

var nombre1 = 0;
var nombre2 = 0;
nombre1++; // = 1
++nombre2; // = 1

Exemple 1

var nombre = 0;
var resultat = ++nombre; // Ici on incrémente 'nombre' puis on l'affecte à 'resultat'
alert(nombre); // = 1
alert(resultat); // = 1

Exemple 2

var nombre = 0;
var resultat = nombre++; // Ici on affecte 'nombre' (qui vaut 0) à 'resultat' puis on incrémente 'nombre'
alert(nombre); // = 1
alert(resultat); // = 0

prompt() permet d'afficher du texte à l'utilisateur pour lui demander une information (paramètre d'entrée) et propose à l'utilisateur de rentrer sa réponse (résultat en sortie), que la fonction va récupérer sous la forme d'une chaîne de caractère :

var prenom = prompt("Quel est votre prénom ?");
alert(prenom);

Le code ci-dessus récupère la réponse de l'utilisateur dans la variable prenom puis la fonction alert() affiche le résultat à l'écran.

prompt() permet aussi de fournir un texte par défaut qui sera pré-rempli. Si l'utilisateur ne met rien à la place, c'est ce texte que la fonction va renvoyer :

var defaut = prompt("Question","Texte par défaut");
alert(defaut);

la fonction confirm() qui permet à l'utilisateur de confirmer (bouton "OK") ou d'infirmer (bouton "annuler") une demande.

Cette fonction retourne en résultat de sortie un booléen :

   var bouton = confirm("Appuyez sur un bouton au choix.");
// Si l'utilisateur appuie sur "OK"
bouton == true;
// Si l'utilisateur appuie sur "Annuler"
bouton == false,

 la fonction console.log(). Placée à des endroits "stratégiques" de votre code, elle permet de vérifier le bon déroulement du script. Par exemple :

var test;
console.log(test);

Le code ci-dessus affichera "undefined" dans la console du navigateur, ce qui permet de savoir que la variable test est undefined car elle ne contient aucune valeur.

la fonction parseInt().

À quoi ça sert ?

    Cette fonction retourne en résultat un nombre en analysant une chaîne de caractères;
    Seul le premier nombre trouvé dans la chaîne de caractère est retourné;
    Si le premier caractère de la chaîne ne peut pas être converti en un nombre, la fonction retourne en résultat NaN (Not A Number);

Exemple :

var texte1 = "Je suis une chaîne de caractère";
var texte2 = "9 février 2016";
parseInt(texte1); // Retourne NaN
parseInt(texte2); // Retourne 9

Si vous essayez de convertir du texte qui ne peut pas être converti en type number, alors Javascript renverra la valeur NaN pour "Not a Number" :

var test1 = parseInt("1");
var test2 = parseInt("Je suis une chaîne de caractères");

Une fonction très similaire à parseInt() existe, c'est parseFloat.

Exemple :

var texte = "3.14";
parseInt(texte); // Retourne 3
parseFloat(texte); // Retourne 3.14

 il existe la propriété length.

À quoi ça sert ?

    Cette propriété retourne un nombre contenant la longueur de la chaîne de caractères qui est analysée;

Exemple :

var maChaine = "Une chaîne de caractères";
var longueur = maChaine.length;
alert(longueur); // Affiche 24

concat().

À quoi ça sert ?

    Cette fonction met bout à bout plusieurs chaînes de caractères;

Exemple :

var chaine1 = "Bonjour, ";
var chaine2 = "comment ça va ? ";
var chaine3 = "Il est quelle heure ?"
var resultat = chaine1.concat(chaine2, chaine3);
alert(resultat); // Affiche "Bonjour, commment ça va ? Il est quelle heure ?"


    charAt() récupère un caractère par rapport à sa position dans la chaîne de caractères;
    la position des caractères est comptée à partir de zéro (les espaces sont pris en compte);

Exemple :

var chaine1 = "Bonjour, comment ça va ?";
var resultat = chaine1.charAt(17);
alert(resultat); // Affiche "ç"


    indexOf() retourne la position d'un caractère ou d'un mot que vous aurez spécifié;
    la position est comptée à partir de zéro;
    si la valeur recherchée apparaît plusieurs fois dans la chaîne, seule la première occurrence est retournée;
    si la valeur n'est pas trouvée, indexOf() retourne -1;

Exemple :

var chaine1 = "Bonjour, comment ça va ?";
var resultat = chaine1.indexOf("ç");
alert(resultat); // Affiche 17

Remarque :

La fonction search() fait la même chose que indexOf() mais permet en plus de faire une recherche par expression régulière.


    replace() remplace soit la première occurrence d'un mot soit toutes les occurrences d'un mot par un autre dans une chaîne de caractères et retourne la chaîne modifiée;
    si vous indiquez un mot spécifique à remplacer et qu'il apparaît plusieurs fois dans la chaîne, seule la première occurrence sera remplacée;
    pour remplacer toutes les occurrences d'un mot, il faut utiliser une expression régulière;

Exemple :

var chaine = "Mr Dupond et Dupont sont policiers.";
var resultat1 = chaine.replace("Dupon","xxx");
var resultat2 = chaine.replace(/Dupon/g,"xxx");
alert(resultat1); // Affiche ""Mr xxxd et Dupont sont policiers."
alert(resultat2); // Affiche ""Mr xxxd et xxxt sont policiers."

Remarque :

Ici, le code /Dupon/g est une expression régulière qui dit de rechercher le texte "Dupon" de façon globale (g) dans la chaîne de caractère. Ainsi toutes les occurrences seront remplacées.


    slice() récupère une partie d'une chaîne de caractères;
    la sélection du texte à extraire utilise la position des caractères dans la chaîne (le premier caractère étant à la position 0);
    la position de début est obligatoire, la position de fin est optionnelle et exclusive (le caractère correspondant ne sera pas sélectionné);
    si la position de fin n'est pas indiquée, tous les caractères jusqu'à la fin de la chaîne seront récupérés à partir de la position de début;
    il est possible de commencer par la fin de la chaîne de caractères en utilisant des chiffres négatifs;

Exemple :

var chaine = "Voici du texte";
var resultat1 = chaine.slice(1,4); // Affiche "oic"
var resultat2 = chaine.slice(0,5); // Affiche "Voici"
var resultat3 = chaine.slice(1); // Affiche "oici du texte"


    substr() récupère une partie d'une chaîne de caractères;
    la sélection du texte à extraire utilise la position du premier caractère à extraire puis la longueur de la sous-chaîne que vous souhaitez extraire;
    la position de début est obligatoire, la longueur est optionnelle;
    si la longueur n'est pas indiquée, tous les caractères jusqu'à la fin de la chaîne seront récupérés à partir de la position de début;

Exemple :

var chaine = "Voici du texte";
var resultat = chaine.substr(9,5); // Affiche "texte"

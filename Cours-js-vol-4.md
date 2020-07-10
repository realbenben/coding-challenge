les tableaux. Un tableau (en anglais "array") permet de stocker une liste de valeurs. Ces valeurs peuvent être du texte, un nombre, un booléen, même un tableau.

Comment déclarer un tableau ?

var monTableau = [];

Il suffit en fait de créer une variable et de lui affecter des crochets []. Le tableau est déclaré mais il est vide. Ci-dessous un exemple de tableau qui contient des valeurs :

var monTableau = ["fruits","légumes",5,[]];

Ici monTableau contient du texte, un nombre et un tableau. Chaque valeur doit être séparée par une ,

############################################################################################################################################################################
Aborder les tableaux en Javascript nécessite de faire un point sur la notion d'objet.

Un objet c'est quoi :

En Javascript, une chaîne de caractères, un nombre, un booléen sont en fait des objets.

var texte = "Je suis une chaîne de caractères.";

Ci-dessus, on créé la variable texte qui contient un objet qui représente une chaîne de caractères. Plus qu'une variable, on a donc créé un objet.

La structure d'un objet :

Un objet contient toujours trois éléments :

    un constructeur;
    des propriétés;
    des méthodes;

Vous avez déjà utilisé des propriétés et des méthodes natives que Javascript met à disposition pour les chaînes, les nombres, etc. Si on reprend le code précédent :

var texte = "Je suis une chaîne de caractères.";
var longueur = texte.length; // Propriété
var maj = texte.toUpperCase(); // Méthode

Dès que l'on créé une chaîne de caractères, pour Javascript ce sera un objet et il propose par défaut certaines propriétés et méthodes qui permettent de manipuler l'objet stocker dans la variable texte.

Le caractère important ici est le point ., il permet de dire que l'on souhaite accéder à la propriété length de texte qui contient l'objet en question, autrement dit la chaîne de caractères.

Pourquoi parler des objets :

Aborder cette notion maintenant est important. Soit le code suivant :

var txt = "blablabla";
var nb = 10;
alert(typeof txt); // affiche "string"
alert(typeof nb); // affiche "number"

Avec typeof on peut connaître le type d'une variable selon ce qu'elle contient. A votre avis, que donne typeof avec un tableau [] ?? Faites l'exercice pour avoir la réponse.

############################################################################################################################################################################

Donc, pour résumé, en Javascript il y a 5 types de variables (ou d'objets pouvant être représentés dans une variable pour être précis) que peut renvoyer typeof :

    string
    number
    boolean
    undefined
    object

Dans cet exercice, vous allez apprendre comment accéder et récupérer un élément grâce aux indices.

Qu'est-ce qu'un indice ?

L'indice est un nombre unique qui correspond à un élément du tableau. Soit le tableau fruits suivant :

var fruits = [Banane,Fraise,Pomme,Poire,Kiwi];

Pour Javascript, voilà à quoi il ressemble :

0 | 1 | 2 | 3 | 4 Banane | Fraise | Pomme | Poire | Kiwi

Chaque valeur possède un indice. Et donc pour récupérer le premier fruit il suffit de faire ainsi :

var banane = fruits[0];

Il suffit d'indiquer l'indice correspondant à la valeur souhaitée entre crochet après le nom de la variable.

Remarque :

Les indices commencent à zéro. Donc pour récupérer la première valeur d'un tableau il faut utiliser [0].

Dans cet exercice, vous allez ajouter un élément à la fin d'un tableau en utilisant la méthode push().

Exemple :

var tab = ['banane','fraise','pomme'];
tab.push('kiwi'); // Ajoute "kiwi" à la fin du tableau


Dans cet exercice, vous allez ajouter un élément au début d'un tableau en utilisant la méthode unshift().

Exemple :

var tab = ['banane','fraise','pomme'];
tab.unshift('kiwi'); // Ajoute "kiwi" au début du tableau



############################################################################################################################################################################

Dans cet exercice, vous allez convertir une chaîne de caractères en tableau avec split().

Exemple :

var texte = 'Voici du texte';
var tableau = texte.split(' ');

Ici le critère de découpage de texte est l'espace indiqué avec split(' '), on obtient donc :

tableau = ['Voici','du','texte'];

############################################################################################################################################################################

Dans cet exercice, vous allez convertir un tableau en chaîne de caractères avec join().

Exemple :

var tableau = ['banane','fraise','pomme'];
var texte = tableau.join(' '); //

Ici les éléments de tableau seront espacés dans texte car on a précisé un espace avec join(' '), on obtient donc :

texte = 'banane fraise pomme';

Si vous utilisez simplement join() (sans espace), les éléments du tableau seront collés les uns aux autres.

############################################################################################################################################################################

Quelle type de boucle utiliser ?

Les boucles while et for permettent de parcourir un tableau. Mais la boucle for semble plus logique à utiliser.
La boucle for utilise forcément un itérateur (le i++) et c'est avec cet itérateur que l'on va parcourir le tableau.

Exemple :

var tableau = ['banane','fraise','pomme'];
var i;
var longueur = tableau.length; // On récupère la longueur une fois pour toute ici car la longueur ne changera pas.
for (i = 0; i < longueur; i++)
&#123;
    alert(tableau[i]);
}

Dans l'exemple, la boucle affiche l'élément du tableau dont l'index (et donc la position dans le tableau) correspond à i, et ce tant que i est inférieur à la longueur du tableau (et donc au nombre d'éléments contenus dedans).

Ici le tableau a une longueur de 3 (car trois éléments), comme i par de zéro pour correspondre à l'index du premier élément, il suffit d'indiquer strictement inférieur à la longueur du tableau.

La boucle fera donc trois itérations avec i = 0, i= 1, i = 2.

############################################################################################################################################################################


Il existe aussi les tableaux associatifs dans lesquels les éléments sont accessibles via un identifiant.

Pour déclarer un tableau associatif on utilise des accolades et non des crochets.

var voiture = &#123;};

Si les indices n'ont pas besoin d'être précisés lors de la déclaration d'un tableau ordonné, les identifiants d'un tableau associatif doivent l'être.
On associe donc un identifiant à une valeur.

Exemple :

var voiture = &#123;
    marque : 'Bugatti',
    modele : 'Chiron',
    couleur : 'bleue',
    annee : 2016
};

Voici un tableau associatif avec des identifiants (marque, modele, couleur, annee) et des valeurs associées.

Remarque :

On pourrait tout mettre sur une même ligne avec le ; à la fin comme d'habitude. Mais pour plus de lisibilité, c'est ainsi qu'on présente un tableau associatif.

Le double-point : séparant identifiant et valeur sont obligatoires ainsi que la virgule , qui sépare chaque couple identifiant/valeur sauf pour le dernier.

############################################################################################################################################################################

Avec les tableaux ordonnés, vous savez comment accéder à un élément en utilisant l'indice :

var fruits = [Banane,Fraise,Pomme,Poire,Kiwi];
var banane = fruits[0];

Et pour les tableaux associatifs ?

var voiture = &#123;
    marque : 'Bugatti',
    modele : 'Chiron',
    couleur : 'bleue',
    annee : 2016
};

Il suffit de faire comme ceci :

var quelleCouleur = voiture.couleur;

On indique la variable qui contient le tableau associatif puis le point . puis l'identifiant souhaité.

Que remarquez-vous ?

La syntaxe est la même que ceci :

var texte = "Voici du texte";
var longueur = texte.length; // Pareil que voiture.couleur

Rappelez-vous, les variables qui contiennent du texte, un nombre, etc. contiennent en fait un objet qui représente du texte, un nombre, etc.

Et les objets possèdent des propriétés. .length est une propriété fournie par défaut par Javascript quand vous créé une chaîne de caractères, comme pour la variable texte ci-dessus.

Un tableau associatif est structuré comme un objet, tel que Javascript le conçoit. Et l'identifiant est en fait une propriété.

voiture contient donc un objet avec des propriétés qui ont des valeurs.

Remarque :

Un tableau associatif ne possède pas de propriétés ou méthodes natives puisque c'est vous qui allez définir les propriétés.

############################################################################################################################################################################

Etant donné qu'un tableau associatif ne possède pas de méthodes par défaut il n'est pas possible d'utiliser push() comme dans un tableau ordonné.

En fait il suffit de spécifier une nouvelle propriété (ainsi que sa valeur) comme ceci :

voiture.prix = "2.4 millions d'euros"; // Oui c'est le prix de la Bugatti !

############################################################################################################################################################################

Pour parcourir un tableau ordonné, la boucle for est adaptée car elle utilise l'indice correspondant à chaque élément du tableau.

Un tableau associatif ne possède pas d'indice numérique donc la boucle for n'est pas adaptée. Il faut utiliser un nouveau type de boucle spécifique aux tableaux associatifs : for in.

Exemple :

var voiture = &#123;
    marque : 'Bugatti',
    modele : 'Chiron',
    couleur : 'bleue',
    annee : 2016
};
// Ci-dessous la boucle
for (var id in voiture)
&#123;
    alert(voiture[id]);
}

Il y a trois mots clés indispensables dans la boucle : for, var, in. Ici, on déclare une nouvelle variable id qui va parcourir chaque propriété du tableau voiture.
Pour chaque propriété, on l'affiche avec alert(voiture[id]).

Remarque :

Utiliser le nom id n'est pas obligatoire, vous pouvez donner le nom que vous voulez, mais c'est conseillé de faire commme ceci.


############################################################################################################################################################################
############################################################################################################################################################################

Dans cet exercice vous allez découvrir ce qu'est une fonction, à quoi ça sert et comment déclarer une fonction.

À quoi ça sert ?

Quand vous allez commencer à écrire des scripts, vous allez vous rendre compte que certains morceaux de code font la même chose et sont répétés à plusieurs endroits dans votre script.

Ceci alourdit le code et n'est pas pratique à maintenir à jour. Si vous souhaitez modifier ce code qui est réutilisé un peu partout dans le script, il faudra le faire pour toutes ses occurrences. Pas pratique. C'est la que les fonctions interviennent.

Une fonction est une sorte de "boîte noire" dans laquelle est écrit une portion de code qui fait quelque chose. Une fonction porte un nom que vous aurez choisi (comme une variable). Il suffira d'appeler ce nom dans le script et le code correspondant sera exécuté.

La syntaxe d'une fonction

function maFonction () &#123;
    // Code a exécuter
}

Pour déclarer une fonction, il faut le mot-clé function suivi du nom que vous voulez donner à cette fonction. Puis un couple de parenthèses () dans lequel vous pourrez donner des paramètres / arguments qui seront utilisés dans la fonction (mais ils ne sont pas obligatoires). Entre les accolades &#123;} se trouve la portion de code à exécuter. Il n'y a pas de ; à la fin : c'est une structure (comme les boucles et les conditions) et non une instruction.

Ici maFonction n'est pas exécutée, juste déclarée. Pour exécuter la fonction il faut l'appeler :

maFonction();

Fonction ou méthode ?

Sans le savoir, vous avez déjà utilisé des fonctions proposées nativement par Javascript : alert(), prompt(), confirm() ...

Il y a aussi toUpperCase() qui permet de mettre du texte en majuscule. C'est une fonction utilisée avec un objet de type chaîne de caractères (string).

Lors de l'introduction sur les objets on avait vu qu'un objet possédait des propriétés et des méthodes. Une méthode est en fait une fonction native d'un objet Javascript, comme toUpperCase() et plein d'autres.
Mais c'est exactement la même chose.

############################################################################################################################################################################

Une fonction est une sorte de boîte noire dans lequel du code est exécuté. Donc ce code est en quelque sorte "isolé" du reste du script.
Si on déclare une variable dans le script, elle est accessible dans l'ensemble du script, c'est donc une variable globale.

Exemple :

// on déclare une variable globale
var maVariable = "Variable globale";
// on déclare une fonction
function test() &#123;
    alert(maVariable);
}
// on exécute la fonction
test();

Ici, la fonction test() va bien afficher "Variable globale" car la variable déclarée dans le script global est accessible dans la fonction.

############################################################################################################################################################################

Si une fonction a accès à une variable globale, cela fonctionne-t-il dans le sens contraire ? Et bien non.

Une variable déclarée au sein même d'une fonction est une variable locale et elle n'est pas accessible dans le reste du script. Et ce pour la bonne raison que une fois la fonction exécutée, la variable locale est détruite.

Exemple :

// on déclare une fonction
function test() &#123;
    var localVar = "Variable locale";
    alert(localVar);
}
// on exécute la fonction
test();
// on affiche directement localVar
alert(localVar);

Ici, la fonction test() va bien afficher "Variable locale" car la fonction a accès à la variable. Mais le alert() qui se trouve dans le script global va renvoyer undefined car il n'a pas accès à la variable déclarée dans la fonction.

Il faut donc faire attention à la portée d'une variable.

Globale ou locale ?

Faut-il donc déclarer toutes les variables globalement ?
Non, car si une variable n'est utilisée que dans une fonction, alors il suffit jsute de la déclarer localement dans la fonction. Elle ne sera pas utile dans le reste du script.

############################################################################################################################################################################

Si une fonction est en partie indépendante du reste du code, il serait quand même pratique de lui donner des informations dont elle pourrait avoir besoin pour exécuter son propre code.

Les arguments

Argument, ou paramètre, ou encore valeur, autant de mots pour désigner la même chose : une information passée en entrée à la fonction pour qu'elle s'en serve dans son code.

alert() est une fonction qui prend en paramètre ce qu'on souhaite qu'elle affiche.

La syntaxe d'une fonction avec un argument

function maFonction (arg) &#123;
    // Code a exécuter
}

Ici on a déclaré une fonction avec un paramètre en plus arg. Il est possible d'en indiquer plusieurs :

function maFonction (arg1,arg2,arg3) &#123;
    // Code a exécuter
}

Exemple :

// on déclare la fonction
function maFonction (prenom) &#123;
    alert('Bonjour '+prenom);
}
// on exécute la fonction
maFonction("Jean");

On indique à la fonction une chaîne de caractère en paramètre d'entrée.
La fonction va comprendre que pour elle prenom = Jean. Elle va donc se servir de ce paramètre comme une variable interne.

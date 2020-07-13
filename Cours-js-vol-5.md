L'un des avantages de Javascript est que c'est un langage exécutée du côté client, donc dans votre navigateur. De ce fait, Javascript a accès à de nombreuses informations sur l'environnement d'exécution d'une page web et donc la fenêtre du navigateur.

Pour Javascript, la fenêtre du navigateur est représentée par l'objet window et alert() est en fait une fonction (ou méthode) de window et l'on pourrait tout aussi bien écrire window.alert(). Idem pour prompt(), confirm().
De même window possède des propriétés permettant de connaître la largeur et hauteur en pixels de la fenêtre du navigateur.

Ce qui nous intéresse ici, c'est l'objet document qui représente la structure HTML de la page web et tout ce qui est contenu dans <html></html>.

document possède aussi des fonctions permettant de manipuler la structure HTML (le DOM) d'une page web.

La structure du DOM

http://www.w3schools.com/js/pic_htmltree.gif

Le DOM est constitué par des noeuds (nodes en anglais) :

    le noeud racine est <html>;
    chaque noeud possède un parent (sauf le noeud racine);
    chaque noeud peut avoir plusieurs enfants;
    chaque noeud peut avoir des noeuds frères / soeurs.

Un noeud peut être une balise HTML mais aussi du texte contenu dans cette balise.

#############################################################################################################################################################################
Dans cet exercice vous allez voir comment trouver un élément HTML par son nom de balise avec la fonction .getElementsByTagName().

DOM :

```
<div>
    <p>Paragraphe</p>
</div>
```

Javascript :

var div = document.getElementsByTagName('div');

Ici la variable div contiendra un objet qui représente l'élément HTML div. Il faut préciser entre les parenthèses le nom de la balise HTML souhaitée.

Si vous avez réussi l'exercice précédent, vous avez donc pu afficher 3 fois ceci :

 [object HTMLParagraphElement]

Grâce à la boucle vous avez donc pu récupérer les trois paragraphes p qui sont stockés chacun dans un objet.

Pour l'instant, vous savez comment récupérer un ou des éléments HTML. Vous verrez dans les exercices suivant comment agir sur ces éléments HTML et donc le DOM.

Il est aussi possible de récupérer les éléments HTML selon la class css qu'ils possèdent avec la fonction suivante :

.getElementsByClassName()

Elle fonctionne de la même manière que la fonction précédente.

Il  est aussi possible de récupérer les éléments HTML selon leur id avec la fonction suivante :

.getElementById()

Elle fonctionne de la même manière que la fonction précédente. La différence est que seul un élément est retourné. En effet, un id en css est censé être unique. Si plusieurs éléments possèdent le même id alors cette fonction retournera que le premier élément trouvé dans le DOM.

Donc ici, pas besoin de boucle.

#############################################################################################################################################################################
l existe un moyen beaucoup plus flexible que les méthodes précédentes pour sélectionner un élément HTML dans le DOM :

.querySelector()

Cette fonction sélectionne un élément en utilisant les sélecteurs css. De ce fait les possibilités sont nombreuses. Il suffit de préciser en paramètres de la fonction un sélecteur css comme vous l'écririez dans un fichier .css

Exemple :

document.querySelector("div > p");

Ici, on sélectionne tous les p qui sont des enfants directs d'un div. Attention, cette fonction ne récupère que le premier élément HTML correspondant. Pas besoin de boucle ici pour parcourir le résultat.

Pour récupérer une liste de plusieurs éléments HTML toujours en utilisant les sélecteurs css, il faut utiliser la fonction .querySelectorAll().

Cette fonction récupère aussi une liste (ou collection) d'éléments (comme getElementsByTagName() et getElementsByClassName()). Il faut donc une boucle pour parcourir les résultats.
########################################################################################################################################################################

Il est possible de récupérer ou de modifier le contenu d'un élément HTML avec la propriété innerHTML.

Récupérer le contenu HTML

var contenu = element.innerHTML;

Modifier le contenu HTML

element.innerHTML = "Nouveau contenu HTML (texte + balises)";

ex
var div = document.querySelector('div > p');
div.innerHTML = "Dernier paragraphe";
########################################################################################################################################################################
Il est possible de modifier un attribut d'un élément HTML.

Modifier l'attribut d'un élément HTML

element.attribute = "Nouvelle valeur";

Ici attribute est à remplacer par le nom de l'attribut en question.

Exemple :

element.src = "monimage.png"

Ici on récupère un élément HTML (une image) et on change le lien vers le fichier en question.

########################################################################################################################################################################

Il est aussi possible d'ajouter un attribut à un élément HTML avec la fonction .setAttribute().

Exemple :

element.setAttribute("class", "democlass");

Ici on récupère un élément HTML et on ajoute une class css appelée democlass.

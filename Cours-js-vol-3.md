Les boucles sont aussi des structures de contrôles qui permettent de contrôler le flux d'exécution de votre script en fonction de critères ou conditions que vous aurez définis. Cela ajoute un degré d'intelligence à votre code.

À quoi ça sert ?

Une boucle permet d'exécuter une portion de code un certain nombre de fois.

La structure de base d'une boucle est très similaire à un if à la différence que le mot-clé n'est pas le même (ce n'est pas if mais un autre mot).
Chaque fois que vous utiliserez une boucle, il faudra s'arranger pour sortir de la boucle à un moment donné : si votre boucle tourne à l'infini, ça fera planter votre navigateur.

Dans cet exercice vous allez voir le premier type de boucle : for.

Exemple théorique :

for (declaration1;declaration2;declaration3)
&#123;
    // Code à exécuter
}

    declaration1 est exécuté avant que la boucle ne commence;
    declaration2 est la condition pour exécuter la boucle;
    declaration3 est exécuté à chaque itération de la boucle;

Exemple pratique :

Ci-dessous un exemple concrêt d'une boucle qui s'exécute tant que number est inférieur ou égal à 5.

for (var i = 0; i <= 5; i++)
&#123;
    alert("La boucle est à l'itération "+i);
}

Ici, la boucle sera exécutée 6 fois, on dit qu'il y a 6 itérations. Pour chaque itération la boucle affichera dans une pop-up le numéro de l'itération.

Comment ça marche :

    avant la première exécution de la boucle, on déclare i = 0;
    tant que i <= 5 on exécute ce qu'il y a dans la boucle;
    à chaque fin d'itération (donc une fois que le code est exécuté), on incrémente i++;

###################################################################################################################################################################


Vous venez de voir la boucle for qui exécute une portion de code un certain nombre de fois selon les déclarations indiquées en entrée de la boucle.

Dans cet exercice vous allez voir la boucle while qui exécute une portion de code tant que la condition en entrée est vérifiée (égale à true).

La différence entre for et while est subtile :

    for utilise un itérateur qui est incrémenté (++) pour permettre de sortir de la boucle à un moment donné;
    while vérifie si une condition est vérifiée et, si à un moment donné elle ne l'est plus, alors on sortira de la boucle;

Exemple théorique :

while (condition)
&#123;
    // Code exécuter tant que condition est vérifiée (true)
}
###################################################################################################################################################################

Dans l'exercice précédent vous avez utilisé la boucle while de la même manière qu'une boucle for, c'est-à-dire avec un itérateur.

MAIS il est tout à fait possible de sortir d'une boucle while sans utiliser d'itérateur. Il suffit de s'arranger pour que la condition en entrée de boucle ne soit plus vérifiée (false). Ce n'est pas le cas de la boucle for qui utilise forcément un itérateur.

Il existe une méthode plus simple pour sortir d'une boucle, avec l'utilisation de break. Vous l'avez déjà vu en abordant les switch.
Dans l'exercice précédent vous avez vu comment sortir d'une boucle en utilisant break.

Il est aussi possible de stopper une itération pour passer à la suivante sans stopper la boucle avec continue.

###################################################################################################################################################################

La structure de boucle do while est similaire à while à la différence qu'ici la boucle sera toujours exécutée au moins une fois.

Avec ce type de structure, la boucle est exécutée une première fois, puis la condition est vérifiée. Il y a donc toujours au moins une itération.

Exemple :

do
&#123;
    // Votre code exécuté au moins une fois
}
while (condition);

Remarque :

Notez la présence du ; à la fin du while.

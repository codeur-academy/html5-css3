# Les bases : titres et paragraphes

<!-- new slide -->

La plupart ``<h1>`` des textes structurés comprennent des titres et des paragraphes, que ce soit dans les romans, les journaux, les livres scolaires, les magazines, etc.

![Exemple d'un texte structurée en titre et paragraphe](../images/image.png)

Le contenu structuré facilite la lecture et la rend plus agréable.

En HTML, les paragraphes doivent être contenus dans un élément ``<p>``, comme ceci :

````html
<p>Je suis un paragraphe.</p>
````

Chaque titre doit être contenu dans un élément titre :

````html
<h1>Je suis le titre de l'article.</h1>
````

Il y a 6 éléments de titre — ``<h1>``, ``<h2>``, ``<h3>``, ``<h4>``, ``<h5>``, et ``<h6>``. Chaque élément représente un niveau de titre différent par exemple : 
- ``<h1>`` représente le titre principal, 
- ``<h2>`` représente un sous-titre, 
- ``<h3>`` représente un sous-sous-titre, 
- et ainsi de suite jusqu'au niveau de titre le plus bas qui correspond à ``<h6>``.

## Implémentation de la hiérarchie structurale

Dans une histoire, la balise <h1> représenterait le titre de l'histoire, les balises <h2> représenteraient les titres des chapitres, les balises <h3> les sous-sections des chapitres, en poursuivant ainsi jusqu'à la balise <h6>.

````html
<h1>L'ennui mortel</h1>
<p>par Chris Mills</p>
<h2>Chapitre I : La nuit noire</h2>
<p>Il faisait nuit noire. Quelque part une chouette ululait. La pluie tombait sur ...</p>
<h2>Chapitre II : Le silence éternel</h2>
<p>Notre protagoniste ne pouvait même pas murmurer à l'ombre de la silhouette...</p>
<h3>Le spectre parle</h3>
<p>Plusieurs heures s'étaient écoulées, quand soudain le spectre assis se releva et s'exclama : « S'il vous plaît, ayez pitié de mon âme ! »...</p>
````

C'est vous qui décidez ce que représentent les éléments utilisés tant que la hiérarchie a du sens. Vous devez cependant garder à l'esprit quelques bonnes pratiques lorsque vous créez de telles structures :

Il est préférable de n'utiliser qu'un seul <h1> par page — c'est le niveau principal, et tous les autres devraient être de niveau inférieur.
Assurez-vous d'utiliser les balise de titre dans l'ordre correct et logique : <h1> puis <h2>, puis <h3> et ainsi de suite.
Bien qu'il y ait 6 niveaux de titre (de <h1> à <h6>), Il est déconseillé d'utiliser plus de trois niveaux dans une page. Les documents avec beaucoup de niveaux deviennent complexes et difficiles à parcourir. Dans ce cas, il est préférable de partager le contenu sur plusieurs pages.

## Pourquoi  faut-il structurer un document ?

Pour répondre à cette question, regardons la page text-start.html — le point de départ de l'exemple que nous allons utiliser dans cet article (une recette). Enregistrez une copie de ce fichier sur votre ordinateur car vous en aurez besoin pour les exercices qui vont suivre. Le corps de ce document contient plusieurs parties sans aucune balise ; elles sont seulement séparées par des retours chariots (obtenus en pressant la touche **Entrée** ou ⏎)

Cependant, si l'on ouvre ce document dans un navigateur, il sera affiché sous forme d'un gros bloc de texte !

![Affichage d'un texte sans structuration](../images/image.png)

Ceci est dû au fait qu'il n'y a aucun élément indiquant la structure du contenu, et donc le navigateur ne sait pas différencier ce qui est un titre d'un paragraphe. De plus :

- Les visiteurs d'une page web la parcourent pour trouver le contenu pertinent. Par conséquent, ils ne lisent souvent que les titres (généralement nous ne passons que très peu de temps sur une page web). S'ils ne trouvent pas le contenu souhaité en quelques secondes, ils seront probablement déçus et chercheront l'information souhaitée ailleurs.
- Les moteurs de recherche, lorsqu'ils indexent votre page, prennent en considération les titres en tant que mots‑clés ce qui influe sur le classement de la page lors d'une recherche. Sans titre, une page aura un faible référencement (SEO (Search Engine Optimization).
- Les personnes malvoyantes ne pouvant lire votre page peuvent utiliser des lecteurs d'écran. Ces logiciels permettent d'accéder rapidement à une partie du texte. Pour cela, ils lisent les titres de votre document aux utilisateurs, leur permettant ainsi de trouver rapidement l'information dont ils ont besoin. Si les titres ne sont pas disponibles, les lecteurs d'écran lisent tout le document, le rendant peu accessible aux personnes avec un handicap visuel.
- Pour composer un style de contenu avec le CSS ou réaliser des choses intéressantes avec le JavaScript, vous devez avoir des éléments enveloppant les contenus pertinents, ce qui permet ensuite de les cibler avec CSS/JavaScript.
  
Il est donc nécessaire d'ajouter des balises de structuration du contenu.

## Pratique : structurer le contenu

## Pourquoi a-t-on besoin de sémantique ?

La sémantique est utilisée partout autour de nous — on se fie à nos précédentes experiences pour savoir à quoi servent les objets du quotidien; quand on voit quelque chose, on sait à quoi cela sert. Par exemple, on s'attend à ce qu'un feu rouge de signalisation signifie « Stop » et qu'un feu vert signifie « Avancez ». Les choses peuvent vite devenir plus compliquées si de mauvaises sémantiques sont appliquées (existe-t-il un pays dans lequel un feu rouge signifie que l'on peut passer ? Je ne l'espère pas.)

Dans la même optique, il faut s'assurer que l'on utilise les bons élements et que l'on donne la bonne signification, la bonne fonction et la bonne apparence à notre contenu. Dans ce contexte, l'élément <h1> est aussi un élement sémantique. Il donne au texte auquel il s'applique la fonction (ou la signification) de « titre principal de la page ».

````html
<h1>Ceci est un titre principal</h1>
````html

Par défaut, le navigateur l'affiche avec une police de caractères de grande taille pour qu'il ait l'apparence d'un titre (même si vous pourriez lui donner l'apparence de n'importe quel élément avec le CSS). Plus important encore, sa valeur sémantique est utilisée de différentes manières, notamment par les moteurs de recherche ou les lecteurs d'écran (comme expliqué plus haut).

D'autre part, vous pouvez faire ressembler n'importe quel élément à un titre principal. Par exemple :

````html
<span style="font-size: 32px; margin: 21px 0;">Est-ce un titre principal?</span>
Copy to Clipboard
````

C'est un élément <span>. Il n'a pas de valeur sémantique. Il s'utilise autour d'un contenu auquel vous souhaitez appliquer un style CSS (ou le modifier avec du JavaScript) sans lui donner une signification supplémentaire (vous en apprendrez plus à ce propos plus loin dans ce cours). Nous lui avons appliqué du CSS pour qu'il ressemble à un titre principal, mais comme il n'a pas de valeur sémantique, il ne bénéficie d'aucune des valeurs sémantiques décrites plus haut. Il est conseillé d'utiliser des éléments HTML adaptés à leur rôle.
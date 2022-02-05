# Création d'hyperliens

## Qu'est-ce un hyperlien ?

Les hyperliens sont l'une des plus passionnantes innovations que le web a à offrir. De fait, ils ont été une fonctionnalité du Web depuis le tout début, mais ils sont ce qui fait du Web une toile — ils nous permettent de lier nos documents à n'importe quel autre document (ou autre ressource) voulu ; nous pouvons faire des liens vers des parties précises de documents et rendre des applications disponibles à une simple adresse web (contrairement aux applications natives, qui doivent être installées et tout le travail). À peu près tout contenu web peut être converti en lien, de sorte que cliqué (ou activé autrement), il dirigera le navigateur vers une autre adresse web (URL).

> Note : Une URL peut pointer vers des fichiers HTML, des fichiers textes, des images, des documents textuels, des fichiers vidéo ou audio et tout ce qui peut exister sur le Web. Si le navigateur Web ne sait pas comment afficher ou gérer un fichier, il vous demande si vous voulez ouvrir le fichier (dans ce cas, la responsabilité de l'ouverture et de la gestion du fichier incombe à l'application native adéquate sur l'appareil) ou bien télécharger le fichier (auquel cas, vous pouvez essayer de vous en occuper plus tard).

La page d'accueil de la BBC, par exemple, contient un nombre important de liens pour pointer, non seulement vers de multiples articles d'actualité, mais encore vers d'autres zones du site (fonctionnalité de navigation) , des pages d'inscription/de connexion (outils utilisateur) et plus encore.

![Exemple pages avec des liens](../images/image.png)

## Anatomie d'un lien

Un lien élémentaire se crée en intégrant le texte (ou tout autre contenu) que vous voulez transformer en lien dans un élément <a> et en lui affectant un attribut href (également connu comme étant une Hypertext Reference) contenant l'adresse web vers laquelle vous voulez que le lien pointe.

````html
<p>Je suis en train de créer un lien à
<a href="https://www.mozilla.org/fr/">la page d'accueil Mozilla</a>.
</p>
````

qui donne le résultat suivant : Je suis en train de créer un lien à la page d'accueil de Mozilla.

## Ajouter des informations d'assistance avec l'attribut title

L'autre attribut qu'il est possible d'ajouter à un lien est title ; il est destiné à contenir des informations utiles supplémentaires à propos du lien, comme le type d'informations contenes dans la page ou ce qu'il faut savoir. Par exemple :

````html
<p>Je suis en train de créer un lien à
<a href="https://www.mozilla.org/fr/"
   title="Le meilleur endroit pour trouver plus d'informations sur la
  mission de Mozilla et la manière de contribuer">la page d'accueil Mozilla</a>.
</p>
````

Voici le résultat (le contenu de title apparaît dans une info-bulle quand le pointeur de souris passe sur le lien) :

## Pratique - création d'un lien

## Liens de niveau bloc

Comme mentionné précédemment, vous pouvez transformer à peu près tout contenu en un lien, même des éléments bloc . Si vous avez une image que vous voulez transformer en lien, vous avez juste à mettre l'image entre les balises <a></a>.

````html
<a href="https://www.mozilla.org/fr/">
  <img src="mozilla-image.png" alt="logo mozilla pointant sur la page d'accueil mozilla">
</a>
````

> Note : Nous vous donnerons beaucoup plus de détails sur l'utilisation d'images sur le Web dans un futur article.


## Fragments de documents

Il est possible de faire un lien vers une partie donnée d'un document HTML (désignée du terme fragment de document), plutôt que juste le haut du document. Pour ce faire, vous devrez d'abord assigner un attribut id à l'élément sur lequel vous voulez pointer. Il est généralement logique d'établir un lien vers une rubrique précise, ainsi cela ressemble à quelque chose comme :

````html
<h2 id="Adresse_mailing">Adresse de mailing</h2>
````

Puis, pour faire un lien vers cet id précisément, il convient de l'indiquer à la fin de l'URL, précédé d'un croisillon (#) :

````html
<p>Vous voulez nous écrire une lettre ? Utilisez notre <a href="contacts.html#Adresse_mailing">adresse de contact</a>.</p>
````

Vous pouvez même utiliser une référence au fragment de document seul pour faire un lien vers une autre partie du même document :

````html
<p>Vous trouverez n l'<a href="#Adresse_mailing">adresse de mailing</a> de notre société au
````

## Meilleures pratiques de liens

Il y a quelques bonnes pratiques à suivre pour l'écriture de liens. Jetons-y un coup d'œil.
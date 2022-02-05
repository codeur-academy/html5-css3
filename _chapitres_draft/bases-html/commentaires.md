# Commentaires en HTML

En HTML, comme pour la plupart des langages de programmation, il existe un mécanisme permettant d'écrire des commentaires dans le code. Les commentaires sont ignorés par le navigateur et invisibles à l'utilisateur. Leur but est de permettre d'inclure des commentaires dans le code pour dire comment il fonctionne, que font les diverses  parties du code, etc. Cela peut s'avérer très utile si vous revenez à un codage que vous n'avez pas travaillé depuis 6 mois et que vous ne pouvez pas vous rappeler ce que vous avez fait — ou si vous donnez votre code à quelqu'un d'autre pour qu'il y travaille.

Pour transformer une section de contenu dans votre fichier HTML en commentaire, vous devez la mettre dans les marqueurs spéciaux ``<!-- et-->``, par exemple :

````html
<p>Je ne suis pas dans un commentaire</p>
<!-- <p>Je suis dans un commmentaire!</p> -->
````


Comme vous pouvez le voir ci-dessous, le premier paragraphe apparaît dans le rendu de l'éditeur en ligne, mais le second n'apparaît pas.

![Commentaires en HTML](../images/bases-html/commentaires/exemple-commentaire.png)

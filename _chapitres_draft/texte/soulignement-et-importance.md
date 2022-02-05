# Soulignement et importance

Dans le langage, nous mettons souvent l'accent sur certains mots pour modifier le sens d'une phrase et pour marquer certains mots comme étant importants ou différents d'une manière ou d'une autre. HTML fournit divers éléments de sémantique pour nous permettre de marquer un contenu textuel avec de tels effets. Dans cette section, nous examinerons quelques-uns des plus courants.

## Emphase

Dans le langage parlé, pour accentuer, nous insistons sur certains mots, modifiant subtilement le sens de ce que nous disons. De même, dans le langage écrit, nous avons tendance à mettre un certain accent sur des mots en les écrivant en italique. Par exemple, les deux phrases suivantes ont des significations différentes.

> « Je suis content que vous n'ayez pas été en retard. »

> « Je suis content que vous n'ayez pas été *en retard.* »

La première phrase semble indiquer que le locuteur est vraiment soulagé que la personne n'aie pas été en retard. En revanche, la seconde a une tonalité sarcastique ou passive-agressive, exprimant la gêne que la personne soit arrivée un peu en retard.

En HTML, nous utilisons l'élément ``<em>`` (emphase) pour marquer ces circonstances. Outre rendre le document plus intéressant à lire, ces marqueurs sont reconnus par les lecteurs d'écran et exprimés sur un ton de voix différent. Les navigateurs utilisent l'italique par défaut, mais il ne faut pas utiliser cette balise pour mettre en italique. Pour cela, utilisez un élément ``<span>`` et du CSS, ou plus simplement un élément ``<i>`` (voir ci-dessous).

````html
<p>Je suis <em>content</em> que vous n'ayez pas été <em>en retard</em>.</p>
````

## Grande importance

Pour mettre l'accent sur des mots très importants, nous les soulignons d'un ton particulier dans la langue parlée et nous les mettons en caractères gras dans la langue écrite. Par exemple :

> Ce liquide est hautement toxique.

> Je compte sur vous. Ne soyez pas en retard !

En HTML, nous utilisons l'élément ``<strong>`` (forte importance) comme balise de telles circonstances. En plus de rendre le document plus lisible, ces balises sont reconnues par les lecteurs d'écran et énoncées avec des intonations différentes. Par défaut, les navigateurs mettent le texte marqué en gras, mais il ne faut pas utiliser cette balise pour mettre en gras. Pour cela, utilisez un élément ``<span>``} et du CSS, ou plus simplement un élément ``<b>`` (voir ci-dessous).

````html
<p>Ce liquide est <strong>hautement toxique</strong>.</p>

<p>Je compte sur vous. <strong>Ne soyez pas en retard</strong> !</p>
````

Il est possible d'imbriquer strong et em :

````html
<p>Ce liquide est <strong>hautement toxique</strong> —
si vous en buvez, <strong>vous pourriez en <em>mourir</em></strong>.</p>
````

## Pratique - Emphase et importance

## Italique, gras, soulignement…

Les éléments dont nous avons discuté jusqu'à présent ont une sémantique bien définie. La situation avec <b>, <i> et <u> est un peu plus complexe. Ils sont apparus pour que les personnes puissent écrire du texte en gras, en italique ou souligné à une époque où le CSS était encore mal ou pas du tout pris en charge. De tels éléments, qui n'affectent que la présentation et non la sémantique, sont appelés éléments de présentation et ne devraient plus être utilisés, car comme nous l'avons vu précédemment, la sémantique a la plus grande importance pour l'accessibilité, le référencement, etc.

````html

<!-- noms scientifiques -->
<p>
  Le colibri à gorge rouge (<i>Archilochus colubris</i>)
  est le colibri le plus courant dans l'ouest de l'Amérique du Nord.
</p>

<!-- mots dans une langue étrangère -->
<p>
  Le menu était un océan de mots exotiques comme <i lang="uk-latn">vatrushka</i>,
  <i lang="id">nasi goreng</i> et <i lang="en">porridge</i>.
</p>

<!-- une faute d'orthographe connue -->
<p>
  Un jour, j'apprendrai comment mieux <u style="text-decoration-line: underline; text-decoration-style: wavy;">épeler</u>.
</p>

<!-- Mettre en évidence les mots‑clés dans un ensemble d'instructions -->
<ol>
  <li>
    <b>Trancher</b> deux morceaux de pain dans la miche.
  </li>
  <li>
    <b>Mettre</b> une rondelle de tomate et une feuille de laitue
    entre les deux tranches de pain.
  </li>
</ol>

````

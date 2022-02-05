# Listes

Intéressons-nous maintenant aux listes. Il y a des listes partout dans la vie — de la liste de courses à la liste de directions que vous suivez inconsciemment pour rentrer chez vous tous les jours,  sans oublier la liste des instructions que vous suivez dans ce tutoriel ! Les listes sont aussi très répandues sur le Web, nous allons nous intéresser aux trois différents types de liste.

## Listes non-ordonnées

Les listes non-ordonnées sont utilisées pour représenter des listes d'éléments pour lesquelles l'ordre n'a pas d'importance. Prenons par exemple une liste de courses :

````html
lait
œufs
pain
````

Les listes non-ordonnées débutent par un élément ``<ul>`` (unorderd list) qui enveloppe tous les éléments de la liste:

````html
<ul>
lait
œufs
pain
</ul>
````

Chaque item est contenu dans un élément <li> (list item):

````html
<ul>
  <li>lait</li>
  <li>œufs</li>
  <li>pain</li>
  <li>houmous</li>
</ul>
````

## Pratique - liste non-ordonnées

## Listes ordonnées

Les listes ordonnées permettent de représenter des listes dans lesquelles l'ordre des éléments a de l'importance — prenons par exemple une série de directions à suivre:

````html
Roulez jusqu'au bout de la route
Tournez à droite
Allez tout droit aux deux premiers ronds-points
Tournez à gauche au troisième rond-point
Roulez sur 300 mètres, l'école est sur votre droite
````

Les balises suivent la même structure que pour les listes ordonnées, à cela près que la liste est contenue dans l'élément <ol> (ordered list), et non dans <ul>:

````html
<ol>
  <li>Roulez jusqu'au bout de la route</li>
  <li>Tournez à droite</li>
  <li>Allez tout droit aux deux premiers ronds-points</li>
  <li>Tournez à gauche au troisième rond-point</li>
  <li>Roulez sur 300 mètres, l'école est sur votre droite</li>
</ol>
````

## Pratique - Recette de cuisine

````html

<h1>Recette rapide de l'houmous</h1>

<p>Cette .</p>

<p>L'houmous </p>

<h2>Ingrédients</h2>

<ul>
<li>1 boîte (400 g) de pois chiches (garbanzos)</li>
<li>175g de crème de sésame</li>
</ul>

<h2>Instructions</h2>

<ol>
<li>Ôter la peau de l'ail et le hacher grossièrement.</li>
<li>Enlever les graines et la tige du poivron, le hacher grossièrement.</li>
</ol>

<p>Pour des saveurs diqui vous va.</p>

<h2>Conservation</h2>

<p>Mete. S'il se met à fermenter, jettez‑le sans hésiter.</p>

````

## Imbriquer des listes

Il est parfaitement possible d'imbriquer une liste dans une autre. Il se peut que vous vouliez insérer une liste à puces derrière une même puce de niveau supérieur. Prenons par exemple la deuxième liste de la recette :

````html
<ol>
  <li>Ôter la peau de l'ail et le hacher grossièrement.</li>
  <li>Enlever les graines et la tige du poivron, le hacher grossièrement.</li>
  <li>Mettre tous les ingrédients dans un robot mixer jusqu'à l'obtention d'une pâte.</li>
  <li>Si vous voulez un houmous grenu, ne le mixez pas trop longtemps.</li>
  <li>Si vous voulez un houmous lisse, mixez-le plus longtemps.</li>
</ol>
````

Comme les deux dernières puces de la liste sont très liées à celle qui les précède (elles semblent être des sous-instructions ou des choix correspondant à cette puce), il peut être judicieux de les regrouper dans une même liste non-ordonnée, et placer cette liste dans le quatrième item. Cela ressemblerait alors à ceci :

````html
<ol>
  <li>Ôter la peau de l'ail et le hacher grossièrement.</li>
  <li>Enlever les graines et la tige du poivron, le hacher grossièrement.</li>
  <li>Mettre tous les ingrédients dans un robot mixer jusqu'à l'obtention d'une pâte.
    <ul>
      <li>Si vous voulez un houmous grenu, ne le mixez pas trop longtemps.</li>
      <li>Si vous voulez un houmous lisse, mixez-le plus longtemps.</li>
    </ul>
  </li>
</ol>
````

N'hésitez pas à revenir au dernier TP pour modifier vous même la liste correspondante dans la recette.
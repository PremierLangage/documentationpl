# `input`

Le modèle `input` permet de fabriquer des exercices avec un champ de réponse textuel libre.

[![](inpu1.png)](https://pl.u-pem.fr/filebrowser/demo/33986/)

## Clés spécifiques

* `text` (chaîne de caractères). Enoncé de l'exercice.
* `solution` (chaîne de caractères). Solution de l'exercice.
* `casesensitive` (booléen). Cette clé détermine si l'évaluation de la réponse tien compte de la casse ou pas. Par défaut, cette clé vaut `false`.
* `diffmeasure` ("EditDist", "EditRatio"). Cette clé définit la mesure utilisée pour calculer l'écart entre la réponse entrée par l'élève et la solution.
* `tolerance` (nombre). Cette clé définit l'écart maximal accepté (pour la mesure définit dans `diffmeasure`).
* `data` (chaîne de caractères au format CSV). Cette clé contient des données qui pourront être utilisées dans les clés `text` et `solution`.
* `delimiter`. Cette clé définiti le délimiteur utilisé pour lire les données de la clé `data`. Le délimiteur par défaut est la virgule.
* `skipinitialspace`.

## Exemples

~~~
extends = /model/basic/input.pl

text ==
Qui a écrit *Les Misérables* ?
==

solution ==
Victor Hugo
Hugo
==
~~~

~~~
extends = /model/basic/input.pl

title ==
Exemple 2
==

data ==
symbole,nom
Hydrogène,H
Hélium,He
Carbone,C
Azote,N
Oxygène,O
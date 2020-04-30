# 1.2  Une solution
Si l’on veut poser le moins possible de barrages, on a intérêt à laisser au monstre le plus petit espace possible. On adonc intérêt à couper l’espace restant en deux parties égales. 
En répétant cette stratégie, on divise le nombre de cases restantes par deux à chaque étape. Plus précisément, à la première étape, on a 127 cases bleues. En plaçant un bloc au milieu, il reste au monstre un espace de $(127−12)/2= 63$ cases.

Compléter le tableau suivant pour déterminer le nombre de cases restantes à chaque étape :


| Nombre de blocs | 0 | 1 |2 |3 | 4| 5| 6 |
------- | -------- | --- |--- |--- |--- |--- |--- |
| $n$ = Nombre de cases bleues|127| ...|...|...|...|...|...|
|Codage en binaire de $n$| 111 111| ...|...|...|...|...|...|


Le nombre minimum de barrages pour coincer le monstre dans le pire des cas dans 127 cases est donc de 6.
On peut constater que 6 est également le nombre de chiffres de 127 lorsqu’il est écrit en binaire.
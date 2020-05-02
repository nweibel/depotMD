---
tags: NSI, dichotomie
---
## Instructions
* Cliquer sur Edit pour modifier le contenu
* S'il restes cases vides dans le tableau : en compléter quelques-unes
* Si vous êtes en désaccord avec une valeur, la corriger et expliquer sous le tableau pourquoi vous pensez que l'ancienne valeur était incorrecte
* Si vous êtes d'accord avec tout et que le document est complet ajoutez votre prénom dans la partie **Validation**

---
# 1.2  Une solution
Si l’on veut poser le moins possible de barrages, on a intérêt à laisser au monstre le plus petit espace possible. On a donc intérêt à couper l’espace restant en deux parties égales. 
En répétant cette stratégie, on divise le nombre de cases restantes par deux à chaque étape. Plus précisément, à la première étape, on a 127 cases bleues. En plaçant un bloc au milieu, il reste au monstre un espace de $(127−12)//2= 63$ cases.

Compléter le tableau suivant pour déterminer le nombre de cases restantes à chaque étape :


| Nombre de blocs | 0 | 1 |2 |3 | 4| 5| 6 |
------- | -------- | --- |--- |--- |--- |--- |--- |
| $n$ = Nombre de cases bleues|127| 63|...|...|...|...|...|
|Codage en binaire de $n$| 111 111| ...|...|...|...|...|...|


Le nombre **minimum** de barrages pour coincer le monstre **dans le pire des cas** dans 127 cases est donc de 6.
On peut constater que 6 est également le nombre de chiffres de 127 lorsqu’il est écrit en binaire.

---

**Arguments de modification** : 

- [ ] modification 1 : à décrire
- [ ] etc

---
**Validation du document** : 
- [x] prénom élève 1 (à remplacer)
- [ ] prénom élève 2
- [ ] prénom élève 3, 
- [ ] etc
---
tags: NSI, dichotomie
---
## Instructions
* Cliquer sur Edit pour modifier le contenu
* S'il reste des cases vides dans le tableau : en compléter quelques-unes
* Si vous êtes en désaccord avec une valeur, la corriger et expliquer sous le tableau pourquoi vous pensez que l'ancienne valeur était incorrecte
* Si vous êtes d'accord avec tout et que le document est complet ajoutez votre prénom dans la partie **Validation**

---
# 1.2  Une solution
Si l’on veut poser le moins possible de barrages, on a intérêt à laisser au monstre le plus petit espace possible. On a donc intérêt à couper l’espace restant en deux parties égales. 
En répétant cette stratégie, on divise le nombre de cases restantes par deux à chaque étape. Plus précisément, à la première étape, on a 127 cases bleues. En plaçant un bloc au milieu, il reste au monstre un espace de $(127−1)//2= 63$ cases.

Compléter le tableau suivant pour déterminer le nombre de cases restantes à chaque étape :


| Nombre de blocs | 0 | 1 |2 |3 | 4| 5| 6 |
|------- | -------- | --- |--- |--- |--- |--- |--- |
| $n$ = Nombre de cases bleues|127| 63 |31 |15|7 |3 |1 |
|Codage en binaire de $n$| 111 1111| 11 1111 |1 1111 |1111 |111 |11 |1 |


Le nombre **minimum** de barrages pour coincer le monstre **dans le pire des cas** dans 127 cases est donc de 6.

On peut constater que 127 possède 7 chiffres lorsqu’il est écrit en binaire, et 1 en possède 1 (!). Chaque division par 2 correspond en binaire à la suppression du chiffre des unités. On obtient donc 1 à partir de 127 en effectuant **6** divisions successives par 2. 

---

**Arguments de modification** : 

- [ ] modification 1 : nombre de case en bleu:(63-1)//2 = 31 , (31-1)//2=15 , (15-1)//2=7 , (7-1)//2=3 , (3-1)//2= 1 
- [ ] modification 2: nombre binaire: 127= 128-1= (2^7) -1 = 0111 1111

---
**Validation du document** : 
- [x] Elma
- [x] Simon
- [x] Laura
- [x] Josuan
- [x] Sofiene
- [x] Kemal
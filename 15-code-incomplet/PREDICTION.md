# Ma prédiction - Exercice 15

## Fonction `trouverMax`

```java
int max = ???;      // Trou 1 : t[0]
for (int i = ???;   // Trou 2 : 1
    if (t[i] ??? max)  // Trou 3 :  >
        max = ???;     // Trou 4 : t[i]
```

**Raisonnement :**
- Trou 1 : on met max a t[0] pour commencer avec le premier element
- Trou 2 : on commence la boucle a 1 parce que le 0 est deja pris
- Trou 3 : on regarde si t[i] est plus grand que max
- Trou 4 : si oui on met max a t[i]

---

## Fonction `contient`

```java
if (??? == ???)     // Trou 1 et 2 : t[i] == val
    return ???;     // Trou 3 : true
return ???;         // Trou 4 : false
```

**Raisonnement :**
- Trous 1-2 : on compare t[i] avec val pour voir si on a trouve la valeur
- Trou 3 :si on trouve on renvoie true
- Trou 4 : si on n a rien trouve on renvoie false

---

## Fonction `sommePairs`

```java
if (t[i] ??? 2 == ???)  // Trou 1 et 2 : % 2 et 0
    somme = somme + ???; // Trou 3 : t[i]
```

**Raisonnement :**
- Trou 1 : on fait t[i] % 2 pour verifier si c est pair
- Trou 2 : on compare avec 0, si reste = 0 c est pair
- Trou 3 : si c est pair on ajoute t[i] a somme

---

## Fonction `dupliquer`

```java
int[] res = new int[t.length ??? 2];  // Trou 1 : * 2
res[i ??? 2] = t[i];                   // Trou 2 : * 2
res[i ??? 2 ??? 1] = t[i];              // Trou 3 et 4 : * 2 + 1 et t[i]
```

**Raisonnement :**
- Trou 1 : on fait un tableau deux fois plus grand pour pouvoir mettre deux fois chaque element
- Trou 2 :on met la premiere copie a i*2
- Trous 3-4 : on met la deuxieme copie a i*2+1
# Ma prédiction - Exercice 06

## Traçage ligne par ligne

**Lignes 3-4 :** Initialisation
- a = 5
- b = 3

---

### Appel 1 : `addition(a, b)` (ligne 6)

**Entrée dans la fonction `addition` :**
- Paramètre x reçoit : a
- Paramètre y reçoit : b

**Ligne 17 :** `int somme = x + y;`
- Calcul : a + b = somme
- somme = 8

**Ligne 18 :** `return somme;`
- Valeur retournée : 8

**Retour dans main :**
- resultat1 = addition(5,3)

**Ligne 7 :** Affichage
```
addition(5, 3) = 8

```

---

### Appel 2 : `carre(a)` (ligne 9)

**Entrée dans la fonction `carre` :**
- Paramètre n reçoit : a

**Ligne 22 :** `return n * n;`
- Calcul : n * n = 25
- Valeur retournée : 25

**Retour dans main :**
- resultat2 = carre(a)

**Ligne 10 :** Affichage
```
carre(5) = 25

```

---

### Appel 3 : `addition(carre(2), b)` (ligne 12)

**Étape 1 : Évaluation de `carre(2)`**
- Paramètre n reçoit : 2
- Calcul : 2 * 2 = 4
- Valeur retournée : 4

**Étape 2 : Appel de `addition(___, b)`**
- Paramètre x reçoit : carre(2)
- Paramètre y reçoit : b
- Calcul : carre(2) + b = 7
- Valeur retournée : 7

**Retour dans main :**
- resultat3 = addition(carre(2), b)

**Ligne 13 :** Affichage
```
addition(carre(2), 3) = 7

```

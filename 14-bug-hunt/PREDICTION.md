# Ma prédiction - Exercice 14

## BUG 1 : fonction `moyenne`

**Ligne suspecte :** for (int i = 0; i <= t.length; i++)

**Description du bug :** Dépassement de la capacité du tableau

**Ce qui va se passer :**  erreur de type index out of range

**Correction proposée :** for (int i = 0; i <= t.length-1; i++)

---

## BUG 2 : fonction `estTrie`

**Ligne suspecte :** for (int i = 0; i < t.length; i++)
                        if (t[i] > t[i + 1])

**Description du bug :** La condition if risque de dépasser les limites du tableau, car elle utilise i+1. Pour le dernier élément, i+1 dépasserait l’index maximal du tableau.

**Ce qui va se passer :**  erreur de type index out of range

**Correction proposée :** for (int i = 0; i < t.length-1; i++)

---

## BUG 3 : fonction `inverse`

**Ligne suspecte :** for (int i = 0; i < t.length; i++) {

**Description du bug :** On échange les cases de façon symétrique, mais comme on parcourt tout le tableau, on finit par rééchanger des trucs qu’on avait déjà inversés

**Ce qui va se passer :** On ne verra rien de changé parce qu’on remet le tableau dans le meme ordre qu’au début

**Correction proposée :** for (int i = 0; i < t.length/2; i++) 

---

## BUG 4 : fonction `compter`

**Ligne suspecte :** return count;

**Description du bug :** Le code s arrête trop tot parce que la ligne n est pas bien indentee

**Ce qui va se passer :** si val est present la fonction va toujours renvoyer 1 meme sil y en a plusieurs

**Correction proposée :** retirer  return count

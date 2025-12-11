# Ma prédiction - Exercice 17

## Fonction `moyenneInef`

**Problème identifié :** a chaque fois il refait la somme depuis le debut alors que c est pas utile

**Nombre d'opérations actuelles (pour n éléments) :** n*(n+1)/2

**Version optimisée :**
```java
public static double moyenneEff(int[] t) {
    int somme = 0;
    for (int i = 0; i < t.length; i++) {
        somme += t[i];
    }
    return (double) somme / t.length;
    
}
```

---

## Fonction `contientDoublonInef`

**Problème identifié :** il compare chaque paire deux fois et meme avec lui meme alors que c est pas necessaire

**Version optimisée :**
```java
public static boolean contientDoublonEff(int[] t) {
     for (int i = 0; i < t.length; i++) {
        for (int j = i + 1; j < t.length; j++) {
            if (t[i] == t[j]) {
                return true;
            }
        }
    }
    return false;
    
}
```

---

## Fonction `premierEtDernierInef`

**Problème identifié :** il parcourt tout le tableau alors que pour le premier et le dernier element c est pas utile

**Version optimisée :**
```java
public static String premierEtDernierEff(int[] t) {
    return t[0] + " et " + t[t.length - 1];
    
}
```

---

## Fonction `rechercheInef`

**Problème identifié :** il continue meme apres avoir trouve la valeur alors que ca sert a rien

**Version optimisée :**
```java
public static int rechercheEff(int[] t, int val) {
     for (int i = 0; i < t.length; i++) {
        if (t[i] == val) {
            return i;
        }
    }
    return -1;
    
}
```

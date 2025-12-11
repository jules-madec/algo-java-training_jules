# Ma prédiction - Exercice 19

## Partie 1 : Comprendre l'existant

### Classe `Produit`

**Attributs (noms cryptiques) :**
- `n` représente : le nom du produit
- `p` représente : le prix du produit
- `q` représente : la quantite en stock

**Méthode `valeur()` :**
- Que calcule-t-elle ? le prix multiplié par la quantite

---

### Classe `Inventaire`

**Attributs :**
- `prods` représente : le tableau de produits
- `nb` représente : le nombre de produits ajoutes

**Méthodes :**
- `ajouter(Produit p)` : ajoute le produit si il y a de la place
- `chercher(String nom)` : cherche un produit par son nom et le retourne sinon null
- `afficher()` : affiche le nom prix et quantite de chaque produit
- `valeurTotale()` : calcule la somme de la valeur de tous les produits

---

## Partie 2 : Prédire la sortie actuelle

```
=== Inventaire ===
Pomme : 2.5 x 100
Pain : 1.2 x 50
Lait : 0.95 x 75
Beurre : 2.1 x 30

=== Recherche 'Pain' ===
Trouve : Pain a 1.2 euros

=== Valeur totale ===
Valeur : 375.5 euros

```

---

## Partie 3 : Ajouter la fonctionnalité

**Fonctionnalité demandée :** 
Ajouter une méthode `afficherCher(double seuil)` qui affiche les produits dont le prix est supérieur au seuil.

**Ma méthode :**
```java
public void afficherCher(double seuil) {
    for (int i = 0; i < nb; i++) {
    Produit p = prods[i];
    if (p.getPrix() > seuil) 
        System.out.println(p.getNom() + " : " + p.getPrix() + " x " + p.getQuantite());
}
    
}
```

**Sortie attendue pour `afficherCher(2.0)` :**
```
Pomme : 2.5 x 100
Beurre : 2.1 x 30

```

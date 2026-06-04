# Chapitre 7 : Les Fonctions en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre ce qu’est une fonction.
* Créer et utiliser des fonctions.
* Passer des paramètres à une fonction.
* Retourner des valeurs avec `return`.
* Réutiliser du code efficacement.
* Organiser un programme de manière modulaire.

---

# 1. Qu'est-ce qu'une fonction ?

Une fonction est un bloc de code réutilisable qui exécute une tâche précise.

### Exemple dans la vie réelle :

```text id="a1b2c3"
Une machine à café :
- Tu appuies sur un bouton
- Elle prépare le café
- Tu reçois le café
```

En programmation :

* Tu appelles une fonction
* Elle exécute une tâche
* Elle retourne un résultat (ou non)

---

# 2. Définir une fonction

En Python, on utilise le mot-clé `def`.

## Syntaxe

```python id="d4e5f6"
def nom_fonction():
    instruction
```

---

## Exemple simple

```python id="g7h8i9"
def saluer():
    print("Bonjour !")

saluer()
```

### Résultat

```text id="j1k2l3"
Bonjour !
```

---

# 3. Les fonctions avec paramètres

Les paramètres permettent de donner des informations à une fonction.

---

## Exemple

```python id="m4n5o6"
def saluer(nom):
    print("Bonjour", nom)

saluer("Bruno")
saluer("Alice")
```

### Résultat

```text id="p7q8r9"
Bonjour Bruno
Bonjour Alice
```

---

# 4. Plusieurs paramètres

```python id="s1t2u3"
def addition(a, b):
    print(a + b)

addition(5, 3)
```

### Résultat

```text id="v4w5x6"
8
```

---

# 5. La fonction return

`return` permet de renvoyer une valeur.

---

## Exemple

```python id="y7z8a9"
def addition(a, b):
    return a + b

resultat = addition(5, 3)

print(resultat)
```

### Résultat

```text id="b1c2d3"
8
```

---

# 6. Différence print vs return

| print                      | return                             |
| -------------------------- | ---------------------------------- |
| Affiche une valeur         | Renvoie une valeur                 |
| Ne peut pas être réutilisé | Peut être stocké dans une variable |

---

## Exemple

```python id="e4f5g6"
def carre(x):
    return x * x

resultat = carre(4)

print(resultat)
```

---

# 7. Fonction avec input()

```python id="h7i8j9"
def demander_nom():
    nom = input("Entrez votre nom : ")
    print("Bonjour", nom)

demander_nom()
```

---

# 8. Fonction de calcul

```python id="k1l2m3"
def calcul(a, b):
    somme = a + b
    produit = a * b
    return somme, produit

s, p = calcul(5, 3)

print("Somme :", s)
print("Produit :", p)
```

---

# 9. Valeurs par défaut

```python id="n4o5p6"
def saluer(nom="Utilisateur"):
    print("Bonjour", nom)

saluer()
saluer("Bruno")
```

---

# 10. Portée des variables

Une variable créée dans une fonction est locale.

---

## Exemple

```python id="q7r8s9"
def test():
    x = 10
    print(x)

test()
```

❌ Erreur si on essaie d'utiliser `x` dehors :

```python id="t1u2v3"
print(x)
```

---

# 11. Fonction imbriquée

```python id="w4x5y6"
def operation(a, b):
    def addition():
        return a + b

    return addition()

print(operation(5, 3))
```

---

# 12. Fonctions utiles en Python

## len()

```python id="z7a8b9"
print(len("Python"))
```

## max() et min()

```python id="c1d2e3"
print(max(5, 10, 2))
print(min(5, 10, 2))
```

---

# 13. Exemple complet

```python id="f4g5h6"
def fiche(nom, age):
    print("Nom :", nom)
    print("Age :", age)

fiche("Bruno", 25)
```

---

# 14. Exemple : calculatrice avec fonctions

```python id="i7j8k9"
def addition(a, b):
    return a + b

def soustraction(a, b):
    return a - b

def multiplication(a, b):
    return a * b

def division(a, b):
    return a / b

a = int(input("Nombre 1 : "))
b = int(input("Nombre 2 : "))

print("Addition :", addition(a, b))
print("Soustraction :", soustraction(a, b))
print("Multiplication :", multiplication(a, b))
print("Division :", division(a, b))
```

---

# 15. Bonnes pratiques

✔ Donner des noms clairs aux fonctions

```python id="l1m2n3"
def calcul_age():
```

✔ Une fonction = une seule tâche

✔ Utiliser `return` pour réutiliser les résultats

---

# Résumé

Dans ce chapitre, nous avons appris :

* Les fonctions `def`
* Les paramètres
* `return`
* Les variables locales
* Les fonctions avec input()
* La réutilisation du code

---

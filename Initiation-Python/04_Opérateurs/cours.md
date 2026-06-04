# Chapitre 4 : Les Opérateurs en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Utiliser les opérateurs arithmétiques.
* Comprendre les opérateurs de comparaison.
* Manipuler les opérateurs logiques.
* Réaliser des calculs et des conditions simples.
* Écrire des expressions complètes en Python.

---

# 1. Qu'est-ce qu'un opérateur ?

Un opérateur est un symbole qui permet d'effectuer une opération sur des valeurs.

Exemple :

```python id="a1k2m3"
a = 10
b = 5

print(a + b)
```

---

# 2. Les opérateurs arithmétiques

Ils servent à effectuer des calculs mathématiques.

| Opérateur | Signification    | Exemple |
| --------- | ---------------- | ------- |
| +         | Addition         | a + b   |
| -         | Soustraction     | a - b   |
| *         | Multiplication   | a * b   |
| /         | Division         | a / b   |
| %         | Modulo (reste)   | a % b   |
| //        | Division entière | a // b  |
| **        | Puissance        | a ** b  |

---

## 2.1 Addition

```python id="b2n3p4"
a = 10
b = 5

print(a + b)
```

Résultat :

```text id="r1d2e3"
15
```

---

## 2.2 Soustraction

```python id="c3o4q5"
a = 10
b = 5

print(a - b)
```

---

## 2.3 Multiplication

```python id="d4p5r6"
a = 10
b = 5

print(a * b)
```

---

## 2.4 Division

```python id="e5q6s7"
a = 10
b = 5

print(a / b)
```

Résultat :

```text id="t7u8v9"
2.0
```

---

## 2.5 Modulo (reste de la division)

```python id="f6r7t8"
a = 10
b = 3

print(a % b)
```

Résultat :

```text id="w8x9y0"
1
```

---

## 2.6 Division entière

```python id="g7s8u9"
a = 10
b = 3

print(a // b)
```

Résultat :

```text id="z1a2b3"
3
```

---

## 2.7 Puissance

```python id="h8t9v0"
a = 2
b = 3

print(a ** b)
```

Résultat :

```text id="c4d5e6"
8
```

---

# 3. Les opérateurs de comparaison

Ils permettent de comparer deux valeurs.

| Opérateur | Signification     |
| --------- | ----------------- |
| ==        | égal à            |
| !=        | différent de      |
| >         | supérieur à       |
| <         | inférieur à       |
| >=        | supérieur ou égal |
| <=        | inférieur ou égal |

---

## Exemple

```python id="i9u0w1"
a = 10
b = 5

print(a == b)
print(a != b)
print(a > b)
print(a < b)
```

Résultat :

```text id="d7e8f9"
False
True
True
False
```

---

# 4. Les opérateurs logiques

Ils permettent de combiner plusieurs conditions.

| Opérateur | Signification |
| --------- | ------------- |
| and       | ET logique    |
| or        | OU logique    |
| not       | NON logique   |

---

## 4.1 AND

Les deux conditions doivent être vraies.

```python id="j1v2x3"
age = 20
niveau = 3

print(age > 18 and niveau > 2)
```

Résultat :

```text id="f0g1h2"
True
```

---

## 4.2 OR

Une seule condition suffit.

```python id="k2w3y4"
age = 16
niveau = 3

print(age > 18 or niveau > 2)
```

Résultat :

```text id="i3j4k5"
True
```

---

## 4.3 NOT

Inverse une condition.

```python id="l3x4z5"
est_connecte = True

print(not est_connecte)
```

Résultat :

```text id="m6n7o8"
False
```

---

# 5. Combinaison d'opérateurs

```python id="p1q2r3"
a = 10
b = 5
c = 2

resultat = (a + b) * c

print(resultat)
```

Résultat :

```text id="s4t5u6"
30
```

---

# 6. Utilisation avec input()

```python id="v7w8x9"
a = int(input("Nombre 1 : "))
b = int(input("Nombre 2 : "))

print("Somme =", a + b)
print("Produit =", a * b)
```

---

# 7. Exemple complet

```python id="y0z1a2"
a = int(input("Nombre 1 : "))
b = int(input("Nombre 2 : "))

print("Addition :", a + b)
print("Soustraction :", a - b)
print("Multiplication :", a * b)
print("Division :", a / b)
print("Reste :", a % b)
```

---

# 8. Priorité des opérateurs

Python respecte un ordre de priorité :

1. Parenthèses `()`
2. Puissance `**`
3. Multiplication / Division `* / // %`
4. Addition / Soustraction `+ -`

---

## Exemple

```python id="b3c4d5"
resultat = 10 + 5 * 2
print(resultat)
```

Résultat :

```text id="e6f7g8"
20
```

---

# 9. Bonnes pratiques

✔ Utiliser des parenthèses pour clarifier les expressions.

```python id="h9i0j1"
resultat = (10 + 5) * 2
```

✔ Donner des noms de variables clairs.

```python id="k2l3m4"
prix_total = 100
```

---

# Résumé

Dans ce chapitre, nous avons appris :

* Les opérateurs arithmétiques
* Les opérateurs de comparaison
* Les opérateurs logiques
* Les priorités des opérations
* L'utilisation des opérateurs avec input()

---


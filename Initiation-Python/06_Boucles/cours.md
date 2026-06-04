# Chapitre 6 : Les Boucles en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre le concept de boucle.
* Utiliser la boucle `while`.
* Utiliser la boucle `for`.
* Répéter des instructions automatiquement.
* Manipuler les instructions `break` et `continue`.
* Créer des programmes répétitifs efficaces.

---

# 1. Qu'est-ce qu'une boucle ?

Une boucle permet de répéter une instruction plusieurs fois sans la réécrire.

### Exemple de la vie réelle :

```text id="a1b2c3"
Faire des exercices 10 fois
```

Sans boucle :

```python id="d1e2f3"
print("Exercice")
print("Exercice")
print("Exercice")
```

Avec boucle :

```python id="g4h5i6"
for i in range(3):
    print("Exercice")
```

---

# 2. La boucle while

La boucle `while` signifie **tant que**.

## Syntaxe

```python id="j7k8l9"
while condition:
    instruction
```

---

## Exemple simple

```python id="m1n2o3"
i = 1

while i <= 5:
    print(i)
    i = i + 1
```

### Résultat

```text id="p4q5r6"
1
2
3
4
5
```

---

# 3. Attention aux boucles infinies

Si la condition n'est jamais fausse, la boucle ne s'arrête jamais.

```python id="s7t8u9"
while True:
    print("Boucle infinie")
```

⚠️ À éviter sauf cas particuliers.

---

# 4. La boucle for

La boucle `for` permet de parcourir une suite de valeurs.

---

## 4.1 Utilisation avec range()

```python id="v1w2x3"
for i in range(5):
    print(i)
```

### Résultat

```text id="y4z5a6"
0
1
2
3
4
```

---

## 4.2 Début et fin personnalisés

```python id="b7c8d9"
for i in range(1, 6):
    print(i)
```

### Résultat

```text id="e1f2g3"
1
2
3
4
5
```

---

## 4.3 Pas d'incrément (step)

```python id="h4i5j6"
for i in range(0, 10, 2):
    print(i)
```

### Résultat

```text id="k7l8m9"
0
2
4
6
8
```

---

# 5. Parcourir une chaîne de caractères

```python id="n1o2p3"
mot = "Python"

for lettre in mot:
    print(lettre)
```

### Résultat

```text id="q4r5s6"
P
y
t
h
o
n
```

---

# 6. Parcourir une liste

```python id="t7u8v9"
fruits = ["pomme", "banane", "orange"]

for fruit in fruits:
    print(fruit)
```

---

# 7. La fonction break

`break` permet d'arrêter une boucle.

```python id="w1x2y3"
for i in range(10):
    if i == 5:
        break
    print(i)
```

### Résultat

```text id="z4a5b6"
0
1
2
3
4
```

---

# 8. La fonction continue

`continue` permet de sauter une itération.

```python id="c7d8e9"
for i in range(5):
    if i == 2:
        continue
    print(i)
```

### Résultat

```text id="f1g2h3"
0
1
3
4
```

---

# 9. Différence entre while et for

| Boucle | Utilisation                                    |
| ------ | ---------------------------------------------- |
| while  | Quand on ne connaît pas le nombre d'itérations |
| for    | Quand on connaît le nombre d'itérations        |

---

# 10. Exemple avec input()

```python id="i4j5k6"
i = 1

while i <= 3:
    nom = input("Entrez votre nom : ")
    print("Bonjour", nom)
    i += 1
```

---

# 11. Exemple complet : table de multiplication

```python id="l7m8n9"
nombre = int(input("Entrez un nombre : "))

for i in range(1, 11):
    print(f"{nombre} x {i} = {nombre * i}")
```

---

# 12. Exemple complet : compteur

```python id="o1p2q3"
compteur = 0

while compteur < 5:
    print("Compteur :", compteur)
    compteur += 1
```

---

# 13. Exemple : somme des nombres

```python id="r4s5t6"
somme = 0

for i in range(1, 6):
    somme += i

print("Somme =", somme)
```

### Résultat

```text id="u7v8w9"
Somme = 15
```

---

# 14. Bonnes pratiques

✔ Toujours modifier la variable dans une boucle while

```python id="x1y2z3"
i += 1
```

✔ Éviter les boucles infinies involontaires

✔ Utiliser `for` quand possible

---

# Résumé

Dans ce chapitre, nous avons appris :

* Les boucles `while`
* Les boucles `for`
* La fonction `range()`
* `break`
* `continue`
* Les boucles sur chaînes et listes
* Les bonnes pratiques

---


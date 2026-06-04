# Chapitre 5 : Les Structures Conditionnelles

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre les structures conditionnelles.
* Utiliser `if`, `else` et `elif`.
* Prendre des décisions dans un programme.
* Combiner les conditions avec les opérateurs logiques.
* Créer des programmes interactifs basés sur des choix.

---

# 1. Qu'est-ce qu'une condition ?

Une condition permet à un programme de prendre une décision.

Exemple dans la vie réelle :

```text id="a1b2c3"
Si il pleut → je prends un parapluie
Sinon → je sors sans parapluie
```

En Python, cela s'appelle une structure conditionnelle.

---

# 2. La structure if

Le mot-clé `if` signifie **si**.

## Syntaxe

```python id="d4e5f6"
if condition:
    instruction
```

---

## Exemple simple

```python id="g7h8i9"
age = 18

if age >= 18:
    print("Vous êtes majeur")
```

---

# 3. La structure if...else

`else` signifie **sinon**.

## Syntaxe

```python id="j1k2l3"
if condition:
    instruction
else:
    instruction
```

---

## Exemple

```python id="m4n5o6"
age = 16

if age >= 18:
    print("Majeur")
else:
    print("Mineur")
```

---

# 4. La structure if...elif...else

`elif` signifie **sinon si**.

## Syntaxe

```python id="p7q8r9"
if condition1:
    instruction
elif condition2:
    instruction
else:
    instruction
```

---

## Exemple

```python id="s1t2u3"
note = 15

if note >= 16:
    print("Très bien")
elif note >= 12:
    print("Bien")
elif note >= 10:
    print("Passable")
else:
    print("Échec")
```

---

# 5. Conditions avec input()

```python id="v4w5x6"
age = int(input("Entrez votre âge : "))

if age >= 18:
    print("Vous êtes majeur")
else:
    print("Vous êtes mineur")
```

---

# 6. Les opérateurs de comparaison

Rappel :

| Opérateur | Signification     |
| --------- | ----------------- |
| ==        | égal              |
| !=        | différent         |
| >         | supérieur         |
| <         | inférieur         |
| >=        | supérieur ou égal |
| <=        | inférieur ou égal |

---

## Exemple

```python id="y7z8a9"
a = 10
b = 5

if a > b:
    print("a est plus grand que b")
```

---

# 7. Conditions multiples avec AND

```python id="b1c2d3"
age = 20
carte = True

if age >= 18 and carte == True:
    print("Accès autorisé")
else:
    print("Accès refusé")
```

---

# 8. Conditions multiples avec OR

```python id="e4f5g6"
jour = "samedi"

if jour == "samedi" or jour == "dimanche":
    print("C'est le week-end")
else:
    print("Jour de travail")
```

---

# 9. Inversion avec NOT

```python id="h7i8j9"
connecte = False

if not connecte:
    print("Veuillez vous connecter")
```

---

# 10. Conditions imbriquées

On peut mettre une condition dans une autre.

```python id="k1l2m3"
age = 20
permis = True

if age >= 18:
    if permis:
        print("Vous pouvez conduire")
    else:
        print("Vous devez obtenir le permis")
```

---

# 11. Exemple complet : système de notes

```python id="n4o5p6"
note = int(input("Entrez votre note : "))

if note >= 16:
    print("Très bien")
elif note >= 14:
    print("Bien")
elif note >= 10:
    print("Passable")
else:
    print("Insuffisant")
```

---

# 12. Exemple complet : accès utilisateur

```python id="q7r8s9"
age = int(input("Age : "))
mot_de_passe = input("Mot de passe : ")

if age >= 18 and mot_de_passe == "admin":
    print("Accès autorisé")
else:
    print("Accès refusé")
```

---

# 13. Bonnes pratiques

✔ Indenter correctement le code

```python id="t1u2v3"
if age >= 18:
    print("OK")
```

✔ Utiliser des conditions claires

```python id="w4x5y6"
if note >= 10:
    print("Admis")
```

✔ Éviter les conditions trop complexes

---

# Résumé

Dans ce chapitre, nous avons appris :

* `if`
* `else`
* `elif`
* Les opérateurs de comparaison
* Les opérateurs logiques (`and`, `or`, `not`)
* Les conditions imbriquées
* Les programmes de prise de décision

---


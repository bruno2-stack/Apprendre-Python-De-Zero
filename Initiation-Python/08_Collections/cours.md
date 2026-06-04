# Chapitre 8 : Les Collections en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre les listes, tuples, dictionnaires et ensembles.
* Manipuler des collections de données.
* Ajouter, modifier et supprimer des éléments.
* Parcourir des collections avec des boucles.
* Choisir la bonne structure selon le besoin.

---

# 1. Qu'est-ce qu'une collection ?

Une collection est une structure qui permet de stocker plusieurs valeurs dans une seule variable.

Exemple :

```python id="a1b2c3"
nombres = [1, 2, 3, 4]
```

---

# 2. Les listes

Une liste est une collection **modifiable**.

---

## 2.1 Création d'une liste

```python id="d4e5f6"
fruits = ["pomme", "banane", "orange"]
```

---

## 2.2 Accéder aux éléments

```python id="g7h8i9"
print(fruits[0])
```

Résultat :

```text id="j1k2l3"
pomme
```

---

## 2.3 Modifier un élément

```python id="m4n5o6"
fruits[1] = "mangue"
print(fruits)
```

---

## 2.4 Ajouter un élément

```python id="p7q8r9"
fruits.append("ananas")
print(fruits)
```

---

## 2.5 Supprimer un élément

```python id="s1t2u3"
fruits.remove("pomme")
print(fruits)
```

---

## 2.6 Parcourir une liste

```python id="v4w5x6"
for fruit in fruits:
    print(fruit)
```

---

# 3. Les tuples

Un tuple est une collection **non modifiable**.

---

## 3.1 Création

```python id="y7z8a9"
couleurs = ("rouge", "vert", "bleu")
```

---

## 3.2 Accès

```python id="b1c2d3"
print(couleurs[0])
```

---

## 3.3 Important

❌ Impossible de modifier un tuple :

```python id="e4f5g6"
couleurs[0] = "jaune"  # Erreur
```

---

# 4. Les dictionnaires

Un dictionnaire stocke des données sous forme **clé : valeur**.

---

## 4.1 Création

```python id="h7i8j9"
etudiant = {
    "nom": "Bruno",
    "age": 25,
    "ville": "Porto-Novo"
}
```

---

## 4.2 Accéder aux valeurs

```python id="k1l2m3"
print(etudiant["nom"])
```

---

## 4.3 Modifier une valeur

```python id="n4o5p6"
etudiant["age"] = 26
```

---

## 4.4 Ajouter une nouvelle clé

```python id="q7r8s9"
etudiant["classe"] = "L2"
```

---

## 4.5 Parcourir un dictionnaire

```python id="t1u2v3"
for cle, valeur in etudiant.items():
    print(cle, ":", valeur)
```

---

# 5. Les ensembles (set)

Un set est une collection **non ordonnée** et **sans doublons**.

---

## 5.1 Création

```python id="w4x5y6"
nombres = {1, 2, 3, 3, 4}
print(nombres)
```

Résultat :

```text id="z7a8b9"
{1, 2, 3, 4}
```

---

## 5.2 Ajouter un élément

```python id="c1d2e3"
nombres.add(5)
```

---

## 5.3 Supprimer un élément

```python id="f4g5h6"
nombres.remove(2)
```

---

# 6. Différences entre les collections

| Type         | Modifiable | Ordonné           | Doublons     |
| ------------ | ---------- | ----------------- | ------------ |
| Liste        | Oui        | Oui               | Oui          |
| Tuple        | Non        | Oui               | Oui          |
| Set          | Oui        | Non               | Non          |
| Dictionnaire | Oui        | Oui (Python 3.7+) | Clés uniques |

---

# 7. Exemple avec liste et boucle

```python id="i7j8k9"
notes = [12, 15, 18, 10]

somme = 0

for note in notes:
    somme += note

print("Moyenne :", somme / len(notes))
```

---

# 8. Exemple avec dictionnaire

```python id="l1m2n3"
etudiant = {
    "nom": "Alice",
    "age": 20
}

print(f"Nom : {etudiant['nom']}")
print(f"Age : {etudiant['age']}")
```

---

# 9. Exemple complet

```python id="p9q8r7"
contacts = []

contacts.append({"nom": "Bruno", "numero": "12345"})
contacts.append({"nom": "Alice", "numero": "67890"})

for contact in contacts:
    print(contact["nom"], contact["numero"])
```

---

# 10. Bonnes pratiques

✔ Utiliser une liste pour des données ordonnées

✔ Utiliser un dictionnaire pour des données structurées

✔ Utiliser un set pour éviter les doublons

---

# Résumé

Dans ce chapitre, nous avons appris :

* Les listes
* Les tuples
* Les dictionnaires
* Les ensembles (sets)
* Les opérations de base sur les collections
* Les parcours avec boucles

---


# Chapitre 2 : Variables et Types de Données

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre le concept de variable.
* Déclarer et utiliser des variables.
* Manipuler les principaux types de données Python.
* Identifier le type d'une variable.
* Convertir un type de donnée vers un autre.

---

# 1. Qu'est-ce qu'une variable ?

Une variable est un espace mémoire permettant de stocker une information.

On peut voir une variable comme une boîte possédant un nom et contenant une valeur.

Exemple :

```python
nom = "Bruno"
```

Ici :

* `nom` est le nom de la variable.
* `"Bruno"` est la valeur stockée.

---

# 2. Création d'une variable

La syntaxe générale est :

```python
nom_variable = valeur
```

Exemples :

```python
nom = "Alice"
age = 20
taille = 1.75
```

---

# 3. Afficher une variable

```python
nom = "Alice"

print(nom)
```

Résultat :

```text
Alice
```

---

# 4. Afficher plusieurs variables

```python
nom = "Alice"
age = 20

print(nom)
print(age)
```

Résultat :

```text
Alice
20
```

---

# 5. Les principaux types de données

Python possède plusieurs types de données.

Les plus utilisés sont :

| Type  | Description    | Exemple   |
| ----- | -------------- | --------- |
| str   | Texte          | "Bonjour" |
| int   | Nombre entier  | 15        |
| float | Nombre décimal | 3.14      |
| bool  | Vrai ou Faux   | True      |

---

# 6. Type chaîne de caractères (str)

Une chaîne de caractères représente du texte.

Exemples :

```python
nom = "Bruno"
ville = "Porto-Novo"

print(nom)
print(ville)
```

---

# 7. Type entier (int)

Les nombres entiers ne possèdent pas de virgule.

Exemples :

```python
age = 25
nombre_etudiants = 40

print(age)
print(nombre_etudiants)
```

---

# 8. Type décimal (float)

Les nombres décimaux possèdent une partie fractionnaire.

Exemples :

```python
temperature = 36.5
prix = 2500.75

print(temperature)
print(prix)
```

---

# 9. Type booléen (bool)

Un booléen peut prendre deux valeurs :

```python
True
False
```

Exemple :

```python
est_connecte = True

print(est_connecte)
```

---

# 10. Vérifier le type d'une variable

Python fournit la fonction `type()`.

Exemple :

```python
nom = "Alice"

print(type(nom))
```

Résultat :

```text
<class 'str'>
```

Autres exemples :

```python
age = 20
print(type(age))

prix = 12.5
print(type(prix))

actif = True
print(type(actif))
```

---

# 11. Modifier la valeur d'une variable

Une variable peut changer de valeur.

Exemple :

```python
score = 10

print(score)

score = 20

print(score)
```

Résultat :

```text
10
20
```

---

# 12. Règles de nommage

Un nom de variable :

✅ Peut contenir :

* lettres
* chiffres
* underscore (_)

❌ Ne peut pas :

* commencer par un chiffre
* contenir des espaces
* utiliser des mots réservés de Python

Valides :

```python
nom
age
prix_total
note1
```

Invalides :

```python
1nom
prix total
for
```

---

# 13. Concaténation de chaînes

Concaténer signifie assembler plusieurs textes.

Exemple :

```python
prenom = "Jean"
nom = "Dupont"

print(prenom + " " + nom)
```

Résultat :

```text
Jean Dupont
```

---

# 14. Utilisation des f-strings

Méthode moderne recommandée.

Exemple :

```python
nom = "Alice"
age = 20

print(f"Je m'appelle {nom} et j'ai {age} ans.")
```

Résultat :

```text
Je m'appelle Alice et j'ai 20 ans.
```

---

# 15. Conversion de types

Parfois, il est nécessaire de convertir une donnée.

## Convertir en entier

```python
age = int("25")

print(age)
```

---

## Convertir en décimal

```python
prix = float("12.5")

print(prix)
```

---

## Convertir en texte

```python
nombre = 50

texte = str(nombre)

print(texte)
```

---

# 16. Exemple complet

```python
nom = "Bruno"
age = 25
taille = 1.75
enseignant = True

print("Nom :", nom)
print("Age :", age)
print("Taille :", taille)
print("Enseignant :", enseignant)
```

Résultat :

```text
Nom : Bruno
Age : 25
Taille : 1.75
Enseignant : True
```

---

# Bonnes pratiques

✅ Utiliser des noms explicites

```python
nom_etudiant = "Alice"
```

❌ Éviter :

```python
x = "Alice"
```

---

# Résumé

Dans ce chapitre, nous avons appris :

✓ Les variables

✓ Les chaînes de caractères (str)

✓ Les entiers (int)

✓ Les décimaux (float)

✓ Les booléens (bool)

✓ La fonction type()

✓ La concaténation

✓ Les f-strings

✓ La conversion de types


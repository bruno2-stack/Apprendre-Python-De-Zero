# Chapitre 3 : Entrées et Sorties

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Afficher des informations à l'écran.
* Utiliser la fonction `print()`.
* Récupérer des informations saisies par l'utilisateur.
* Utiliser la fonction `input()`.
* Convertir les données saisies.
* Créer des programmes interactifs.

---

# 1. Introduction

Un programme informatique communique avec l'utilisateur grâce :

* aux **sorties** (affichage d'informations),
* aux **entrées** (saisie d'informations).

Exemple :

```text
Programme : Quel est votre nom ?
Utilisateur : Bruno
Programme : Bonjour Bruno
```

---

# 2. Les sorties avec print()

La fonction `print()` permet d'afficher du texte ou des valeurs à l'écran.

Syntaxe :

```python
print(valeur)
```

Exemple :

```python
print("Bonjour")
```

Résultat :

```text
Bonjour
```

---

# 3. Afficher plusieurs informations

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

# 4. Afficher du texte et une variable

```python
nom = "Alice"

print("Nom :", nom)
```

Résultat :

```text
Nom : Alice
```

---

# 5. Affichage sur plusieurs lignes

```python
print("Bonjour")
print("Bienvenue")
print("En Python")
```

Résultat :

```text
Bonjour
Bienvenue
En Python
```

---

# 6. Les caractères spéciaux

### Retour à la ligne

```python
print("Bonjour\nPython")
```

Résultat :

```text
Bonjour
Python
```

---

### Tabulation

```python
print("Nom\tAge")
```

Résultat :

```text
Nom     Age
```

---

# 7. La fonction input()

La fonction `input()` permet de récupérer une information saisie par l'utilisateur.

Syntaxe :

```python
variable = input("Message")
```

Exemple :

```python
nom = input("Entrez votre nom : ")

print("Bonjour", nom)
```

Exécution :

```text
Entrez votre nom : Bruno
Bonjour Bruno
```

---

# 8. Stocker une saisie utilisateur

```python
ville = input("Votre ville : ")

print(ville)
```

Exemple :

```text
Votre ville : Porto-Novo
Porto-Novo
```

---

# 9. Plusieurs saisies utilisateur

```python
nom = input("Nom : ")
prenom = input("Prénom : ")
```

Puis :

```python
print(nom)
print(prenom)
```

---

# 10. Attention : input() retourne du texte

Toutes les valeurs saisies avec `input()` sont considérées comme des chaînes de caractères (`str`).

Exemple :

```python
age = input("Age : ")

print(type(age))
```

Résultat :

```text
<class 'str'>
```

Même si l'utilisateur tape :

```text
25
```

Python considère cette valeur comme du texte.

---

# 11. Conversion en entier

Pour effectuer des calculs, il faut convertir la saisie.

Exemple :

```python
age = int(input("Age : "))

print(age)
```

---

# 12. Conversion en décimal

```python
taille = float(input("Votre taille : "))

print(taille)
```

Exemple :

```text
Votre taille : 1.75
```

---

# 13. Addition de deux nombres

Sans conversion :

```python
a = input("Nombre 1 : ")
b = input("Nombre 2 : ")

print(a + b)
```

Exécution :

```text
Nombre 1 : 5
Nombre 2 : 3
53
```

Python concatène les textes.

---

# 14. Addition correcte

```python
a = int(input("Nombre 1 : "))
b = int(input("Nombre 2 : "))

print(a + b)
```

Résultat :

```text
8
```

---

# 15. Les f-strings

Méthode moderne pour afficher du texte.

Exemple :

```python
nom = "Alice"
age = 20

print(f"{nom} a {age} ans.")
```

Résultat :

```text
Alice a 20 ans.
```

---

# 16. Exemple complet

```python
nom = input("Nom : ")
prenom = input("Prénom : ")
age = int(input("Age : "))

print()
print("===== INFORMATIONS =====")
print(f"Nom : {nom}")
print(f"Prénom : {prenom}")
print(f"Age : {age}")
```

Exécution :

```text
Nom : Bruno
Prénom : Fambo
Age : 25

===== INFORMATIONS =====
Nom : Bruno
Prénom : Fambo
Age : 25
```

---

# 17. Mini Application : Calcul de l'âge futur

```python
nom = input("Votre nom : ")
age = int(input("Votre âge : "))

age_futur = age + 10

print(f"{nom}, dans 10 ans vous aurez {age_futur} ans.")
```

---

# Bonnes pratiques

✅ Toujours expliquer clairement ce que l'utilisateur doit saisir.

Exemple :

```python
nom = input("Entrez votre nom : ")
```

❌ Éviter :

```python
nom = input()
```

---

✅ Convertir les nombres avant de calculer.

```python
nombre = int(input("Nombre : "))
```

---

# Résumé

Dans ce chapitre, nous avons appris :

✓ La fonction `print()`

✓ La fonction `input()`

✓ Les entrées utilisateur

✓ Les sorties écran

✓ Les conversions avec `int()`

✓ Les conversions avec `float()`

✓ Les f-strings

✓ Les programmes interactifs

---

# Chapitre 10 : Les Exceptions en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre ce qu’est une exception.
* Gérer les erreurs en Python.
* Utiliser `try`, `except`, `finally`.
* Éviter les plantages de programmes.
* Créer des programmes plus robustes.

---

# 1. Qu'est-ce qu'une exception ?

Une exception est une **erreur qui survient أثناء l'exécution du programme**.

Exemple :

```text id="a1b2c3"
Division par zéro
Fichier introuvable
Erreur de type
```

---

# 2. Exemple d’erreur

```python id="d4e5f6"
a = 10
b = 0

print(a / b)
```

Résultat :

```text id="g7h8i9"
ZeroDivisionError
```

---

# 3. Pourquoi gérer les exceptions ?

Sans gestion d’erreur :

```text id="j1k2l3"
Le programme s’arrête brutalement
```

Avec gestion d’erreur :

```text id="m4n5o6"
Le programme continue de fonctionner
```

---

# 4. Structure try / except

## Syntaxe

```python id="p7q8r9"
try:
    instruction
except:
    gestion_erreur
```

---

## Exemple

```python id="s1t2u3"
try:
    a = 10
    b = 0
    print(a / b)

except:
    print("Erreur : division impossible")
```

---

# 5. Gestion d’un type d’erreur spécifique

```python id="v4w5x6"
try:
    a = int(input("Nombre : "))
    print(10 / a)

except ZeroDivisionError:
    print("Erreur : division par zéro")

except ValueError:
    print("Erreur : vous devez entrer un nombre")
```

---

# 6. Bloc else

Le bloc `else` s’exécute si aucune erreur ne survient.

```python id="y7z8a9"
try:
    a = int(input("Nombre : "))
    print(10 / a)

except:
    print("Erreur")

else:
    print("Aucune erreur détectée")
```

---

# 7. Bloc finally

Le bloc `finally` s’exécute toujours.

```python id="b1c2d3"
try:
    a = int(input("Nombre : "))
    print(10 / a)

except:
    print("Erreur")

finally:
    print("Fin du programme")
```

---

# 8. Exemple avec fichier

```python id="e4f5g6"
try:
    fichier = open("data.txt", "r")
    print(fichier.read())

except FileNotFoundError:
    print("Fichier introuvable")
```

---

# 9. Exemple complet

```python id="h7i8j9"
try:
    nom = input("Nom : ")
    age = int(input("Age : "))

    print(f"{nom} a {age} ans")

except ValueError:
    print("Erreur : âge invalide")
```

---

# 10. Lever une exception (raise)

On peut créer ses propres erreurs.

```python id="k1l2m3"
age = int(input("Age : "))

if age < 0:
    raise ValueError("L'âge ne peut pas être négatif")
```

---

# 11. Exemple pratique : calcul sécurisé

```python id="n4o5p6"
try:
    a = int(input("Nombre 1 : "))
    b = int(input("Nombre 2 : "))

    resultat = a / b
    print("Résultat :", resultat)

except ZeroDivisionError:
    print("Impossible de diviser par zéro")

except ValueError:
    print("Veuillez entrer des nombres valides")
```

---

# 12. Bonnes pratiques

✔ Toujours prévoir les erreurs possibles

✔ Utiliser des exceptions spécifiques

✔ Ne pas utiliser `except:` seul si possible

---

# Résumé

Dans ce chapitre, nous avons appris :

* Les exceptions
* `try`
* `except`
* `else`
* `finally`
* `raise`
* La gestion des erreurs

---


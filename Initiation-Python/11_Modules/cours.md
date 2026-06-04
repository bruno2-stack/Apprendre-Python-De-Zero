# Chapitre 11 : Les Modules en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre ce qu’est un module.
* Utiliser les modules intégrés de Python.
* Importer des fonctions depuis un module.
* Créer tes propres modules.
* Organiser un projet Python de manière professionnelle.

---

# 1. Qu'est-ce qu'un module ?

Un module est un **fichier Python contenant du code réutilisable** (fonctions, variables, classes).

Exemple :

```text id="a1b2c3"
math.py → module
```

---

# 2. Importer un module

Python possède des modules intégrés.

## Syntaxe

```python id="d4e5f6"
import nom_module
```

---

## Exemple avec math

```python id="g7h8i9"
import math

print(math.sqrt(16))
```

Résultat :

```text id="j1k2l3"
4.0
```

---

# 3. Importer une fonction spécifique

```python id="m4n5o6"
from math import sqrt

print(sqrt(25))
```

---

# 4. Alias (renommer un module)

```python id="p7q8r9"
import math as m

print(m.sqrt(36))
```

---

# 5. Modules intégrés utiles

## 5.1 math

```python id="s1t2u3"
import math

print(math.pi)
print(math.sqrt(9))
```

---

## 5.2 random

```python id="v4w5x6"
import random

print(random.randint(1, 10))
```

---

## 5.3 datetime

```python id="y7z8a9"
import datetime

print(datetime.datetime.now())
```

---

# 6. Créer son propre module

Tu peux créer ton propre fichier Python.

---

## Exemple

Créer un fichier :

```text id="b1c2d3"
operations.py
```

Contenu :

```python id="e4f5g6"
def addition(a, b):
    return a + b

def multiplication(a, b):
    return a * b
```

---

## Utilisation du module

```python id="h7i8j9"
import operations

print(operations.addition(5, 3))
print(operations.multiplication(4, 2))
```

---

# 7. Importation partielle

```python id="k1l2m3"
from operations import addition

print(addition(10, 5))
```

---

# 8. Organisation d’un projet

Exemple de structure :

```text id="n4o5p6"
projet_python/
│
├── main.py
├── operations.py
├── utils.py
└── data/
```

---

# 9. Le module **name**

Permet de distinguer un fichier exécuté directement ou importé.

```python id="q7r8s9"
if __name__ == "__main__":
    print("Fichier exécuté directement")
```

---

# 10. Exemple complet

### operations.py

```python id="t1u2v3"
def carre(x):
    return x * x
```

---

### main.py

```python id="w4x5y6"
import operations

nombre = int(input("Nombre : "))

print("Carré :", operations.carre(nombre))
```

---

# 11. Bonnes pratiques

✔ Organiser son code en modules

✔ Donner des noms clairs aux fichiers

✔ Éviter les fichiers trop longs

✔ Réutiliser les fonctions au lieu de dupliquer le code

---

# Résumé

Dans ce chapitre, nous avons appris :

* Les modules Python
* `import`
* `from ... import`
* Les modules intégrés (math, random, datetime)
* Création de modules personnalisés
* Organisation de projet

---


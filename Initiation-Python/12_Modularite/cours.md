# Chapitre 12 : La Modularité en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre le concept de modularité.
* Organiser un projet Python proprement.
* Découper un programme en plusieurs fichiers.
* Appliquer les principes de réutilisation du code.
* Construire des projets structurés et évolutifs.

---

# 1. Qu'est-ce que la modularité ?

La modularité consiste à **diviser un programme en plusieurs parties indépendantes** appelées modules.

## Avantages :

* Code plus lisible
* Code réutilisable
* Facile à maintenir
* Travail en équipe simplifié

---

# 2. Mauvaise approche (tout dans un seul fichier)

```python id="a1b2c3"
def addition(a, b):
    return a + b

def soustraction(a, b):
    return a - b

def multiplication(a, b):
    return a * b

# tout est dans un seul fichier
```

---

# 3. Bonne approche (modularité)

On sépare le code en plusieurs fichiers.

```text id="d4e5f6"
projet/
│
├── main.py
├── calculs.py
├── affichage.py
└── utils.py
```

---

# 4. Exemple de module : calculs.py

```python id="g7h8i9"
def addition(a, b):
    return a + b

def soustraction(a, b):
    return a - b

def multiplication(a, b):
    return a * b
```

---

# 5. Utilisation dans main.py

```python id="j1k2l3"
import calculs

a = 10
b = 5

print(calculs.addition(a, b))
print(calculs.soustraction(a, b))
print(calculs.multiplication(a, b))
```

---

# 6. Séparer les responsabilités

Chaque fichier doit avoir un rôle précis :

| Fichier      | Rôle                     |
| ------------ | ------------------------ |
| main.py      | Point d'entrée           |
| calculs.py   | Opérations mathématiques |
| affichage.py | Affichage des résultats  |
| utils.py     | Fonctions générales      |

---

# 7. Exemple module affichage

```python id="m4n5o6"
def afficher_resultat(valeur):
    print("Résultat :", valeur)
```

---

# 8. Utilisation complète

```python id="p7q8r9"
import calculs
import affichage

resultat = calculs.addition(5, 3)
affichage.afficher_resultat(resultat)
```

---

# 9. Import partiel

```python id="s1t2u3"
from calculs import addition

print(addition(10, 20))
```

---

# 10. Organisation professionnelle d’un projet

```text id="v4w5x6"
mon_projet/
│
├── main.py
├── modules/
│   ├── calculs.py
│   ├── affichage.py
│   └── gestion.py
├── data/
├── tests/
└── README.md
```

---

# 11. Le fichier **init**.py

Permet de transformer un dossier en package Python.

```text id="y7z8a9"
modules/
│
├── __init__.py
├── calculs.py
```

---

# 12. Exemple d’utilisation d’un package

```python id="b1c2d3"
from modules import calculs

print(calculs.addition(2, 3))
```

---

# 13. Bonnes pratiques de modularité

✔ Un fichier = une responsabilité

✔ Éviter les fichiers trop longs

✔ Nommer clairement les modules

✔ Réutiliser les fonctions

✔ Tester chaque module séparément

---

# 14. Exemple de projet complet

### calculs.py

```python id="e4f5g6"
def carre(x):
    return x * x
```

---

### affichage.py

```python id="h7i8j9"
def afficher(valeur):
    print("Valeur :", valeur)
```

---

### main.py

```python id="k1l2m3"
import calculs
import affichage

n = int(input("Nombre : "))

resultat = calculs.carre(n)
affichage.afficher(resultat)
```

---

# 15. Erreurs fréquentes

❌ Tout mettre dans un seul fichier
❌ Noms de modules peu clairs
❌ Code non structuré
❌ Mélanger logique et affichage

---

# Résumé du chapitre

Dans ce chapitre, nous avons appris :

* La modularité
* L’organisation d’un projet Python
* La séparation du code
* Les packages Python
* Les bonnes pratiques de structure

---

# Résultat final du cours

Tu as maintenant terminé :

* Les bases de Python
* Les structures de contrôle
* Les fonctions
* Les collections
* Les fichiers
* Les exceptions
* Les modules
* La modularité

---

# Projet final conseillé

Créer un projet complet :

```text id="n4o5p6"
gestion_etudiants_pro/
```

Fonctionnalités :

* Ajout d’étudiants
* Sauvegarde dans fichier
* Gestion par fonctions
* Organisation en modules
* Interface console

---

# Félicitations 🎉

Tu viens de terminer une formation complète en Python du niveau débutant à structuration avancée.

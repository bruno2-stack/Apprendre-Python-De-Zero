# Chapitre 9 : Les Fichiers en Python

## Objectifs du chapitre

À la fin de ce chapitre, vous serez capable de :

* Comprendre le rôle des fichiers en programmation.
* Lire un fichier texte.
* Écrire dans un fichier texte.
* Ajouter du contenu à un fichier existant.
* Manipuler les fichiers avec Python.
* Créer de petites applications de stockage.

---

# 1. Pourquoi utiliser les fichiers ?

Les fichiers permettent de **stocker des données de manière permanente**.

Contrairement aux variables :

```text id="a1b2c3"
Les variables disparaissent quand le programme s'arrête
```

Les fichiers permettent de sauvegarder :

* Notes
* Utilisateurs
* Données d'application
* Résultats

---

# 2. Ouvrir un fichier

Python utilise la fonction `open()`.

## Syntaxe

```python id="d4e5f6"
open("nom_fichier", "mode")
```

---

# 3. Les modes d'ouverture

| Mode | Description                  |
| ---- | ---------------------------- |
| "r"  | Lecture                      |
| "w"  | Écriture (écrase le fichier) |
| "a"  | Ajout                        |
| "r+" | Lecture + écriture           |

---

# 4. Écrire dans un fichier

## Mode "w"

```python id="g7h8i9"
fichier = open("data.txt", "w")

fichier.write("Bonjour Python")

fichier.close()
```

⚠️ Le mode `"w"` écrase tout le contenu existant.

---

# 5. Ajouter du contenu

## Mode "a"

```python id="j1k2l3"
fichier = open("data.txt", "a")

fichier.write("\nNouvelle ligne")

fichier.close()
```

---

# 6. Lire un fichier

## Mode "r"

```python id="m4n5o6"
fichier = open("data.txt", "r")

contenu = fichier.read()

print(contenu)

fichier.close()
```

---

# 7. Lire ligne par ligne

```python id="p7q8r9"
fichier = open("data.txt", "r")

for ligne in fichier:
    print(ligne)

fichier.close()
```

---

# 8. Bonne pratique : with open()

C’est la méthode recommandée.

```python id="s1t2u3"
with open("data.txt", "r") as fichier:
    contenu = fichier.read()
    print(contenu)
```

✔ Le fichier se ferme automatiquement

---

# 9. Écrire plusieurs lignes

```python id="v4w5x6"
with open("data.txt", "w") as fichier:
    fichier.write("Ligne 1\n")
    fichier.write("Ligne 2\n")
    fichier.write("Ligne 3\n")
```

---

# 10. Exemple complet : journal

```python id="y7z8a9"
with open("journal.txt", "a") as fichier:
    texte = input("Écrivez une note : ")
    fichier.write(texte + "\n")
```

---

# 11. Exemple : lecture d’un journal

```python id="b1c2d3"
with open("journal.txt", "r") as fichier:
    print(fichier.read())
```

---

# 12. Vérifier si un fichier existe

```python id="e4f5g6"
import os

if os.path.exists("data.txt"):
    print("Le fichier existe")
else:
    print("Le fichier n'existe pas")
```

---

# 13. Exemple : compteur dans un fichier

```python id="h7i8j9"
with open("compteur.txt", "r") as fichier:
    valeur = int(fichier.read())

valeur += 1

with open("compteur.txt", "w") as fichier:
    fichier.write(str(valeur))

print("Compteur :", valeur)
```

---

# 14. Exemple complet : enregistrement utilisateur

```python id="k1l2m3"
nom = input("Nom : ")
age = input("Age : ")

with open("utilisateurs.txt", "a") as fichier:
    fichier.write(nom + "," + age + "\n")
```

---

# 15. Lire des données structurées

```python id="n4o5p6"
with open("utilisateurs.txt", "r") as fichier:
    for ligne in fichier:
        nom, age = ligne.strip().split(",")
        print(nom, "-", age)
```

---

# 16. Bonnes pratiques

✔ Toujours fermer les fichiers (ou utiliser `with open()`)

✔ Ne pas écraser un fichier important sans précaution

✔ Structurer les données (CSV simple)

---

# Résumé

Dans ce chapitre, nous avons appris :

* Lire un fichier
* Écrire dans un fichier
* Ajouter du contenu
* Utiliser `with open()`
* Manipuler des données simples
* Vérifier l'existence d'un fichier

---


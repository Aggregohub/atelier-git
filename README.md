# 📘 Guide Git 

Ce document présente les **commandes Git essentielles** à utiliser au quotidien pour travailler efficacement sur nos projets..

-----

## 🧭 Etapes Git recommandé

Voici un exemple simple des étapes à suivre pour éviter les erreurs :

```
      +----------------------------+
      | git checkout ma-branche    | ← Ou vérifier où je me situe avec **git branch**
      +----------------------------+
                    |
                    v
      +------------------+
      |    git pull      | ← Récupère les modifs
      +------------------+
                    |
                    v
===> Je fais mes modifications
                    |
                    v
      +------------------+
      |    git add .     | ← Prépare les modifs
      +------------------+
                    |
                    v
      +-----------------------------+
      | git commit -m "mon message" | ← Sauvegarde locale
      +-----------------------------+
                    |
                    v
      +------------------+
      |    git push      | ← Envoie sur GitHub
      +------------------+
```

-----

## 🚀 Les 4 commandes Git indispensables

### 1\. `git pull`

✅ **Récupère les dernières modifications du dépôt distant (GitHub) vers ta branche locale.**

Utilise cette commande **avant de commencer à travailler**, pour t’assurer que tu travailles bien sur la dernière version à jour. Cela évite les conflits avec le travail des autres.

```bash
git pull
```

### 2\. `git add .`

✅ **Prépare les fichiers modifiés pour le prochain commit.**

Cette commande **ajoute tous les fichiers modifiés à l’index Git** (zone de préparation).

Tu peux aussi ajouter un fichier précis si besoin :

```bash
git add nom_du_fichier.php
```

Mais `git add .` est plus rapide pour tout ajouter d’un coup.

### 3\. `git commit -m "Message explicite"`

✅ **Enregistre un instantané du travail avec un message décrivant ce qui a été fait.**

Un bon message de commit doit **expliquer clairement la modification**.
Exemple :

```bash
git commit -m "Ajout de la section contact sur la page d'accueil"
```

### 4\. `git push`

✅ **Envoie tes commits vers le dépôt distant (GitHub) pour partager ton travail.**

Toujours pousser vers la bonne branche :

```bash
git push
```

-----

⚠️ **Toujours vérifier la branche active**

Avant de commencer à travailler, assure-toi d’être sur la bonne branche :

```bash
git branch
```

La branche active est marquée par une étoile `*`.
Par exemple : `* feature/ajout-carousel`

Changer de branche si besoin :

```bash
git checkout nom_de_branche
```

Travailler sur la mauvaise branche peut écraser ou perturber le travail des autres.

-----

## 🔧 Autres commandes utiles

  * **Voir les fichiers modifiés en attente :**
    ```bash
    git status
    ```
  * **Voir les différences dans le code :**
    ```bash
    git diff
    ```
  * **Créer une nouvelle branche :**
    ```bash
    git checkout -b nom_de_branche
    ```
  * **Revenir à une version précédente d’un fichier :**
    ```bash
    git restore nom_du_fichier
    ```
  <!-- * **Fusionner une autre branche dans la tienne :**
    ```bash
    git merge nom_de_branche
    ``` -->
   ---

## 🔧 Commandes Git pour gérer le stash (sauvegarde temporaire)

* **Sauvegarder temporairement ses modifications en cours (stash)**
  Cette commande met de côté toutes tes modifications locales (non commitées) pour nettoyer ton espace de travail,
  par exemple si tu veux essayer plusieurs manière de coder ou changer rapidement de branche sans perdre ton travail en cours.
  ```bash
  git stash
  ```
* **Lister les sauvegardes temporaires existantes**
  Affiche la liste des stashes que tu as mis de côté, avec un identifiant (stash@{0}, stash@{1}, etc.).
  Utile si tu veux choisir lequel récupérer.
  ```bash
  git stash list
  ```
* **Récupérer et appliquer la dernière sauvegarde stash, puis la supprimer de la liste**
  Cette commande remet tes modifications dans ton espace de travail, comme si tu n’avais jamais stashé.
  Attention : elle supprime la sauvegarde du stash après application.
  ```bash
  git stash pop
  ```
* **(Bonus) Récupérer une sauvegarde stash sans la supprimer**
  Utile si tu veux réappliquer plusieurs fois la même sauvegarde.
  ```bash
  git stash apply stash@{0}
  ```
* **(Bonus) Supprimer une sauvegarde stash spécifique**
  Pour faire un ménage dans tes stashes.
  ```bash
  git stash drop stash@{0}
  ```
-----

## ✅ Bonnes pratiques

  * **🔁 Toujours faire un `git pull` avant de commencer.**
  * **✏️ Faire des commits petits et clairs.**
  * **🧪 Tester avant de faire un `push`.**
  * **🚫 Ne pas travailler directement sur `main` ou `master` sans raison valable.**
  * **👀 Toujours vérifier la branche active avec `git branch`.**




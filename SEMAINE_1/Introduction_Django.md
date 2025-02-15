
# Introduction à Django

## Installation de Python et Django

1. **Installer Python**:
    - Téléchargez et installez Python depuis [python.org](https://www.python.org/downloads/).
    - Assurez-vous que Python est ajouté à votre PATH.

2. **Installer Django**:
    - Ouvrez un terminal et exécutez la commande suivante pour installer Django :
    ```bash
    pip install django
    ```

## Création d'un projet Django

1. **Créer un nouveau projet**:
    - Dans le terminal, naviguez vers le répertoire où vous souhaitez créer votre projet,
    - Exécutez la commande suivante pour créer un nouveau projet Django nommé `blog` :
    ```bash
    django-admin startproject blog .
    ```

2. **Démarrer le serveur de développement**:
    - Exécutez la commande suivante pour créer les migrations :
    ```bash
    python manage.py makemigrations
    ```
    - Exécutez la commande suivante pour exécuter ces migrations :
    ```bash
    python manage.py migrate
    ```
    - Exécutez la commande suivante pour démarrer le serveur de développement :
    ```bash
    python manage.py runserver
    ```
    - Ouvrez votre navigateur et accédez à `http://127.0.0.1:8000/` pour voir votre projet en cours d'exécution.

## Structure d'un projet Django

Voici la structure de base d'un projet Django nommé `blog` :

```
manage.py
blog/
    __init__.py
    settings.py
    urls.py
    wsgi.py
```

- `manage.py` : Un script qui vous permet d'interagir avec votre projet Django de différentes manières.
- `blog/` : Le répertoire contenant les fichiers de configuration de votre projet.
    - `__init__.py` : Un fichier vide qui indique à Python que ce répertoire doit être considéré comme un package Python.
    - `settings.py` : Le fichier de configuration de votre projet Django.
    - `urls.py` : Le fichier de définition des URL pour votre projet Django.
    - `wsgi.py` : Un fichier pour déployer votre projet sur un serveur web.

## ⚠️ **A savoir** 

- `makemigrations` : 
    - `Rôle` : Cette commande génère des fichiers de migration qui décrivent les modifications apportées au modèle (comme l'ajout ou la suppression de champs dans une table, la modification de types de données, etc.).
    - `Pourquoi c'est important` :
        - `Enregistrement des changements` : Elle permet de capturer les modifications des modèles dans des fichiers de migration, qui sont ensuite utilisés pour synchroniser la base de données avec les nouveaux modèles.
        - `Suivi des modifications` : Elle facilite le suivi des modifications de la base de données au fil du temps, en créant des versions de migrations à appliquer au fur et à mesure du développement.

- `migrate`
    - `Rôle` : Après avoir créé des fichiers de migration avec makemigrations, vous utilisez migrate pour appliquer ces migrations à la base de données réelle. Cela permet de mettre à jour la base de données en fonction des modifications effectuées sur les modèles.
    - `Pourquoi c'est important` :
        - `Synchronisation avec la base de données` : Elle met à jour la structure de la base de données en fonction des changements de vos modèles.
        - `Applications des migrations` : Cette commande permet d'appliquer toutes les migrations en attente et garantit que votre base de données est à jour par rapport aux modèles définis dans votre projet Django.

- `runserver`
    - `Rôle` : Cette commande lance le serveur de développement intégré de Django, permettant de tester et d'interagir avec l'application en local via un navigateur web.
    - `Pourquoi c'est important` :
Test local : Elle permet de tester votre application dans un environnement local avant de la déployer en production.
Développement continu : Elle redémarre automatiquement le serveur à chaque modification du code source, ce qui facilite un développement rapide et dynamique.
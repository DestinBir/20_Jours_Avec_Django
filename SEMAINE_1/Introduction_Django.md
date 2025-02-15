
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
blog/
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


# Guide pratique pour le développement d'API Rest avec FastAPI et Python

A l'intention des étudiants en Bachelor IT de [Collège de Paris Togo](https://togo.collegedeparis.fr/).

## Introduction

Ce guide vous accompagnera dans la création d'API Rest fonctionnelles et performantes en utilisant le framework FastAPI et le langage Python.

## Prérequis

- Python 3.7 ou version ultérieure.
- Pip.

## Installation de FastAPI

Commençons par installer FastAPI :

`pip install fastapi`

`pip install uvicorn`

## Structure du projet

Un projet FastAPI typique peut est structuré comme suit :

project_root/
├── docs                        # Documentation de l'API
├── models                      # Modèles de données
├── tests                       # Tests unitaires
├── main.py                     # Point d'entrée de l'application
└── requirements.txt            # Dépendances du projet

## Créer une API simple avec FastAPI

Créez un fichier `main.py` et ajoutez le code suivant :

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def hello_world():
    return {"message": "Hello, World!"}

```

Exécutez le code suivant pour lancer le serveur :

`uvicorn main:app --reload --port=8000`

Votre API est maintenant accessible sur le [http://localhost:8000/](http://localhost:8000/) et sa documentation sur le [http://localhost:8000/docs](http://localhost:8000/docs).


NB : La commande `uvicorn main:app --reload --port=8000` se divise en 4 parties :

* `main`: le fichier `main.py` (le "module" Python à exécuter).
* `app`: l'objet principal créé dans le fichier `main.py` avec la ligne `app = FastAPI()`.
* `--reload`: redémarre le serveur en cas de modification ; utile en mode développement.
* `--port=8000`: Indique le port sur lequel le processus sera exécuté.

## Aller plus loin

* Documentation de FastAPI : [FastAPI (tiangolo.com)](https://fastapi.tiangolo.com/)
* Tutoriels pas à pas, code à l'appui : [ChristopherGS/ultimate-fastapi-tutorial: The Ultimate FastAPI Tutorial (github.com)](https://github.com/ChristopherGS/ultimate-fastapi-tutorial)
* Liste d'outils et de contenus liés à FastAPI : [mjhea0/awesome-fastapi: A curated list of awesome things related to FastAPI (github.com)](https://github.com/mjhea0/awesome-fastapi)
* Meilleurs pratiques dans le développement d'API avec FastAPI : [zhanymkanov/fastapi-best-practices: FastAPI Best Practices and Conventions we used at our startup (github.com)](https://github.com/zhanymkanov/fastapi-best-practices)

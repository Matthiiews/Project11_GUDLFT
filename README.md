# GUDLFT-registration Projet 11 DA-Python Openclassromms

[![forthebadge](https://forthebadge.com/images/badges/cc-0.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)

***Livrable du Projet 11 du parcours D-A Python d'OpenClassrooms***

Plateforme de réservation de places à des compétitions de force pour l'entreprise Güdlft.

L'objectif du projet est de corriger les erreurs et bugs présents dans le projet
[Python_Testing](https://github.com/OpenClassrooms-Student-Center/Python_Testing),
ainsi que d'implémenter de nouvelles fonctionnalités. Chaque correction / ajout se trouve sur sa propre branche,
et est supporté(e) par une suite de tests via Pytest et Locust.

_Windows 10 - Python 3.11.2 - Flask 3.0.2_

## Initialisation du projet

### Windows :

```
git clone https://github.com/Matthiiews/Project11_GUDLFT.git

cd Project11_GUDLFT
python -m venv env 
env\Scripts\activate

pip install -r requirements.txt
```

### MacOS et Linux :

```
git clone https://github.com/Matthiiews/Project11_GUDLFT.git

cd Project11_GUDLFT 
python3 -m venv env 
source env/bin/activate

pip install -r requirements.txt
```

## Utilisation

1. Lancer le serveur Flask :

```
$env:FLASK_APP = "server.py"
flask run
```

2. Pour accéder au site, se rendre sur l'adresse par défaut : [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

## Tests

- **Note : Tous les packages nécessaires à l'exécution de ces tests sont inclus dans 'requirements.txt'.**

### Tests unitaires / tests d'intégration

Les tests unitaires et d'intégration sont exécutés grâce à [Pytest](https://docs.pytest.org/en/8.0.0/index.html) (version 8.0.0).

Pour effectuer l'ensemble des tests unitaires et d'intégration, entrer la commande :

```
pytest tests
```
Le module [Coverage](https://coverage.readthedocs.io/en/7.4.1/) (version 7.4.1) est utilisé pour le rapport de couverture des tests.
Il s'exécute via la commande :
```
coverage run -m pytest tests
coverage report
```

### Test de performances

Il est possible d'effectuer un test de performance grâce au module [Locust](https://locust.io) (version 2.23.1).
Pour lancer le serveur de test, entrer la commande :

```
locust tests/performance_tests/locustfile.py 
```

Se rendre sur l'adresse [http://localhost:8089](http://localhost:8089) et entrer les options souhaitées, avec pour 'host' l'adresse par défaut du site (http://127.0.0.1:5000/).

### Rapports

Les captures d'écran des derniers rapports de tests sont disponibles dans le dossier 'reports'.

- [Rapport pytest](reports/pytest.PNG) (tous les tests réussis)

- [Rapport de couverture](reports/coverage_report.PNG) (100% de couverture)

- [Rapport de performances locust](reports/locust.PNG) (8 utilisateurs, 1 par seconde)

## Installation et utilisation d'un environnement virtuel Python

### Installation de `python3-venv`
```sh
sudo apt install python3-venv
```

### Création d'un environnement virtuel
Créer un environnement virtuel avec la commande :
```sh
python3 -m venv .venv
```

### Activation de l'environnement virtuel
Activer l'environnement virtuel :
```sh
source .venv/bin/activate
```
modifie la variable d'environnement `PATH` pour inclure `.venv/bin/`.

### Installation de packages avec `pip`
Une fois l'environnement activé, installer des packages depuis PyPI avec :
```sh
pip install requests
```

### Utilisation sans activation de l'environnement virtuel
Si on ne souhaite pas activer/désactiver l'environnement virtuel à chaque fois, exécuter `pip` et `python` directement depuis `.venv/` :
```sh
.venv/bin/pip install requests
.venv/bin/python
```
Puis, dans l'interpréteur Python :
```python
>>> import requests

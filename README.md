# 4ETI-ADMCODE-202520226-TP1

# TP : Créer le paquet Python `calculator`

## Objectif

En respectant au maximum les bonnes pratiques modernes de développement Python, créer un **paquet Python** `calculator` qui expose une classe `SimpleCalculator` implémentant les opérations testées ci-dessous.

Les tests fournis doivent passer **sans modification**.

## Structure de projet attendue

```
calculator-project/
├─ pyproject.toml
├─LICENCE
├─ src/
│  └─ calculator/
│     ├─ __init__.py
│     └─ simple_calculator.py  # ou calculator.py selon ton choix
└─ tests/
   └─ test_simple_calculator.py
```


**Contraintes** :
- Paquet installable nommé `calculator`
- Import dans les tests : `from calculator import SimpleCalculator`

# SimpleCalculator

Implémentation d'une classe `SimpleCalculator` fournissant des opérations arithmétiques de base avec validation stricte des types.

---

## Spécification

### Instanciation

La classe est instanciable sans argument :

```python
calc = SimpleCalculator()
```

---

## Méthodes publiques

```python
fsum(a: int, b: int) -> int
substract(a: int, b: int) -> int
multiply(a: int, b: int) -> int
divide(a: int, b: int) -> float
```

---

## Règles communes

### Types acceptés

- `int`
- `float`
Par  exemple :
- `str` → `TypeError`
- `None` → `TypeError`

Les arguments doivent être strictement des entiers (ou booléens).

---

## Détails par méthode

### `fsum(a, b) -> int`

Addition de deux entiers.

- Retourne un `int`

---

### `substract(a, b) -> int`

Soustraction de deux entiers.

- Retourne un `int`

---

### `multiply(a, b) -> int`

Multiplication de deux entiers.

- Retourne un `int`

---

### `divide(a, b) -> float`

Division de deux entiers.

- Retourne toujours un `float`

#### Cas particuliers :

- `0 / n` → `0.0`
- `n / 0` → `ZeroDivisionError`
- Types invalides → `TypeError`



## Contraintes de style

- Annotations de type obligatoires
- Docstring pour la classe
- Docstrings pour toutes les méthodes
- Séparation claire du projet :





## `pyproject.toml` mon choix perso
```toml
[project]
name = "TestSimpleCalculator_2026_FJ"
version = "0.0.1"
authors = [{name = "Fabrice Jumel"}]
description = "Simple calculator for packaging demo"
license = {text = "Unlicense"}
requires-python = ">=3.10"

[project.optional-dependencies]
test = ["pytest>=7.0", "pytest-cov", "pylint", "black", "radon"]

[tool.setuptools.packages.find]
where = ["src"]

[tool.pytest.ini_options]
testpaths = ["tests"]
pythonpath = ["src"]
```

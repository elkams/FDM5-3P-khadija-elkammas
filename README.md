# FDM5-3P-khadija-elkammas
# FD M5 – Python pour la Physique : notebooks complétés

**Étudiante :** Khadija EL KAMMAS — Doctorante (Formation Doctorale, module M5)
**Enseignant :** Pr. Abderrahman EL KHARRIM
**Dépôt du cours :** [aelkharrim/FDM5-3P](https://github.com/aelkharrim/FDM5-3P)

Ce dépôt contient les notebooks du cours, avec **tous les blocs `# Votre code ici` complétés**.
Chaque notebook a été exécuté entièrement (*Tout exécuter*) : les résultats et les figures sont visibles directement sur GitHub.

---

## Contenu

| Notebook | Thème | Exercices complétés | Ouvrir dans Colab |
|---|---|:---:|---|
| `00_environnement.ipynb` | Installation de Python, venv, Jupyter, Colab | — (aucun exercice) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/00_environnement.ipynb) |
| `01_python_bases.ipynb` | Types de base, conteneurs, affectation | 1 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/01_python_bases.ipynb) |
| `02_python_structures_fonctions.ipynb` | Structures de contrôle, fonctions, modules, exceptions | 4 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/02_python_structures_fonctions.ipynb) |
| `03_numpy.ipynb` | Tableaux NumPy, indexation, broadcasting, tri | 14 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/03_numpy.ipynb) |
| `04_matplotlib.ipynb` | Graphiques 2D/3D, sous-graphiques | 2 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/04_matplotlib.ipynb) |
| `05_scipy.ipynb` | Fonctions spéciales, ajustement, optimisation, EDO, FFT | 8 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/05_scipy.ipynb) |
| `06_sympy.ipynb` | Calcul symbolique, équations, EDO, `lambdify` | 6 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/06_sympy.ipynb) |
| `07_pandas.ipynb` | DataFrame, `groupby`, CSV, ajustement | 2 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/07_pandas.ipynb) |
| `08_incertitudes.ipynb` | Incertitudes de type A/B, propagation, χ² | 4 | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/08_incertitudes.ipynb) |
| `sample.ipynb` | Exemple : script d'analyse statistique (`%%writefile`, `%run`) | — (aucun exercice) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elkams/FDM5-3P-khadija-elkammas/blob/main/sample.ipynb) |
| | | **Total : 41** | |

---

## Exercices réalisés (résumé)

- **01 – Bases :** durée de chute libre $t = \sqrt{2h/g}$.
- **02 – Structures et fonctions :** π par la formule de Wallis, suite de Fibonacci, tri rapide (*Quicksort*), fonction `vitesse()` avec levée et capture d'une `ValueError`.
- **03 – NumPy :** création de tableaux (`arange`, `linspace`, `diag`, `tile`…), découpage et indexation avancée, crible d'Ératosthène, opérations et `%timeit`, réductions et fonction `mon_std`, vues/copies (`ravel`/`flatten`), tri, trajectoire d'un projectile, statistiques sur la période d'un pendule.
- **04 – Matplotlib :** oscillation amortie avec enveloppe, trajectoires et portée d'un projectile (2 sous-graphiques).
- **05 – SciPy :** polynômes de Legendre, ajustement des températures en Alaska, minimum du potentiel de Lennard-Jones, test *t* de Student, moment d'inertie (`quad`), chute avec frottements (`solve_ivp`), repliement de spectre, synthèse oscillateur amorti (ajustement + TFD + résidus).
- **06 – SymPy :** √2 à 100 décimales, développements et simplifications, limites et dérivées, système d'équations et logique booléenne, équation de Bernoulli, portée d'un projectile (symbolique → `lambdify`).
- **07 – Pandas :** statistiques par groupe (`groupby`), loi d'Ohm (ajustement $U = RI$ par résistance).
- **08 – Incertitudes :** incertitude de type A et coefficient de Student, propagation (SymPy et Monte-Carlo), effet d'une incertitude sous-estimée sur le χ² réduit, célérité du son (ajustement, χ² réduit, écart normalisé).

---

## Cellules « Erreur volontaire » : corrigées

Les cellules qui produisaient une erreur volontaire (pour illustrer les messages d'erreur) ont été **corrigées**.
Dans chacune, **la ligne d'origine est conservée en commentaire** avec le message d'erreur produit, suivie d'un commentaire `# CORRIGÉ :` qui explique la cause et la correction.

| Notebook | Ligne d'origine | Erreur | Correction |
|---|---|---|---|
| 01 | `a[2] = 'z'` | `TypeError` (chaîne immuable) | nouvelle chaîne `a[:2] + 'z' + a[3:]` |
| 02 | `double()` | `TypeError` (argument manquant) | `double(5)` |
| 02 | `1/0` | `ZeroDivisionError` | `try / except ZeroDivisionError` |
| 02 | `1 + 'e'` | `TypeError` (int + str) | `str(1) + 'e'` |
| 02 | `d[3]` | `KeyError` | `d.get(3, ...)` |
| 02 | `l[4]` | `IndexError` | indice valide `l[-1]` |
| 02 | `l.foobar` | `AttributeError` | méthodes existantes (`dir(l)`, `l.count`) |
| 02 | `int('a')` + `finally` | `ValueError` | ajout de `except ValueError` |
| 02 | `filtre_nom('Stéfan')` | `UnicodeEncodeError` | `try / except UnicodeError` |
| 03 | `a + np.array([1, 2])` | `ValueError` (broadcasting) | tableau de même forme `[1, 2, 1, 2]` |
| 03 | `b = a; a.resize((4,))` | `ValueError` (tableau référencé) | `np.resize(a, (4,))` |

**Compatibilité Colab :** dans `07_pandas.ipynb`, la ligne `refroid['residu'].std().round(3)` provoque une `AttributeError` avec la version récente de pandas sur Colab (`.std()` renvoie un `float` Python). Elle a été remplacée par `round(refroid['residu'].std(), 3)`, la ligne d'origine étant conservée en commentaire.

À part les blocs `# Votre code ici` et ces corrections signalées, **le contenu des notebooks du cours n'a pas été modifié**.

---

## Exécution

Tous les notebooks s'exécutent de bout en bout **sans erreur** (*Exécution → Tout exécuter*) sur Google Colab, où NumPy, SciPy, Matplotlib, SymPy et pandas sont préinstallés. Ils peuvent aussi être exécutés en local dans un environnement virtuel :

```bash
python -m venv .venv
source .venv/bin/activate          # Windows : .\.venv\Scripts\Activate.ps1
pip install numpy scipy matplotlib sympy pandas jupyterlab
jupyter lab
```

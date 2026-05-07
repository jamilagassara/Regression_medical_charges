# 🏥 Prédiction des Charges Médicales  
### Projet Machine Learning — Régression  

---

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-FF9F00?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)

---

## 📑 Table des matières

- [Présentation du projet](#présentation-du-projet)
- [Objectif](#objectif)
- [Dataset](#dataset)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Méthodologie](#méthodologie)
- [Résultats](#résultats)
- [Conclusion](#conclusion)
- [Technologies](#technologies)
- [Auteur](#auteur)

---

## 📌 Présentation du projet

Ce projet a été réalisé dans le cadre du module **Machine Learning / Régression**.

Il consiste à analyser et modéliser un dataset de **charges médicales individuelles aux États-Unis** en suivant une démarche complète de Data Science :

> **Analyse exploratoire → Prétraitement → Modélisation → Évaluation → Sélection de variables**

---

## 🎯 Objectif

L’objectif principal est de :

> 💡 **Prédire le montant des charges médicales (`charges`)** en fonction des caractéristiques d’un individu.

Variables utilisées :
- Âge
- Sexe
- IMC (BMI)
- Nombre d’enfants
- Statut fumeur
- Région

---

## 📊 Dataset

- **Fichier** : `medical-charges.csv`  
- **Nombre d’observations** : ~1338  
- **Variables** : 7 (6 features + 1 cible)

| Variable | Description |
|----------|------------|
| age | Âge |
| sex | Sexe |
| bmi | Indice de masse corporelle |
| children | Nombre d’enfants |
| smoker | Statut fumeur |
| region | Région |
| charges | Charges médicales (variable cible) |

---

## ⚙️ Installation

### Prérequis
- Python 3.8+
- Jupyter Notebook

### Installation des dépendances

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels jupyter
```

---

## ▶️ Utilisation

1. Cloner le dépôt :

```bash
git clone https://github.com/jamilagassara/Regression_medical_charges.git
```

2. Accéder au dossier :

```bash
cd medical-charges-ml
```

3. Lancer Jupyter Notebook :

```bash
jupyter notebook
```

4. Ouvrir le fichier :

```
Medical_charges_projet_DS_ML.ipynb
```

---

## 🔬 Méthodologie

### 1. Analyse Exploratoire (EDA)
- Inspection des données (`info`, `describe`)
- Analyse des distributions (histogrammes, boxplots)
- Analyse des relations avec la variable cible
- Matrice de corrélation
- Détection des outliers (méthode IQR)

---

### 2. Prétraitement des données
- Vérification des valeurs manquantes → aucune détectée
- Suppression des doublons
- Encodage :
  - Label Encoding (variables binaires)
  - One-Hot Encoding (région)
- Normalisation des variables (StandardScaler)
- Séparation des données (80% entraînement / 20% test)

---

### 3. Modélisation

Modèles utilisés :
- Régression Linéaire
- Ridge Regression (L2)
- Lasso Regression (L1)
- ElasticNet (L1 + L2)

Optimisation des hyperparamètres via validation croisée.

---

### 4. Évaluation

Métriques utilisées :
- RMSE
- MAE
- R²
- R² ajusté

Analyses complémentaires :
- Étude des résidus
- Comparaison valeurs réelles vs prédites

---

### 5. Sélection de variables

Méthodes appliquées :
- Backward Elimination (p-values)
- Analyse des coefficients Lasso
- RFE (optionnel)

Objectif :
> Simplifier le modèle tout en conservant de bonnes performances

---

## 📈 Résultats

- Le statut **fumeur** est la variable la plus influente
- L’IMC et l’âge ont un impact significatif
- Les modèles régularisés améliorent la stabilité
- La sélection de variables réduit la complexité sans perte majeure

---

## 🧠 Conclusion

Ce projet a permis de :

✔️ Construire une pipeline complète de Machine Learning  
✔️ Comparer plusieurs modèles de régression  
✔️ Identifier les variables les plus importantes  

### 🔍 Limites
- Dataset relativement petit
- Hypothèse de linéarité

### 🚀 Perspectives
- Modèles non linéaires (Random Forest, XGBoost)
- Feature Engineering (interactions, transformations)
- Ajout de nouvelles données

---

## 🛠️ Technologies

- Python
- Jupyter Notebook
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- statsmodels

---

## 👩‍💻 Auteur

**Jamila Gassara**

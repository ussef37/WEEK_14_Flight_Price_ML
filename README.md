# ✈️ Prédiction du prix des billets d’avion

## 📌 Présentation du projet

Le tarif d’un billet d’avion varie selon plusieurs critères, notamment la compagnie aérienne, le nombre d’escales, la durée du trajet ainsi que le délai entre la réservation et le départ.

Dans ce projet, l’objectif est de développer un modèle de régression capable d’estimer le prix d’un billet à partir des caractéristiques disponibles dans les données.

Le jeu de données utilisé contient plus de **300 000 enregistrements de vols**, offrant une base solide pour analyser les comportements tarifaires et construire un modèle prédictif pertinent.

L’objectif final est d’obtenir des prédictions fiables avec une **erreur moyenne inférieure à 15 €**.

---

## 🎯 Objectifs

Les principales étapes du projet sont :

- explorer les données pour mieux comprendre leur structure ;
- identifier les variables qui influencent le prix des billets ;
- vérifier statistiquement certaines hypothèses observées dans l’analyse ;
- préparer les données pour l’apprentissage automatique ;
- comparer plusieurs algorithmes de régression ;
- retenir le modèle offrant les meilleures performances.

---

## 📊 Démarche du projet

### 1. Importation et exploration initiale

La première étape consiste à charger les bibliothèques nécessaires, importer le dataset et examiner sa structure générale afin de vérifier les dimensions, les types de variables et la cohérence des données.

---

### 2. Étude des variables

Une analyse est réalisée pour distinguer les variables numériques des variables catégorielles et repérer les traitements nécessaires avant la modélisation.

Cette étape permet de mieux comprendre la nature des informations disponibles et de préparer les transformations adaptées.

---

### 3. Analyse descriptive

Une analyse univariée est effectuée afin d’étudier chaque variable séparément :

- les variables catégorielles sont examinées à travers leur répartition ;
- les variables numériques sont étudiées à l’aide de statistiques descriptives et de visualisations.

Cette phase aide à détecter les déséquilibres, les valeurs atypiques et les tendances générales.

---

### 4. Analyse des relations avec le prix

Une analyse multivariée permet d’évaluer l’impact de plusieurs facteurs sur le prix des billets :

- durée du vol ;
- compagnie aérienne ;
- nombre d’escales ;
- nombre de jours avant le départ.

Des visualisations comparatives sont utilisées pour mettre en évidence les relations entre ces variables et la variable cible.

---

### 5. Validation statistique

Les observations issues de l’analyse exploratoire sont confirmées grâce à des tests statistiques adaptés :

- tests de comparaison de moyennes ;
- analyse de variance ;
- corrélations ;
- tests d’indépendance.

Ces tests permettent de déterminer si les relations observées sont statistiquement significatives.

---

### 6. Préparation des données

Avant l’entraînement des modèles, plusieurs transformations sont appliquées :

- traitement des valeurs manquantes ;
- encodage des variables catégorielles ;
- normalisation des variables numériques ;
- intégration des étapes dans une pipeline.

Cette préparation garantit un traitement cohérent des données tout au long du processus.

---

### 7. Entraînement des modèles

Plusieurs modèles de régression sont testés afin d’identifier la meilleure approche :

- un modèle de référence simple ;
- une régression linéaire ;
- une régression Ridge ;
- une forêt aléatoire.

Les modèles sont évalués à l’aide de métriques telles que **MAE**, **RMSE** et **R²**, avec validation croisée.

---

### 8. Sélection du modèle final

Le modèle le plus performant est ensuite entraîné sur les données d’apprentissage complètes puis évalué sur un ensemble de test afin de mesurer sa capacité de généralisation.

---

### 9. Estimation de l’incertitude

Une estimation de l’incertitude est réalisée autour de l’erreur moyenne afin de calculer un intervalle de confiance à 95 %.

Cette étape permet de mieux interpréter la stabilité des performances obtenues.

---

### 10. Sauvegarde du modèle

Enfin, le pipeline complet contenant le prétraitement et le modèle final est sauvegardé pour être réutilisé sur de nouvelles données.

Cette sauvegarde facilite l’intégration future du modèle dans un environnement de production.

---

## 🚀 Résultat attendu

Le projet vise à produire un modèle capable d’estimer le prix d’un billet d’avion de manière fiable, avec une erreur moyenne faible et une bonne robustesse sur des données inédites.

L’objectif est d’obtenir un outil prédictif exploitable dans un contexte réel d’aide à la tarification ou à la recommandation.
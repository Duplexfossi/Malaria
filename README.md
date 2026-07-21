# 🦟 Malaria Vector Control Strategy & Geospatial Targeting
---

## 📌 Présentation du Projet

Dans les régions tropicales, la transmission du paludisme présente une grande hétérogénéité spatiale influencée par des variables environnementales (altitude, précipitations, température, humidité) et climatiques. Face à des budgets de santé publique limités, les campagnes de prévention massives manquent souvent de ciblage géographique précis.

**Objectif principal :** Identifier les moteurs environnementaux clés de la densité parasitaire et déterminer des seuils d'altitude prédictifs pour guider le déploiement ciblé des interventions antivectorielles (Moustiquaires Imprégnées d'Insecticide à Longue Durée - MILD, et Pulvérisation Intradomiciliaire d'Insecticide - PID).

---

## 🔬 Méthodologie & Approche Statistique

La modélisation s'appuie sur une démarche rigoureuse d'analyse de données d'observation et de sélection de modèles :

1. **Diagnostic & Prétraitement des Données :**
   * Évaluation de la distribution de la densité parasitaire et identification de la non-normalité des résidus.
   * Vérification des hypothèses classiques du modèle linéaire classique (**Gauss-Markov**).
   * Prise en compte de la structure spatiale et des gradients d'altitude.

2. **Sélection de Modèle & Optimisation :**
   * Formulation de Modèles Linéaires Généralisés (GLM) adaptables aux structures de données de santé publique.
   * Utilisation du **critère d'information d'Akaike (AIC)** et du **BIC** pour la sélection de variables et l'arbitrage entre parcimonie et qualité d'ajustement.
   * Détermination de seuils d'altitude critiques au-delà desquels la pression de transmission chute significativement.

---

## 🛠️ Stack Technique & Bibliothèques

* **Langage :** Python
* **Analyse Statistique & Modélisation :** `statsmodels`, `scipy`
* **Manipulation de Données :** `pandas`, `numpy`
* **Visualisation & Cartographie :** `matplotlib`, `seaborn`
* **Environnement de Travail :** Jupyter Notebook / VS Code

---

## 📊 Résultats Clés & Impact Décisionnel

* **Facteurs Déterminants :** L'altitude et la température moyenne de la saison des pluies sont ressorties comme les prédicteurs les plus significatifs ($p < 0.05$) de la densité parasitaire.
* **Ciblage Stratégique :** L'analyse a permis de définir une note stratégique recommandant une priorisation des interventions dans les zones situées sous le seuil critique identifié, optimisant ainsi l'impact sanitaire par franc investi.



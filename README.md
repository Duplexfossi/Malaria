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

### 📈 Constat Statistique (Modélisation GLM/MCO)
* **Échantillon & Validation :** Analyse menée sur **237 observations complètes**. Les hypothèses de Gauss-Markov ont été validées (résidus normaux via Shapiro-Wilk, homoscédasticité), garantissant la fiabilité des estimations.
* **Sélection de variables par AIC :** Réduction d'un modèle complexe à 6 variables (incluant température, humidité, précipitations et biodiversité aviaire) vers un **modèle parcimonieux à 2 déterminants robustes** :
  * ⛰️ **Altitude du lieu de résidence**
  * 💧 **Distance au point d'eau stagnante le plus proche**
* **Pouvoir Prédictif :** Ces 2 variables expliquent à elles seules **88,2 % de la variance** de la densité parasitaire (R^2 = 0,882), éliminant la multicolinéarité sans perte de précision prédictive.

---

### 💡 Recommandations Opérationnelles (Santé Publique)
1. **Ciblage géographique simplifié :** Prioriser l'allocation des **MILDA** et les campagnes de **pulvérisation intra-domiciliaire** dans les zones cumulant *basse altitude* et *proximité immédiate des points d'eau stagnante*.
2. **Optimisation des coûts :** Exploiter les Modèles Numériques de Terrain (MNT) existants pour la cartographie au lieu d'investir dans des stations météo locales coûteuses (l'apport de la température/humidité étant redondant une fois l'altitude prise en compte).
3. **Assainissement ciblé :** Concentrer les actions anti-larvaires (drainage, larvicides) prioritairement sur les points d'eau en zones de basse altitude.

---




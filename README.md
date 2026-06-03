## 🎯 Purpose of This Analysis

- Understand **multicollinearity** between features before building regression models
- Identify **redundant variables** (e.g., Fat & Fat Uptake are perfectly correlated)
- Guide **feature selection** for future predictive modeling
- Visualize data relationships in an intuitive, easy-to-interpret format

## 📌 Project Overview

This project explores the **statistical relationships** between various physical and chemical properties of food products using a **Correlation Heatmap** built in Python (Google Colab). The goal is to identify which variables are strongly or weakly correlated with each other, which is a key step in **data analysis and feature selection** for machine learning models.

---

## 📂 Dataset Description

The dataset contains **8 numerical variables** related to food science measurements:

| Column | Description |
|--------|-------------|
| **Moisture** | Water content percentage in the food sample |
| **Fat** | Fat content percentage |
| **TBARS** | Thiobarbituric Acid Reactive Substances — measures lipid oxidation/rancidity |
| **Texture** | Mechanical texture value of the food sample |
| **Fat Uptake** | Amount of fat absorbed during processing |
| **Batter Viscosity** | Viscosity (thickness) of the batter |
| **Oleogel Viscosity** | Viscosity of the oleogel used in the product |
| **Canola Oil Viscosity** | Viscosity of canola oil component |

---

## 🛠️ Tools & Libraries Used

- **Python 3** (Google Colab)
- **Pandas** — data loading and manipulation
- **Seaborn** — heatmap visualization
- **Matplotlib** — figure customization

---

## 🖼️ Heatmap Preview

<img width="993" height="768" alt="Screenshot 2026-06-04 003156" src="https://github.com/user-attachments/assets/8ce5f343-7d9f-4421-a2dc-39cbb6a6d5ec" />


> *Color scale: Deep Blue = Strong Positive | White = No Correlation | (negative values shown as light blue)*

## 📊 Key Findings from the Heatmap

### ✅ Strong Positive Correlations (darker blue):
- **Moisture ↔ Batter Viscosity** → `0.78` — Higher moisture leads to higher batter viscosity
- **Moisture ↔ Oleogel Viscosity** → `0.85` — Strong relationship between moisture and oleogel thickness
- **Batter Viscosity ↔ Oleogel Viscosity** → `0.93` — These two are very strongly linked

### ❌ Strong Negative Correlations (lighter/white):
- **Fat ↔ Texture** → `-0.72` — Higher fat content reduces texture hardness
- **Fat Uptake ↔ Texture** → `-0.72` — More fat uptake = softer texture
- **Fat ↔ Fat Uptake** → `1.0` — These are perfectly correlated (same measure)

### ➡️ Weak/No Correlations (near 0):
- **TBARS ↔ Batter Viscosity** → `-0.022` — Oxidation level has no effect on viscosity
- **TBARS ↔ Oleogel Viscosity** → `-0.058` — Similarly no meaningful relationship

---








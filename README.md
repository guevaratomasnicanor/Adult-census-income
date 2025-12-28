# 🧠 Adult Income Analysis

El objetivo del proyecto es **predecir si una persona gana más de 50 000 USD anuales** a partir de características demográficas, laborales y educativas.

---

## 📊 Dataset

El dataset proviene del clásico **Adult Census Income Dataset (UCI Machine Learning Repository)**.  
Un censo de Estados Unidos en 1994 sobre más de 48 000 individuos y 16 variables.

**Variables principales:**
- `income` → variable objetivo (`>50K` o `<=50K`)
- `age`
- `education_num`
- `hours_per_week`
- `capital_gain`
- `capital_loss`
- `race`
- `sex`
- `occupation`
- `workclass`
- `marital_status`
- `relationship`
- `native_country`

---

## 🔍 Exploratory Data Analysis (EDA)

### Principales hallazgos

- **Ingresos:** 
- **Demografía:**  
   mujeres, personas afroamericanas y nativos americanos tienden a ganar menos. En los grupos de mayor ingreso se encuentran hombres, blancos y asiaticos.
- **Educación:**  
  Menor nivel educativo → menores ingresos promedio.
  
<img width="1353" height="693" alt="Captura de pantalla 2025-11-11 155110" src="https://github.com/user-attachments/assets/21870135-4018-418f-bfe3-69298488ae91" />
- **Edad:**
  Entre los 17 y los 35 años es mas probable que los ingresos sean menores a 50.000 u$d, de los 35 a 65 es cuando se gana mas dinero.
- **Carga laboral:**
  A mayor carga laboral, mejores ingresos.
  
   <img width="1355" height="690" alt="Captura de pantalla 2025-11-11 162354" src="https://github.com/user-attachments/assets/7bcbe167-756c-46c5-8946-e1ea599901ca" />

- **Brecha de género:**  
  Se explica en gran parte por las horas trabajadas y las ganancias de capital.
- **Brecha racial:**  
  Está relacionada con las diferencias en capital gain.
- **Ocupación:**  
  Profesiones con mayores ingresos: `Exec-managerial`, `Prof-specialty`, `Tech-support`, `Sales`.  
  Profesiones con menores ingresos: `Priv-house-serv`, `Handlers-cleaners`, `Farming-fishing`.
- **Estado civil:**  
  Las personas casadas presentan mayores ingresos.

---
Grupos con mayor probabilidad de ingresos >50K

| Puesto | Perfil demográfico           | Ocupación        | Total (n) | >50K | Probabilidad |
|--------|-----------------------------|------------------|-----------|------|--------------|
| 1      | Male / White                | Exec-managerial  | 3,980     | 2,313| 58.12%       |
| 2      | Male / Other                | Prof-specialty   | 21        | 12   | 57.14%       |
| 3      | Male / White                | Prof-specialty   | 3,513     | 2,004| 57.05%       |
| 4      | Male / Asian-Pac-Islander   | Prof-specialty   | 211       | 115  | 54.50%       |
| 5      | Male / Asian-Pac-Islander   | Exec-managerial  | 135       | 73   | 54.07%       |
Grupos con menor probabilidad de ingresos >50K

| Puesto | Perfil demográfico           | Ocupación           | Total (n) | >50K | Probabilidad |
|--------|-----------------------------|---------------------|-----------|------|--------------|
| 1      | Female / Asian-Pac-Islander | No registrada (NA)  | 47        | 0    | 0.00%        |
| 2      | Female / Black              | Priv-house-serv     | 51        | 0    | 0.00%        |
| 3      | Female / Other              | Other-service       | 24        | 0    | 0.00%        |
| 4      | Male / Amer-Indian-Eskimo   | Handlers-cleaners   | 29        | 0    | 0.00%        |
| 5      | Male / Black                | Farming-fishing     | 49        | 0    | 0.00%        |

## ⚙️ Modelado Predictivo

Se probaron distintos modelos supervisados.  
El mejor desempeño se obtuvo con **XGBoost**:

| Modelo | Accuracy | Precision | Recall | F1 Score |
|---------|-----------|-----------|---------|-----------|
| XGBoost | **0.87** | **0.78** | 0.75 | 0.76 |

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R  
- **Bibliotecas:** `xgboost`, `lightgbm`, `ggplot2`, `dplyr`, 
- **Técnicas:** EDA, PCA, MCA, Feature Engineering, Cross Validation





  

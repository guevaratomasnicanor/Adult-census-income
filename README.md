# 🧠 Adult Income Analysis

El objetivo del proyecto es **predecir si una persona gana más de 50 000 USD anuales** a partir de características demográficas, laborales y educativas.

---

## 📊 Dataset

El dataset proviene del clásico **Adult Census Income Dataset (UCI Machine Learning Repository)**.  
Contiene información sobre más de 48 000 individuos.

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

- **Demografía:**  
  Jóvenes, mujeres, personas afroamericanas y nativos americanos tienden a ganar menos.  
- **Brecha de género:**  
  Se explica en gran parte por las horas trabajadas y las ganancias de capital.
- **Brecha racial:**  
  Está relacionada con las diferencias en capital gain.
- **Educación:**  
  Menor nivel educativo → menores ingresos promedio.
- **Ocupación:**  
  Profesiones con mayores ingresos: `Exec-managerial`, `Prof-specialty`, `Tech-support`, `Sales`.  
  Profesiones con menores ingresos: `Priv-house-serv`, `Handlers-cleaners`, `Farming-fishing`.
- **Estado civil:**  
  Las personas casadas presentan mayores ingresos.

---

## ⚙️ Modelado Predictivo

Se probaron distintos modelos supervisados.  
El mejor desempeño se obtuvo con **XGBoost**:

| Modelo | Accuracy | Precision | Recall | F1 Score |
|---------|-----------|-----------|---------|-----------|
| XGBoost | **0.87** | **0.78** | 0.75 | 0.76 |

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R  
- **Bibliotecas:** `xgboost`, `lightgbm`, `ggplot2`, `dplyr`, `caret`
- **Técnicas:** EDA, PCA, MCA, Feature Engineering, Cross Validation

---

## 📈 Visualizaciones

Algunos gráficos generados:
- Distribución de ingresos por sexo y edad  
- Ingreso promedio por nivel educativo  
- Boxplots de horas trabajadas vs ingreso  
- Matriz de correlación entre variables numéricas


  

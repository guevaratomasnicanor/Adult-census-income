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
  Entre los 17 y los 35 años es mas probable que los ingresos sean menores a 50.000 u$d, de los 35 a 45 es cuando se gana mas dinero.
- **Carga laboral:**
  A mayor carga laboral, mejores ingresos.
  
   <img width="1355" height="690" alt="Captura de pantalla 2025-11-11 162354" src="https://github.com/user-attachments/assets/7bcbe167-756c-46c5-8946-e1ea599901ca" />

- **Brecha de género:**  
La ventaja salarial masculina es un efecto multiplicador de dos niveles. Primero, el sesgo de género directo otorga un 105% de ventaja adicional por el solo hecho de ser hombre —a igualdad de puesto, horas y capital—. Segundo, el comportamiento (6 horas más de trabajo y $745 extra de capital) suma un 51% de ventaja en las probabilidades de éxito. En conjunto, el hombre promedio posee una ventaja competitiva del 211%, demostrando que la valoración sistémica del mercado pesa incluso más que las diferencias en disponibilidad horaria o recursos financieros.
- **Brecha racial:**  
  Solo por el hecho racial, los asiáticos tienen una probabilidad 42% mayor a los blancos y 72% a los afroamericanos a ganar mas. Esto implica que los blancos tienen una ventaja racial del 21% frente a los de piel negra. En cuanto a las diferencias de comportamiento, estas se denotan en la educación y las ganancias de capital: Los asiaticos tienen un 46% mas de probabilidades que los blancos y 118% mas respecto a afrodescendientes. Lo que implica un 54% de ventaja de blancos sobre negros.
- **Ocupación:**  
  Profesiones con mayores ingresos: `Exec-managerial`, `Prof-specialty`, `Tech-support`, `Sales`.  
  Profesiones con menores ingresos: `Priv-house-serv`, `Handlers-cleaners`, `Farming-fishing`.
- **Estado civil:**  
  Las personas casadas presentan mayores ingresos.

## ⚙️ Modelado Predictivo

Se probaron distintos modelos supervisados.  
El mejor desempeño se obtuvo con **XGBoost**: El modelo tiene un 87% de exactitud (casi 9 de cada 10 predicciones acertadas). Además posee una capacidad de discriminación de clases excelente, distinguiendo a que clase de ingresos pertenece cada individuo 

| Modelo |  Accuracy | Precision | AUC ROC |
|---------|-----------|-----------|-----------|
| XGBoost | **0.87** | **0.785** | **0.928** |

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R  
- **Bibliotecas:** `xgboost`, `lightgbm`, `ggplot2`, `dplyr`, 
- **Técnicas:** EDA, PCA, MCA, Feature Engineering, Cross Validation





  

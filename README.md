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
   Mujeres, personas afroamericanas y nativos americanos tienden a ganar menos. En los grupos de mayor ingreso se encuentran hombres, blancos y asiaticos.
- **Educación:**  
  Menor nivel educativo → menores ingresos promedio.
  
<img width="1353" height="693" alt="Captura de pantalla 2025-11-11 155110" src="https://github.com/user-attachments/assets/21870135-4018-418f-bfe3-69298488ae91" />

- **Edad y carga laboral:**
  El perfil de personas de mayor ingresos es mayor en edad y trabaja mas horas promedio que el de menores ingresos.

<img width="644" height="365" alt="Captura de pantalla 2026-01-08 110012" src="https://github.com/user-attachments/assets/1193b0f6-1dcb-4236-98fc-5e8f0853397b" />
 
- **Brecha de género:**  
La ventaja salarial masculina es un efecto multiplicador de dos niveles. Primero, el sesgo de género directo otorga un 105% de ventaja adicional por el solo hecho de ser hombre —a igualdad de puesto, horas y capital—. Segundo, el comportamiento (6 horas más de trabajo y $745 extra de capital) suma un 51% de ventaja en las probabilidades de éxito. En conjunto, el hombre promedio posee una ventaja competitiva del 211%, demostrando que la valoración sistémica del mercado pesa incluso más que las diferencias en disponibilidad horaria o recursos financieros. Si los hombres tuvieran la misma distribución de empleo que las mujeres, la brecha se reduciría en un 10%.

- **Brecha racial:**  
  El factor racial directo otorga a los asiáticos una ventaja del 42% sobre los blancos y del 72% sobre los afroamericanos (situando a los blancos con un beneficio del 21% frente a los negros). Las diferencias en el perfil de comportamiento —educación, capital y horas— amplían drásticamente estas brechas. Bajo este análisis, el perfil competitivo de los asiáticos les otorga un 46% más de probabilidades de éxito que a los blancos y un 118% más respecto a los afrodescendientes, mientras que la población blanca mantiene una ventaja del 54% sobre la negra basada exclusivamente en recursos. Al consolidar ambos factores, el impacto total es contundente: los asiáticos duplican las probabilidades de éxito de los blancos (2.07x) y casi cuadruplican las de los afroamericanos (3.75x), mientras que un trabajador blanco posee casi el doble de probabilidades (1.86x) de alcanzar el grupo de ingresos altos en comparación con un trabajador negro. En cuanto a la ocupación, si los asiáticos estuvieran en empleos de blancos, la brecha se reduce en un 70%. Si los blancos tuvieran la distribución de empleos de las personas de tez morena, la brecha se reduciría en un 22%. 
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
- **Bibliotecas:** `xgboost`, `ggplot2`, `dplyr`.
- **Técnicas:** EDA, Cross validation, Random search.





  

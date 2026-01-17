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

El análisis de la brecha de género revela que la desigualdad no es un fenómeno puramente técnico, sino una acumulación de barreras estructurales y sistémicas. El factor más determinante es el efecto directo del género (25%), lo que sugiere que, a igualdad de condiciones, el simple hecho de ser mujer reduce drásticamente la probabilidad de altos ingresos debido a sesgos o discriminación no observada. A este componente se suma un 21% explicado por disparidades estructurales, tales como la menor carga horaria semanal y la segregación en ocupaciones con techos salariales más bajos, mientras que los factores demográficos como la edad (19%) y la brecha en la acumulación de riqueza a través de ganancias de capital (10.18%) terminan de configurar este escenario.

- **Brecha racial:**  

   A diferencia de la brecha de género, la disparidad de ingresos entre individuos blancos y negros está impulsada principalmente por el acceso diferencial al mercado laboral y al capital humano. La intensidad laboral (17.5%) y el nivel educativo (17.2%) emergen como los factores más críticos, explicando conjuntamente casi el 35% de la brecha, lo que señala que las diferencias en la trayectoria académica y la carga horaria son las barreras primarias para la equidad. A esto se suma un bloque de influencia equilibrado entre la segregación ocupacional (14.7%), las ganancias de capital (14.6%) y la edad (14.0%), factores que reflejan una menor acumulación de riqueza generacional y una inserción tardía en puestos de alta jerarquía. No obstante, persiste un 8.6% de efecto directo por raza que el modelo no logra explicar mediante méritos o perfiles laborales, evidenciando un residuo de discriminación sistémica que, aunque menor en magnitud que en la brecha de género, actúa como un filtro persistente que limita el ascenso económico independientemente de la calificación profesional.

- **Ocupación:**  
  Profesiones con mayores ingresos: `Exec-managerial`, `Prof-specialty`, `Tech-support`, `Sales`.  
  Profesiones con menores ingresos: `Priv-house-serv`, `Handlers-cleaners`, `Farming-fishing`.

- **Estado civil:**  
  Las personas casadas presentan mayores ingresos.

- **Ganancias de capital**:
 Esta es una de las variables mas esenciales, ya que hay una diferencia de media de ganancias abrumadora entre Ingresos Altos(4000$) e Ingresos Bajos(140$). El 91% de las personas reportó ganancias nulas. El perfil con mayores ganancias de capital está dominado por la alta especialización académica y el emprendimiento corporativo: quienes poseen títulos profesionales (Prof-school) lideran con un promedio mensual de $882, duplicando incluso a los doctorados. Esta capacidad de generar riqueza se concentra en dueños de empresas incorporadas (Self-emp-inc) y especialistas técnicos, lo que sugiere que el excedente para inversión en este dataset no proviene del ahorro salarial común, sino de la propiedad de activos y el ejercicio de profesiones de élite.

  
## ⚙️ Modelado Predictivo

Se probaron distintos modelos supervisados.  
El mejor desempeño se obtuvo con **XGBoost**: El modelo tiene un 87% de exactitud (casi 9 de cada 10 predicciones acertadas). Además posee una capacidad de discriminación de clases excelente, distinguiendo a que clase de ingresos pertenece cada individuo 

| Modelo |  Accuracy | Precision | AUC ROC |
|---------|-----------|-----------|-----------|
| XGBoost | **87.5%** | **78.3%** | **92.75** |

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R  
- **Bibliotecas:** `xgboost`, `ggplot2`, `dplyr`.
- **Técnicas:** EDA, Cross validation, Random search.





  

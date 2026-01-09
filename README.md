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

El análisis de la brecha de género revela que el factor más determinante es el efecto directo del género (42.3%), lo que sugiere que, a igualdad de condiciones, el simple hecho de ser mujer reduce drásticamente la probabilidad de altos ingresos debido a factores no observados o discriminación sistémica. A esto se suma un 21.5% explicado por diferencias estructurales en el mercado laboral, específicamente la menor carga de horas semanales y la segregación en ocupaciones con menores techos salariales. El componente de riqueza, reflejado en las ganancias de capital (9.1%), y factores demográficos como la edad (6.6%), terminan de configurar una desigualdad donde incluso si las mujeres replicaran exactamente el perfil laboral y de inversión de los hombres, la brecha no se cerraría por completo, dejando un 21% de la diferencia sin explicar por las variables tradicionales del modelo.

- **Brecha racial:**  

   El análisis demuestra que la brecha de ingresos no es producto de un solo factor, sino de una acumulación de desventajas estructurales donde la educación y el tipo de ocupación son los motores principales, explicando juntos casi el 40% de la desigualdad total. Llama la atención que el "efecto raza" puro (el cambio de etiqueta sin alterar otra variable) represente un 15% de la brecha, lo que sugiere la existencia de barreras directas o sesgos en el mercado laboral. Conforme sumamos factores como la riqueza acumulada (capital gain) y la experiencia (edad), logramos explicar el 84% de la diferencia inicial, dejando claro que la desigualdad no se debe a cuánto tiempo trabaja la población negra, sino a las barreras de acceso a formación de alto nivel y a sectores profesionales mejor remunerados.

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
| XGBoost | **87.5%** | **78.3%** | **92.75** |

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R  
- **Bibliotecas:** `xgboost`, `ggplot2`, `dplyr`.
- **Técnicas:** EDA, Cross validation, Random search.





  

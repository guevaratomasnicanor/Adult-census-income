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

- **Ingresos:** El 76% de los inividuos censados no llegan a ganar mas de 50.000 Dolares anuales. El 24% restante se encuentra con salarios mayores a ese monto.

- **Demografía:**  **Mujeres**, **personas afroamericanas** y **nativos americanos** tienden a ganar menos. En los grupos de mayor ingreso se encuentran **hombres**, **blancos** y **asiaticos**.

- **Educación:**  
  Menor nivel educativo → menores ingresos promedio.
  
<img width="1353" height="693" alt="Captura de pantalla 2025-11-11 155110" src="https://github.com/user-attachments/assets/21870135-4018-418f-bfe3-69298488ae91" />

- **Edad y carga laboral:**
  El perfil de personas de mayor ingresos es mayor en edad y trabaja mas horas promedio que el de menores ingresos.

<img width="644" height="365" alt="Captura de pantalla 2026-01-08 110012" src="https://github.com/user-attachments/assets/1193b0f6-1dcb-4236-98fc-5e8f0853397b" />
 

- **Brecha de género:**  

El análisis de la brecha de género revela que la desigualdad no es un fenómeno puramente técnico, sino una acumulación de barreras estructurales y sistémicas. El factor más determinante es el efecto directo del género (20%), lo que sugiere que, a igualdad de condiciones, el simple hecho de ser mujer reduce drásticamente la probabilidad de altos ingresos debido a sesgos o discriminación no observada. A este componente se suma un 21% explicado por disparidades estructurales, tales como la menor carga horaria semanal y la segregación en ocupaciones con techos salariales más bajos, mientras que los factores demográficos como la edad (19%) y la brecha en la acumulación de riqueza a través de ganancias de capital (12.07%) terminan de configurar este escenario.

- **Brecha racial:**  

   A diferencia de la brecha de género, la disparidad de ingresos entre individuos blancos y negros está cimentada primordialmente en el acceso al capital humano, donde el nivel educativo (17%) se consolida como el factor más crítico, superando a la segregación ocupacional (14.6%) y a las ganancias de capital (14.5%) en la jerarquía de barreras económicas. Este panorama sugiere que la desigualdad no solo se origina en el aula, sino que se perpetúa mediante una inserción en sectores de menor remuneración y una histórica dificultad para acumular riqueza generacional. Aunque la intensidad laboral (13.4%) y la edad (12%) aportan una capa adicional de explicación vinculada a la experiencia y la carga horaria, persiste un 6.6% de efecto directo por raza que resulta inexplicable bajo criterios de mérito o perfil profesional. Este porcentaje, aunque menor que en otros indicadores, confirma la existencia de un residuo de discriminación sistémica que actúa como un techo invisible, penalizando el progreso económico independientemente de la excelencia académica o la productividad demostrada.

- **Ocupación:**  
  Profesiones con mayores ingresos: **Ejecutivo-Manager**, **Especialidad profesional**, **Soporte técnico** , **Ventas**.  
  Profesiones con menores ingresos: **Empleados domésticos**, **Limpieza Y mantenimiento** , **Granja/pesca**.

- **Estado civil:**  
  Las personas casadas presentan mayores ingresos.

- **Ganancias de capital**:
 Esta es una de las variables mas esenciales, ya que hay una diferencia de media de ganancias abrumadora entre Ingresos Altos(4000$) e Ingresos Bajos(140$). El 91% de las personas reportó ganancias nulas. El perfil con mayores ganancias de capital está dominado por la alta especialización académica y el emprendimiento corporativo: quienes poseen títulos profesionales (Prof-school) lideran con un promedio de 10854$, duplicando incluso a los doctorados. Esta capacidad de generar riqueza se concentra en dueños de empresas incorporadas (Self-emp-inc) y especialistas técnicos, lo que sugiere que el excedente para inversión en este dataset no proviene del ahorro salarial común, sino de la propiedad de activos y el ejercicio de profesiones de élite.

  
## ⚙️ Modelado Predictivo

Se probaron distintos modelos supervisados.  
El mejor desempeño se obtuvo con **XGBoost**: El modelo tiene un 87% de exactitud (casi 9 de cada 10 predicciones acertadas). Además posee una capacidad de discriminación de clases excelente, distinguiendo a que clase de ingresos pertenece cada individuo 

| Modelo |  Accuracy | Precision | Recall | F1 Score |
|---------|-----------|-----------|-----------| -------|
| XGBoost | **86.6%** | **72.3%** | **64.75%** | 72.93% |

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R  
- **Bibliotecas:** `xgboost`, `ggplot2`, `dplyr`.
- **Técnicas:** EDA, Cross validation, Random search.





  

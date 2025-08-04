# 📘 Informe de Análisis de Evasión de Clientes (Churn)

---

## 🔹 1. Objetivo del Análisis

El propósito de este análisis es identificar los factores que influyen en la **evasión de clientes** dentro de una empresa de telecomunicaciones. A través del análisis de datos históricos, buscamos entender las características comunes de los clientes que cancelan el servicio (`Churn = yes`) y proponer estrategias para mejorar la retención.

---

## 🔹 2. Preparación y Limpieza de los Datos

- Los datos fueron extraídos desde un archivo JSON en línea.
- Se utilizó `pandas` para **normalizar** y convertir la estructura a un `DataFrame`.
- Se verificó que **no existen valores nulos** en las columnas.
- Se convirtió la columna `account_Charges_Total` de tipo `object` a `float64` usando `pd.to_numeric`.
- Se creó la variable **`Cuentas_Diarias`**, dividiendo el cargo mensual entre 30 para estimar el gasto diario.
- Se estandarizaron las variables categóricas con valores `"Yes"/"No"` a `1/0`.
- Se renombraron algunas columnas para mejorar su comprensión.

---

## 🔹 3. Análisis Exploratorio

### 🔸 3.1 Distribución de la Evasión

- Se identificó que el **28.8% de los clientes cancelaron** el servicio.
- Gráficos de barras y pastel mostraron un **desbalance de clases**, con mayoría de clientes retenidos.

### 🔸 3.2 Relación de variables categóricas con Churn

- **Clientes con contrato mensual** tienen mayor tasa de evasión.
- Los métodos de pago como **"cheque electrónico"** presentan mayor churn comparado con pagos automáticos.
- Las personas **sin pareja o dependientes** muestran una mayor probabilidad de cancelar.

### 🔸 3.3 Relación de variables numéricas con Churn

- Clientes con menor **tiempo de contrato (`tenure`)** tienen más probabilidad de cancelar.
- El gasto total acumulado es menor en los clientes que se van, lo que puede reflejar menor lealtad o satisfacción.

Gráficos de líneas y boxplots interactivos en Plotly mostraron estas diferencias de forma clara.

---

## 🔹 4. Conclusiones Principales

- El churn no ocurre al azar: está relacionado con **el tipo de contrato, método de pago, tiempo como cliente y gasto total**.
- El grupo más vulnerable está compuesto por:
  - Nuevos clientes.
  - Contratos mensuales.
  - Personas sin compromisos familiares.
  - Clientes con métodos de pago manuales.

---

## 🔹 5. Recomendaciones Estratégicas

1. **Incentivar la migración a contratos a largo plazo** mediante promociones y precios diferenciados.
2. **Ofrecer beneficios a nuevos clientes** en sus primeros 3 meses para fomentar permanencia.
3. **Automatizar los pagos** con incentivos por uso de débito automático o tarjeta.
4. **Aplicar modelos predictivos de churn** para anticiparse a la cancelación.
5. **Segmentar campañas de retención** según perfiles de riesgo detectados en este análisis.

---

## 🧩 Consideraciones Finales

Este análisis provee una base sólida para la toma de decisiones enfocadas en reducir la evasión. Con una estrategia proactiva basada en datos, es posible aumentar la satisfacción del cliente, mejorar la retención y reducir pérdidas.


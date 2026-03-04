
<div align="center">
<h1> ✨ CHALLENGE - TelecomX2_LATAM ✨ </h1>
<h2> Modelado Predictivo de Deserción de Clientes (Churn) </h2>
</div>

![Badge en Desarrollo](https://img.shields.io/badge/ENTREGA-%2004/03/2026-pink)

<h3> 📌 Introducción </h3>

En esta segunda etapa del proyecto TelecomX_LATAM se desarrollan modelos de Machine Learning con el objetivo de predecir qué clientes tienen mayor probabilidad de cancelar sus servicios.

A partir de los datos tratados en el Challenge 1, se construyen y comparan distintos modelos predictivos para identificar patrones de deserción y generar estrategias de retención basadas en evidencia.

<h1></h1>

<h3> 🛠️ Preparación y Tratamiento de Datos </h3>

Para el desarrollo de los modelos se realizaron los siguientes pasos:

* Se importó el archivo CSV con los datos previamente tratados.
* Se eliminó la columna ID por no aportar valor predictivo.
* Se definieron:
  * Variables explicativas (X)
  * Variable objetivo (y → Churn)
* Se realizó análisis de correlación entre variables.
* Se aplicó normalización de datos numéricos.
* Se realizó balanceo de clases para mejorar el rendimiento predictivo.
* Se aplicó codificación One-Hot Encoding para variables categóricas.
* Se construyeron y evaluaron cuatro modelos de clasificación:
  * Regresión Logística
  * Random Forest
  * Decision Tree
  * XGBoost
* Se compararon métricas de rendimiento.
* Se analizó la importancia de variables en cada modelo.

<h1></h1>

<h3> 📊 Análisis Dirigido </h3>

<p align="center">
  <img width="500" height="547" src="https://github.com/user-attachments/assets/0b89572e-efc9-4065-b13d-836e2b7383bb" />
  <img width="500" height="547" src="https://github.com/user-attachments/assets/f7d0ab28-cbbd-4d7b-b20f-5757edf63ff5" />
</p>

<p align="center">
  <img width="699" height="315" src="https://github.com/user-attachments/assets/07a60cde-d5c9-4f40-953b-29b2b4b24e15" />
</p>

A partir del análisis gráfico se observa que:

* Los clientes que cancelan suelen tener baja antigüedad.
* Existe una relación directa entre:
  
  Mayor tiempo de contrato → Mayor gasto total → Menor probabilidad de churn.

<h1></h1>

<h3> 🔎 Análisis de Correlación </h3>

<p align="center">
  <img width="1886" height="1059" src="https://github.com/user-attachments/assets/820a56b5-763c-4d3e-ac92-a064063ffa86" />
</p>

<p align="center">
  <img width="500" height="323" src="https://github.com/user-attachments/assets/1a11c19d-a85b-42b9-a9f2-62ca7217ce92" />
</p>

La matriz de correlación muestra:

* 1.0 → correlación perfecta (variable consigo misma).
* Morado intenso → correlación positiva fuerte.
* Morado claro → correlación negativa fuerte.
* Blanco → baja o nula correlación.

Esto permitió identificar relaciones relevantes entre antigüedad, cargos y tipo de contrato.

<h1></h1>

<h3> 🤖 Modelos de Clasificación y Comparación </h3>

<p align="center">
  <img width="500" height="265" src="https://github.com/user-attachments/assets/5997e2ee-3a6b-437f-8578-7e712cdf6043" />
</p>

<p align="center">
  <img width="1662" height="606" src="https://github.com/user-attachments/assets/b664b772-60e9-43d2-a298-df6a822c38ca" />
</p>

Las métricas clave evaluadas fueron:

* **Recall** → Capacidad del modelo para detectar clientes que realmente cancelan.
* **F1-Score** → Balance entre:
  * Precision → Qué tan confiable es cuando predice churn.
  * Recall → Qué tanto churn real detecta.
* **AUC (ROC Curve)** → Capacidad de separación del modelo:
  * 0.50 → Modelo aleatorio
  * 0.70 - 0.80 → Aceptable
  * 0.80 - 0.90 → Muy bueno
  * 0.90+ → Excelente

📌 El modelo con mejor desempeño general fue la **Regresión Logística**, logrando un balance adecuado entre Recall, F1-Score y AUC.

<h1></h1>

<h3> 📈 Importancia de Variables </h3>

<p align="center">
  <strong>Importancia - Regresión Logística</strong>
</p>
<p align="center">
  <img width="500" height="181" src="https://github.com/user-attachments/assets/10ae8fdd-52b7-48c1-aa22-36b925613c70" />
</p>

<p align="center">
  <strong>Importancia - Random Forest</strong>
</p>
<p align="center">
  <img width="500" height="179" src="https://github.com/user-attachments/assets/dbc235d9-d276-44cf-801a-bd85cea57791" />
</p>

<p align="center">
  <strong>Importancia - XGBoost</strong>
</p>
<p align="center">
  <img width="500" height="176" src="https://github.com/user-attachments/assets/7a85f334-1c73-4ea9-a033-58b00a41fccc" />
</p>

Los modelos coinciden en que las variables más influyentes son:

* Tipo de contrato
* Antigüedad del cliente
* Cargos mensuales y totales
* Tipo de servicio de internet (Fibra óptica)

<h1></h1>

<h3> 🧠 Conclusiones Estratégicas </h3>

* El tipo de contrato es determinante:
  * Mes a mes → Mayor riesgo de churn.
  * Dos años → Menor riesgo.

* La antigüedad del cliente reduce significativamente la probabilidad de cancelación.

* Cargos mensuales elevados incrementan la probabilidad de churn.

* El servicio de fibra óptica presenta mayor riesgo, posiblemente asociado a:
  * Costos más altos.
  * Expectativas de servicio.
  * Experiencia inicial.

📌 Enfoque recomendado:
- Estrategias de retención para clientes nuevos.
- Seguimiento en contratos mensuales.
- Planes personalizados para clientes con cargos elevados.
- Mejora en experiencia y soporte del servicio de fibra.

<h1></h1>

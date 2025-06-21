# Airbnb-NewYork-2019-price-prediction
# 🏙️ Predicción de Precios de Airbnb en Nueva York (AB_NYC_2019)

Este proyecto analiza y modela los precios de los alojamientos de Airbnb en Nueva York a partir del dataset público `AB_NYC_2019`. Se realiza una exploración de datos, limpieza, filtrado de outliers, transformación de variables y comparación entre modelos de regresión.

## 📊 Objetivo

Evaluar la capacidad de diferentes algoritmos de Machine Learning para predecir el precio de los alojamientos en función de las características presentes en este dataset.

---

## 🔍 Exploración de Datos

Se analizaron las variables más relevantes y se detectó la necesidad de:
- Eliminar valores atípicos en `price` y `minimum_nights`
- Estandarizar variables numéricas
- Convertir variables categóricas con **One Hot Encoding**

Algunos insights iniciales:
- El precio presenta una distribución muy sesgada (outliers a >$300).
- Manhattan y Brooklyn concentran la mayoría de alojamientos.
- El tipo de habitación influye claramente en el precio.

![Mapa alojamientos](images/mapa_airbnb.png)
![Distribución precio](images/distribucion_precio.png)

---

## 🧼 Preprocesado de Datos

- Se eliminaron outliers (precios > 300€, estancias > 8 noches).
- Se estandarizaron variables numéricas.
- Se codificaron variables categóricas (`neighbourhood_group`, `room_type`) mediante One Hot Encoding.
- Se crearon nuevas variables como `days_since_last_review`.

---

## 🤖 Modelado

Se compararon tres algoritmos de regresión:

| Modelo             | MSE   | R² Score |
|--------------------|-------|----------|
| Linear Regression  | 0.53  | 0.47     |
| Random Forest      | 0.54  | 0.46     |
| XGBoost            | 0.52  | 0.48     |

> 📌 *El modelo XGBoost fue el más preciso, aunque todos mostraron un rendimiento limitado debido a la naturaleza del dataset.*

---

## 🧠 Conclusiones

- El precio es difícil de predecir con alta precisión debido a factores no incluidos en el dataset (número de habitaciones, calidad, fotos, etc.).
- Aun así, el análisis ayuda a entender las variables que más afectan al precio: **ubicación**, **tipo de habitación** y **disponibilidad**.
- Este proyecto demuestra un flujo completo de trabajo en Machine Learning aplicado a datos reales del sector turístico.

---


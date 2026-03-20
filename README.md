# 🚍 Predicción de Demanda de Transporte Público en CABA

Proyecto de ciencia de datos enfocado en analizar y predecir la demanda de viajes en colectivo en la Ciudad Autónoma de Buenos Aires (CABA), utilizando técnicas de Machine Learning.

---

## 📌 Descripción

La red de transporte público en CABA presenta un desbalance entre la oferta de servicios y la demanda real de pasajeros, lo que genera:

- Costos operativos elevados  
- Mala experiencia de usuario  
- Ineficiencia en la asignación de recursos  

Este proyecto busca resolver ese problema mediante el análisis de datos históricos y la construcción de un modelo predictivo capaz de anticipar la demanda de viajes por comuna y franja horaria.

---

## 🎯 Objetivo

Desarrollar un modelo de Machine Learning que permita:

- Predecir la cantidad de viajes en colectivo  
- Identificar patrones de demanda  
- Optimizar la planificación del transporte público  

---

## 📊 Dataset

Se utilizaron dos fuentes principales de datos:

### 1. Viajes (SUBE)
- ~7.000.000 registros  
- Día hábil tipo (2023)  
- Información sobre:
  - Origen y destino
  - Cantidad de etapas
  - Medio de transporte  

📌 Se filtraron únicamente viajes en colectivo.

---

### 2. Paradas de colectivo
- ~7.000 registros  
- Incluye:
  - Latitud y longitud  
  - Comuna  

---

## 🧹 Procesamiento de datos

### Limpieza
- Conversión de tipos de datos  
- Manejo de valores nulos  
- Estandarización de columnas  

### Feature Engineering
- Asignación de `comuna_origen` mediante KNN (k=1)  
- Selección de variables relevantes  

---

## 🔍 Análisis Exploratorio (EDA)

Se realizaron distintos análisis para entender los datos:

- 📈 Distribución de viajes por hora  
- 🗺️ Heatmap de paradas  
- 🏙️ Top comunas con mayor demanda  
- 🚌 Uso por medio de transporte  
- ⏰ Distribución por rango horario  

### Hallazgos clave:

- Picos de demanda en:
  - 06:00 - 10:00  
  - 14:00 - 18:00  

- Más de **2.8 millones de usuarios diarios** utilizan colectivos  
- Fuerte desigualdad territorial en la cobertura  

---

## 🤖 Modelo Predictivo

Se utilizó un modelo de:

### 🌲 Random Forest Regressor

#### Variables:
- `comuna_origen`
- `hora`

#### Target:
- `cantidad_viajes`

#### División de datos:
- 80% entrenamiento  
- 20% test  

---

## 📈 Resultados

- **R² = 0.936**  
  → El modelo explica el 93.6% de la variabilidad  

- **RMSE = ±6488 viajes**  
  → Error promedio bajo considerando el volumen de datos  

📌 El modelo logra capturar patrones complejos y no lineales en la demanda.

---

## 📊 Visualización

Se desarrolló un dashboard interactivo con:

- Demanda por comuna  
- Distribución horaria  
- Comparación real vs predicho  
- Mapa de infraestructura  

---

## 🧠 Conclusiones

- Existe un desbalance entre oferta y demanda en distintas comunas  
- Hay zonas con:
  - Alta cobertura pero baja demanda  
  - Baja cobertura y alta necesidad  

- La demanda está fuertemente concentrada en horarios pico  
- El uso de Machine Learning permite predecir la demanda con alta precisión  


---

## 🛠️ Tecnologías utilizadas

- Python  
- Pandas  
- Scikit-learn  
- Jupyter Notebook  
- Looker Studio (visualización)  

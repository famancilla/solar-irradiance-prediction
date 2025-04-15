# solar-irradiance-prediction
# Solar Irradiance Forecasting with Machine Learning & Deep Learning

Este proyecto corresponde al Trabajo de Fin de Máster de Felipe Andrés Mancilla Cofré, presentado en la Universidad Complutense de Madrid, como parte del Máster en Data Science, Big Data & Business Analytics (2023-2024).

## 🎯 Objetivo

Desarrollar un sistema de predicción para estimar tres tipos de irradiancia solar en condiciones de cielo despejado:

- **DHI (Direct Horizontal Irradiance)**
- **DNI (Direct Normal Irradiance)**
- **GHI (Global Horizontal Irradiance)**

A partir de datos meteorológicos históricos recogidos durante 10 años con una frecuencia de 30 minutos.

## 📁 Dataset

Dataset público proporcionado por Wipro Limited en colaboración con MachineHack, disponible en [Kaggle](https://www.kaggle.com/competitions/sustainability-hackathon/data).  
Contiene variables climáticas como temperatura, humedad, presión, tipo de nube, dirección y velocidad del viento, entre otras.

## ⚙️ Metodología

1. Exploración y análisis descriptivo de variables
2. Preprocesamiento: limpieza, combinación de variables temporales, escalado
3. Entrenamiento de modelos:
   - Regresión Lineal
   - XGBoost
   - Random Forest (con hiperparámetros ajustados)
   - 5 modelos distintos de RNN:
     - LSTM simples
     - LSTM con Early Stopping
     - LSTM con regularización
     - LSTM + GRU con ReduceLROnPlateau
     - Bi-LSTM + GRU (mejor modelo)

## 📈 Resultados

- El modelo **Bidirectional LSTM + GRU** obtuvo los mejores resultados en casi todas las métricas.
- El modelo **Random Forest** también logró un excelente rendimiento, con menor coste computacional.
- Métricas utilizadas: `MSE`, `R²`, `Loss`, `Validation Loss`.

## 🧠 Tecnologías usadas

- Python
- Pandas, NumPy, Scikit-learn
- TensorFlow / Keras
- Matplotlib, Seaborn
- Jupyter Notebook

## 📌 Conclusiones

Las redes neuronales recurrentes, especialmente arquitecturas complejas como Bi-LSTM + GRU, son herramientas muy potentes para la predicción de variables climáticas. No obstante, modelos como Random Forest pueden lograr resultados competitivos con menor complejidad computacional.

## 📂 Estructura del repositorio


# 🧠 Model Fitness: Predicción y Retención de Clientes en un Gimnasio con Machine Learning

Este proyecto explora cómo predecir la cancelación de membresías en una cadena de gimnasios utilizando modelos de machine learning, con el objetivo de mejorar la retención de clientes y diseñar estrategias basadas en datos.

## 📌 Objetivo

- Predecir qué clientes es probable que cancelen su membresía el próximo mes.
- Analizar los factores que influyen en la cancelación.
- Crear perfiles de clientes y agruparlos en clústeres.
- Generar recomendaciones para mejorar la atención y fidelización de usuarios.

---

## 📊 Dataset

El dataset proporcionado incluye datos de clientes actuales y su comportamiento en el gimnasio. Contiene información como:

- Datos personales: género, edad, ubicación.
- Datos de comportamiento: frecuencia de visitas, uso de servicios adicionales.
- Información contractual: tipo de contrato, meses restantes, participación en clases grupales.
- Etiqueta de cancelación (`Churn`): si el cliente canceló o no en el mes siguiente.

📁 Archivo: `/datasets/gym_churn_us.csv`

---

## ⚙️ Tecnologías y herramientas

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Scipy (para clustering jerárquico)

---

## 🧪 Desarrollo del proyecto

### 1. Análisis exploratorio de datos (EDA)

- Revisión de valores nulos y tipos de datos.
- Estadísticas descriptivas.
- Comparación de características entre usuarios que cancelaron y los que no.
- Visualización de distribuciones y correlaciones.

### 2. Modelado predictivo

Se entrenaron dos modelos de clasificación binaria:

- **Regresión logística**
- **Random Forest**

Métricas utilizadas:
- Accuracy
- Precision
- Recall

📌 El modelo de Random Forest obtuvo mejor rendimiento general y mayor recall para detectar cancelaciones.

### 3. Segmentación de clientes (Clustering)

- Estandarización de variables.
- Dendrograma para estimar número de clústeres.
- K-Means con `n=5` clústeres.
- Análisis del comportamiento típico por clúster (frecuencia, gastos, cancelación).

---

## 🔍 Principales hallazgos

- Los clientes con contratos más cortos y menor frecuencia de visitas son más propensos a cancelar.
- Aquellos que participan en clases grupales y tienen membresías anuales muestran mayor lealtad.
- El gasto en servicios adicionales está correlacionado con una mayor retención.

---

## ✅ Recomendaciones

1. **Fomentar contratos largos**: Incentivar la contratación de planes de 6 o 12 meses con promociones especiales.
2. **Promover clases grupales**: Los clientes que asisten a sesiones grupales cancelan menos. Se puede ofrecer una clase gratis al mes o crear retos grupales.
3. **Identificar clientes en riesgo**: Con el modelo entrenado, se puede generar alertas para clientes con alta probabilidad de cancelación y contactarlos proactivamente.
4. **Incentivar uso de servicios adicionales**: Ofrecer descuentos o puntos de fidelidad por consumir en cafetería, masajes o productos deportivos.

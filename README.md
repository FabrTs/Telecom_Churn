# 📡 Interconnect Churn Prediction
## Telecom Customer Churn Modeling – Machine Learning Project

<p align="center"> <img src="https://img.shields.io/badge/Status-Completed-brightgreen" /> <img src="https://img.shields.io/badge/Notebook-Jupyter-orange" /> <img src="https://img.shields.io/badge/Python-3.10-blue" /> <img src="https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-yellow" /> <img src="https://img.shields.io/badge/ML-LogisticRegression%20%7C%20RandomForestRegression%20%7C%20LightGBM%20%7C%20XGBoost%20%7C%20CatBoost-violet" /> </p>


📚 Tabla de Contenidos

- 📄 Descripción del Proyecto
- 🧰 Tecnologías Utilizadas
- 🛠️ Proceso de Desarrollo
- 📊 Resultados del Modelo
- 🧠 Conclusiones


📄 Descripción del Proyecto

El operador de telecomunicaciones Interconnect busca anticipar la cancelación de clientes (churn) para mejorar sus estrategias de retención mediante promociones, descuentos y cambios de plan personalizados.

El objetivo es desarrollar un modelo de Machine Learning capaz de predecir con alta precisión si un cliente dará de baja sus servicios.

La información proviene de cuatro archivos:

- contract.csv — datos del contrato
- personal.csv — información personal del cliente
- internet.csv — servicios relacionados a Internet
- phone.csv — servicios telefónicos

La variable objetivo es churn (1 = canceló, 0 = activo).

La métrica principal es AUC-ROC, y la métrica secundaria Accuracy.

🧰 Tecnologías Utilizadas

- Python 3.10+
- Pandas, NumPy — análisis y manipulación de datos
- Matplotlib, Seaborn — visualización
- Scikit-Learn — modelos, pipelines y métricas
- Jupyter Notebook — experimentación y documentación
- GridSearchCV / RandomizedSearchCV — tuning de hiperparámetros
- CatBoost
- XGBoost
- LightGBM

🛠️ Proceso de Desarrollo
1. Exploración y Limpieza de Datos
    - Unión de tablas con customerID.
    - Conversión de fechas (BeginDate, EndDate).
    - Cálculo de la antigüedad del cliente: tenure_months.
    - Limpieza de valores nulos:
    - Servicios de Internet → NoInternet
    - Servicios telefónicos → NoPhone
    - TotalCharges faltantes → MonthlyCharges × tenure
    - Conversión de variables binarias (Yes/No → 1/0).
    - Normalización de variables categóricas mediante One-Hot Encoding.

2. Análisis Exploratorio (EDA)

    - Identificación de patrones de churn:
      - Los clientes con contratos month-to-month presentan mayor tasa de cancelación.
      - La tecnología Fiber Optic incrementa la probabilidad de churn.
      - Las facturas electrónicas y métodos de pago automáticos muestran comportamientos distintos.
    - Visualización de distribuciones, correlaciones y relaciones clave.

3. Entrenamiento de Modelos

- Modelos evaluados:
    - Regresión Logística
    - Random Forest
    - Gradient Boosting
    - XGBoost
    - LightGBM
    - Árboles de decisión

- Incluyendo:
    - Manejo de desbalance con class_weight = 'balanced'
    - Búsqueda de hiperparámetros
    - Evaluación con AUC-ROC, Accuracy, Matriz de Confusión

📊 Resultados del Modelo

| Modelo             | AUC-ROC         | Accuracy |
| ------------------ | --------------- | -------- |
| Mejor Modelo Final | **0.84 – 0.87** | ~80%     |


✔ El modelo seleccionado muestra una capacidad robusta para identificar clientes con alta probabilidad de cancelar.
✔ Se logra un equilibrio adecuado entre sensibilidad y especificidad, crucial en proyectos de churn.

Estos resultados permiten a Interconnect aplicar estrategias proactivas de retención.


🧠 Conclusiones

- El modelo desarrollado permite identificar de forma anticipada a clientes con riesgo de cancelación.
- La empresa puede implementar acciones enfocadas en retención: descuentos, mejoras de plan, beneficios especiales.
- Las variables más relevantes fueron:
    - Tipo de contrato
    - Tecnología de Internet
    - Método de pago
    - Antigüedad del cliente
- El proyecto demuestra un pipeline completo de ciencia de datos: EDA → Preparación → Modelado → Evaluación.

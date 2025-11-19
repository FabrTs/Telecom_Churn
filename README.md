# Games
Proyecto de análisis de datos históricos de ventas y reseñas de videojuegos, para identificar patrones que indiquen cuáles tienen mayor probabilidad de éxito.

🎮 Video Game Sales Analysis — Ice Store (2016)
<p align="center"> <img src="https://img.shields.io/badge/Status-Completed-brightgreen" /> <img src="https://img.shields.io/badge/Notebook-Jupyter-orange" /> <img src="https://img.shields.io/badge/Python-3.10-blue" /> <img src="https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-yellow" /> </p>

📑 Tabla de Contenidos

- 📌 Descripción del Proyecto
- 🧠 Enfoque de la Solución
- 🛠️ Tecnologías Utilizadas
- 📊 Principales Hallazgos
  - 📈 Evolución de la industria
  - 🎮 Plataformas más rentables
  - 🧩 Géneros más exitosos
  - 🌍 Preferencias por región
  - ⭐ Influencia de las reseñas
  - 🔬 Resultados de hipótesis
- 🧾 Conclusiones


📌 Descripción del Proyecto

Este proyecto analiza datos históricos de ventas y reseñas de videojuegos para Ice, una tienda online de distribución global de títulos y consolas.

El objetivo principal es identificar patrones que indiquen cuáles videojuegos tienen mayor probabilidad de éxito, con el fin de planificar las campañas de marketing y priorizar lanzamientos para el año 2017, situándonos analíticamente en diciembre de 2016.

Los datos incluyen:

- Ventas por región (NA, EU, JP, Others)
- Puntuaciones de usuarios y críticos
- Género del juego
- Plataforma
- Año de lanzamiento
- Clasificación ESRB

🧠 Enfoque de la Solución

El análisis fue estructurado en seis etapas clave:

1. Preparación y Limpieza de Datos

- Estandarización de columnas (snake_case)
- Conversión de tipos y tratamiento de valores faltantes
- Gestión de categorías desconocidas (unknown)
- Creación de la métrica total_sales

2. Análisis Exploratorio (EDA)

- Frecuencia de lanzamientos por año
- Ciclos de vida de plataformas
- Identificación de plataformas líderes
- Análisis de géneros y ventas globales
- Estudio de juegos multiplataforma

3. Selección de Datos Relevantes

Se seleccionó el período 2013–2015, ya que los datos de 2016 parecen incompletos y estos tres años representan mejor el comportamiento reciente del mercado.

4. Perfil de Usuario por Región

Para NA, EU y JP se identificaron:

- Plataformas top
- Géneros con mayor impacto
- Influencia de la clasificación ESRB

5. Correlaciones

Comparación del efecto de:

- Puntajes de críticos vs ventas
- Puntajes de usuarios vs ventas

6. Pruebas de Hipótesis

Se aplicó test t de Student (Welch) para:

- XOne vs PC → ¿tienen la misma calificación promedio?
- Action vs Sports → ¿promedios iguales?

🛠️ Tecnologías Utilizadas

Lenguaje:

- Python 3.10

Librerías principales:

- pandas → Limpieza y análisis
- numpy → Operaciones numéricas
- matplotlib & seaborn → Visualizaciones
- scipy.stats → Pruebas de hipótesis
- Jupyter Notebook → Documentación y desarrollo

📊 Principales Hallazgos
📈 Evolución de la industria

- La cantidad de lanzamientos creció fuertemente hasta 2008–2009.
- A partir de 2010, el número disminuye gradualmente.
- Los años más confiables para análisis son desde 2000 en adelante.

🎮 Plataformas más rentables (2013–2015)

Las plataformas con más ventas totales fueron:

| Plataforma   | Ventas Totales (M) |
| ------------ | ------------------ |
| **PS4**      | 244.89             |
| **PS3**      | 177.83             |
| **Xbox 360** | 135.28             |
| **Xbox One** | 133.17             |
| **3DS**      | 128.11             |


➡️ PS4 y Xbox One son las únicas que muestran crecimiento, mientras las demás están en declive.

🧩 Géneros más exitosos

- Los géneros con mayor venta global fueron: Action, Shooter, Role-Playing.
- Los géneros con mayor promedio por juego incluyen: Sports y Platform.
- La correlación entre cantidad de juegos publicados y ventas es alta (0.86).

🌍 Preferencias por región

Norteamérica (NA)

- Destacan: Action, Shooter, Sports
- Dominan plataformas: PS4, XOne, X360

Europa (EU)

- Patrones similares a Norteamérica
- Fuerte preferencia por PS4

Japón (JP)

- Domina Role-Playing
- Plataformas portátiles (3DS, PSV) son líderes
- Comportamiento de compra distinto al resto del mundo

⭐ Influencia de las reseñas

- La correlación entre críticas profesionales y ventas en PS4 es moderada (0.43).
- La correlación con reseñas de usuarios es casi nula (0.02).

➡️ Las reseñas de expertos influyen más en las ventas que las de usuarios.

🔬 Resultados de hipótesis
1. Xbox One vs PC

- p-value < 0.05 : ➡️ Las calificaciones promedio son significativamente diferentes.

2. Acción vs Deportes

- p-value < 0.05 : ➡️ También son diferentes en promedio.

🧾 Conclusiones

- PS4 y Xbox One son las plataformas más rentables para campañas de marketing en 2017.
- Los géneros Action, Shooter y Sports deben ser prioridad para alcanzar un mayor impacto global.
- Japón requiere una estrategia distinta, enfocándose en Role-Playing y plataformas portátiles.
- Las críticas profesionales tienen mayor influencia comercial que las reseñas de usuarios.
- Los patrones de ventas varían significativamente por región, por lo que la estrategia debe adaptarse al mercado objetivo.





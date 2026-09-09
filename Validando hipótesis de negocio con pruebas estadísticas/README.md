# 📊 Experimento A/B en Landing Page

## 🎯 Objetivo del proyecto

Evaluar un **experimento A/B** realizado sobre una página de inicio (landing page), comparando las versiones **A y B**, con el propósito de apoyar una decisión de negocio basada en datos.

El análisis busca determinar si existen diferencias estadísticamente significativas entre ambas versiones en:

- El **gasto promedio** de los usuarios que realizaron una conversión.
- La **tasa de conversión**.
- El comportamiento según la **fuente de tráfico**.
- El comportamiento según el **tipo de usuario**.

Finalmente, los resultados se traducen en un **insight ejecutivo y recomendaciones de negocio**.

---

## 📂 Dataset utilizado

El proyecto utiliza un único dataset:

### `landing_experiment.csv`

Contiene información de usuarios expuestos a las dos versiones de la landing page durante el experimento A/B.

### Variables

| Variable | Descripción |
|---|---|
| `user_id` | Identificador único del usuario |
| `date` | Fecha en la que el usuario fue expuesto a la página |
| `landing` | Versión de la landing page mostrada: A o B |
| `region` | Región geográfica del usuario |
| `dispositivo` | Tipo de dispositivo utilizado |
| `traffic_source` | Canal por el que llegó el usuario |
| `user_type` | Tipo de usuario según su historial previo |
| `converted` | Indica si el usuario realizó una conversión |
| `gasto` | Monto gastado por el usuario; 0 si no convirtió |

---

## 🔎 Etapas del análisis

### 1. Carga y validación de datos

- Importación de las librerías necesarias.
- Carga del archivo CSV.
- Exploración inicial del dataset.
- Revisión de información general y tipos de datos.
- Comprobación de usuarios duplicados.
- Revisión del rango temporal.
- Análisis descriptivo de `gasto`.
- Validación de las categorías de las variables categóricas.
- Identificación de valores ausentes.

### 2. Comparación del gasto promedio: página A vs. B

Se analizaron únicamente los usuarios que realizaron una conversión.

Proceso:

1. Separación de usuarios convertidos de las páginas A y B.
2. Comparación de sus gastos.
3. Aplicación de la prueba de **Levene** para evaluar la igualdad de varianzas.
4. Debido a que las varianzas resultaron diferentes, se utilizó un **t-test de Welch** (`equal_var=False`).
5. Interpretación de la diferencia desde una perspectiva de negocio.

### 3. Comparación de la tasa de conversión

Se compararon las tasas de conversión de las páginas A y B.

Proceso:

1. Conteo de usuarios convertidos por versión.
2. Conteo total de usuarios por versión.
3. Cálculo de las tasas de conversión.
4. Aplicación de una **prueba Z para dos proporciones**.
5. Interpretación del resultado.

### 4. Relación entre fuente de tráfico y conversión

Se evaluó si `traffic_source` y `converted` presentan una asociación estadísticamente significativa.

Se utilizó:

- Tabla de contingencia.
- Prueba **Chi-cuadrada de independencia**.
- Comparación de volúmenes y tasas de conversión.
- Visualizaciones de barras agrupadas y apiladas.

### 5. Relación entre tipo de usuario y conversión

Se analizó la asociación entre `user_type` y `converted` mediante una prueba **Chi-cuadrada**.

### 6. Visualización de resultados

Se generaron visualizaciones para complementar los resultados estadísticos:

- Conversiones por fuente de tráfico.
- Tasas de conversión por fuente de tráfico.
- Conversiones por tipo de usuario.
- Tasas de conversión por tipo de usuario.

Estas visualizaciones permiten analizar tanto el **volumen absoluto** como la **eficiencia relativa** de cada segmento.

### 7. Insight ejecutivo y recomendaciones

Finalmente, los resultados se transformaron en conclusiones orientadas a stakeholders y recomendaciones de negocio.

---

## 🧰 Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Jupyter Notebook
- Google Colab

### Pruebas estadísticas utilizadas

- Prueba de Levene
- t-test de Welch
- Z-test para dos proporciones
- Chi-cuadrada de independencia

---

## 🔄 Guía breve de reproducción

Para reproducir el análisis:

1. Descargar el notebook.
2. Descargar `landing_experiment.csv`.
3. Colocar el CSV en una ubicación accesible para el notebook.
4. Abrir el notebook en Google Colab o Jupyter Notebook.
5. Verificar y ajustar la ruta del dataset si es necesario.
6. Instalar las dependencias indicadas.
7. Ejecutar las celdas en orden.
8. Revisar la exploración y validación inicial de los datos.
9. Reproducir la comparación del gasto promedio mediante Levene y t-test de Welch.
10. Reproducir la comparación de tasas de conversión mediante Z-test.
11. Reproducir las pruebas Chi-cuadrada para fuente de tráfico y tipo de usuario.
12. Revisar las visualizaciones y el insight ejecutivo final.

---

## 💡 Habilidades demostradas

### 🧪 Experimentación y A/B Testing

* Análisis de un experimento A/B para comparar el desempeño de dos versiones de una landing page.
* Definición y análisis de métricas de conversión.
* Comparación del comportamiento de los grupos A y B.
* Evaluación de resultados para apoyar una decisión de negocio basada en evidencia.

### 📊 Análisis estadístico

* Selección de pruebas estadísticas de acuerdo con la pregunta de negocio y el tipo de variable.
* Aplicación de **prueba de Levene** para evaluar la igualdad de varianzas.
* Aplicación de **t-test de Welch** para comparar el gasto promedio entre grupos.
* Aplicación de **Z-test para dos proporciones** para comparar tasas de conversión.
* Aplicación de **prueba Chi-cuadrada de independencia** para analizar asociaciones entre variables categóricas.
* Interpretación de valores p y significancia estadística.

### 🐍 Análisis de datos con Python

* Manipulación y análisis de datos utilizando **Pandas y NumPy**.
* Preparación y validación de datos.
* Cálculo de métricas y estadísticas.
* Uso de **SciPy y Statsmodels** para análisis estadístico.

### 📈 Visualización de datos

* Creación de visualizaciones para comparar conversiones y tasas de conversión.
* Análisis visual del desempeño según fuente de tráfico.
* Comparación del comportamiento según tipo de usuario.
* Uso de **Matplotlib y Seaborn** para comunicar resultados.

### 🔎 Análisis de segmentos

* Segmentación de resultados por **fuente de tráfico**.
* Análisis de conversión según **tipo de usuario**.
* Comparación entre volumen de conversiones y tasa de conversión.
* Identificación de segmentos con diferencias relevantes.

### 💼 Pensamiento analítico y de negocio

* Traducción de resultados estadísticos en conclusiones de negocio.
* Diferenciación entre **significancia estadística y relevancia de negocio**.
* Identificación de oportunidades para optimizar la conversión.
* Formulación de recomendaciones a partir de evidencia cuantitativa.
* Comunicación de resultados mediante un **insight ejecutivo**.

### 🔄 Reproducibilidad

* Desarrollo de un análisis estructurado en Jupyter Notebook.
* Documentación del proceso desde la exploración de datos hasta las recomendaciones.
* Aplicación de un flujo de trabajo reproducible:

**Datos → Validación → EDA → Pruebas estadísticas → Visualización → Insights → Recomendaciones**

## 👩‍💻 Autora

**Patricia Matute**

Data Analytics | Python | SQL | Power BI

Este proyecto forma parte de mi portafolio de proyectos de análisis de datos.

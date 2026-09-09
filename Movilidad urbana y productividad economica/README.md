# 🚦 Movilidad Urbana y Productividad Económica en Latinoamérica

## 🎯 Objetivo del proyecto

Evaluar cómo la **movilidad urbana** se relaciona con la **productividad económica** en las principales ciudades latinoamericanas, utilizando indicadores de congestión vehicular y datos económicos.

El objetivo es identificar patrones entre el **retraso generado por la congestión (`jams_delay`)** y el **PIB per cápita por ciudad (`city_gdp_capita`)**, para detectar ciudades en las que podría ser conveniente profundizar el análisis o priorizar inversiones en infraestructura de transporte.

> **Nota:** el análisis es exploratorio. Una relación observada entre dos variables no implica necesariamente causalidad.

---

## 📂 Datasets utilizados

- `tomtom_traffic.csv`
- `oecd_city_economy.csv`

## 🔎 Etapas del análisis

1. Carga y exploración inicial
2. Limpieza y preparación de datos
3. Filtrado del período de análisis
4. Agregación de indicadores de tráfico
5. Integración de movilidad y economía
6. Análisis visual
7. Interpretación y recomendaciones
8. Exportación del dataset final

## 🧰 Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Google Colab

---

## 🔄 Guía breve de reproducción

Para reproducir el proyecto:

1. Descargar el notebook:
   `S5 ladb_mobility_economy_project_student.ipynb`
2. Descargar los datasets:
   - `tomtom_traffic.csv`
   - `oecd_city_economy.csv`
3. Abrir el notebook en **Google Colab** o **Jupyter Notebook**.
4. Cargar los dos archivos CSV en el entorno de ejecución.
5. Verificar las rutas de acceso a los archivos. El notebook utiliza originalmente:
   ```python
   traffic = pd.read_csv('/datasets/tomtom_traffic.csv')
   eco = pd.read_csv('/datasets/oecd_city_economy.csv')
   ```
6. Si se utiliza Google Colab, modificar las rutas si los archivos fueron cargados en otra ubicación.
7. Ejecutar las celdas en orden.
8. Revisar la limpieza y transformación de los datasets.
9. Verificar la creación de `traffic_2024`, `eco_2024` y `traffic_city_year_2024`.
10. Comprobar la integración final en `merged`.
11. Revisar las visualizaciones y conclusiones.
12. Ejecutar la última sección para generar:
   `ladb_mobility_economy_2024_clean.csv`.

---

## 💡 Habilidades demostradas

### Data Analytics
- Exploratory Data Analysis (EDA)
- Data Cleaning
- Data Wrangling
- Data Transformation
- Data Integration
- Análisis de indicadores urbanos y económicos
- Interpretación de resultados

### Python
- Pandas
- NumPy
- Manipulación de DataFrames
- `groupby()` y agregaciones
- `merge()`
- Conversión de tipos de datos
- Exportación de datasets

### Visualización
- Boxplots
- Histogramas
- Gráficos de barras
- Identificación visual de outliers
- Comparación de indicadores

### Pensamiento analítico
- Formulación de preguntas de negocio
- Identificación de patrones
- Interpretación de resultados
- Identificación de limitaciones
- Generación de recomendaciones

### Reproducibilidad
- Documentación del proceso de análisis
- Preparación de datasets para análisis posterior
- Exportación de resultados

---

## 👩‍💻 Autora

**Patricia Matute**

Data Analytics | Python | SQL | Power BI

Este proyecto forma parte de mi portafolio de proyectos de análisis de datos.

# 📊 NovaRetail+ — Análisis de factores asociados al ingreso anual

## 🎯 Objetivo del proyecto

Analizar qué factores del comportamiento de los clientes están más fuertemente asociados con el **ingreso anual generado** por NovaRetail+, una plataforma de comercio electrónico en Latinoamérica.

El análisis tiene un enfoque **correlacional y exploratorio**: busca identificar relaciones entre variables de comportamiento y el ingreso anual, sin interpretar las asociaciones como relaciones de causa y efecto.

> **Importante:** correlación ≠ causalidad.

## 📂 Dataset utilizado

**`novaretail_comportamiento_clientes_2024.csv`**

El dataset contiene **15.000 registros y 12 variables**, sin valores faltantes.

| Variable | Descripción |
|---|---|
| `id_cliente` | Identificador único del cliente |
| `edad` | Edad del cliente |
| `nivel_ingreso` | Ingreso anual estimado del cliente |
| `visitas_mes` | Número de visitas mensuales |
| `compras_mes` | Número de compras mensuales |
| `gasto_publicidad_dirigida` | Gasto en anuncios asignado al usuario |
| `satisfaccion` | Calificación de satisfacción de 1 a 5 |
| `miembro_premium` | 1 si el cliente es Premium, 0 si no |
| `abandono` | 1 si abandonó la plataforma, 0 si no |
| `tipo_dispositivo` | Móvil, escritorio o tablet |
| `region` | Norte, sur, oeste o este |
| `ingreso_anual` | Ingreso anual generado por el cliente |

## 🔎 Etapas del análisis

### 1. Carga y exploración
- Carga del CSV.
- Revisión de estructura y dimensiones.
- Inspección de tipos de datos.
- Revisión de valores faltantes.
- Exploración de las primeras filas.

### 2. Preparación y limpieza
- Revisión de variables numéricas, binarias y categóricas.
- Conversión de `edad` de `float` a `int`.
- Validación de variables binarias y categóricas.

### 3. Análisis exploratorio (EDA)
- Estadísticas descriptivas.
- Distribución de edad e ingresos.
- Análisis de visitas y compras.
- Evaluación de satisfacción y publicidad dirigida.
- Análisis de membresía Premium y abandono.
- Distribución por dispositivo y región.

### 4. Visualización
- Heatmaps de correlación.
- Scatterplots para explorar relaciones entre variables.

### 5. Análisis estadístico
Se aplicaron diferentes métodos según el tipo de variable:
- **Pearson:** relaciones lineales entre variables numéricas.
- **Spearman:** relaciones monótonas.
- **Punto-biserial:** variable numérica frente a variable binaria.
- **V de Cramér:** asociación entre variables categóricas.

### 6. Interpretación de resultados
Los hallazgos se interpretaron desde una perspectiva de negocio, diferenciando asociación estadística de causalidad.

### 7. Limitaciones y próximos pasos
Se evaluaron posibles problemas de colinealidad, variables no medidas y oportunidades para futuros análisis y experimentos.

## 📈 Principales resultados

- `compras_mes` vs. `ingreso_anual`: **Pearson = 0.967**, una correlación positiva muy fuerte.
- `visitas_mes` vs. `ingreso_anual`: **Pearson = 0.337** y **Spearman = 0.321**, asociación positiva moderada.
- `miembro_premium` vs. `abandono`: **V de Cramér = 0.120**, asociación débil.
- El abandono observado fue **4.36% en clientes Premium** frente a **16.81% en clientes no Premium**.

Estos resultados describen asociaciones observadas en los datos; no permiten establecer relaciones causales.

## 🧰 Tecnologías utilizadas

- Python 3.9+
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook
- Google Colab

## ▶️ Cómo ejecutar el notebook

### Google Colab

1. Abre Google Colab.
2. Selecciona **Archivo → Subir cuaderno**.
3. Sube `S8_Student_Version_Project_NovaRetail.ipynb`.
4. Sube `novaretail_comportamiento_clientes_2024.csv`.
5. Revisa la ruta utilizada para cargar el CSV.
6. Ejecuta las celdas en orden.

El notebook originalmente utiliza:

```python
df = pd.read_csv("/datasets/novaretail_comportamiento_clientes_2024.csv")
```

En Google Colab puede ser necesario modificar esta ruta según la ubicación del archivo.

### Jupyter Notebook

Instala las dependencias:

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

Ejecuta:

```bash
jupyter notebook
```

Abre `S8_Student_Version_Project_NovaRetail.ipynb` y ejecuta las celdas secuencialmente.

## 🔄 Guía breve de reproducción

1. Descargar el notebook.
2. Descargar `novaretail_comportamiento_clientes_2024.csv`.
3. Colocar ambos archivos en un entorno accesible.
4. Abrir el notebook en Google Colab o Jupyter.
5. Verificar la ruta del CSV.
6. Instalar las dependencias.
7. Ejecutar las celdas en orden.
8. Revisar las estadísticas descriptivas y visualizaciones.
9. Reproducir las correlaciones de Pearson y Spearman.
10. Reproducir las asociaciones punto-biserial y V de Cramér.
11. Revisar las conclusiones, limitaciones y próximos pasos.

## ⚠️ Limitaciones

- Correlación no implica causalidad.
- La fuerte correlación entre `compras_mes` e `ingreso_anual` puede implicar colinealidad.
- Pueden existir variables no medidas, como promociones, valor promedio de compra, antigüedad del cliente o estacionalidad.
- Los resultados corresponden al conjunto de datos analizado y podrían variar en otros periodos o poblaciones.

## 👩‍💻 Autora

**Patricia Matute**

Data Analytics | Python | SQL | Power BI

Este proyecto forma parte de mi portafolio de proyectos de análisis de datos.

# Proyecto RappiPlus: De Datos a Decisiones de Negocio 🚀

## 🎯 Objetivo del Proyecto

Evaluar el desempeño operativo y financiero del servicio **RappiPlus**, identificando la rentabilidad del negocio, los cuellos de botella en la conversión de usuarios, los niveles de retención por cohortes y el impacto estadístico de experimentos en la plataforma.

---

## 📂 Datasets Utilizados

El proyecto integra múltiples fuentes de datos transaccionales, relacionales y de comportamiento:

* **`rappiplus_orders_raw.csv`**: Información de pedidos, productos, precios, descuentos y montos totales.
* **`rappiplus_catalog.csv`**: Catálogo de productos, categorías, costos unitarios y proveedores.
* **`rappiplus_marketing_spend.csv`**: Inversión publicitaria desglosada por canal, fecha y país.
* **Base de datos SQL (`events`, `users`, `user_activity`)**: Registros de navegación, funnel de eventos y retención de usuarios en la plataforma.
* **`experiment_checkout_ui.csv`**: Resultados de un experimento A/B aplicado sobre la interfaz de *checkout*.

---

## 📑 Etapas del Análisis

El proyecto sigue un flujo analítico riguroso estructurado en 6 pasos:

1. **🔍 Calidad y Limpieza de Datos (Python):** 
   * Tratamiento de valores faltantes/nulos mediante imputación informada por patrones e historiales.
   * Identificación y corrección de outliers o incongruencias numéricas en montos y cantidades.
   * Estandarización de variables categóricas, tipos de fecha y deduplicación de registros.
2. **💰 Análisis de Rentabilidad y KPIs Comercial (Python):** 
   * Cálculo de métricas financieras clave: *Revenue*, Costo Total, Inversión en Marketing, *Profit*, Margen de Ganancia, ROI de marketing, ticket promedio y productos promedio por pedido.
   * Evaluación de rendimiento por categoría, país y producto (identificando productos deficitarios).
3. **🛒 Análisis del Funnel de Conversión (SQL):** 
   * Construcción del embudo de conversión a partir de eventos en la plataforma.
   * Identificación del principal punto de pérdida de usuarios entre el paso de pago y la compra final.
4. **🔁 Análisis de Retención por Cohortes (SQL):** 
   * Agrupación de usuarios por mes de registro y seguimiento de actividad semanal (Semanas 1 a 4).
   * Identificación de patrones de retención constantes (~40%-43%).
5. **🧪 Validación de Experimentos A/B (Estadística):** 
   * Prueba de hipótesis mediante **Z-Test de proporciones** para evaluar el impacto del cambio de interfaz en la conversión.
   * Validación estadística del experimento, determinando la falta de significancia para el cambio.
6. **📊 Visualización e Insights de Negocio (Power BI):** 
   * Modelado de datos en Power BI con tabla calendario y medidas DAX avanzadas.
   * Diseño de Dashboards interactivos (Overview Ejecutivo y Vista Detallada) para monitorear el desempeño del negocio.
	**Detalle / Drill-Through:** Tabla a nivel de producto con formato condicional para identificar margen negativo, volumen de ventas y análisis de pricing bajo costo.

---

## 🛠️ Habilidades Demostradas

**Análisis de Datos y Estadística**
* Limpieza y manipulación de datos con **Python (Pandas, NumPy)**.
* Visualización de distribución de datos e inspección de outliers con **Matplotlib / Seaborn**.
* Pruebas de hipótesis y pruebas A/B con **Statsmodels (`proportions_ztest`)**.

**Bases de Datos y Consultas Avanzadas**
* Modelado de consultas analíticas complejas en **SQL (PostgreSQL / SQLAlchemy)**.
* Uso de Funciones de Agregación, Expresiones Comunes de Tabla (CTEs) y `LEFT JOINs` para la construcción de funnels y análisis de cohortes.

**Business Intelligence y Visualización**
* Diseño de informes interactivos en **Power BI**.
* Modelado en estrella (*Star Schema*) y creación de relaciones inter-tablas.
* Creación de medidas y cálculos temporales (YTD, YoY, MoM) con **DAX**.
* Traducción de hallazgos analíticos en recomendaciones estratégicas sobre *pricing* y retención de usuarios.


## 👩‍💻 Autora

**Patricia Matute**

Data Analytics | Python | SQL | Power BI

Este proyecto forma parte de mi portafolio de proyectos de análisis de datos.


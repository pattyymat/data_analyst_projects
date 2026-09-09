# 📊 Proyecto: Análisis Comercial e Inmobiliario (Grupo Andes)

## 📌 Objetivo del Proyecto
El objetivo principal de este proyecto es evaluar el desempeño comercial, la rentabilidad y el comportamiento de recurrencia de clientes para una empresa del sector inmobiliario. A través de la construcción de un dashboard ejecutivo e interactivo en Tableau, se busca dar respuesta a preguntas clave sobre ventas, canales de distribución, tipos de propiedades y cohortes de clientes para impulsar la toma de decisiones estratégicas basadas en datos.

---

## 📂 Datasets Utilizados
El proyecto se estructuró mediante un **Esquema Estrella** compuesto por las siguientes tablas:

* **`hecho_ventas_propiedades`:** Tabla transaccional central con registros de transacciones (precio de venta, comisión, cliente, propiedad, canal y fecha).
* **`dim_clientes`:** Tabla dimensional con la información sociodemográfica y segmentación de clientes.
* **`dim_propiedades`:** Tabla dimensional con atributos de las propiedades (tipo de inmueble, tamaño, ubicación).
* **`dim_fecha`:** Jerarquías temporales integradas nativamente mediante el campo `fecha_venta` para el análisis de tendencias y métricas de inteligencia de tiempo.

---

## 🛠️ Etapas del Análisis Realizadas

### 1. 🧹 Limpieza y Validación de Datos
* Verificación de claves primarias en `dim_clientes` y `dim_propiedades` para garantizar la ausencia de registros duplicados.
* Configuración de tipos de datos adecuados (fechas en formato *Date*, valores monetarios formateados y `porcentaje_comision` en formato de porcentaje).
* Auditoría de valores nulos para asegurar la integridad de la base de datos.

### 2. 🧩 Modelado de Datos
* Construcción de un **Esquema Estrella** relacionando la tabla de hechos `hecho_ventas_propiedades` con las dimensiones de clientes y propiedades mediante relaciones de cardinalidad **uno a muchos (1:*)**.

### 3. 📊 Creación de Campos Calculados y Medidas
* **Métricas Base:** Cálculo de *Ingreso Total*, *Cantidad de Ventas*, *Ticket Promedio*, *Comisión Total* y YoY%.
* **Modificación de Contexto y Participación (%):** Implementación de **Expresiones LOD (`FIXED`)** para calcular la contribución relativa por tipo de propiedad, canal de venta y segmento de cliente sin alterar los filtros aplicados.
* **Inteligencia de Tiempo:** Cálculo de métricas interanuales como el Crecimiento **Year-over-Year (YoY)** y rendimiento acumulado **Year-to-Date (YTD)**.
* **Lógica para Análisis de Cohortes:** Creación de columnas calculadas para determinar la *Primera compra por cliente*, el *Mes Cohorte* y el *Mes Venta*.

### 4. 📈 Estructuración e Implementación del Dashboard (Tableau)
El reporte se organizó en 3 vistas principales:
1. **Overview Ejecutivo:** Tarjetas de KPI principales, evolución de ventas en el tiempo y rendimiento por ciudad (México vs. Bogotá).
2. **Análisis Comercial:** Desglose de ingresos por canal, segmento de cliente y tipo de propiedad con tablas enriquecidas mediante formato condicional semáforo y *Tooltips* interactivos.
3. **Análisis de Cohortes:** Matriz térmica para monitorear la tasa de retención y compras recurrentes mes a mes por cohorte de adquisición.

---

## 🏆 Habilidades Demostradas

* **Tableau Desktop / Tableau Public:** Diseño UX/UI para dashboards ejecutivos, mapas de calor, matrices de cohortes y formato condicional.
* **Cálculos Avanzados en Tableau:** Expresiones de Nivel de Detalle (**LOD `FIXED`**), agregaciones personalizadas, campos de fecha calculados e indicadores interanuales YoY.
* **Modelado de Datos:** Arquitectura de Esquema Estrella y gestión de relaciones de base de datos.
* **Análisis Estadístico y de Negocio:** Análisis de cohortes (retención), segmentación de mercado y evaluación de rendimiento comercial.

---

## 👩‍💻 Autora

**Patricia Matute**

Data Analytics | Python | SQL | Power BI

Este proyecto forma parte de mi portafolio de proyectos de análisis de datos.

🔗 **[Ver Dashboard Interactivo en Tableau Public](https://public.tableau.com/views/Sprint11-Proyecto/DesempeoGeneral?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**
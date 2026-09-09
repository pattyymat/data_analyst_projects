# 📊 Dashboard de Desempeño Comercial (2024–2025) - Andes Retail Group

> **Proyecto de Portafolio - Análisis de Datos & Business Intelligence**  
> *Herramientas:* Power BI / Power Query / DAX / Excel  
> *Dominio:* Retail & Análisis Comercial

---

## 🎯 Objetivo del Proyecto
El objetivo de este proyecto es analizar el desempeño comercial de la empresa **Andes Retail Group** durante el periodo **2024–2025** para responder preguntas estratégicas sobre la evolución de los ingresos, el volumen de ventas, la rentabilidad y el comportamiento de los clientes. 

A través del desarrollo de un dashboard interactivo de dos niveles (Visión General y Detalle Analítico), se busca identificar patrones estacionales, oportunidades de crecimiento por mercado y segmentación de productos/clientes para guiar la toma de decisiones directivas basada en datos.

---

## 📂 Datasets Utilizados y Estructura
- **Fuente de Datos:** Archivo Excel (`Andes_Retail_Group_2024_2025.xlsx`)
- **Variables Clave:**
  * **Variables / Columnas clave:**
  * `ID_Pedido`: Identificador único de la transacción.
  * `ID_Cliente`: Identificador del cliente.
  * `Fecha_pedido`: Fecha en la que se realizó la compra.
  * `País`: Mercado/ubicación geográfica (ej. Perú, Chile, etc.).
  * `Segmento de cliente`: Categorización del cliente (ej. Premium, Estándar).
  * `Categoría de Producto`: Clasificación de los productos vendidos.
  * `Ingresos`: Venta bruta total (métrica numérica).
  * `Utilidad`: Ganancia neta generada (métrica numérica).
  * `Unidades Vendidas`: Volumen de artículos en el pedido.
  * `Nivel_Venta`: Columna calculada/derivada mediante regla de negocio.

---

## 🔬 Etapas del Análisis Realizadas

### 1. Exploración e Ingesta de Datos
* Conexión del archivo de datos a Power BI Desktop.
* Auditoría de estructura, identificación de claves primarias y validación inicial de campos.

### 2. Preparación y Transformación de Datos (ETL)
* **Ajuste Regional:** Configuración de la columna `Fecha_pedido` a formato fecha en *Español (Latinoamérica)*.
* **Normalización de Tipos:** Conversión de columnas numéricas (`Ingresos`, `Utilidad`, `Unidades Vendidas`) a formatos de moneda/entero.
* **Lógica de Negocio (`Nivel_Venta`): ** Creación de columna condicional:
  - Si `Ingresos` ≥ 1000 ➔ `"Venta Alta"`
  - De lo contrario ➔ `"Venta Baja"`
* **Control de Calidad:** Activación del *Perfil de Columna* en Power Query para verificar la ausencia de inconsistencias o valores nulos.

### 3. Diseños y Planificación del Dashboard
Estructuración de la solución en dos pestañas estratégicas:
* **Vista 1: Overview Ejecutivo (Visión General)**
  * **KPIs Directivos:** Ingresos Totales, Unidades Vendidas, Utilidad y Margen (%).
  * **Evolución Temporal:** Gráfico de líneas para evaluar la tendencia de ingresos 2024–2025.
  * **Análisis Combinado (Ingresos vs Utilidad):** Gráficos de columnas con eje Y secundario para evaluar volumen vs. rentabilidad por **País**, **Segmento de Cliente** y **Categoría de Producto**.
* **Vista 2: Análisis Detallado**
  * **Análisis de Estacionalidad:** Gráficos de líneas temporales por mes/estación para diagnosticar caídas o incrementos periódicos.
  * **Tabla Operativa (7 Columnas agregadas):** Conteo de `ID_Pedido`, Conteo Único de `ID_Cliente`, `País`, `Segmento`, `Categoría`, Suma de `Ingresos` y Suma de `Utilidad`.

### 4. Construcción y Modelado (DAX)
* Definición de medidas DAX para cálculo dinámico de métricas principales e índices de rentabilidad.
* Aplicación de jerarquía visual (priorización de KPIs superiores, gráficos generales al centro, filtros en panel lateral).

### 5. Narrativa de Datos (Modelo SCQA) e Insights
* **Diagnóstico General:** Negocio estable con mayor peso en segmentos **Premium** y **Estándar** en los mercados de **Perú** y **Chile**.
* **Hallazgo Clave:** Caída pronunciada de ingresos durante la época de **invierno** en Perú y Chile, así como variabilidad temporal en segmentos Premium y Estándar.
* **Comunicación:** Elaboración de un resumen ejecutivo sintetizado formato Slack para alineación de stakeholders.

---

## 🧠 Principales Aprendizajes
Este proyecto permitió consolidar habilidades técnicas y de pensamiento analítico en el ciclo de vida del análisis de datos:

1. **Diseño Orientado al Usuario (UX para BI):** Aprendí a estructurar la información jerárquicamente diferenciando entre un nivel directivo (*Overview*) y uno táctico (*Detalle*), respondiendo preguntas de negocio específicas sin saturar visualmente al usuario.
2. **Análisis de Rentabilidad vs. Ingreso Bruto:** Comprendí la importancia de evaluar gráficos combinados (Ingresos vs. Utilidad/Margen), evitando tomar decisiones basadas únicamente en el volumen de ventas sin considerar la ganancia real.
3. **Detección de Patrones de Estacionalidad:** Desarrollé sensibilidad analítica para identificar fluctuaciones periódicas en los datos (como la caída estacional de invierno) y traducirlas en oportunidades comerciales concretas.
4. **Transformación Eficiente con Power Query:** Reforcé buenas prácticas en la etapa ETL, incluyendo tipado estricto, lógica condicional eficiente y parametrización regional para evitar errores de interpretación de fechas.
5. **Comunicación Ejecutiva con SCQA:** Mejoré la habilidad para traducir hallazgos técnicos complejos en narrativas breves y accionables para la toma de decisiones directivas mediante el modelo Situación-Complicación-Pregunta-Respuesta.



## 👩‍💻 Autora

**Patricia Matute**

Data Analytics | Python | SQL | Power BI

Este proyecto forma parte de mi portafolio de proyectos de análisis de datos.

#  Retail Analytics Pipeline with Apache Spark

##  Descripción del Proyecto

Este proyecto implementa un pipeline completo de análisis de datos y Machine Learning utilizando Apache Spark, aplicado a un entorno de e-commerce.

El objetivo es procesar grandes volúmenes de datos, generar métricas de negocio y construir modelos escalables que permitan comprender y predecir el comportamiento de los usuarios.

---

##  Objetivos

* Procesar datos masivos en un entorno distribuido
* Aplicar transformaciones con RDDs y DataFrames
* Realizar análisis con Spark SQL
* Construir modelos de Machine Learning con MLlib
* Generar insights accionables para marketing

---

##  Arquitectura del Pipeline

```
Fuentes de Datos (CSV)
        ↓
Ingesta con Spark
        ↓
Procesamiento (RDDs + DataFrames)
        ↓
Análisis con Spark SQL
        ↓
Feature Engineering
        ↓
Machine Learning (MLlib)
        ↓
Resultados e Insights
```

---

##  Estructura del Proyecto

```
 project/
│
├── L1_BigData.ipynb
├── L2_SparkConfig.ipynb
├── L3_RDD.ipynb
├── L4_DataFrames_SQL.ipynb
├── L5_SparkMLlib.ipynb
│
├── data/
│   ├── ecommerce_client_data.csv
│   └── visitor_metrics.csv
│
└── README.md
```

---

##  Tecnologías utilizadas

* Apache Spark (PySpark)
* Python
* Spark SQL
* Spark MLlib
* Pandas (exportación alternativa)

---

##  Dataset

Se utilizó un dataset de comportamiento de usuarios en e-commerce que incluye:

* Interacciones de navegación
* Variables de comportamiento (BounceRate, PageValues, etc.)
* Tipo de visitante (VisitorType)
* Conversión (Revenue)

---

##  Desarrollo por etapas

### 🔹 Lección 1: Fundamentos de Big Data

* Análisis de las 5V
* Identificación de fuentes de datos
* Diseño de arquitectura

---

### 🔹 Lección 2: Configuración de Spark

* Inicialización de SparkSession
* Creación de RDDs
* Primeras acciones y validaciones

---

### 🔹 Lección 3: RDDs, Transformaciones y Acciones

* Uso de map, filter, flatMap, distinct, sortBy
* Creación de Pair RDDs
* Cálculo de métricas (sum, mean, stdev)
* Análisis del DAG

---

### 🔹 Lección 4: DataFrames y Spark SQL

* Conversión de RDD a DataFrame
* Definición de esquema
* Consultas SQL
* Agregaciones de negocio

 Resultado clave:

```
VisitorType, avg_page_value
Other → 18.19
New_Visitor → 10.77
Returning_Visitor → 5.00
```

---

### 🔹 Lección 5: Machine Learning con MLlib

#### 🔸 Modelo supervisado

* Regresión Logística
* Predicción de conversión (Revenue)
* Evaluación con AUC

#### 🔸 Modelo no supervisado

* K-Means
* Segmentación de usuarios

#### 🔸 Feature Engineering

* Incorporación de métricas agregadas (`avg_page_value`)

---

## 📈 Insights de negocio

* Los usuarios tipo **"Other"** generan mayor valor promedio
* Los **New Visitors** tienen alto potencial de conversión
* Los **Returning Visitors** presentan menor valor promedio → oportunidad de upselling

Aplicaciones:

* Segmentación de clientes
* Personalización de campañas
* Optimización del funnel de conversión

---

##  Consideraciones técnicas

Debido a limitaciones del entorno local en Windows (configuración de Hadoop), no fue posible persistir datos en formato Parquet.

Como alternativa, se utilizó CSV para garantizar la ejecución completa del pipeline.

 En entornos productivos se recomienda:

* Uso de Parquet
* Cluster distribuido
* Optimización con Catalyst

---

##  Conclusión

El proyecto demuestra la integración de Big Data y Machine Learning en un flujo completo utilizando Apache Spark.

Se logró:

* Procesar grandes volúmenes de datos
* Generar métricas relevantes
* Construir modelos escalables
* Obtener insights accionables

---

##  Autor

Proyecto desarrollado como parte del módulo de Big Data y Machine Learning.

---

##  Próximos pasos

* Implementación en entorno cluster
* Uso de Parquet y optimización de storage
* Deploy de modelos en producción
* Integración con dashboards (Power BI / Tableau)

---

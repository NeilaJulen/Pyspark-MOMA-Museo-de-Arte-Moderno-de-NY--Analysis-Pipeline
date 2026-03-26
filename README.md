# Pyspark-MOMA-Museo-de-Arte-Moderno-de-NY--Analysis-Pipeline
Pipeline de ETL y análisis avanzado de la colección del MoMA utilizando PySpark. Implementación de transformaciones complejas, UDFs, funciones de ventana y discretización de datos.

# MoMA Collection Analysis with PySpark 🎨⚡

Este proyecto realiza un proceso de ETL (Extract, Transform, Load) y análisis exploratorio avanzado sobre el dataset de la colección del **Museo de Arte Moderno (MoMA)** de Nueva York, utilizando **Apache Spark**.

## 🎯 Objetivo del Proyecto
El objetivo es transformar un dataset crudo y complejo (con múltiples autores por obra y formatos de fecha inconsistentes) para analizar la productividad de los artistas según su rango de edad y década de nacimiento.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python
* **Motor de Procesamiento:** Apache Spark (PySpark SQL & MLlib)
* **Entorno:** Jupyter Notebook / Databricks

## 🚀 Desafíos Técnicos Resueltos
En este análisis se aplicaron técnicas avanzadas de procesamiento de datos masivos:

* **Manejo de Tipos Complejos:** Uso de `arrays_zip` y `explode` para normalizar obras con múltiples autores, transformando estructuras anidadas en un modelo relacional plano.
* **Limpieza con Regex:** Implementación de `regexp_replace` y `regexp_extract` para la limpieza de años y biografías.
* **UDFs Personalizadas:** Creación de *User Defined Functions* para validación lógica de tipos de datos dentro de estructuras de Spark.
* **Funciones de Ventana (Window Functions):** Cálculo de estadísticas agregadas (medianas) por partición de autor sin necesidad de realizar `JOINs` costosos.
* **Feature Engineering:** Uso de `Bucketizer` y `Pipelines` de Spark ML para la discretización de variables continuas en categorías generacionales.

## 📊 Insights Obtenidos
El análisis final permite visualizar la distribución porcentual de la creación de obras de arte a lo largo del ciclo de vida de los artistas, segmentado por su época de nacimiento.

## 📁 Dataset
El dataset original puede encontrarse en [Kaggle - MoMA Post-War and Contemporary Art](https://www.kaggle.com/momanyc/museum-collection). 
*Nota: Por razones de tamaño y licencias, el archivo CSV no se incluye en este repositorio.*

---
Desarrollado con fines analíticos para demostrar capacidades en Ingeniería de Datos.

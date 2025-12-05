# Análisis y Visualización de Reembolsos de Trayectos

## 1. Resumen y Objetivos
Este proyecto se enfoca en el análisis de los gastos de traslado y el proceso de reembolso asociado a los trayectos laborales de una persona que se desplaza frecuentemente entre la Quinta Región y la Tercera Región de Chile. El objetivo principal es visualizar la eficiencia del proceso de reembolso, cuantificar el Gasto No Cubierto, e identificar los trayectos más costosos.
Una regla de negocio crucial es el límite de reembolso de $150.000 por cada subida de gasto.

## 2. Tecnologías y Herramientas
Herramienta	Función Principal
Excel	Almacenamiento inicial de los registros de trayectos.
Python	Consolidación de múltiples archivos de datos de subidas individuales.
Power BI	Modelado, limpieza (Power Query), creación de métricas (DAX), y visualización de datos geográficos.

## 3. Desarrollo y Metodología de Datos
El proceso inicia con el registro de cada solicitud de reembolso. Inicialmente, los datos se encuentran dispersos en múltiples archivos Excel; cada archivo representa una subida de reembolso individual (ej. 09-09-2025.xlsx).
### A. Consolidación (Python)
Se implementa un script de Python para unir todos los archivos Excel en un único dataset general, lo que permite un análisis consolidado de todos los trayectos y gastos.
### B. Transformación y Métricas (Power BI)
La tabla unificada se importa a Power BI para su depuración y la creación de métricas clave. El proceso de Power Query se centra en la limpieza de datos y la garantía de su calidad.
Para el análisis, se crearon métricas en DAX que cuantifican:
#### 1.	Reembolso_Real: El monto efectivamente devuelto (máximo de $150.000).
#### 2.	Gasto No Cubierto: La diferencia entre el valor del gasto y el monto reembolsado.
#### 3.	Tabla Calendario: permitir los filtros temporales.

### 4. Resultados y Análisis Clave
El dashboard de Power BI proporciona una visión clara de la dinámica de gastos y la exposición al límite de reembolso.
#### •	Métricas Globales:
##### o	Gasto Total: $2.280.957.
##### o	Reembolso Total: $2.004.618.
##### o	Gasto No Cubierto: La diferencia acumulada asciende a $276.339.
#### •	Impacto del Límite:
##### o	42,86% de los casos (6 transacciones) se ubicaron "Sobre-Tope", lo que significa que el costo del trayecto superó el límite de $150.000, generando un gasto no cubierto para el usuario4444.
##### o	Solo el 35,71% (5 transacciones) estuvo "Tope" (igual o por debajo del valor reembolsado).
#### •	Trayectos Más Costosos: El análisis de los trayectos más caros indica que los viajes del 3 de noviembre ($231.056) y el del día 12 de octubre ($195.788) son las de mayor valor.
#### •	Visualización Geográfica: El mapa de trayecto muestra claramente los puntos de origen y destino más frecuentes, concentrándose la actividad entre la Región de Valparaíso (Villa Alemana / La Calera) y la Región de Atacama (Copiapó / El Salvador).


# Sistema de análisis de riesgo crediticio

## Descripción general

Este proyecto fue diseñado como un caso más realista sobre cómo podría organizarse, revisarse, limpiarse y monitorearse información crediticia dentro de un contexto bancario para apoyar la evaluación de solicitudes de préstamo.

El objetivo principal fue simular cómo un analista puede ayudar a la toma de decisiones identificando perfiles de mayor o menor riesgo a partir de variables como:

- finalidad del préstamo
- tipo de vivienda
- ingresos del solicitante
- monto solicitado
- tasa de interés
- historial crediticio
- antecedentes de incumplimiento

Más que enfocarse únicamente en la predicción, el proyecto fue estructurado como un sistema de apoyo a la decisión que combina organización de datos, limpieza, análisis y visualización orientada al negocio.

## Contexto del problema

En un entorno bancario real, las decisiones de aprobación de crédito no dependen de una sola variable. Requieren revisar el perfil financiero del solicitante, las características del préstamo solicitado y señales asociadas a su comportamiento crediticio previo.

Este proyecto explora cómo la información histórica puede transformarse en un sistema estructurado de apoyo para responder preguntas como:

- ¿Qué perfiles de solicitantes parecen más confiables?
- ¿Qué factores se asocian con mayor riesgo de incumplimiento?
- ¿Qué casos requieren una revisión más cuidadosa?
- ¿Cómo pueden los patrones históricos apoyar un proceso de evaluación más ordenado?

## Objetivo del proyecto

El objetivo de este trabajo fue construir un flujo aplicado de análisis de riesgo crediticio capaz de:

- organizar mejor la información disponible
- detectar problemas en la base original
- limpiar los datos sin alterar la fuente original
- comparar la base antes y después de la limpieza
- entregar un dashboard interactivo para revisión de negocio
- preparar una base más confiable para una futura etapa predictiva

## Fuente de datos

El proyecto utiliza una base pública de riesgo crediticio obtenida originalmente desde Kaggle y reutilizada como caso práctico de portafolio para fines de análisis y experimentación.

Fue seleccionada porque contiene suficientes variables demográficas, financieras y crediticias para simular un flujo de evaluación de crédito relativamente realista, permitiendo desarrollar análisis descriptivo, revisión de calidad de datos y una futura etapa de modelamiento.

Entre las variables principales se encuentran:

- edad del solicitante
- ingreso anual
- tipo de vivienda
- antigüedad laboral
- finalidad del préstamo
- calificación crediticia del préstamo
- monto solicitado
- tasa de interés
- estado histórico del préstamo
- proporción del préstamo respecto al ingreso
- antecedentes de incumplimiento
- antigüedad del historial crediticio

## ¿Por qué se utilizó primero Google Sheets?

La primera etapa del proyecto se desarrolló en Google Sheets.

Esta decisión se tomó intencionalmente para:

- organizar mejor la base de datos
- inspeccionar la información con mayor control visual
- filtrar registros de manera dinámica
- revisar estadísticos descriptivos de forma más clara
- identificar patrones, datos faltantes y valores atípicos con mayor cuidado
- definir reglas de limpieza antes de pasar a Python

Además, se construyó una hoja de apoyo con identificadores específicos para revisar observaciones problemáticas de forma más ordenada y detectar con mayor claridad dónde estaban los principales errores o anomalías de la base.

Esta etapa fue especialmente útil para entender la calidad de los datos antes de automatizar la limpieza.

## Estrategia de limpieza

Una vez terminada la revisión inicial, la limpieza se realizó en Python.

Esta decisión fue importante por dos motivos:

1. permitir que el proceso de limpieza fuera reproducible y transparente  
2. evitar modificar o perder la base de datos original

En lugar de sobrescribir la fuente original, se generó una tabla auxiliar limpia. Esto permitió:

- conservar la base cruda
- documentar con claridad la lógica de limpieza
- comparar la base antes y después del tratamiento
- utilizar datos limpios tanto en Python como en Google Sheets sin eliminar registros de la fuente original

La limpieza se centró en aspectos como:

- valores poco realistas
- datos faltantes
- outliers sospechosos
- campos que requerían estandarización para análisis posteriores

## Flujo de trabajo analítico

El flujo seguido en este proyecto puede resumirse así:

1. Revisión de la base original en Google Sheets  
2. Exploración de estadísticos descriptivos y revisión visual de valores problemáticos  
3. Definición de criterios de limpieza en función de la interpretación de negocio  
4. Aplicación de reglas de limpieza en Python, conservando la fuente original  
5. Comparación de la base antes y después de la limpieza  
6. Exportación de una versión limpia para análisis y visualización  
7. Construcción de un dashboard interactivo para revisión gerencial

## Propósito del dashboard

Después de la etapa de limpieza, la información fue visualizada en un dashboard diseñado para apoyar la revisión de negocio.

El dashboard permite a un supervisor o tomador de decisiones filtrar e inspeccionar los casos de forma más dinámica, incluyendo aspectos como:

- clientes que ya cumplieron correctamente con sus pagos
- solicitantes con historial negativo
- patrones de riesgo según la finalidad del préstamo
- comportamiento del riesgo según el tipo de vivienda
- carga del préstamo respecto al ingreso
- segmentos que podrían requerir mayor atención

El objetivo del dashboard no es reemplazar el criterio del analista, sino hacer el proceso de revisión más estructurado, rápido y fácil de interpretar.

## Recursos visuales

### Flujo de trabajo en Google Sheets

Video corto mostrando cómo se utilizó la hoja de cálculo para ordenar, filtrar y revisar la información antes de la limpieza en Python.

[Ver video del flujo en Google Sheets](https://youtu.be/0oH_PFn1qwk)

### Recorrido del dashboard en Tableau

Video corto mostrando cómo se puede explorar la información ya limpia desde el dashboard interactivo.

[Ver video del dashboard en Tableau](https://youtu.be/8y5rvR5nX7c)

### Versión interactiva del dashboard

[Ver dashboard en Tableau Public](https://public.tableau.com/views/Analisis_Riesgo_Crediticio/RiesgoCrediticio?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Herramientas utilizadas

- Google Sheets
- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Tableau Public
- SQLite

## Entregables del proyecto

Actualmente, este proyecto incluye:

- base de datos original
- base de datos limpia
- notebook de análisis exploratorio y limpieza
- documentación del proceso de limpieza
- capa de apoyo en Google Sheets
- dashboard interactivo en Tableau

## Recursos interactivos

- Hoja de apoyo en Google Sheets:  
  [Ver Google Sheets](https://docs.google.com/spreadsheets/d/1c2M-y9EaVsJferSnKHW8X4KZPHc7syRw1yLrfvo3NxQ/edit?gid=311571590#gid=311571590)

- Dashboard interactivo en Tableau:  
  [Ver Tableau Dashboard](https://public.tableau.com/views/Analisis_Riesgo_Crediticio/RiesgoCrediticio?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Próximo paso

La siguiente etapa del proyecto consiste en utilizar la base limpia como soporte para futuros ejercicios de modelamiento predictivo, incluyendo la posible construcción de una red neuronal orientada a la estimación del riesgo crediticio.

La intención es mantener primero una base sólida de interpretación de negocio y análisis de datos, para luego extender el proyecto hacia machine learning como una capa complementaria.

# 🏦 Sistema de análisis de riesgo crediticio

> Caso práctico orientado a la evaluación de solicitudes de crédito mediante organización de datos, limpieza analítica y visualización para apoyo a la toma de decisiones.

## ✨ Resumen ejecutivo

Este proyecto fue construido como una simulación más realista de cómo podría gestionarse información crediticia dentro de un entorno bancario para apoyar la evaluación de préstamos.

La idea central fue responder una pregunta simple pero relevante:

**¿Cómo apoyar la decisión de otorgar o revisar un crédito usando información histórica del solicitante y del préstamo?**

Para ello, el proyecto se estructuró como un sistema de apoyo a la decisión que combina:

- 📋 organización y revisión visual en Google Sheets
- 🐍 limpieza y trazabilidad en Python
- 📊 visualización ejecutiva e interactiva en Tableau
- 🧠 base analítica preparada para una futura etapa predictiva

---

## 🎯 Objetivo del proyecto

Desarrollar un flujo de trabajo aplicado para analizar riesgo crediticio y transformar una base de datos cruda en una herramienta más útil para revisión de negocio.

Este sistema busca ayudar a identificar perfiles de mayor o menor riesgo a partir de variables como:

- finalidad del préstamo
- tipo de vivienda
- ingresos del solicitante
- monto solicitado
- tasa de interés
- historial crediticio
- antecedentes de incumplimiento

Más que enfocarse solo en predecir, el proyecto fue pensado para **ordenar, limpiar, interpretar y comunicar** mejor la información.

---

## 🧩 Contexto del problema

En un escenario bancario real, la evaluación de solicitudes no depende de una sola variable. Un analista necesita revisar el perfil del solicitante, las condiciones del préstamo y señales asociadas a su comportamiento crediticio previo.

A partir de esa lógica, este proyecto busca apoyar preguntas como:

- ¿Qué perfiles parecen más confiables?
- ¿Qué factores se relacionan con mayor riesgo de incumplimiento?
- ¿Qué casos requieren una revisión más cuidadosa?
- ¿Cómo ordenar mejor la evaluación de solicitudes usando información histórica?

---

## 🗂️ Flujo general del proyecto

| Etapa | Herramienta principal | Propósito |
|---|---|---|
| Revisión inicial | Google Sheets | Ordenar, filtrar y detectar problemas visualmente |
| Limpieza de datos | Python | Aplicar reglas reproducibles sin alterar la base original |
| Comparación antes/después | Python | Validar cómo cambió la base tras la limpieza |
| Visualización final | Tableau | Facilitar la revisión ejecutiva e interactiva |
| Siguiente etapa | Modelamiento | Preparar una futura red neuronal predictiva |

---

## 🧾 Fuente de datos

El proyecto utiliza una base pública de riesgo crediticio obtenida originalmente desde Kaggle y reutilizada como caso práctico de portafolio.

Se eligió porque contiene suficientes variables demográficas, financieras y crediticias para simular un flujo de evaluación razonablemente realista.

### Variables utilizadas

| Nombre original | Traducción / interpretación | ¿Qué aporta al análisis? |
|---|---|---|
| `person_age` | Edad del solicitante | Ayuda a contextualizar el perfil del cliente |
| `person_income` | Ingreso anual | Permite evaluar capacidad económica |
| `person_home_ownership` | Tipo de vivienda | Entrega contexto patrimonial y estabilidad |
| `person_emp_length` | Antigüedad laboral | Aporta señales sobre estabilidad laboral |
| `loan_intent` | Finalidad del préstamo | Permite segmentar el riesgo según propósito |
| `loan_grade` | Calificación del préstamo | Resume una evaluación crediticia previa |
| `loan_amnt` | Monto solicitado | Permite medir exposición financiera |
| `loan_int_rate` | Tasa de interés | Ayuda a contextualizar costo y riesgo del crédito |
| `loan_status` | Estado histórico del préstamo | Variable clave para analizar cumplimiento/incumplimiento |
| `loan_percent_income` | Proporción préstamo / ingreso | Mide carga financiera relativa |
| `cb_person_default_on_file` | Antecedentes de incumplimiento | Señal directa de riesgo histórico |
| `cb_person_cred_hist_length` | Antigüedad del historial crediticio | Entrega contexto sobre experiencia financiera |

---

## 📋 ¿Por qué se utilizó primero Google Sheets?

La primera etapa del proyecto se trabajó en Google Sheets para tener una revisión más visual, ordenada y controlada de la base.

Esto permitió:

- filtrar registros dinámicamente
- revisar estadísticos descriptivos con mayor claridad
- detectar datos faltantes y valores atípicos
- construir reglas iniciales de limpieza antes de pasar a Python
- identificar observaciones problemáticas con una hoja auxiliar y un ID personalizado

En otras palabras, Google Sheets funcionó como una **capa previa de inspección y criterio de negocio**.

---

## 🧼 Estrategia de limpieza

Después de la revisión inicial, la limpieza se realizó en Python.

Esto se hizo por dos razones clave:

1. mantener el proceso de limpieza de forma **reproducible y transparente**
2. evitar alterar o perder la **base de datos original**

En lugar de sobrescribir la fuente inicial, se creó una tabla auxiliar limpia. Esto permitió:

- conservar la base cruda
- documentar las decisiones tomadas
- comparar el antes y el después
- reutilizar datos limpios en Python, Tableau y Google Sheets

La limpieza se centró en:

- valores poco realistas
- datos faltantes
- outliers sospechosos
- campos que requerían estandarización

---

## 📈 ¿Qué entrega el dashboard?

Luego de la limpieza, los datos fueron integrados en un dashboard para apoyar la revisión ejecutiva.

Este tablero permite explorar de forma dinámica aspectos como:

- clientes que ya cumplieron correctamente sus pagos
- solicitantes con historial negativo
- patrones de riesgo según finalidad del préstamo
- comportamiento del riesgo según tipo de vivienda
- carga del préstamo respecto al ingreso
- segmentos que podrían requerir mayor atención

El objetivo no es reemplazar al analista, sino **hacer la revisión más clara, rápida y estructurada**.

---

## 🎥 Recursos visuales

### Google Sheets · flujo de trabajo

[![Ver video del flujo en Google Sheets](https://img.youtube.com/vi/0oH_PFn1qwk/hqdefault.jpg)](https://youtu.be/0oH_PFn1qwk)

Video corto mostrando cómo se utilizó la hoja de cálculo para ordenar, filtrar y revisar la información antes de la limpieza en Python.

### Tableau · recorrido del dashboard

[![Ver video del dashboard en Tableau](https://img.youtube.com/vi/8y5rvR5nX7c/hqdefault.jpg)](https://youtu.be/8y5rvR5nX7c)

Video corto mostrando cómo se puede explorar la información ya limpia desde el dashboard interactivo.

### Tableau Public · versión interactiva

🔗 [Ver dashboard en Tableau Public](https://public.tableau.com/views/Analisis_Riesgo_Crediticio/RiesgoCrediticio?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 🛠️ Herramientas utilizadas

- Google Sheets
- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Tableau Public
- SQLite

---

## 📦 Entregables del proyecto

Actualmente, este proyecto incluye:

- base de datos original
- base de datos limpia
- notebook de análisis exploratorio y limpieza
- documentación del proceso de limpieza
- capa de apoyo en Google Sheets
- dashboard interactivo en Tableau

---

## 🔗 Recursos interactivos

- 📄 [Hoja de apoyo en Google Sheets](https://docs.google.com/spreadsheets/d/1c2M-y9EaVsJferSnKHW8X4KZPHc7syRw1yLrfvo3NxQ/edit?gid=311571590#gid=311571590)
- 📊 [Dashboard interactivo en Tableau](https://public.tableau.com/views/Analisis_Riesgo_Crediticio/RiesgoCrediticio?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 🚀 Próximo paso

La siguiente etapa del proyecto consiste en utilizar la base limpia como soporte para futuros ejercicios de modelamiento predictivo, incluyendo la posible construcción de una red neuronal orientada a la estimación del riesgo crediticio.

La idea es mantener primero una base sólida de interpretación de negocio y análisis de datos, para luego extender el proyecto hacia machine learning como una capa complementaria.

# Sistema de análisis de riesgo crediticio

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

## Descripción del proyecto

Este proyecto fue construido como un caso práctico para simular cómo podría organizarse, limpiarse, analizarse y visualizarse información crediticia dentro de un contexto bancario.

La idea principal fue desarrollar un sistema de apoyo a la decisión que ayude a evaluar solicitudes de crédito a partir de variables como la finalidad del préstamo, tipo de vivienda, ingresos, monto solicitado, tasa de interés e historial crediticio.

Más que enfocarse solo en predecir, el proyecto busca responder una pregunta concreta:

**¿Cómo transformar una base de datos cruda en una herramienta útil para revisar perfiles de riesgo de forma más clara, ordenada y accionable?**

---

## Flujo del proyecto

| Etapa | Herramienta principal | Propósito |
|---|---|---|
| Revisión inicial | Google Sheets | Ordenar, filtrar y detectar problemas visualmente |
| Limpieza de datos | Python | Aplicar reglas reproducibles sin alterar la base original |
| Comparación antes/después | Python | Validar cómo cambió la base tras la limpieza |
| Visualización final | Tableau | Facilitar la revisión ejecutiva e interactiva |
| Siguiente etapa | Modelamiento | Preparar una futura red neuronal predictiva |

---

## Fuente de datos

El proyecto utiliza una base pública de riesgo crediticio obtenida originalmente desde Kaggle y reutilizada como caso práctico de portafolio.

Se eligió porque contiene suficientes variables demográficas, financieras y crediticias para simular un flujo de evaluación relativamente realista.

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

## Enfoque de trabajo

La revisión inicial se realizó en Google Sheets para ordenar la base, filtrar con mayor cuidado la información y detectar visualmente datos faltantes, valores atípicos y registros poco realistas.

Con esa primera lectura se definieron reglas de limpieza más claras, que luego fueron aplicadas en Python para mantener el proceso documentado, reproducible y sin modificar la base original. En lugar de sobrescribir la fuente inicial, se generó una tabla auxiliar limpia para comparar el antes y el después.

Finalmente, la información depurada fue llevada a Tableau para construir un dashboard de apoyo a la revisión gerencial, permitiendo explorar casos como clientes con historial negativo, patrones de riesgo por finalidad del préstamo, carga financiera respecto al ingreso y segmentos que requieren mayor atención.

---

## Recursos visuales

### Flujo de trabajo en Google Sheets

[![Ver video del dashboard en Tableau](https://img.youtube.com/vi/8y5rvR5nX7c/hqdefault.jpg)](https://youtu.be/8y5rvR5nX7c)

Video corto mostrando cómo se utilizó la hoja de cálculo para ordenar, filtrar y revisar la información antes de la limpieza en Python.

### Recorrido del dashboard en Tableau

[![Ver video del flujo en Google Sheets](https://img.youtube.com/vi/0oH_PFn1qwk/hqdefault.jpg)](https://youtu.be/0oH_PFn1qwk)

Video corto mostrando cómo se puede explorar la información ya limpia desde el dashboard interactivo.

### Versión interactiva del dashboard

[Ver dashboard en Tableau Public](https://public.tableau.com/views/Analisis_Riesgo_Crediticio/RiesgoCrediticio?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## Recursos interactivos

- [Hoja de apoyo en Google Sheets](https://docs.google.com/spreadsheets/d/1c2M-y9EaVsJferSnKHW8X4KZPHc7syRw1yLrfvo3NxQ/edit?gid=311571590#gid=311571590)
- [Dashboard interactivo en Tableau](https://public.tableau.com/views/Analisis_Riesgo_Crediticio/RiesgoCrediticio?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## Stand by

La siguiente etapa del proyecto será utilizar la base limpia como soporte para una futura red neuronal orientada a la estimación del riesgo crediticio.

La meta es extender este sistema hacia una capa predictiva, manteniendo primero una base sólida de interpretación de negocio, limpieza de datos y visualización analítica.

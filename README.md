# Detección de Vulnerabilidad Infantil en Contextos de Movilidad Humana
Modelo explicativo con XGBoost + SHAP para fortalecer políticas públicas basadas en evidencia

Autora: Alejandra Otero Leyton

🌍 Descripción General

Este proyecto desarrolla una herramienta explicativa para identificar hogares con media o alta vulnerabilidad infantil en contextos de movilidad humana en Colombia.
Fue desarrollado como parte del Datathon ACNUR – UNHCR 2024, utilizando datos del High Frequency Survey (HFS) entre 2021 y 2024.

El modelo combina:

Análisis descriptivo y social

Construcción de un índice de vulnerabilidad infantil

Clasificación con XGBoost

Interpretabilidad con SHAP

Un sistema tipo semáforo útil para decisiones humanitarias
🔍 Metodología
1️⃣ Consolidación de Datos

Se integraron más de 13.000 encuestas HFS, limpiando, estandarizando y organizando la información.
Se seleccionaron 7.916 hogares con menores de edad para el análisis.

2️⃣ Construcción del Índice de Vulnerabilidad Infantil

Se creó un índice continuo basado en:

asistencia escolar

modalidad de estudio

dificultades de acceso

razones de no asistencia

dimensiones sociales del hogar
| Nivel    | Rango     |
| -------- | --------- |
| 🟩 Baja  | ≤ 0.33    |
| 🟧 Media | 0.33–0.66 |
| 🟥 Alta  | > 0.66    |

3️⃣ Modelo XGBoost

Se formuló un modelo de clasificación binaria:

0 = baja vulnerabilidad

1 = media + alta vulnerabilidad

Resultados principales:
| Métrica   | Clase 1  |
| --------- | -------- |
| Recall    | **0.77** |
| Precision | 0.38     |
| F1        | 0.51     |
➤ Se prioriza el recall, clave en contextos humanitarios para no dejar hogares vulnerables por fuera.

4️⃣ Interpretabilidad con SHAP

El análisis SHAP identificó como principales factores de riesgo:

Falta de documentación del menor o acudientes

Ausencia de beneficios sociales

Historial de violencia, abuso o discriminación

Trabajos precarios del cuidador o jefatura femenina sin apoyo

Movilidad reciente por inseguridad o pérdida de vivienda

Esto permite entregar explicaciones claras a los equipos de campo:

“La clasificación se debe principalmente a falta de documentos y ausencia de beneficios sociales.”

5️⃣ Sistema Tipo Semáforo

Se desarrolló un sistema interpretativo sencillo:

🟥 Riesgo Alto: ≥2 factores críticos

🟧 Riesgo Medio: 1 factor crítico

🟩 Riesgo Bajo: ninguno

Incluye texto explicativo automático generado desde los valores SHAP.

🌱 Impacto Social

Esta herramienta:

facilita la identificación temprana de hogares vulnerables

prioriza la atención en contextos de movilidad humana

ofrece explicaciones claras y accionables

permite escalabilidad a nuevos territorios o bases

Es un ejemplo de cómo la ciencia de datos puede apoyar decisiones humanas y sociales.

🛠 Tecnologías

Python

Pandas / NumPy

XGBoost

SHAP

Matplotlib / Seaborn

Scikit-learn

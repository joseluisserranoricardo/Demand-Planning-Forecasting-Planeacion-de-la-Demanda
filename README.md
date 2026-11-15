# Demand Planning & Forecasting | Planeación de la Demanda

<img width="1303" height="732" alt="dashboard_sc" src="https://github.com/user-attachments/assets/8152027b-2562-43cc-a646-7a7d4ecc28ef" />

## Descripción del proyecto

Desarrollo de un proyecto de análisis de datos enfocado en la planeación de la demanda, mediante el estudio de ventas históricas, modelos estadísticos de pronóstico y herramientas de análisis de inventarios.

El objetivo es identificar patrones de comportamiento de la demanda, estimar ventas futuras y generar recomendaciones de abastecimiento que contribuyan a mejorar la disponibilidad de productos y la planificación de compras.

## Objetivos

- Analizar el comportamiento histórico de ventas por producto.
- Identificar tendencias y patrones de estacionalidad.
- Desarrollar y comparar modelos estadísticos de pronóstico.
- Evaluar el desempeño de los pronósticos mediante métricas de error.
- Estimar la demanda para los siguientes 12 meses.
- Calcular niveles de inventario, stock de seguridad y puntos de reorden.
- Generar recomendaciones de compra.
- Construir un dashboard para visualizar indicadores y apoyar la toma de decisiones.

## Herramientas y tecnologías

| Herramienta | Aplicación |
|---|---|
| Python | Análisis y procesamiento de datos |
| Pandas | Manipulación y transformación de datos |
| NumPy | Cálculos estadísticos |
| Statsmodels | Modelos de series temporales |
| Matplotlib / Seaborn | Visualización de datos |
| Power BI | Dashboard e indicadores de negocio |
| Jupyter Notebook | Desarrollo y documentación del análisis |

## Información analizada

El análisis comprende:

- 300 registros.
- 5 productos (SKU).
- 60 meses de información.
- Periodo: enero de 2021 a diciembre de 2025.
- Frecuencia de observación: mensual.

Variables principales:

- Fecha.
- Identificador y nombre del producto.
- Categoría.
- Unidades vendidas.
- Precio unitario.
- Indicador de promociones.
- Inventario final.

## Metodología

### 1. Exploración y validación de datos
Revisión de estructura, tipos de variables, valores nulos, registros duplicados y estadísticas descriptivas.

### 2. Análisis exploratorio (EDA)
Análisis de la evolución de ventas por producto, identificación de tendencias, estacionalidad y variabilidad de la demanda.

### 3. Descomposición de series temporales
Aplicación del modelo aditivo para estudiar los componentes de tendencia, estacionalidad y residuos.

### 4. Modelado estadístico de pronósticos
Construcción y comparación de dos métodos:

- **Naive estacional:** utiliza como referencia las ventas del mismo periodo del año anterior.
- **Holt-Winters:** incorpora componentes de tendencia y estacionalidad mediante suavizamiento exponencial.

### 5. Evaluación de modelos
Separación de los datos en entrenamiento (2021–2024) y prueba (2025).

Métricas utilizadas:

- MAE: Error Absoluto Medio.
- RMSE: Raíz del Error Cuadrático Medio.
- MAPE: Error Porcentual Absoluto Medio.
- BIAS: Sesgo del pronóstico.

### 6. Pronóstico de demanda
Selección del método con mejor desempeño y generación de proyecciones para los siguientes 12 meses, utilizando el histórico completo.

### 7. Planeación de inventarios
Cálculo de indicadores para apoyar las decisiones de abastecimiento:

- Stock de seguridad.
- Demanda durante el tiempo de reposición.
- Punto de reorden (ROP).
- Stock objetivo.
- Cantidad de compra recomendada.

Se consideraron los siguientes parámetros:

- Nivel de servicio: 95%.
- Tiempo de reposición: 15 días.
- Periodo de revisión: 30 días.

### 8. Dashboard en Power BI
Construcción de un tablero de control para visualizar los principales indicadores de demanda e inventario.

## Resultados

El modelo Holt-Winters presentó un mejor desempeño que el método Naive estacional en los cinco productos evaluados.

**Resultados MAPE de Holt-Winters:**

| Producto | MAPE |
|---|---:|
| Arroz 1 kg | 7.66% |
| Aceite 1 L | 8.67% |
| Detergente 1 kg | 7.16% |
| Papel higiénico 4 pzas | 10.65% |
| Leche 1 L | 11.42% |

La evaluación permitió identificar diferencias en el comportamiento de cada producto y cuantificar los errores de pronóstico para mejorar la planificación de la demanda.

## Dashboard

El dashboard desarrollado en Power BI contempla:

- Demanda pronosticada para 2026.
- MAPE del modelo.
- Evolución histórica de ventas.
- Comparación entre demanda real y pronosticada.
- Inventario disponible.
- Cantidad de compra recomendada por producto.



## Conclusiones

El proyecto integra técnicas de análisis estadístico, pronóstico de series temporales y planeación de inventarios para convertir información histórica de ventas en recomendaciones operativas.

Los resultados muestran la utilidad de los modelos estadísticos tradicionales para estimar la demanda, evaluar desviaciones y anticipar necesidades de abastecimiento.

La integración de Python y Power BI permite desarrollar un flujo de trabajo que conecta el análisis de datos con la visualización de indicadores y el apoyo a la toma de decisiones empresariales.

---

**Autor:** José Luis Serrano

**Áreas de interés:** Data Analytics | Business Intelligence | Demand Planning | Forecasting

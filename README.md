# 🗽 NYC Business Density & Demographic Predictor

## 📋 Descripción del Proyecto
Este proyecto de Data Science analiza la relación entre los microdatos demográficos de la Ciudad de Nueva York y la actividad económica local (licencias comerciales e individuales). A través de un proceso de ETL, análisis exploratorio (EDA) y modelado predictivo, se busca identificar los factores demográficos que impulsan la densidad de negocios en los distintos ZIP Codes de la ciudad.

## 🚀 Hallazgos Clave
* **Capacidad Predictiva:** Se logró validar que la demografía explica el **91% de la variabilidad** en la densidad comercial.
* **Correlación de Negocios (Business):** Se identificó una correlación crítica de **0.90** entre la población Asiática y la densidad de licencias corporativas.
* **Emprendimiento Individual:** Las zonas con mayoría Hispana presentan la mayor densidad de autoempleo (**6.2** vs 2.1 en zonas de mayoría Blanca).
* **Industria Dominante:** "Home Improvement Salesperson" destaca como la actividad líder en licencias individuales en todos los sectores analizados.

## 🧠 Justificación del Modelo: ¿Por qué Regresión Lineal?
Para este análisis, se seleccionó la **Regresión Lineal Múltiple** como algoritmo de aprendizaje supervisado por las siguientes razones:

1. **Naturaleza de los Datos:** Al trabajar con una variable objetivo continua (`biz_density`), la regresión es el marco estadístico adecuado.
2. **Interpretabilidad:** A diferencia de modelos de "caja negra", la regresión lineal permite extraer **coeficientes exactos** (como el impacto de +295 en la población Asiática), facilitando la toma de decisiones basada en datos.
3. **Eficiencia:** Dado que el EDA reveló relaciones lineales fuertes, este modelo ofrece una alta precisión (**R²: 0.91**) sin el riesgo de sobreajuste (*overfitting*) que presentan modelos más complejos.
4. **Navaja de Ockham:** Se optó por la solución más sencilla y explicativa que cumpliera con los estándares de precisión requeridos para un análisis sociodemográfico.

## 📊 Métricas del Modelo
* **R2 Score:** 0.9110
* **MAE (Error Medio Absoluto):** 1.4491
* **Coeficientes Principales:**
    * `percent_asian_non_hispanic`: 295.22
    * `percent_black_non_hispanic`: 216.73
    * `percent_white_non_hispanic`: 44.13

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 
* **Librerías:** Pandas, Scikit-Learn, Matplotlib, Seaborn.
* **Herramientas:** Jupyter Notebook.

## 📁 Estructura del Repositorio
* `analisis_nyc.ipynb`: Flujo completo desde la limpieza hasta el modelo.
* `nyc_final_analysis.csv`: Dataset final con predicciones incluidas.
* `README.md`: Documentación del proyecto.
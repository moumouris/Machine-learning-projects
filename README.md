# Portafolio de Prácticas: Aprendizaje Computacional

Este repositorio reúne una colección de 5 proyectos prácticos diseñados para explorar y validar experimentalmente algoritmos fundamentales de Machine Learning. 

Los proyectos abordan desafíos técnicos específicos, desde la aproximación de funciones matemáticas altamente no lineales y el análisis de estructuras fractales (Mandelbrot), hasta la compresión de imágenes mediante aprendizaje no supervisado.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.x
* **Librerías Core:** NumPy.
* **Machine Learning:** Scikit-Learn (Regresión, Clasificación, Clustering, Model Selection).
* **Visualización:** Matplotlib.

## 📂 Descripción de los Proyectos

### 1. Ingeniería de Características en Regresión Lineal
* **Archivo:** `01_Linear_Regression_Sin_Approx.ipynb`
* **Reto:** Aproximar la función no lineal $y = \sin(1/(x_1 \cdot x_2))$ en el intervalo $[-1,1]$ utilizando un modelo estrictamente lineal.
* **Metodología:**
    * Análisis de curvas de aprendizaje (MSE/MAE/R²) para diagnosticar *Underfitting*.
    * Visualización del error de estimación mediante mapas de calor (*Heatmaps*).
    * **Mejora del modelo:** Implementación de estrategias para capturar la no linealidad utilizando únicamente `LinearRegression`.

### 2. Clasificación de Fronteras Complejas con Regresión Logística
* **Archivo:** `02_Logistic_Regression_Sign_Classification.ipynb`
* **Reto:** Predecir el **signo** (positivo/negativo) de la función oscilante $y = \sin(1/(x_1 \cdot x_2))$.
* **Modelo:** Regresión Logística.
* **Desafío Técnico:**
    * Evaluar el comportamiento de un clasificador lineal frente a una frontera de decisión geométrica compleja (patrones de ondas concéntricas).
    * Análisis de las probabilidades predichas y la precisión del modelo en regiones de alta frecuencia.

### 3. Regresión en Fractales: SVR vs. MLP
* **Archivo:** `03_Mandelbrot_Regression_SVR_MLP.ipynb`
* **Objetivo:** Predicción de valores continuos derivados del conjunto de Mandelbrot (ej. iteraciones de escape).
* **Modelos:** * Support Vector Regression (SVR).
    * Perceptrón Multicapa (MLP - Red Neuronal Artificial).
* **Metodología:**
    * **Optimización de Hiperparámetros:** Uso de `GridSearchCV` para ajustar *kernels*, regularización ($C$) y parámetros de la red neuronal.
    * Comparación de la capacidad de generalización entre modelos basados en kernels y redes neuronales.

### 4. Clasificación No Lineal: SVC vs. Naive Bayes
* **Archivo:** `04_Mandelbrot_Classification_SVC_NB.ipynb`
* **Objetivo:** Clasificación binaria para determinar la pertenencia de un punto al conjunto de Mandelbrot.
* **Comparativa:**
    * **SVC (Support Vector Classifier):** Enfoque discriminativo maximizando el margen.
    * **Naive Bayes:** Enfoque probabilístico generativo.
* **Implementación:** Ajuste fino de modelos mediante búsqueda en rejilla (`GridSearchCV`) y análisis de métricas de clasificación.

### 5. Cuantización de Imágenes con K-Means (No Supervisado)
* **Archivo:** `05_Image_Quantization_KMeans.ipynb`
* **Aplicación:** Compresión de imágenes mediante la reducción de la paleta de colores (agrupamiento de píxeles RGB).
* **Análisis Estadístico:**
    * **Validación Cruzada:** 10-fold Cross-Validation para asegurar la robustez del error (MSE/MAE).
    * **Benchmarking:** Uso de diagramas de caja (*Boxplots*) para comparar la estabilidad de K-Means frente a una asignación de color aleatoria.
    * Evaluación visual de la reconstrucción de la imagen variando el número de clusters ($k=2, 5, 10...$).

---
**Nota:** Cada notebook contiene el flujo de trabajo completo: generación/carga de datos, entrenamiento, validación y discusión detallada de los resultados.

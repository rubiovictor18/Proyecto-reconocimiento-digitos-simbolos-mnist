# Reconocimiento Óptico de Dígitos y Operadores Matemáticos

## 🎯 Objetivo del Proyecto
Desarrollar y comparar múltiples modelos de Machine Learning y Deep Learning para la clasificación precisa de dígitos manuscritos (0 al 9) y símbolos de operaciones matemáticas básicas (suma, resta, multiplicación y división).

## 🗄️ Conjuntos de Datos (Datasets)
El entrenamiento de los modelos requirió dos fuentes de datos distintas para abordar la naturaleza de los caracteres:
* **Dígitos (0-9):** Se utilizó la base de datos estándar **MNIST**, extrayendo las imágenes normalizadas para el entrenamiento base.
* **Símbolos Matemáticos:** Ante la falta de un dataset estandarizado que se ajustara a nuestras necesidades, **creamos un conjunto de datos propio y colaborativo**. Se recolectaron muestras manuscritas de múltiples personas con el objetivo de introducir una alta varianza en la caligrafía y los trazos. Esto garantizó que los modelos no se sobreajustaran a un único estilo de escritura y fueran robustos ante escenarios reales.

## 🛠️ Modelado y Arquitectura
El proyecto evalúa la precisión y eficiencia de algoritmos tradicionales frente a redes de aprendizaje profundo, segmentados de la siguiente manera:

**1. Clasificación de Dígitos (MNIST):**
Se entrenaron y contrastaron tres enfoques algorítmicos distintos:
* **Random Forest:** Para evaluar el rendimiento de métodos de ensamble.
* **Máquinas de Vectores de Soporte (SVM):** Utilizando transformaciones del hiperplano para separar las clases numéricas.
* **Redes Neuronales Convolucionales (CNN):** Para extraer mapas de características espaciales directamente de los píxeles.

**2. Clasificación de Símbolos Matemáticos Propios:**
Dada la complejidad morfológica de los símbolos generados colaborativamente, el análisis se enfocó en los modelos de mayor capacidad de generalización:
* **Máquinas de Vectores de Soporte (SVM)**
* **Redes Neuronales Convolucionales (CNN)**

## 📊 Resultados y Conclusiones

Tras el entrenamiento y evaluación de los modelos, los resultados demostraron la superioridad de las arquitecturas de aprendizaje profundo para la extracción de características espaciales, aunque los algoritmos tradicionales de Machine Learning mantuvieron un rendimiento competitivo.

**1. Clasificación de Dígitos (MNIST):**
* **Red Neuronal Convolucional (CNN):** Alcanzó la mayor precisión con un **97.75%** en el conjunto de prueba, consolidándose como el modelo más robusto.
* **Máquinas de Vectores de Soporte (SVM):** Obtuvo un rendimiento sobresaliente del **96.30%** tras la optimización de hiperparámetros (Kernel RBF, C=10).
* **Random Forest:** Logró una precisión del **94.20%**, posicionándose como el modelo con menor rendimiento comparativo en esta tarea.

**2. Clasificación de Símbolos Matemáticos (Dataset Colaborativo):**
* **Red Neuronal Convolucional (CNN):** Logró una precisión del **95.29%**.
* **Máquinas de Vectores de Soporte (SVM):** Alcanzó un **90.88%** de precisión general, mostrando mayores dificultades relativas para clasificar el símbolo de división (77% de precisión específica).

**Conclusión:**
La Red Neuronal Convolucional (CNN) superó de manera sistemática al Random Forest y a la Máquina de Vectores de Soporte en ambos escenarios. La diferencia fue especialmente notable en el dataset propio de símbolos matemáticos; ante la alta varianza caligráfica introducida por los múltiples autores, la CNN demostró una capacidad de generalización significativamente superior, validando su uso para problemas reales de visión por computadora con datos no estandarizados.

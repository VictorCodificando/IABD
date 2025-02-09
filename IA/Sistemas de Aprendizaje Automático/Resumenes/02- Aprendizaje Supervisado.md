# Unidad Temática 2 - Aprendizaje Supervisado

## Introducción
El aprendizaje supervisado es una de las ramas más utilizadas dentro del aprendizaje automático. Se caracteriza por el uso de datos etiquetados, donde cada observación incluye un conjunto de variables de entrada (tambén llamadas características o "features") y una variable de salida (etiqueta o "label"). 

El objetivo de un modelo de aprendizaje supervisado es aprender patrones a partir de los datos de entrenamiento para realizar predicciones sobre datos nuevos no observados anteriormente. Durante la fase de entrenamiento, el modelo ajusta sus parámetros internos para minimizar el error en las predicciones. Posteriormente, se evalúa su desempeño en datos de prueba para verificar su capacidad de generalización.

Existen dos tipos principales de problemas dentro del aprendizaje supervisado:

1. **Clasificación**: Se utiliza cuando la variable de salida es categórica, es decir, pertenece a un conjunto finito de clases o categorías. Puede tratarse de una **clasificación binaria** (dos clases, por ejemplo, "aprobado" o "reprobado") o **multiclase** (más de dos clases, por ejemplo, clasificación de imágenes en "perro", "gato" o "pájaro").

2. **Regresión**: Se emplea cuando la variable de salida es numérica y continua. En este caso, el modelo intenta predecir un valor específico, por ejemplo, el precio de una vivienda en función de su tamaño, ubicación y antigüedad.

## Ejemplos

- **Clasificación**:
  - Dado un conjunto de imágenes médicas, predecir si un tumor es benigno o maligno.
  - Identificar correos electrónicos como spam o no spam.
  - Determinar si un cliente realizará un pago puntual o si es probable que incurra en morosidad.
  
- **Regresión**:
  - Estimar la edad de una persona a partir de una imagen.
  - Predecir el precio de un vehículo según su marca, modelo, kilometraje y estado general.
  - Pronosticar las ventas futuras de una empresa basándose en tendencias históricas y estacionales.

## Algoritmos de Aprendizaje Supervisado

### 1. Regresión Lineal
Este algoritmo busca establecer una relación lineal entre una variable dependiente y una o más variables independientes. Es ampliamente utilizado para predecir valores numéricos en problemas de regresión. Sus variantes incluyen:

- **Regresión Lineal Simple**: Se modela la relación entre una sola variable independiente y la variable dependiente a través de una línea recta.
- **Regresión Lineal Múltiple**: Se incluyen varias variables independientes para mejorar la capacidad predictiva del modelo.

La ecuación de una regresión lineal simple es:
\[ Y = \beta_0 + \beta_1X + \varepsilon \]
Donde \( \beta_0 \) es el intercepto, \( \beta_1 \) es la pendiente y \( \varepsilon \) representa el error.

### 2. Regresión Logística
Utilizada en problemas de clasificación, especialmente cuando se trata de una clasificación binaria. Emplea la función sigmoide para transformar las predicciones en probabilidades entre 0 y 1. La fórmula de la regresión logística es:
\[ P(Y=1) = \frac{1}{1 + e^{-z}} \]
Donde \( z \) es una combinación lineal de las variables de entrada.

### 3. k-Nearest Neighbors (k-NN)
Este algoritmo basado en instancias no requiere un modelo previo. En cambio, almacena los datos de entrenamiento y compara la distancia entre ellos y una nueva instancia para realizar predicciones. Las distancias comunes usadas incluyen Euclideana, Manhattan y Minkowski.

### 4. Árboles de Decisión
Dividen el espacio de características en segmentos basados en condiciones de las variables de entrada. Se utilizan en clasificación y regresión, y pueden combinarse en modelos más complejos como Random Forest.

### 5. Support Vector Machines (SVM)
Encuentra un hiperplano que maximiza la separación entre clases. En problemas no lineales, usa la técnica de "kernels" para transformar el espacio de representación.

## Métricas de Evaluación
Para evaluar un modelo de aprendizaje supervisado se utilizan varias métricas:

### Para Clasificación:
- **Precisión (Accuracy)**: Proporción de predicciones correctas.
- **Precisión y Recall**: Indicadores clave en problemas con clases desbalanceadas.
- **F1-Score**: Promedio armónico de Precisión y Recall.
- **Matriz de Confusión**: Muestra los aciertos y errores en cada clase.

### Para Regresión:
- **Error Cuadrático Medio (MSE)**: Penaliza errores grandes.
- **Raíz del Error Cuadrático Medio (RMSE)**: Interpretación en la misma escala que los datos.
- **Coeficiente de Determinación (R²)**: Indica cuánta variabilidad explican las variables predictoras.

## Conclusión
El aprendizaje supervisado es una de las técnicas más utilizadas en machine learning debido a su capacidad de aprender patrones a partir de datos etiquetados. Dependiendo del problema, se pueden utilizar diferentes algoritmos y métricas de evaluación para garantizar un modelo preciso y eficiente.
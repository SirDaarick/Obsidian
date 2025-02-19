El **ENTE** es nuestro objeto de estudio, que puede ser:

- Rostros humanos (reconocimiento facial).
- Detectar algún tipo de enfermedad (Ejemplo: Parkinson).
- Algún tipo de señal (AM: Amplitud modulada, FM: Frecuencia modulada, PM: Fase modulada).
- Etcétera.

**Pixel:** Es el "Picture Element", la unidad fundamental de la imagen. En la notación **F(x, y)**, **F** es el nivel de brillo, y **x** e **y** representan la posición en la imagen.

**Histograma:** Muestra la frecuencia con la que aparecen los diferentes niveles de intensidad en cada pixel de la imagen.

Los humanos reconocemos objetos mediante el color, la forma y la textura.

El **preprocessing** mejora la imagen desde el punto de vista del Sistema Visual Humano (SVH), facilitando la extracción de características al eliminar el ruido, ajustar el contraste o corregir la iluminación.

## **Feature extraction**:

**Descriptor:**  
Un **descriptor** es una representación matemática de una característica visual de la imagen, utilizada para la identificación y clasificación de objetos.

- **Descriptores locales:** Analizan regiones específicas de la imagen, como bordes o puntos clave (Ej: SIFT, ORB).
- **Descriptores globales:** Consideran la imagen en su totalidad (Ej: histograma de color, textura global).

Generalmente, se crean ventanas de descripciones locales (pixeles) para extraer información global de lo que hay en la imagen.

Un vector es una descripción de un objeto.

**O1 = [x1, x2, x3, x4, x5 … , xn]**

donde **x1, x2, ..., xn** contienen las características del objeto. Por ejemplo:

**O1 = [alto, ancho, color, textura,…]**



### **Diferencias entre vector y array:**

- **Vector:** Una estructura unidimensional. Puede representarse en un espacio de características.
- **Array:** Puede ser multidimensional y almacenar datos en varias dimensiones.

Los vectores se grafican en un espacio multidimensional, y deben quedar agrupados de forma que sean separables. Esto se puede lograr de las siguientes maneras:

- **Separabilidad lineal:** Se utiliza una línea recta para separar las características de dos objetos, con una pendiente definida.
- **Separabilidad cuadrática:** Las características se separan mediante una parábola.
- **Separabilidad polinómica:** Las Redes Neuronales Artificiales (ANN) utilizan funciones polinómicas para separar las características.

Este espacio se llama **Feature extraction domain**.

### **Classifier:**

Se segmentan las imágenes para extraer las frutas de manera separada, y se ingresan todas las características en una base de datos para poder clasificarlas según sus atributos.

### **Train:**

Con todas las imágenes, se le enseña a la computadora a identificar un objeto basándose en ciertas características. Con esta información, es capaz de detectar otros objetos similares.

### **Testing:**

Se verifica si el sistema ha aprendido correctamente y si es capaz de identificar objetos de manera efectiva.

[[Niveles de visión artificial]]
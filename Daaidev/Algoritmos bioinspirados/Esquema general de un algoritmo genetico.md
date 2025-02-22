### **1. Generación de Población Inicial**

Para comenzar un algoritmo genético, se debe generar una **población inicial** con diversidad suficiente para explorar el espacio de soluciones de manera eficiente. Sin embargo, debe ser lo suficientemente pequeña para evitar un alto costo computacional.

#### **Métodos de Generación de Población**

- **Distribución Uniforme Aleatoria**: Generar individuos distribuidos de manera aleatoria en el espacio de búsqueda.
- **Diseño de Experimentos (Ejemplo: Hipercubos Latinos)**: Técnica que garantiza una mejor cobertura del espacio de búsqueda.
- **Incorporación de Soluciones Prometedoras**: Si se tienen soluciones parciales o heurísticas previas, se recomienda agregarlas para mejorar la convergencia.

#### **Ejemplos de Distribuciones**

- **Distribución Uniforme**: Todos los valores tienen la misma probabilidad de ser seleccionados.
- **Secuencia de Halton**: Técnica que genera números cuasi-aleatorios con buena dispersión.
- **Hipercubos Latinos**: Técnica de muestreo que evita la sobreconcentración de puntos en ciertas regiones.

### **2. Evaluación y Selección de Padres**

El objetivo es seleccionar los individuos con **mejor desempeño** (fitness) para la siguiente generación.

#### **Métodos de Selección**

##### **2.1. Selección por Torneo**

- Se eligen al azar grupos de individuos para competir.
- Gana el individuo con mejor **aptitud (fitness)** en cada torneo.
- **Tamaño del torneo**: Si es mayor, hay más presión selectiva (se favorece la élite).
- **Torneo Binario**: Se comparan pares de individuos, eliminando el de menor aptitud hasta quedar con un grupo reducido de padres.

##### **2.2. Selección Proporcional (Ruleta)**

- Se asigna a cada individuo una probabilidad de ser seleccionado basada en su fitness.
- **Valor de Esperanza**: Esperanza=Fitness del individuoFitness promedio de la poblacioˊn\text{Esperanza} = \frac{\text{Fitness del individuo}}{\text{Fitness promedio de la población}}Esperanza=Fitness promedio de la poblacioˊnFitness del individuo​
- Se elige un número aleatorio y se acumulan valores hasta encontrar el primer individuo que supere el umbral.

**Variantes**:

- **Ruleta con reemplazo**: Se mantiene a los padres en la población para formar múltiples parejas (mayor presión de selección).
- **Ruleta sin reemplazo**: Se eliminan los individuos seleccionados, reduciendo la presión de selección.

### **3. Reproducción y Mutación**

- Se cruzan los individuos seleccionados para generar hijos.
- Los hijos **sufren mutaciones** para introducir variabilidad.
- Se evalúan nuevamente para decidir si sobreviven en la siguiente generación.
Son tres niveles principales:

- **Visión de bajo nivel:** Se trabaja directamente con los píxeles de la imagen para extraer sus características, como área, perímetro, color o textura.
- **Visión de nivel intermedio:** Agrupa los elementos obtenidos para identificar bordes o regiones, generalmente con el propósito de segmentar la imagen.
- **Visión de alto nivel:** Está relacionada con la semántica de la imagen, es decir, con el verdadero significado o entendimiento. Se centra en el reconocimiento de objetos o el análisis de la escena.

Un píxel tiene 4 vecinos en el caso de la **C_4** (conectividad 4) y 8 vecinos en el caso de la **C_8** (conectividad 8).

Para ilustrarlo:


**Conectividad 4 

|     | V   |     |
| --- | --- | --- |
| V   | P   | V   |
|     | V   |     |
**Conectividad 8

| V   | V   | V   |
| --- | --- | --- |
| V   | P   | V   |
| V   | V   | V   |

En una matriz **a** de resolución 5x5, todos los elementos distintos de 0 se consideran "elementos". Un ejemplo de matriz sería:

| 0   | 0   | 0   | 0   | 0   |
| --- | --- | --- | --- | --- |
| 0   | 1   | 2   | 3   | 0   |
| 0   | 9   | 10  | 4   | 0   |
| 0   | 8   | 7   | 6   | 5   |
| 0   | 0   | 0   | 0   | 0   |
[[Ejercicio 1]]
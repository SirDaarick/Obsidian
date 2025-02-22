### 1. **Clase**:

- Una **clase** se refiere a una categoría o tipo de objeto que comparte características similares. Por ejemplo, en un sistema de reconocimiento de imágenes, las clases podrían ser "perro", "gato", "coche", "árbol", etc.
    
- Las clases son conceptos abstractos que definen un grupo de objetos con propiedades comunes.
    
- En tareas de clasificación, el objetivo es asignar una etiqueta de clase a una imagen o región de una imagen (por ejemplo, determinar si una imagen contiene un "perro").
    

### 2. **Objeto**:

- Un **objeto** es una instancia específica de una clase en una imagen. Por ejemplo, si la clase es "coche", un objeto sería un coche específico detectado en una imagen.
    
- Los objetos tienen una ubicación espacial definida en la imagen (coordenadas de un bounding box, por ejemplo) y pueden ser contados, localizados o segmentados.
    
- En tareas de detección o segmentación, el objetivo es identificar y localizar objetos individuales dentro de una imagen.

``` mathlab
clc 
clear all
close all
warning off all 

#Programa que genera N clases con m representante cada clase

c1x = randn(1,10)
c1y = rand(1,10)

c2x = randn(1,10)+3 #se suma para mover su centro de gravedad
c2y = rand(1,10)+8

c3x = (randn(1,10)-15)*5
c3y = (rand(1,10)-20)*5 #Dispersion respecto al centro de gravedad

plot(c1x(1,:), c1y(1,:), 'Ko', 'MarkerSize', 15)
grid on
hold on 
plot(c2x(1,:), c2y(1,:), 'Ko', 'MarkerSize', 15)
plot(c3x(1,:), c3y(1,:), 'Ko', 'MarkerSize', 15)
```

[[Practica 2 (Mier 5 Marzo)]]
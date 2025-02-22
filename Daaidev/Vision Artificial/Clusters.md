
Imaginemos que tenemos 3 alumnos inscritos a Vision Artificial y 3 inscritos formales, ambos conjuntos estan representados por un vector cada alumno, y tenemos otro alumno que esta representado por un vector y queremos saber cual es su grupo ideal

para abordar el problema deberiamos encontrar el centro de masa de cada conjunto, el cual se calcula de la siguiente manera Promedio = 1/n( sum x / sum y)

una vez teniendo el centro de gravedad, debemos calcular la distancia desde el vector del alumno que queremos unir a un grupo hacia los centros de gravedad y dependiendo del mas pequeño ese será su grupo ideal

![[Pasted image 20250218192457.png]]


```
se puede crear un arreglo a = [1,2,3,4]
whos
b = randn(3,4) genera una matriz de 3x4 aleatoria
c = b(2,3)
d = b(2:3, :) imprime de la linea 2 a la 3 en todas las columnas
e = b(2:end, :) imprime desde la columna 2 hasta el final 

clc % limpia pantalla
clear all % limpiar todo
close all % cierra todo 
warning off all % desactiva los warning

%Programa que hace la toma de decision con base al criterio de la minima distancia

%Generando las clases de pertenencia

c1 = [0 1 2 ; 0 2 3]; % con ; haces que no se despliegue en la consola
c2 = [5 7 9 ; 6 8 10];
c3 = [7 8 9; 2 4 5]

vector = [4;2]
vx = input("Dame el valor en x =")
vy = input("Dame el valor en y =")
vector = [vx ; vy]
%Calculando los parametros
media1 = mean(c1,2)
media2 = mean(c2,2)
media3 = mean(c3,2)

dist1 = norm(media1 - vector)
dist2 = norm(media2 - vector)
dist3 = norm(media3 - vector)

dist_total = [dist1 dist2 dist3]

minimo = min(dist_total)
dato = find(minimo == dist_total)
fprintf("El vector desconocido pertenece a la clase %d", dato)
%Graficando las clases

figure(1)
plot(c1(1,:), c1(2,:), 'ro', 'MarkerSize', 10, 'MarkerFaceColor', 'r') %r0 es de red y circulo para que se grafique un punto rojo

grid on %Activa la cuadricula

hold on %Mantiene la grafica para mandar mas cosas, si no se borran las graficas anteriores

plot(c2(1,:), c2(2,:), 'ro', 'MarkerSize', 10, 'MarkerFaceColor', 'b')
plot(c3(1,:), c3(2,:), 'ro', 'MarkerSize', 10, 'MarkerFaceColor', 'g')

plot(vector(1,:), vector(2,:), 'ro', 'MarkerSize', 10, 'MarkerFaceColor', 'k')

legend('clase1', 'clase2', 'clase3', 'vector')
disp('Hola mundo') %desplegar en pantalla

```

[[Practica 1]]
[[Generación de N clusters]]

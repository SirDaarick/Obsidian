Tenemos la siguiente matriz de 5x5.

| 0   | 0   | 0   | 0   | 0   |
| --- | --- | --- | --- | --- |
| 0   | 4   | 6   | 3   | 0   |
| 0   | 4   | 5   | 4   | 0   |
| 0   | 6   | 3   | 5   | 6   |
| 0   | 0   | 0   | 0   | 0   |
Para calcular el perímetro, se toma la distancia de cada uno de los pixeles del borde del objeto, hacia el objeto siguiente:
$$
\begin{aligned}
d(1,2) &= 1 \\
d(2,3) &= 1 \\
d(3,4) &= 1 \\
d(4,5) &= \sqrt{2} \\
d(5,6) &= 1 \\
d(6,7) &= 1 \\
d(7,8) &= 1 \\
d(8,9) &= 1 \\
d(9,1) &= 1
\end{aligned}
$$
Sumamos todos y el perimetro del elemento es de 9.4142 y ese valor se asigna al descriptor
O = [9.4142]
y para calcular el centro de gravedad de un objeto usamos la siguiente formula (teniendo en cuenta que las X son las filas y las Y son las columnas de la imagen. 

![[Pasted image 20250218191929.png]]

donde se realiza la sumatoria de cada elemento de una linea y se multiplica por la linea y la sumatoria de f(x,y) es la suma de todos los valores del elemento, dando como resultados para x = 3.15 y para y = 3.21

ahora agregamos esos resultados al descriptor O = [9.4142, 3.15, 3.21]

Ahora calculamos el area, con la siguiente formula

donde el objetivo es sumas el valor de veces en el que aparecen datos en las filas y los renglones y dividiendolo entre la cantidad de elementos que haya en el objeto

![[Pasted image 20250218192223.png]]
ahora agregamos esos resultados al descriptor O = [9.4142, 3.15, 3.21, 3.1, 3.2], como vemos que los elementos 1, 2 y 3 del vector son muy parecidos, podemos reducir la dimension de 5 a 2, eliminando los datos que se parecen entre ellos y dejando 1 solo que los representen

en este caso nuestro vector de caracteristicas quedara como O = [9.4142, 3.15]
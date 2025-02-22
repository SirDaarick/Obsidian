Para cada pareja se decide con una cierta probabilidad (p ej, 0.6) si se recombinaran para generar nuevos decendientes

P. ej, suponga que solo se decidio recombinar las parejas (s1, s2) and (s5, s6)

Para cada pareja, se aplica un operador de combinacion. Por ejemplo: cruza de un punto.

## Cruza de un punto en codificacion binaria
Padres antes de la cruza : 

S1 = 1111**010101**
S2 = 1100*110101*

decendientes  despues de la cruza

S1´ = 1111*110101*
S2´ = 1100**010101**

Se intercambian una parte de la cadena escogiendo un punto de cruza, en este caso fue en 4 digito

## Cruza de dos puntos 
- Se seleccionan aleatoriamente 2 puntos de cruza
- Se realiza la division de la informacion con esos puntos
- Se intercambia la informacion genetica como sigue: 

	Padres: 
		S1 = 11**010101**11
		S2 = 110*110101*0

	Hijos: 
		S1´ = 11*110101*11
		S2´ = 11**010101**00
## Cruza de N puntos
- Selecciona aleatoriamente n puntos de cruza
- Se divide cromosoma en estos puntos 
- Alterna entre los dos padres para generar los descendientes

	Padres: 
		s1 = **0000000000000000000000000000**
		s2 = *1111111111111111111111111111*
		
	Hijos: 
		s1 = **0000111100000000011111100000**
		s2 = *1111000011111111100000011111*
## Cruza uniforme
Se recorre uno a uno los elementos del cromosoma y se elige aleatoriamente si se selecciona la informacion de uno u otro padre (Como si se tratara de un volado "Flip")

Padres : 
		s1 = **0000000000000000000000000000**
		s2 = *1111111111111111111111111111*
Hijos: 
		s1 = 0101010101110100010010011110
		s2 = 1010101010001011101101100001

## Mutacion 
Pequeños cambios en la cadena genetica, es aleatorio si cambia y quienes cambian, lo recomendable es que la mutacion se presente en menos del 10% de la cadena (Porcentaje de mutacion)

antes de la mutacion 

s1 = 111011**0**101

despues de la mutacion 
 
s1 = 111011**1**101


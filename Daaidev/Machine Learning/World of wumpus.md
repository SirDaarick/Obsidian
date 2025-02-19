Hay que buscar una manera de representar todo el conocimiento, en este caso una tabla.

El estado de nuestro mundo de wumpus, realizamos un proceso de inferencia (lo que sabemos a partir de lo que detectamos en la casilla mediante lógica), representamos el conocimiento en la tabla y finalmente tomamos decisiones mediante acciones.

## Movimiento 1

![[Pasted image 20250218172812.png]]

**Estado** : (1,1)

**Inferencia:**

	~S ⇒ ~W(1,2) ^ ~W(2,1)
	
	~B ⇒ ~P(1,2) ^ ~P(2,1)

**Representación del conocimiento: **

| Estado | Visit V | Stench S | Breeze B | Glitter R | Wumpus W | Pit ´P | Gold |
| ------ | ------- | -------- | -------- | --------- | -------- | ------ | ---- |
| (1,1)  | 1       | 0        | 0        | 0         | 0        | 0      | 0    |
| (1,2)  | 0       |          |          |           | 0        | 0      | 0    |
| (2,1)  | 0       |          |          |           | 0        | 0      | 0    |
**Acciones:** 

	A(1,1) ⇒ A(1,2)

## Movimiento 2

**Estado:** (1,2)

![[Pasted image 20250218173407.png]]

**Inferencia:**

~S(1,2) ⇒ ~W(1,3) ^ ~W(2,2)

B(1,2) ⇒ P(1,3) v P(2,2)

**Representacion del conocimiento:**

|Estado|Visit V|Stench S|Breeze B|Glitter R|Wumpus W|Pit ´P|Gold|
|---|---|---|---|---|---|---|---|
|(1,1)|1|0|0|0|0|0|0|
|(1,2)|1|0|1|0|0|0|0|
|(2,1)|0||||0|0|0|
|(1,3)|0||||0|?|0|
|(2,2)|0||||0|?|0|

**Acción:**
	
	A(1,2) ⇒ A(1,1) ⇒ A(2,1)

## Movimiento 3

**Estado:** (2,1)

![[Pasted image 20250218173520.png]]

**Inferencia:**

	~S(2,1) ⇒ ~W(2,2) ^ ~W(3,1)
	
	~B(2,1) ⇒ ~P(2,2) ^ ~P(3,1)
	
	~P(2,2) ⇒ P(1,3)
	
	P(1,3) ⇒ B(2,3) ^ B(1,4)

**Representacion del conocimiento:**

|Estado|Visit V|Stench S|Breeze B|Glitter R|Wumpus W|Pit ´P|Gold|
|---|---|---|---|---|---|---|---|
|(1,1)|1|0|0|0|0|0|0|
|(1,2)|1|0|1|0|0|0|0|
|(2,1)|1|0|0|0|0|0|0|
|(1,3)|0||1||0|1|0|
|(2,2)|0||||0|0|0|
|(3,1)|0||||0|0|0|
|(1,4)|0||1|||||

**Accion:**

A(2,1) ⇒ A(3,1)

## Movimiento 4

**Estado:** (3,1)

![[Pasted image 20250218173531.png]]

**Inferencia:**

~S(3,1) ⇒ ~W(3,2) ^ ~W(4,1)

~B(3,1) ⇒ ~P(3,2) ^ ~P(4,1)

**Representacion del conocimiento :**

|Estado|Visit V|Stench S|Breeze B|Glitter R|Wumpus W|Pit ´P|Gold|
|---|---|---|---|---|---|---|---|
|(1,1)|1|0|0|0|0|0|0|
|(1,2)|1|0|1|0|0|0|0|
|(2,1)|1|0|0|0|0|0|0|
|(1,3)|0||1||0|1|0|
|(2,2)|0||||0|0|0|
|(3,1)|1|0|0|0|0|0|0|
|(3,2)|0||||0|0|0|
|(4,1)|0||||0|0|0|
|(1,4)|0||1|||||

**Acciones:**

A(3,1) ⇒ A(3,2)

## Movimiento 5

**Estado:** (3,2)

![[Pasted image 20250218173540.png]]

**Inferencia:**

~S(3,2) ⇒ ~W(3,3) ^ ~W(4,2)

~B(3,2) ⇒ ~P(3,3) ^ ~P(4,2)

**Representacion del conocimiento :**

|Estado|Visit V|Stench S|Breeze B|Glitter R|Wumpus W|Pit ´P|Gold|
|---|---|---|---|---|---|---|---|
|(1,1)|1|0|0|0|0|0|0|
|(1,2)|1|0|1|0|0|0|0|
|(2,1)|1|0|0|0|0|0|0|
|(1,3)|0||1||0|1|0|
|(2,2)|0||||0|0|0|
|(3,1)|1|0|0|0|0|0|0|
|(3,2)|1|0|0|0|0|0|0|
|(4,1)|0||||0|0|0|
|(4,2)|0||||0|0|0|
|(3,3)|0||||0|0|0|
|(1,4)|0||1|||||

**Acciones:**

A(3,2) ⇒ A(3,3)

## Movimiento 6

**Estado:** (3,3)

![[Pasted image 20250218173557.png]]

**Inferencia:**

~S(3,3) ⇒ ~W(3,4) ^ ~W(4,3)

~B(3,3) ⇒ ~P(3,4) ^ ~P(4,3)

**Representacion del conocimiento :**

|Estado|Visit V|Stench S|Breeze B|Glitter R|Wumpus W|Pit ´P|Gold|
|---|---|---|---|---|---|---|---|
|(1,1)|1|0|0|0|0|0|0|
|(1,2)|1|0|1|0|0|0|0|
|(1,3)|0||1||0|1|0|
|(1,4)|0||1|||||
|(2,1)|1|0|0|0|0|0|0|
|(2,2)|0||||0|0|0|
|(3,1)|1|0|0|0|0|0|0|
|(3,2)|1|0|0|0|0|0|0|
|(4,1)|0||||0|0|0|
|(4,2)|0||||0|0|0|
|(3,3)|1|0|0|0|0|0|0|
|(3,4)|0||||0|0|0|
|(4,3)|0||||0|0|0|

**Acciones:**

A(3,3) ⇒ A(4,3)

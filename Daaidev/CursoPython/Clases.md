Las clases sirven para dotar de principio y de fin a un objeto. Todo lo que esta dentro de la clase, entonces todo responde a cierta logica.
Las clases se declaran de la siguiente manera: 

``` Python
class Person:
	pass #Se ignora el error de la clase vacia
```

Se puede crear funciones dentro de las clases, pero es necesario tener un constructor, el cual se genera de la siguiente manera, pasandole el parametro self para referirse a si mismo, e incluso se puede poner valores por defecto en los parametros

 ``` Python
 class Person:
    def __init__(self, name = "Daarick " , surname):
```

De esta manera podemos llamar a la clase y agregar parametros dentro y almacenarlos, al igual que podemos crear mas funciones e incluso llamar variables de otros metodos dentro del objeto 

``` Python
class Person:
    def __init__(self, name, surname):
        self.name = name
        self.surname = surname

    def walk(self):
        print(f"{self.name} {self.surname} está caminando")

my_person = Person("Daarick", "Rodriguez")
print(my_person.name)
my_person.walk()
```

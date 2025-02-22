- Validacion cruzada de k pliegues (k-fold cross-validation)
	- Se separa el conjunto en k pliegues distintos. 
	- El conjunto de prueba se divide a la mitad y se entrena con una mitad y se prueba con el otro (En caso de k se entrena con todos menos con uno y se pueba en el otro )
	- Se invierten los papeles
	- Se saca un porcentaje de accuracy de ambas pruebas y se promedian 
- Dejar uno fuera (Leave one out cross validation)
	- Por cada paso se deja un ejemplo fuera para prueba y con el resto se entrena 
- Bootstrap sampling
	- se hacen 3 conjuntos con t elementos, y se toman t elementos aleatorios (Se permite repeticion)
	- los conjuntos escogidos aleatoria mente se toman como entrenamiento
	- se practica con un conjunto generado con los elementos que no fueron escogidos (En caso de ser un conjunto vacio, se descarta el conjunto aleatorio)

	
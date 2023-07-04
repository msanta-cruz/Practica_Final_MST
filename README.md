# Practica_Final_MST
 Materia Tratamiento de Datos 
#ImageDataGenerator(): 

Crea una instancia de la clase ImageDataGenerator, que se utiliza para generar lotes de datos de imágenes con aumento de datos opcional, preprocesamiento y otras configuraciones.

#.flow_from_directory(train_path, target_size=(224,224), classes=['CLASS_01', 'CLASS_02', 'CLASS_03', 'CLASS_04', 'CLASS_05', 'CLASS_06', 'CLASS_07', 'CLASS_08'], batch_size=10): 

Este método se llama en la instancia de ImageDataGenerator para generar el flujo de datos desde un directorio de entrenamiento específico.

		#train_path: 
		 Ruta al directorio de entrenamiento que contiene las imágenes clasificadas en subdirectorios según su clase.

		#target_size=(224,224): 
		
		Especifica el tamaño al que se deben redimensionar las imágenes cargadas. 
		En este caso, las imágenes se redimensionarán a una forma de 224x224 píxeles.

		#classes=['CLASS_01', 'CLASS_02', 'CLASS_03', 'CLASS_04', 'CLASS_05', 'CLASS_06', 'CLASS_07', 'CLASS_08']: 
		Especifica las clases a las que pertenecen las imágenes. Estas clases se deben nombrar según los subdirectorios dentro del directorio de entrenamiento.

		#batch_size=10: 
		Establece el tamaño del lote, es decir, cuántas imágenes se cargarán en cada iteración del generador. 
		En este caso, se establece en 10, lo que significa que se cargarán 10 imágenes en cada lote.

#def plots(ims, figsize=(20,6), rows=2, interp=False, titles=None):
Definición de una función llamada plots que toma como argumentos:
		#ims: 
		Las imágenes que se van a trazar.
		#figsize: 
		El tamaño de la figura (ancho, alto) en pulgadas. Por defecto, se establece en (20, 6).
		#rows: 
		El número de filas de subgráficos para mostrar las imágenes. Por defecto, se establece en 2.
		#interp: 
		Indicador booleano que especifica si se debe utilizar interpolación al mostrar las imágenes. Por defecto, se establece en False.
		#titles: 
		Una lista opcional de títulos para las imágenes. Por defecto, se establece en None.
		
		
		
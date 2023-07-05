# Practica_Final_MST

Materia Tratamiento de Datos 

Este repositorio proporciona una implementación de clasificación de imágenes usando una red neuronal convolucional que adapta y optimiza el modelo VGG16 pre-entrenado usando la técnica de transferencia de aprendizaje. 
El modelo es capaz de clasificar imágenes de animales en las siguientes 8 clases:

['CLASS_01', 'CLASS_02', 'CLASS_03', 'CLASS_04', 'CLASS_05', 'CLASS_06', 'CLASS_07', 'CLASS_08']

Dependencies
- Python
- Frameworks
- Matplotlib, Scikit-learn, Numpy, TensorFlow, Keras
- Jupyter Notebook

Entrene, pruebe y guarde el modelo

Ejecute 'Proyecto_Final_MST.ipynb' con Jupyter Notebook. 
Los datos de muestra en la carpeta de clases 'CLASS_01', 'CLASS_02', 'CLASS_03', 'CLASS_04', 'CLASS_05', 'CLASS_06', 'CLASS_07', 'CLASS_08' como referencia.

Se pueden agregar sus propias imágenes o modificar el conjunto de datos por completo. 

#ImageDataGenerator(): 

Crea una instancia de la clase ImageDataGenerator, que se utiliza para generar lotes de datos de imágenes con aumento de datos opcional, preprocesamiento y otras configuraciones.

#.flow_from_directory(train_path, target_size=(224,224), classes=['CLASS_01', 'CLASS_02', 'CLASS_03', 'CLASS_04', 'CLASS_05', 'CLASS_06', 'CLASS_07', 'CLASS_08'], batch_size=10): 

Este método se llama en la instancia de ImageDataGenerator para generar el flujo de datos desde un directorio de entrenamiento específico.

#train_path: 
	 Ruta al directorio de entrenamiento que contiene las imágenes clasificadas en subdirectorios según su clase.
  	#target_size=(224,224):
   	Especifica el tamaño al que se deben redimensionar las imágenes cargadas. En este caso, las imágenes se redimensionarán a una forma de 		224x224 píxeles.
    	#classes=['CLASS_01', 'CLASS_02', 'CLASS_03', 'CLASS_04', 'CLASS_05', 'CLASS_06', 'CLASS_07', 'CLASS_08']:
     	Especifica las clases a las que pertenecen las imágenes. Estas clases se deben nombrar según los subdirectorios dentro 		del 		directorio de entrenamiento.
      	#batch_size=10: 
   	Establece el tamaño del lote, es decir, cuántas imágenes se cargarán en cada iteración del generador. En este caso, se establece en 10, lo 	que significa que se cargarán 10 imágenes en cada lote.

#def plots(ims, figsize=(20,6), rows=2, interp=False, titles=None):
Definición de una función llamada plots que toma como argumentos:
		#ims: 
		Las imágenes que se van a trazar.
		#figsize: 
		El tamaño de la figura (ancho, alto) en pulgadas. Por defecto, se establece en (20, 6).
		#rows: 
		El número de filas de subgráficos para mostrar las imágenes. Por defecto, se establece en 2.
		#interp: 
		Indicador booleano que especifica si se debe utilizar interpolación al mostrar las imágenes. Por defecto, se establece 		en False.
		#titles: 
		Una lista opcional de títulos para las imágenes. Por defecto, se establece en None.
		
# Utilización de Red Neuronal VGG16

red neuronal VGG16 utilizando Keras y TensorFlow.

# Dentro de la linea15 "keras.engine.training.Model"

Comenzaremos a entrenar nuestro modelo 
#Proceso de entrenamiento del modelo, como el optimizador, la función de pérdida y las métricas de evaluación.

Se utiliza el optimizador Adam con una tasa de aprendizaje (learning rate) de 0.07. El optimizador Adam es una opción comúnmente utilizada en el entrenamiento de modelos de aprendizaje profundo.

La función de pérdida se establece en 'categorical_crossentropy'.

Esta función de pérdida se utiliza comúnmente en problemas de clasificación multiclase, cuando las etiquetas de clase se representan en forma de codificación one-hot.

Por último, se especifica que la métrica de evaluación a utilizar durante el entrenamiento es 'accuracy', que representa la precisión (accuracy) del modelo en la clasificación de los datos.

#Metodo de entrenamiento
Para entrenar el modelo utilizando los datos de entrenamiento y validación especificados.

En este caso, se utilizan los siguientes parámetros:#train_batches: Representa los datos de entrenamiento, que pueden ser generados por un generador de datos o simplemente un conjunto de datos de numpy.
#steps_per_epoch=1: 
Indica el número de pasos que se tomarán en cada época de entrenamiento. En este caso, se toma solo un paso, lo que 		significa que se procesa solo un lote de datos en cada época.
		#validation_data=test_batches: 
		Representa los datos de validación, que también pueden ser generados por un generador de datos o un conjunto de datos 		de numpy.
		#validation_steps=10: 
		Indica el número de pasos que se tomarán durante la evaluación del modelo en cada época de validación. En este caso, 		se toman 10 pasos, lo que significa que se evalúan 10 lotes de datos en cada época de validación.
		#epochs=20:
		Especifica el número de épocas de entrenamiento. Cada época representa una pasada completa a través de los datos de 		entrenamiento.
		#verbose=2: 
		Controla el nivel de detalle de los mensajes de registro durante el entrenamiento. Un valor de 2 muestra una barra 		de progreso por cada época y muestra información detallada sobre el progreso del entrenamiento.

Resultado

Los resultados de entrenar y probar el modelo en el conjunto de datos de muestra son los siguientes:
Precisión de entrenamiento: 1.0000
Pérdida de entrenamiento: 1.1913
Precisión de validación: 1.0000
Pérdida de validación: 2.1054


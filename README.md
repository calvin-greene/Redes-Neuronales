Hola, usé Google Translate para traducir algunos cosas entonces perdona si hay errores en grammatica o si parece mal escrito. 

Para este proyecto, se utilizó el conjunto de datos CIFAR-100 para entrenar una red neuronal convolucional (CNN). El análisis de datos inicial implicó:
Normalización de datos: los valores de píxeles se normalizaron para oscilar entre 0 y 1 dividiéndolos por 255,0.
Exploración de datos: examinó brevemente imágenes de muestra y sus etiquetas correspondientes para comprender la diversidad y complejidad del conjunto de datos.

comencé con una arquitectura CNN simple que utiliza dos capas convolucionales con filtros de 32, y 64, seguida de una agrupación promedio global y una capa de salida densa para clasificación.
Se intentó implementar el aumento de datos utilizando ImageDataGenerator para mejorar la diversidad de datos:. A pesar de implementar técnicas de aumento de datos como rotación, desplazamientos y volteos, el modelo no mostró la mejora esperada en la precisión de la validación. posiblemente debido a que la arquitectura del modelo no era lo suficientemente sólida como para beneficiarse de los datos aumentados. En consecuencia, decidió volver a la configuración de capacitación original sin aumento de datos para mantener un mejor control sobre el proceso de aprendizaje.

Se notó baja precisión y signos de desajuste; Aumentó el número de filtros en las capas convolucionales para mejorar la capacidad del modelo para aprender patrones complejosÑ agregué un capa de convolucion con 128 filtros, lo cual mejoré las prediciones. 
Tambien, ajusté el cantidad de epochs de 2 a 30 y finalmente a 50 para encontrar el mejor nivel de optimizacion

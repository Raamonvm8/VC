# Nombres grupo 12:
Ramón Valls Martin
Noah Ramos González

## TAREAS:

### Tarea 1: 

Tarea 1:
Empezamos cargando la imagen con ruido, seguida de la conversión a escala de grises. Posteriormente, se aplican un método de umbralizado, Otsu, ya que nos daban complicaciones al detectar contornos en la foto. Luego, se suaviza la imagen mediante un filtro Gaussiano para reducir el ruido, y se extraen los contornos utilizando el método cv2.findContours. Los contornos externos los dibujamos basándonos en su área y redondez, y los contornos redondos se almacenan. 
El usuario puede interactuar con la imagen para seleccionar una moneda haciendo clic sobre ella, lo cual permite calcular la relación píxeles por milímetro utilizando el diámetro conocido de la moneda. A continuación, se identifican las monedas detectadas comparando sus diámetros con valores de referencia, y se cuentan las cantidades de monedas de cada tipo. Finalmente, se calcula el valor total de las monedas y se muestra el número de monedas detectadas junto con su valor total y la clasificación por tipo, utilizando funciones como cv2.drawContours para visualizar los contornos en la imagen original y manejando eventos de clic para la selección de monedas en la interfaz de usuario.

Los problemas que hemos visto es que no es eficaz al 100%, hay veces que detecta a la perfección todas las monedas, y otras veces que falla en algunas por diferencias de diámetros.


### Tarea 2: Clasificación de particulas

**Introducción**

En esta tarea, se ha desarrollado un sistema de clasificación de partículas en imágenes utilizando técnicas de procesamiento de imágenes y aprendizaje automático. El objetivo es identificar y clasificar tres tipos de partículas: fragmentos, pellets y alquitrán, a partir de imágenes capturadas sin redimensionar. Para lograr esto, se ha implementado un flujo de trabajo que incluye el preprocesamiento de imágenes, la extracción de características geométricas y visuales, la aumentación de datos, y finalmente, el entrenamiento y evaluación de un clasificador basado en Random Forest.

**Desarrollo de la Tarea**

El primer paso del proceso consistió en cargar las imágenes de las tres clases de partículas. Para cada imagen, se aplicaron técnicas de preprocesamiento que incluían la conversión a escala de grises, el desenfoque gaussiano y el umbralizado binario. Esto permitió resaltar los contornos de las partículas, facilitando su análisis.

Una vez obtenidos los contornos, se desarrolló una función para extraer características geométricas y visuales de cada partícula, incluyendo el área, perímetro, compacidad, relación de área con el contenedor, relación de aspecto, y características de textura representadas por histogramas de intensidad. Estas características son cruciales para la posterior clasificación de las partículas.

Para mejorar la robustez del modelo, se implementó un aumento de datos que consistía en aplicar transformaciones como el volteo horizontal, rotaciones y ajustes de brillo a las imágenes. Esto permitió generar un conjunto de datos más variado y ayudar al modelo a generalizar mejor en situaciones no vistas durante el entrenamiento.

Tras el preprocesamiento y la extracción de características, los datos se organizaron en un DataFrame para su análisis. Se dividieron en conjuntos de entrenamiento y prueba, utilizando una proporción del 70% para el entrenamiento y el 30% para la evaluación del modelo. A continuación, se utilizó un clasificador Random Forest, que se entrenó con los datos de entrenamiento para aprender a distinguir entre las diferentes clases de partículas.

Finalmente, se evaluó el rendimiento del modelo utilizando métricas como precisión, recall y F1-score, junto con la matriz de confusión, lo que permitió identificar el desempeño del clasificador en cada clase. Los resultados mostraron que el modelo tenía un buen rendimiento, con altas precisiones y recalls en general, aunque con algunas variaciones entre las clases.

**Conclusión**

En resumen, el sistema desarrollado ha demostrado ser efectivo para la clasificación de partículas en imágenes. La combinación de técnicas de procesamiento de imágenes, extracción de características y aprendizaje automático ha permitido lograr resultados satisfactorios. Las métricas de evaluación indican que el modelo puede identificar con precisión las partículas, aunque se pueden realizar mejoras en la clasificación de algunas clases. 

![image](https://github.com/user-attachments/assets/c04a667c-a450-423e-b81a-d2b32c76c70f)

![image](https://github.com/user-attachments/assets/0a24a023-b6a0-4263-ae41-f3753151a44a)









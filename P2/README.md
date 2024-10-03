## Práctica 2. Funciones básicas de OpenCV

### Tarea 1
Objetivo:
Determinar el número máximo de píxeles blancos por fila y por columna en una imagen procesada por el algoritmo Canny, y contar cuántas filas y columnas tienen un número de píxeles blancos superior o igual al 95% del valor máximo.

Desarrollo:
Se utiliza el algoritmo Canny para detectar bordes en la imagen y se cuenta el número de píxeles blancos (255) por filas y columnas mediante la función cv2.reduce. Estos conteos se normalizan dividiendo por el producto del valor máximo de píxel (255) y el número de columnas o filas, obteniendo el porcentaje de píxeles blancos. 

A continuación, se calcula el número máximo de píxeles blancos tanto por filas como por columnas, y se define un umbral del 95% del valor máximo para identificar cuántas filas y columnas tienen un número de píxeles blancos superior o igual a ese umbral. 

Finalmente, los resultados se visualizan mostrando un gráfico que refleja la cantidad de píxeles blancos por fila, junto con la imagen de salida de Canny, y se imprimen los valores máximos y las filas y columnas que cumplen con el umbral.

<img width="360" alt="0 2024-10-03 a las 12 26 43" src="https://github.com/user-attachments/assets/a02676c3-9a3a-4e0c-87f5-a210f78a4a6a">


### Tarea 2
Objetivo:
Aplicar umbralizado a la imagen resultante de Sobel, realizar el conteo de píxeles no nulos por filas y columnas, calcular los máximos por cada uno, determinar cuáles están por encima del 95% del máximo, y remarcar visualmente dichas filas y columnas. Comparar estos resultados con los obtenidos utilizando la técnica de Canny.

Desarrollo:
Se inicia aplicando el filtro Sobel para detectar bordes en las direcciones horizontal y vertical de la imagen suavizada con un filtro gaussiano. 

Posteriormente, se combinan los resultados de ambos ejes y se convierte la imagen a 8 bits. Luego, se aplica un umbral para binarizar la imagen y se genera una imagen binaria umbralizada. 

Con esta imagen, se cuenta el número de píxeles no nulos por filas y columnas utilizando cv2.countNonZero, y se calcula el número máximo de píxeles por filas y columnas. Se establece un umbral del 95% de ese valor máximo, determinando cuáles filas y columnas superan este umbral. 

Finalmente, se remarca visualmente esta información mediante gráficos que muestran tanto los píxeles no nulos por filas y columnas como las imágenes de Sobel y Canny, permitiendo una comparación directa de los resultados de ambos enfoques.

<img width="783" alt="0 2024-10-03 a las 12 20 32" src="https://github.com/user-attachments/assets/eb16e224-7ab7-4fd0-bc01-664acf74c2ed">
<img width="592" alt="0 2024-10-03 a las 12 25 48" src="https://github.com/user-attachments/assets/c1dbc0ed-3b0e-446f-8843-56fc53ec5b32">


### Tarea 3
Objetivo: 
El objetivo de esta tarea fue crear un demostrador que capture imágenes en tiempo real desde la cámara y aplique técnicas de procesamiento de imágenes con OpenCV. Además de mostrar la imagen original, el demostrador debía incluir al menos dos ejemplos prácticos de lo aprendido en las prácticas.

Desarrollo: 
Se utilizaron las siguientes técnicas:

Filtro Sobel: El operador Sobel se aplicó para detectar bordes en las direcciones horizontal y vertical, combinando ambos resultados para mostrar los bordes presentes en la imagen.

Filtro Canny: Se utilizó el algoritmo de Canny para detectar bordes de manera más precisa y detallada, siguiendo un proceso de suavizado, derivación y umbralización.

Conteo de píxeles blancos por filas y columnas: En la imagen resultante del filtro Canny, se contó el número de píxeles blancos por filas y columnas. Se destacó visualmente las filas y columnas con una cantidad de píxeles mayor o igual al 95% del máximo.

Conclusiones: 
El demostrador mostró claramente la diferencia entre los filtros Sobel y Canny. Mientras Sobel detecta bordes más suaves en direcciones específicas, Canny es más preciso en la detección de contornos definidos. El análisis de píxeles blancos permitió identificar y resaltar las regiones con mayor cantidad de bordes en la imagen, facilitando la detección de áreas importantes.

![image](https://github.com/user-attachments/assets/912243d6-6052-4bad-86e9-927e11c77870)

![image](https://github.com/user-attachments/assets/39b39573-9cb6-449b-b4dc-124e9b744c89)

![image](https://github.com/user-attachments/assets/1685ee19-d605-4948-bdca-b080e894dac6)

![image](https://github.com/user-attachments/assets/2fe504e6-480f-425d-ac2f-57f5d2957251)


### Tarea 4

Objetivo: 
El objetivo de esta tarea es desarrollar un demostrador interactivo inspirado en las instalaciones visuales de los vídeos “**My Little Piece of Privacy**” y “**Virtual Air Guitar**”. Utilizando herramientas de procesamiento de imágenes en OpenCV, debemos capturar el movimiento del usuario frente a la cámara y generar efectos gráficos visuales en tiempo real basados en dicho movimiento. Esto permite interpretar de forma creativa los cambios en la imagen y exhibir lo aprendido sobre detección de movimiento y procesamiento visual.

Desarrollo:

1. **Captura de video**: 
   Se inicia capturando la imagen de la webcam utilizando `cv2.VideoCapture(0)`. Cada frame se procesa en tiempo real, convirtiéndose a escala de grises y aplicando un filtro Gaussiano para suavizar la imagen y reducir el ruido.

2. **Detección de movimiento**: 
   El movimiento se detecta comparando el frame actual con el anterior mediante la función `cv2.absdiff`. A partir de esta diferencia, se aplica un umbral que destaca las áreas donde hay cambios significativos. Luego, se buscan los contornos de estas zonas de movimiento para proceder a la creación de efectos visuales.

3. **Generación de efectos gráficos**: 
   Para representar el movimiento, se dibujan:
   - **Círculos** que siguen el área de movimiento, cuyo tamaño depende del área de los contornos detectados.
   - **Líneas diagonales** que atraviesan las zonas activas para indicar la dirección del movimiento.

4. **Superposición en la imagen original**: 
   Los efectos gráficos generados se dibujan sobre un lienzo negro y luego se superponen a la imagen original de la cámara con la función `cv2.addWeighted`, lo que permite mostrar tanto la imagen en vivo como los efectos generados en tiempo real.

5. **Interacción en tiempo real**: 
   El programa se ejecuta continuamente, procesando cada frame hasta que el usuario presione "ESC", momento en el cual se detiene la captura de video y se cierran las ventanas.

Conclusiones: 
Este demostrador interactivo utiliza técnicas de detección de movimiento basadas en la diferencia de fotogramas y visualización gráfica para generar efectos en tiempo real. Se ha logrado aplicar lo aprendido en la detección de bordes y contornos para crear una experiencia visual que responde al movimiento, reimaginando los conceptos vistos en los vídeos. Esto permite a los usuarios interactuar con el sistema de forma creativa, mostrando cómo el procesamiento de imágenes en tiempo real puede tener aplicaciones artísticas.

![alt text](<0 2024-10-03 a las 13.47.18.png>)


1. Creación de una Imagen con Textura de Tablero de Ajedrez:

Primero de todo usamos un tablero de 350x350 y los cuadrados son de 50x50 píxeles. 
Para pintarlos usamos un bucle for i-j que parte desde 0 hasta el ancho y alto recorriendo todo el tablero, poniendo como medio la medida de la casilla (50px). De esta forma, si la fila/celda + columna/celda es impar, pinta esa celda de negro, si es par de blanco, y así conseguimos terminar el tablero de ajedrez.

2. Creación de una Imagen al Estilo Mondrian:

Se ha creado una imagen de 350 x 350, donde se han pintado los rectangulos de forma aleatoria. La generación de rectángulos se hace for filas, dictaminando el tamaño de la fila, por el tamaño del primer rectángulo generado, las coordenadas de los rectángulos serán guardadas en una lista, para posteriormente, en las siguientes filas a dibujar, tener encuenta la altura del rectángulo superior y quitar el riesgo a superponer los rectángulos.

3. Creación de una Imagen al Estilo trablero de ajedrez usando OpenCV:



4. Modificación de los Valores de un Plano de la Imagen:

Seguimos los pasos propuestos de la práctica usando la cámara web cam y modificamos los valores de los canales verde y azul. Primero separando los 3 canales y luego creando variables para su modificación. El canal rojo lo dejamos sin modificar para poder comparar con una imagen original, el canal verde lo modificamos haciendo un efecto de difuminado, y el canal azul lo modificamos haciendo un efecto de detección de bordes, que lo que hace es resaltar por ejemplo el pelo cuando nos enfoca la camara o algun objeto como la cabecera de una cama. Y por último los mostramos en el collage de forma vertical en la pantalla.

5. Pintura de Círculos en las Posiciones del Píxel Más Claro y Más Oscuro de la Imagen:

Lo que hicimos para esto fue pasar una imagen cualquiera a escalado de grises para detectar mejor los pixeles mas claros y oscuros ya que van de intensidad 0 hasta 255. Creamos variables pixel_oscuro y pixel_claro para detectar cual era el más oscuro y claro y variables de las coordenadas de esos pixeles para colocar el circulo encima. 
Creamos los circulos con cv2.circle() y por último mostramos la imagen marcando el pixel más claro y más oscuro con plt.imshow().

6. Propuesta de Pop-Art:



Referencias:

https://chat.openai.com

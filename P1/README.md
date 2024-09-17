Creación de una Imagen con Textura de Tablero de Ajedrez:

Mi compañero y yo, hemos llegado a una solución parecida sobre la creación de un tablero de ajedrez, para ello, utilizamos un tablero de 800x800 y los cuadrados son de 40x40 píxeles, para el pintado, se ha utilizado dos bucles for, haciendo que se pinten cada cuadrado teniendo encuenta el espacion en blanco y el desfase de las filas pares.

Creación de una Imagen al Estilo Mondrian:

Se ha creado una imagen de 500 x 500, donde se han pintado los rectangulos de forma aleatoria. La generación de rectángulos se hace for filas, dictaminando el tamaño de la fila, por el tamaño del primer rectángulo generado, las coordenadas de los rectángulos serán guardadas en una lista, para posteriormente, en las siguientes filas a dibujar, tener encuenta la altura del rectángulo superior y quitar el riesgo a superponer los rectángulos.

Creación de una Imagen al Estilo trablero de ajedrez:

Para la realización de esta tarea, replicamos los hecho en la tarea 1, pero añadiendo las herramientas de creación de rectángulos de OpenCV, por lo tanto, simplemente usando la misma metodología de un doble bucle pintamos los rectángulos en la posición indicada.
Modificación de los Valores de un Plano de la Imagen:

Juan Jesús se encargo de en base a una imagen generar 3 copias, una ajusta los valores de los canales rojo y azul disminuyendolos, luego en otra la pone a escala de grises y la última en blanco y negro.
Antonio se encargo de realizar una captura de video de la webcam y por cada fotograma separa el canal azul, y de manera aleatoria modifica su valor mostrandolo de imagen.
Pintura de Círculos en las Posiciones del Píxel Más Claro y Más Oscuro de la Imagen:

Juan Jesús se encargo de en base a una imagen, sacó las posiciones del valor máximo y mínimo de los pixeles de la imagen y en esas posiciones pinto un círculo rojo para el pixel más oscuro y un círculo verde para el pixel más claro.
Antonio se encargo de realizar una captura de video de la webcam y por cada fotograma lo transformó en escala de grises para mejorar la captación de las intensidades de los pixeles, para luego sacar las posiciones del valor máximo y mínimo de los pixeles de la imagen y en esas posiciones pintar un círculo rojo para el pixel más oscuro y un círculo verde para el pixel más claro.
Propuesta de Pop-Art:

Se realiza una captura de video de la webcam y por cada fotograma se copia 4 veces; la primera copia será convertida con colores inversos, la segunda copia dejará únicamente el canal rojo presente, la tercera copia dejará el canal verde presente y la última copia tendrá el canal azul presente. Luego se juntan mostrandolas.

Referencias:

https://chat.openai.com

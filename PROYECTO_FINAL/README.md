## Práctica FINAL

Grupo 12: 
Ramón Valls Martin.
Noah Ramos González.

## Introducción:
En esta práctica final, hemos desarrollado una calculadora interactiva que permite realizar operaciones matemáticas. La calculadora tendrá 2 modalidades, la primera, mediante la tecnología de reconocimiento de manos de MediaPipe, los usuarios que la usen podrán realizar operaciones como suma, resta, multiplicación y divisiones, controlando la aplicación de manera intuitiva y con ayuda de imagenes para los gestos de las operaciones, y haciendo los respectivos numeros con la mano para que vayan apareciendo en pantalla. Además, la calculadora cuenta con una segunda modalidad que trata de...
Para cambiar de modo en la calculadora se deberán pulsar las teclas '1' para el modo 1 y la '2' para cambiar al modo 2.


## 1. Modo 1: Calculadora con gestos de manos
Este primer modo, como dijimos, permite al usuario realizar cálculos utilizando gestos de la mano. Con la tecnología de MediaPipe, la app es capaz de detectar diferentes posiciones de los dedos y asignarles números y operaciones en tiempo real.

Funcionamiento:
El usuario debe gesticular con los dedos el número que desee, si levanta 2 dedos, saldrá un 2 en pantalla, si sigue gesticulando números se pondrán en fila uno a la derecha de otro y formarán un entero más grande, esto ocurre hasta que detecta un signo de operación matemática, los cuales se puede ver en la parte derecha inferior de la pantalla cuando se inicia este modo para saber cual es cada uno. 
Desde que gesticulas un signo de operación, detecta que se quiere operar el entero que está a la izquierda del signo por el que viene a continuación a la derecha. Ahora debemos de seguir añadiendo el número que queremos como segundo factor, y así hasta que se detecte el signo igual (también se puede ver la imagen en la pantalla). Cuando detecta el signo igual entonces devuelve el resultado de la operación y detiene la detección de dedos hasta pasados 5 segundos que se reincia a otra operación.


## 2. Modo 2: 
(Descripción pendiente)




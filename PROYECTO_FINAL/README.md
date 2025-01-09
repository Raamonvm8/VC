## Práctica FINAL

Grupo 12: 
Ramón Valls Martin.
Noah Ramos González.

## Introducción:
En esta práctica final, hemos desarrollado una calculadora interactiva que permite realizar operaciones matemáticas. La calculadora tendrá 2 modalidades, la primera, mediante la tecnología de reconocimiento de manos de MediaPipe, los usuarios que la usen podrán realizar operaciones como suma, resta, multiplicación y divisiones, controlando la aplicación de manera intuitiva y con ayuda de imagenes para los gestos de las operaciones, y haciendo los respectivos numeros con la mano para que vayan apareciendo en pantalla. Además, la calculadora cuenta con una segunda modalidad que trata de resolver operaciones matemáticas como las anteriores en la que se nos mostrará por pantalla dicha operación y el usuario debe de introducir la solución a la espera de ver si es correcta o no.
Para cambiar de modo en la calculadora se deberán pulsar las teclas '1' para el modo 1 y la '2' para cambiar al modo 2.


## 1. Modo 1: Calculadora con gestos de manos
Este primer modo, como dijimos, permite al usuario realizar cálculos utilizando gestos de la mano. Con la tecnología de MediaPipe, la app es capaz de detectar diferentes posiciones de los dedos y asignarles números y operaciones en tiempo real.

Funcionamiento:
El usuario debe gesticular con los dedos el número que desee, si levanta 2 dedos, saldrá un 2 en pantalla, si sigue gesticulando números se pondrán en fila uno a la derecha de otro y formarán un entero más grande, esto ocurre hasta que detecta un signo de operación matemática, los cuales se puede ver en la parte derecha inferior de la pantalla cuando se inicia este modo para saber cual es cada uno. 
Desde que gesticulas un signo de operación, detecta que se quiere operar el entero que está a la izquierda del signo por el que viene a continuación a la derecha. Ahora debemos de seguir añadiendo el número que queremos como segundo factor, y así hasta que se detecte el signo igual (también se puede ver la imagen en la pantalla). Cuando detecta el signo igual entonces devuelve el resultado de la operación y detiene la detección de dedos hasta pasados 5 segundos que se reincia a otra operación.


## 2. Modo 2: Resolución de operaciones con gestos de mano
Este segundo modo se basa principalmente en que por pantalla se muestra una operación que el usuario deberá de resolver mediante gestos con la mano. Al igual que en el otro modo utilizamos la tecnología de MediaPipe para detectar las diferentes posiciones de los dedos y así escribir los números en tiempo real.

Funcionamiento:
El usuario una vez entra en este modo verá en pantalla una operación de dos números y debajo saldrá una zona donde irá la solución. El usuario a través de los gestos con la mano irá introduciendo la cifra que crea que es la solución de la operación. Por ejemplo, se muestra por pantalla la operación 8*3, el usuario para resolver la operación deberá de levantar primero 2 dedos para que se muestre en la parte de la solución un 2 y luego un 4 para que seguidamente del 2 aparezca el 4. Una vez que el usuario considera que ha introducido el resultado correcto de la operación, hará el símbolo que tenemos establecido como igual con la mano. Luego de esto si el resultado es correcto, se mostrará en la pantalla CORRECTO!. En cambio, si no lo es se mostrará INCORRECTO! y el resultado correcto de la operación. Una vez resulta la operación con el paso de varios segundos aparecerá en pantalla un nueva operación a resolver.





Nombres grupo 12:
Ramón Valls Martin
Noah Ramos González

TAREAS:

Tarea 1:
Empezamos cargando la imagen con ruido, seguida de la conversión a escala de grises. Posteriormente, se aplican un método de umbralizado, Otsu, ya que nos daban complicaciones al detectar contornos en la foto. Luego, se suaviza la imagen mediante un filtro Gaussiano para reducir el ruido, y se extraen los contornos utilizando el método cv2.findContours. Los contornos externos los dibujamos basándonos en su área y redondez, y los contornos redondos se almacenan. 
El usuario puede interactuar con la imagen para seleccionar una moneda haciendo clic sobre ella, lo cual permite calcular la relación píxeles por milímetro utilizando el diámetro conocido de la moneda. A continuación, se identifican las monedas detectadas comparando sus diámetros con valores de referencia, y se cuentan las cantidades de monedas de cada tipo. Finalmente, se calcula el valor total de las monedas y se muestra el número de monedas detectadas junto con su valor total y la clasificación por tipo, utilizando funciones como cv2.drawContours para visualizar los contornos en la imagen original y manejando eventos de clic para la selección de monedas en la interfaz de usuario.

Los problemas que hemos visto es que no es eficaz al 100%, hay veces que detecta a la perfección todas las monedas, y otras veces que falla en algunas por diferencias de diámetros.
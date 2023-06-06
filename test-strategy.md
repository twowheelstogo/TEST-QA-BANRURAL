Se inicia con el proceso de QA sobre el codigo publicado en GITHUB
Se ejecutó el programa index.html y se probó la funcionalidad.
Tal como lo indica en las intrucciones se utilizó la consola del navegador para poder visualizar los errores que mostrara.

1. Se ingresa un número aleatorio, sin obtención de ninguna respuesta, se valida en la consola.
   En esta indica que hay un error en la línea 81 en la sintaxis del evento .addeventListener(Uncaught TypeError: guessSubmit.addeventListener is not a function), el evento estaba mal escrito ya que la forma correcta es .addEventListener.

   1.5 Tambien se presenta en la línea 89 dicho problema de sintaxis.

2. Se procede a corregir dicha sintaxis.

3. Luego de la corrección y ejecución del programa, ve verifica nuevamente y se encuentra con un error en la linea 70, (Uncaught TypeError: Cannot set properties of null (setting 'textContent') ).

4. Esto se corrige en la linea 41 (const lowOrHi = document.querySelector('.lowOrHi')), se le agrega "." para poder hacer un correcto llamado del elemento.

5. Se corrige ortografía de la linea 63, ya que la palabra correcta es "Perdiste".

6. Se verifica que hay un error con la generación de números aleatorios en la linea 36, en lugar de generar un número aleatorio entre 1 y 100, el código solo genera un número aleatorio entre 0 y 10.

7. Se procede a la corrección del mismo modificando la linea de codigo por la siguiente: let randomNumber = Math.floor(Math.random() * 100) + 1; para generar un número aleatorio entre 1 y 100.

8. En la linea 37, se indica que se tienen 5 intentos para mostrar mensaje de error (const ATTEMPS = 5).

9. Se corrige colocando 10 tal como lo indican las instrucciones (const ATTEMPS = 10).

10. El código no valida si el número ingresado es entero

11. Se agrega una comprobación para verificar si el número ingresado es valido en la linea 48, utilizando la función Number.isNaN. Si el número no es un entero, mostrar una alerta y detener la ejecución del código.

12. Hay un error con la asignación de color cuando muestra el mensaje "Perdiste", en vez de asignar rojo, asigna negro.

13. Se reemplaza la palabra "black" por "red" para la correcta asignación, esto en la línea 68. 

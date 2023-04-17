--FREDY JOEL SIS YOL-- FREDYSIS2001@GMAIL.COM --
--PRUEBAS REALIZADAS SEGUN INSTRUCCIONES--
Como paso inicial se formateó el código para verlo de una manera mas ordenada y poder trabajar mas cómodo
el contenido de la etiqueta script debe estar dentro de todo el cuerpo html
1) Ingresar un número: error encontrado que no arroja ningún resultado por lo que se procedió a revisar ciertas partes de la consola encontrando lo siguiente:
   -error en la línea 91 en la sintaxis del evento .addeventListener, claramente el evento estaba mal escrito ya que la sintaxis correcta es la siguiente .addEventListener.
   se proceció a solucionar el error y arroja el mensaje 
   -En la linea 99  se localizó otro error de sintaxis del mismo tipo, .addeventListener y se corrigió a .addEventListener y este evento se encarga de limpiar la respuesta anterior en el label "Número aleatorio anterior"
   
2) En la linea 53 const "lowOrHi = document.querySelector('lowOrHi');" le faltaba el punto antes de '.lowOrHi' en si esta linea de codigo es la que se encarga de mostrar el 
   mensaje de si el numero que se ingreso es mayor o menor al numero correcto que esta generado para ganar el juego.
   -al hacer esta correccion cuando se ingresa el numero en la caja de texto muestra el mensaje de que el numero es < o > 

3) En la linea 46 no esta generando el numero aleatorio del 1 al 100 como se espera, al hacer pruebas de la generacion de numeros aleatorios se encontro el error que los numeros
   que esta generando numeros flotantes por lo que se tiene que sustituir la linea de codigo que es la siguiente "let randomNumber = Math.random() * 10;" por la siguiente "let randomNumber = Math.floor(Math.random() * 100) + 1;", la linea de codigo corregida se asegura de que los numeros generados sean entre 1 a 10 y estos multiplicados por 10.
   - al igual se hizo el mismo cambio en la linea 118 donde se sustitiyo la linea anterior por la siguiente "randomNumber = Math.floor(Math.random() * 100) + 1;"

   Al no sustituir esa linea de codigo, generaba numeros con decimales, tipo flotantes


4) Aunque ingrese un numero incorrecto pero sigo intentando, en el quinto intento me sale que el resultado es correcto, con cualquier combinacion de numeros en el quinto intento 
   sale correcto, cuando los intentos deben ser hasta 10, asi que se cambia el valor de la variable "ATTEMPS = 10" para subir el numero de intentos como se indica en las
   instrucciones del juego
   -aunque se hayan cambiado la cantidad de intentos, en el ultimo arroja el resultado correcto por lo que se el error esta en la funcion "checkGuess" en el primer else if donde se estaba comparando el contador de intentos "guessCount" con el numero de intentos "ATTEMPS" entonces esto detectaba que el intento numero 10 era igual numero de intentos 10, por eso todos los resultados daban correctos en el intento numero 5 0 10.
   -se sustituyo por el valor ingresado por el usuario "userGues" y el "randomNumber" para ver si los valores son los mismos.
   -se comprueba imprimiendo la variable "randomNumber" en consola para ver el numero generado y se ingresa comprobando que la comparacion es correcta en valor y tipo 
   -se cambia el primer "else if" por el "if" porque de no hacerlo al ingresar la respuesta correcta en el intento #10 arrojaba un resultado incorrecto aunque no lo fuera.

5) en la validacion si el numero era entero o decimal sin que se sumara un intento se le agrego un if usando el operador isNan validando los parametros solicitados, comprobando que no se suman los intentos.

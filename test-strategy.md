Buenos días, he realizado el testeo al juego de adivinar el número, los hallazgos son los siguientes:

1) Se encontró que el tipo de input es de text, lo que se quiere ingresar es un numero entero, por lo que se cambio de tipo "text" a tipo "number".

    Solución: Linea 32, <input type="number" id="guessField" class="guessField">

2) Se encontro que la variable ATTEMPS, es quíen posee el número máximo de intentos, por lo que se cambió a 10 intentos máximos.
    Solución: Línea 47,  const ATTEMPS = 10;

3) En el apartado de la declaración de las constantes, precisamente en la constante lowOrHi, se observó la falta de un "."(punto), por lo que no realizaba el evento de cambiar el texto y no dejaba proceder con el resto.
    Solución: Línea 50, const lowOrHi = document.querySelector('.lowOrHi');

4) El evento Click esta mal escrito, precisamente en ".addEventListener", la letra E de "Event" estaba escrito en minúscula, por lo que se corrigió su sintaxis.
    Solución: Línea 95,  guessSubmit.addEventListener('click', checkGuess);
    
5) El número aleatorio se realizaba del 0 al 9, dicho número era decimal, se requiere que el número sea del 1 al 100, perteneciendo al grupo de enteros, por ello se agregó la función "Math.floor" lo que realiza la función, es redondear el número decimal hacia abajo, de esta manera conseguir un número entero, agregando una adición para que no posea el número cero.
    Solución:  Línea 45, let randomNumber = Math.floor(Math.random() * 100) + 1;

6) La variable userGuess se esta obtiniendo correctamente, con la diferencia que el tipo de dato almacenado es de tipo String, por lo que se realizó una conversión para obtener el dato en tipo númerico con punto flotante, de esta manera el dato podrá ingrese a las condicionales If.
    Solución: Línea 59-60
                let userGuessString = guessField.value;
                let userGuess = parseFloat(userGuessString);

7) En el apartado de la lógica del juego (En los condicionales "If"), se tiene inverso las condiciones, debido a que al evaluar el número ingresado por el usuario, al ser igual que el random debe de indicar que Ganó, pero se encontro que idicaba al usuario que perdio, de esta misma forma al evaluar el número de intentos.
    Solución: Línea 71-79

8) El evento Click esta mal escrito, precisamente en ".addEventListener", la letra E de "Event" estaba escrito en minúscula, por lo que se corrigió su sintaxis.
    Solución: Línea 103,  resetButton.addEventListener('click', resetGame);

9) El número aleatorio se realizaba unicamente el cero, luego se le sumaba un 1, por tal razón el número aleatorio siempre era 1, por ello se agregó la función "Math.floor" lo que realiza la función, es redondear el número decimal hacia abajo, de esta manera conseguir un número entero, agregando una adición para que no posea un cero.
    Solución:  Línea 122, randomNumber = Math.floor(Math.random() * 100) + 1;

10) En la concatenación de los números ingresados, se agregó un guión para separar visualmente los numeros ya ingresados.
    Solución: Línea 69.

11) Realizar un condicional "If" antes de comprobar si igual al número random, con el objetivo de capturar el número y verificar si es sistinto de entero, si es distinto indicar al usuario que el número a ingresar debe ser entero, luego retornar a una nueva captura de número ingresado.
    Solución: Línea 62-66.
    Recomendación: En la Línea 60, Se puede realizar el cambio en la conversión del número ingresado, en vez de utilizar "parseFloat(userGuessString)", se puede utilizar "parseInt(userGuessString);", de esta manera se puede quitar la condicional "If" de las líneas 62-66, ya que el número se convertirá en número entero, sin importar si el usuario ingresa un decimal.
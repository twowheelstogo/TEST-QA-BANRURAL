Visualizando el codigo note los siguientes errores
1. La variable randomNumber me puede arrojar valores con punto decimal, ademas se esta multiplicando
   unicamente por 10 cuando tendria que ser por 100 ya que funcion Math.random genera vales entre 0 y 1, 
   una recoemndacion seria utilizar la funcion Math.floor
2. En las instruccion especificaba que serian 10 intentos para adivinar el
   numero, pero en el codigo tenemos solo 5 intentos disponibles.
3. Note que si el numero ingresado es igual al random tenia un mensaje de PERDISTE con color negro y tenia que decir 
   FELICITACIONES, ADIVINASTE EL NUMERO y tenia que ser en color verde.
4. Cuando llego al limite de los intentos salta un mensaje de FELICITACIONES, cuando deberia ser PERDISTE.
5. Cuando aun no se ha adivinado el numero me arroja el mensaje de INCORRECTO con color verde y deberia ser color Negro.

La notación científica permite escribir de modo abreviado números muy grandes (con muchos dígitos enteros) y números muy cercanos a cero (con muchos dígitos fraccionarios).
Las expresiones que utilizan esta notación cuentan con dos partes:

* *Mantisa*: representa la parte significativa del número. Toma un valor en el intervalo (0,9]
* *Exponente*: Permite “recordar” dónde estaba la coma antes de abreviar.

Ejemplos:

* 62000000000000000000000 = 62 * 10²⁰
* 0,0000000000000000000062 = 62 * 10⁻²⁰

Si quisiésemos aprovechar esto en la representación de números dentro de una computadora, usaríamos base 2: Por ejemplo, suponer la cadena ```11000000```. Su interpretación en ***punto fijo BSS(8,0)*** es: 

* I(11000000) = 2⁷+2⁶ = 64+128 = 192

Si buscamos  “comprimirla” debemos correr la coma 6 lugares, es decir remover los 0s de la derecha y escalar una cadena más chica (11). 

* I(11000000) = I(11) * 2⁶ = ( 2²+2¹ )*2⁶ = 3 * 64 = 192

Veamos cómo se almacena esta cadena ahora: 

* La mantisa es 11
* El exponente es 110
* La base del exponente no hace falta registrarla porque es siempre 2

Entonces a la hora de almacenarlas, se concatenan ambas subcadenas: ```11110``` (mantisa/exponente), aunque podría elegirse concatenar en otro orden (11011).
Así, con pocos bits de exponente se pueden guardar números muy grandes. Veamos: 

* Con 2 bits se puede representar (en bss) hasta el número 3, y por lo tanto se pueden “comprimir” 3 posiciones (o ceros).
* Con 4 bits se puede representar (en bss) hasta el número 15, y por lo tanto se pueden “comprimir” 15 posiciones (o ceros). I(1100000000000000)  =  I(11)*2¹⁵

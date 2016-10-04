Las cadenas se pueden guardar en el formato que se elija, pero se define una vez para todo el sistema. Entonces también se elige un sistema para la mantisa y otro para el exponente (entre los que ya conocemos).

Los pasos entonces para interpretar una cadena:

1. Interpretar la mantisa m=I(M)
2. Interpretar el exponente e = I(E)
3. Componer el número N=m * 2^e

Veamos un ejemplo en un sistema ```[mantisa BSS(2)][exponente EXC(2,2)]```.  ¿Cuánto vale I(0110)? 

* Ibss(01) = 1 
* Iex(10) = 2-2 = 0 
* Por lo tanto N = 1*2⁰ = 1

### Poner en práctica

¿Cuánto vale I(1111)? 

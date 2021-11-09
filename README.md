# Compilación y ejecución en el laboratorio en línea

## Etapas del desarrollo de programas

Para resolver un problema utilizando un programa de ordenardor tenemos que pasar por las siguientes etapas

- **Análisis** Definición clara de lo que hace el programa: especificación de la información de entrada y de salida, lista de tareas (funciones o requisitos) de manipulación de información a realizar.
- **Diseño**  del algoritmo (método para resolver el problema mediante una serie de pasos claramente detallados)
- **Codificación** Escritura del algoritmo en un lenguaje de programación normalmente de alto nivel y almacenamiento del mismo en un archivo fuente (programa fuente).
- **Traducción** (compilación) del programa fuente a un programa objeto (en lenguaje máquina). El resultado será bien un archivo objeto o bien un listado de errores de compilación; en este último caso habrá que corregir dichos errores y volver a traducir hasta obtener el programa objeto.
- **Montaje** (mezcla, fusión, enlace o “linkado”): combinación del programa objeto con otros módulos de librería no incorporados durante la fase de traducción, generándose como resultado un programa ejecutable.
- **Prueba** Verificación y depuración del programa mediante conjuntos de datos de prueba para comprobar que el programa es correcto (se ajusta a la especificación dada en la fase de análisis). Si el programa no funciona correctamente habrá que volver a re-diseñar el algoritmo. La ejecución del programa se puede realizar desde el sistema operativo o a través de otros mecanismos.

{% spoiler "Sin embargo" %}

Aun es pronto, es lo que aprenderá a hacer en la asignatura.
Primero veamos con compilar y ejecutar un programa.

![primero aprendamos a comer antes de ser cocineros](ppio.png)



{% endspoiler %}


{% next %}


## Primer programa en la Universidad


Escribiremos un programa que nos muestre un saludo en la pantalla. Hay un dicho en programación que dice que cuando un programador nace no llora dice 

**Hola mundo**


## Edición

Completar el programa para que su contenido sea

```
#include <stdio.h>

/* Programa inicial */
int main(){
	printf(Hola.\n");
	printf("Este es mi primer programa\n");
	printf("escrito en C de la carrera.\n");
	printf("Adios.\n");
	printf("\n\n\nPulse una tecla para finalizar");
	getchar();
	return 0;
}
```

{% spoiler "Save automático"%}

Cuidado aquí se guarda automáticamente pero esto no pasa siempre

{% endspoiler %}



### Compilación. 
	
	Se realiza la “traducción” del programa a lenguaje máquina (código objeto), primer paso para la construcción del ejecutable. Para ello podemos utilizar

```
$ make hola
```

Con esto traducimos el programa

Pero 


```
$ ./hola
Height: 8
       #
      ##
     ###
    ####
   #####
  ######
 #######
########
```

Here's how the program might work if the user inputs `4` when prompted:

```
$ ./mario
Height: 4
   #
  ##
 ###
####
```

Here's how the program might work if the user inputs `2` when prompted:

```
$ ./mario
Height: 2
 #
##
```

And here's how the program might work if the user inputs `1` when prompted:

```
$ ./mario
Height: 1
#
```

If the user, when prompted, doesn't input a positive integer between 1 and 8, inclusive, the program should re-prompt the user until they cooperate:

```
$ ./mario
Height: -1
Height: 0
Height: 42
Height: 50
Height: 4
   #
  ##
 ###
####
```

{% spoiler "Try It" %}

To try out the staff's implementation of this problem, execute

```
./mario
```

within [this sandbox](http://bit.ly/2VAClIi).

{% endspoiler %}

How to begin? Let's approach this problem one step at a time.

{% video https://www.youtube.com/watch?v=NAs4FIWkJ4s %}

{% next %}

## Pseudocode

First, write in `pseudocode.txt` at right some pseudocode that implements this program, even if not (yet!) sure how to write it in code. There's no one right way to write pseudocode, but short English sentences suffice. Recall how we wrote pseudocode for [finding Mike Smith](https://docs.google.com/presentation/d/17wRd8ksO6QkUq906SUgm17AqcI-Jan42jkY-EmufxnE/edit?usp=sharing). Odds are your pseudocode will use (or imply using!) one or more functions, conditions, Boolean expressions, loops, and/or variables.

{% spoiler %}

There's more than one way to do this, so here's just one!

1. Prompt user for height
1. If height is less than 1 or greater than 8 (or not an integer at all), go back one step
1. Iterate from 1 through height:
    1. On iteration *i*, print *i* hashes and then a newline

It's okay to edit your own after seeing this pseudocode here, but don't simply copy/paste ours into your own!

{% endspoiler %}

{% next %}

## Prompting for Input

Whatever your pseudocode, let's first write only the C code that prompts (and re-prompts, as needed) the user for input.

Specifically, modify `mario.c` at right in such a way that it prompts the user for the pyramid's height, storing their input in a variable, re-prompting the user again and again as needed if their input is not a positive integer between 1 and 8, inclusive. Then, simply print the value of that variable, thereby confirming (for yourself) that you've indeed stored the user's input successfully, a la the below.

```
$ ./mario
Height: -1
Height: 0
Height: 42
Height: 50
Height: 4
Stored: 4
```

{% spoiler "Hints" %}

* Recall that you can compile your program with `make`.
* Recall that you can print an `int` with `printf` using `%i`.
* Recall that you can get an integer from the user with `get_int`.
* Recall that `get_int` is declared in `cs50.h`.
* Recall that we prompted the user for a positive integer in class via [`positive.c`](https://sandbox.cs50.io/b56865fd-c861-425f-aad7-4adcf6831139).

{% endspoiler %}

## Building the Opposite

Now that your program is (hopefully!) accepting input as prescribed, it's time for another step.

It turns out it's a bit easier to build a left-aligned pyramid than right-, a la the below.

```
#
##
###
####
#####
######
#######
########
```

So let's build a left-aligned pyramid first and then, once that's working, right-align it instead!

Modify `mario.c` at right such that it no longer simply prints the user's input but instead prints a left-aligned pyramid of that height.

{% spoiler "Hints" %}

* Keep in mind that a hash is just a character like any other, so you can print it with `printf`.
* Just as Scratch has a [Repeat](https://docs.google.com/presentation/d/17wRd8ksO6QkUq906SUgm17AqcI-Jan42jkY-EmufxnE/edit?usp=sharing) block, so does C have a [`for`](https://docs.google.com/presentation/d/191XW0DHWlW6WmAhYuFUYnZKUlDx0N4u4Fp81AeW-uNs/edit?usp=sharing) loop, via which you can iterate some number times. Perhaps on each iteration, *i*, you could print that many hashes?
* You can actually "nest" loops, iterating with one variable (e.g., `i`) in the "outer" loop and another (e.g., `j`) in the "inner" loop. For instance, here's how you might print a square of height and width `n`, below. Of course, it's not a square that you want to print!

    ```
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            printf("#");
        }
        printf("\n");
    }
    ```

{% endspoiler %}

{% next %}

## Right-Aligning with Dots

Let's now right-align that pyramid by pushing its hashes to the right by prefixing them with dots (i.e., periods), a la the below.

```
.......#
......##
.....###
....####
...#####
..######
.#######
########
```

Modify `mario.c` in such a way that it does exactly that!

{% spoiler "Hint" %}

Notice how the number of dots needed on each line is the "opposite" of the number of that line's hashes. For a pyramid of height 8, like the above, the first line has but 1 hash and thus 7 dots. The bottom line, meanwhile, has 8 hashes and thus 0 dots. Via what formula (or arithmetic, really) could you print that many dots?

{% endspoiler %}

### How to Test Your Code

Does your code work as prescribed when you input

* `-1` (or other negative numbers)?
* `0`?
* `1` through `8`?
* `9` or other positive numbers?
* letters or words?
* no input at all, when you only hit Enter?

{% next %}

## Removing the Dots

All that remains now is a finishing flourish! Modify `mario.c` in such a way that it prints spaces instead of those dots!

### How to Test Your Code

Execute the below to evaluate the correctness of your code using `check50`. But be sure to compile and test it yourself as well!

```
check50 cs50/problems/2019/fall/mario/less
```

Execute the below to evaluate the style of your code using `style50`.

```
style50 mario.c
```

{% spoiler "Hint" %}

A space is just a press of your space bar, just as a period is just a press of its key! Just remember that `printf` requires that you surround both with double quotes!

{% endspoiler %}

{% next %}

## How to Submit

Execute the below, logging in with your GitHub username and password when prompted. For security, you'll see asterisks (`*`) instead of the actual characters in your password.

```
submit50 cs50/problems/2019/fall/mario/less
```

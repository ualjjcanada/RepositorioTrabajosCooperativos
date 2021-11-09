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


{% next %}

### Compilación 
	
Se realiza la “traducción” del programa a lenguaje máquina (código objeto), primer paso para la construcción del ejecutable. Para ello podemos utilizar
una orden desde la terminal que hace a la vez la **compilación** y el **montaje**, la orden *make*, seguido por el nombre del archivo que queremos compilar

```
$ make hola
```

Con esto traducimos el programa,  y si todo va bien obtendríamos en la terminal un mensaje como este
```
clang -fsanitize=signed-integer-overflow -fsanitize=undefined -ggdb3 -O0 -std=c11 -Wall -Werror -Wextra -Wno-sign-compare -Wno-unused-parameter -Wno-unused-variable -Wshadow    hola.c  -lcrypt -lcs50 -lm -o hola
$
```

{% spoiler "Sin embargo" %}


```
clang -fsanitize=signed-integer-overflow -fsanitize=undefined -ggdb3 -O0 -std=c11 -Wall -Werror -Wextra -Wno-sign-compare -Wno-unused-parameter -Wno-unused-variable -Wshadow    hola.c  -lcrypt -lcs50 -lm -o hola
hola.c:6:14: error: expected identifier
        printf(Hola.\n");
                    ^
hola.c:6:9: error: use of undeclared identifier 'Hola'
        printf(Hola.\n");
               ^
hola.c:6:16: error: missing terminating '"' character [-Werror,-Winvalid-pp-token]
        printf(Hola.\n");
                      ^
hola.c:13:2: error: expected '}'
}
 ^
hola.c:5:11: note: to match this '{'
int main(){
          ^
4 errors generated.
<builtin>: recipe for target 'hola' failed
make: *** [hola] Error 
	
```

Nos indica que hay un error. Aparecen los errores detectados, con indicación del nº de línea en que se producen y un mensaje de error asociado, apareciendo destacada en el editor la línea que contiene el primer error detectado.


Los errores pueden ser graves (“Errors”) o leves (“Warnings”: avisos), según que el compilador no pueda encontrar ninguna forma de continuar o haya alguna (aunque dudosa). Si marcamos sobre uno de ellos (en nuestro caso el primero), se activará la ventana de edición y el cursor se colocará en el punto en el que el compilador ha encontrado el correspondiente conflicto.



{% endspoiler %}


{% next %}
	

En nuestro caso, se trata de unas comillas (delimitadoras de una cadena de caracteres) que faltan. Rectificamos el error, modificando la sexta línea del programa de la forma:

```
printf("Hola.\n");
```

Si volvemos a compilar, no nos dará ningún error.


{% next %}


## Ejecución

Finalmente podemos ejecutar el programa, para lo que se utiliza la orde **./**

```
$ ./hola

Este es mi primer programa
escrito en C de la carrera.
Adios.



Pulse una tecla para finalizar
```





## How to Submit

Execute the below, logging in with your GitHub username and password when prompted. For security, you'll see asterisks (`*`) instead of the actual characters in your password.

```
submit50 cs50/problems/2019/fall/mario/less
```

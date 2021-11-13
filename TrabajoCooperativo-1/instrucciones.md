# Entornos de programación integrados

### Objetivos
-	Manejar un entorno integrado de desarrollo de programas en lenguaje C y usarlo para desarrollar programas.
-	Ejecutar los programas desarrollados bien desde el sistema operativo o bien desde el soporte de ejecución del entorno integrado.
-	Conocer las principales prestaciones del editor integrado.
-	Identificar algunos elementos sintácticos del lenguaje de programación C y corregir errores en la fase de compilación.
-	Presentar adecuadamente los resultados de salida de un programa mediante el formateo de salida de datos numéricos y textuales.

### Competencias a desarrollar

[X]	RD1: Poseer y comprender conocimientos
[X]	RD2: Aplicación de conocimientos
[X]	UAL1: Conocimientos básicos de la profesión
[X]	UAL3: Capacidad para resolver problemas
[X]	UAL6: Trabajo en equipo
[X]	FB3: Conocimientos básicos sobre el uso y programación de los ordenadores, sistemas operativos, bases de datos y programas informáticos con aplicación en la ingeniería.

### Tareas a realizar 	

- Inicializar los entornos de trabajo
- Revisar y probar los ejemplos includos
- Realizar los ejercicios 1 al 9 de esta ficha y dejar los resultados en el repositorio creado. 

### Edición, compilación y ejecución de un programa 

Abrir el archivo de nombre SALUDO.c

Completarlo para que su contenido sea:

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

Compilar el programa

### Ejercicio 1. Modificación del archivo de Saludo

 Cargar en el editor el programa SALUDO.C creado en el ejemplo de sesión de trabajo. Modificar el mensaje de salida, de forma que ahora escriba:

    Aqui estoy de nuevo.
    Este es mi segundo programa de la asignatura.
    Me he limitado a cambiar el texto de una orden de escritura.

- Grabar dicha modificación en un archivo con el nombre ejercicio1.c, 
- Compilar dicho archivo creando un archivo ejecutable en disco. 
- Descargar el archivo ejercicio1.exe si trabaja con el IDE online.
- Ejecutar desde el sistema operativo dicho programa.

### Ejercicio 2. Saludo Formal

Copie lo siguiente en el editor del IDE y guárdelo en el disco de prácticas con el nombre ejercicio2.c; tras comprobar que es ejecutable, realice los pasos que se indican al final del ejercicio


     /* Ejercicio 2 del Trabajo cooperativo 1 */
    #include <stdio.h>
    int main(){
 	    char nombre[30];
        printf("Por favor, introduzca su nombre: ");
	    scanf(" %[^\n]s",nombre);
	    printf("\n\nSaludos D. %s", nombre);
	    printf("\nBienvenido al fantastico mundo de la programacion");
	    printf("\n\nPulse una tecla para finalizar");
	    getchar();
	    return 0;
    }

-	Seleccione como bloque las líneas 5 y 6 del programa.
-	Copie el bloque inmediatamente debajo.
-	Cambie el identificador  nombre, por apellidos en la copia.
-	Seleccione como bloque la 4 línea del programa.
-	Cópielo inmediatamente debajo (queda como línea 5).
-	Cambie el identificador nombre, por apellidos en la nueva línea.
-	Elimine la línea 10 utilizando una única orden. 
-	Inserte una nueva línea en la posición que tenía la que acaba de borrar:

		printf("\n\nSaludos D. %s %s", nombre, apellidos);


Compruebe que la nueva versión del programa funciona correctamente y grábela.

### Ejercicio 3. Calculadora básica

Entrar en el editor del IDE y copiar las siguientes líneas:


```

/* Ejercicio 3  */

#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

int main(){
	int a, b;
	char operacion, c;

	do{ 
		printf("Vamos a realizar una operacion aritmetica simple:\n\n");
		printf("Introduzca el primer valor con que vamos a operar: ");
		scanf(" %d",&a);
		printf("Introduzca el segundo valor con que vamos a operar: ")
		scanf(" %d",&b);
		printf("\n");
		printf("Introduzca + para sumar, - para restar o * para multiplicar: ");
		scanf(" %c",&operacion);
		switch(operacion){
		case '+': printf("El resultado es: %d\n", a+b);
			      break;
		case '-': printf("El resultado es: %d\n", a-b);
                  break;
		case '*': printf("El resultado es: %d\n", a*b);
                  break;
		default:  printf("Operacion incorrecta\n");
		          break;
		}
		printf("\nDesea efectuar una nueva operacion (S/N)? ");
				scanf(" %c",&c);   
	}while ((c!='N') && (c!='n'));
	return 0;
}
```

Compile el programa anterior, que se habrá almacenado previamente como ejercicio3. Aparecerá un error al compilarlo: 
   
 
 En este caso, se trata de que en la línea 18, una antes del punto en que encuentra el error, falta un punto y coma. Corrija el error, colocando el punto y coma al final de la instrucción: 
```
	printf("Introduzca el segundo valor con que vamos a operar: ");
```




Vuelva a compilarlo y una vez que esté sin errores, ejecútelo. Pruebe con los valores que se le indican a continuación la corrección del programa y anote en la siguiente tabla los valores de prueba utilizados y el resultado obtenido. 


Valor 1	Valor 2	Código de operación	Resultado
			Dev cpp	Code::Blocks
10	10	+		
10	10	-		
10	10	*		
-50	50	*		
-50	0	*		
0	0	-		
0	0	*		
20000	20000	+		
50000	50000	*		

¿Ha observado algún resultado anómalo? ¿Cuál puede ser la causa del mismo? 


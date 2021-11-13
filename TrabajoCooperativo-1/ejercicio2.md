## Saludo Formal

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


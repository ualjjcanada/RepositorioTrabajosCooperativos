## Entrar en el editor del IDE y copiar las siguientes líneas:

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



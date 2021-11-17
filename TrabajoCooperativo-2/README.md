# Sintaxis de C. Programación Estructurada: instrucción de control secuencial

### Objetivos
- Conocer la sintaxis básica del lenguaje de programación C: tipos de datos, constantes, variables, operadores, instrucciones de asignación y de control. Identificar algunas características genuinas de este lenguaje de programación.
- Conocer las principales funciones de la biblioteca estándar de C para la entrada/salida de información por el terminal así como para cálculos matemáticos básicos.
- Implementar algoritmos sencillos que hagan uso de las construcciones estructuradas de control (programación estructurada): secuencia, selección y repetición.
- Identificar y corregir errores sintácticos del lenguaje de programación C que surgen durante la codificación.
- Utilizar adecuadamente la función scanf para la entrada de datos al programa a través del teclado.
- Presentar adecuadamente en pantalla los resultados de salida de un programa mediante la función printf. 
- Probar con datos operacionales la correctitud de los programas desarrollados e identificar y corregir los errores lógicos que surjan.


### Competencias a desarrollar

- [X]	RD1: Poseer y comprender conocimientos
- [X]	RD2: Aplicación de conocimientos
- [X]	UAL1: Conocimientos básicos de la profesión
- [X]	UAL3: Capacidad para resolver problemas
- [X]	UAL6: Trabajo en equipo
- [X]	FB3: Conocimientos básicos sobre el uso y programación de los ordenadores, sistemas operativos, bases de datos y programas informáticos con aplicación en la ingeniería.

### Tareas a realizar

Desarrollar los programas correspondientes a los 6 ejercicios propuestos en esta ficha de trabajo 

### Plan de trabajo

**Lectura** individual de la ficha de trabajo por parte del alumno. 
Estudio, codificación y prueba (individual o por parejas) de los ejemplos presentados en teoría de la instrucción de control secuencial (el código fuente en C se encuentra en esta ficha de trabajo).

**Diseño e implementación en C**: Realización individual (o por parejas) de los 6 ejercicios propuestos previa distribución del trabajo entre los miembros del equipo de acuerdo con el siguiente esquema (grupos de 3 ó 4 miembros) sobre los repositorios compartidos:

- A - ejercicios 1,4                     A,B - ejercicios 1,3,5
- B - ejercicios 2,5                     C,D - ejercicios 2,4,6
- C - ejercicios 3,6

    Nota: para la implementación en lenguaje C de los programas correspondientes a los algoritmos diseñados, puede utilizar las plantillas genéricas de programas que encontrará en esta ficha de trabajo (o bien puede utilizar cualquiera de los programas de ejemplo), con el fin de optimizar la codificación en C de los archivos fuente.


**Reunión del equipo base**: cada miembro (o pareja de miembros) explica su trabajo realizado a los otros miembros del equipo y recibe la explicación del trabajo de los otros miembros. Objetivo: cada integrante del equipo debe saber resolver cualquiera de los ejercicios planteados.

**Pruebas**: los programas desarrollados serán validados de forma cruzada por los miembros del equipo utilizando como mínimo los datos de prueba suministrados, de acuerdo con el siguiente esquema:

- A - ejercicios 3,5                     A,B - ejercicios 2,4,6
- B - ejercicios 1,6                     C,D - ejercicios 1,3,5
- C - ejercicios 2,4

    Nota: en caso de detectar errores en esta fase de pruebas, estos deberán ser corregidos por los miembros del equipo que las realicen, modificando el código fuente y/o el algoritmo correspondiente. 

**Reunión del equipo base**: Configuración definitiva del repositorio. Cada miembro del equipo repoducirá en su repositorio individual el trabajo realizado por el resto de los miembros del equipo.


### Ejemplos de programas con construcción de control secuencial 

A continuación se incluyen tres problemas tipo, que se recomienda que los alumnos prueben antes de empezar con sus propias soluciones a los ejercicios.

---
#### Construir un programa que calcule la masa en kilogramos de una bola de hierro dado su diámetro en centímetros.

&ensp;&ensp;&ensp;  [  CalculoMasaBolaHierro.psc](https://github.com/MaterialesProgramacion/ProblemasProgramacion/blob/master/Secuencial/CalcularMasaBolaHierro.psc)
&ensp;&ensp;&ensp;  [ CalculoMasaBolaHierro.c](https://github.com/MaterialesProgramacion/ProblemasProgramacion/blob/master/Secuencial/CalcularMasaBolaHierro.c)


----
#### Construir un programa que lea por teclado los componentes espaciales de dos vectores y que calcule e imprima en pantalla la suma de los dos vectores, su producto escalar y  vectorial.

&ensp;&ensp;&ensp;  [calculoVectorial.psc](https://github.com/MaterialesProgramacion/ProblemasProgramacion/blob/master/Secuencial/calculoVectorial.psc)
&ensp;&ensp;&ensp;  [  calculoVectorial.c](https://github.com/MaterialesProgramacion/ProblemasProgramacion/blob/master/Secuencial/calculoVectorial.c)

----
#### Una empresa de envasado automático de aceite dispone de diversos tipos de envases con capacidades de 50, 20, 10, 5, 2 y 1 litro, respectivamente. Construir un programa que dado por teclado un número entero de litros a envasar, determine el menor número de envases completos necesarios e indique el número de envases de cada tipo, presentándolos en pantalla

&ensp;&ensp;&ensp;  [ calcularNumeroEnvases.psc](https://github.com/MaterialesProgramacion/ProblemasProgramacion/blob/master/Secuencial/calcularNumeroEnvases.psc)
&ensp;&ensp;&ensp;  [ calcularNumeroEnvases.c](https://github.com/MaterialesProgramacion/ProblemasProgramacion/blob/master/Secuencial/calcularNumeroEnvases.c)

-----

### Ejercicio 1. 



### Ejercicio 2. 



### Ejercicio 3. 



### Ejercicio 4. 



### Ejercicio 5. 



### Ejercicio 6. 



### Ejercicios adicionales

#### 1

¿Cómo se representan en lenguaje de programación C los datos lógicos? 


#### 2

Listar los operadores específicos de lenguaje de programación C que no hemos presentado en la notación de diseño e indicar su significado:
Operador exclusivo de C	Significado
	
	
	
	

#### 3

Calcular los rangos de los tipos de datos enteros del entorno de trabajo Dev-c++/ Code::blocks y anotarlos en la siguiente tabla:

Tipo de datos	Identificador de tipo	Rango	Tamaño
Enteros	short int
signed short int		
	int
signed int		
	long int
signed long int		
	unsigned int		
	unsigned long int		
Nota: utilizar el operador sizeof para calcular el tamaño en bytes de los diferentes tipos.

¿Qué diferencias encuentran con otros entornos de trabajo con tamaños de enteros de 2 bytes (int y short) y 4 bytes para enteros largos (long int)?

#### 4

 Realizar nuevas pruebas del programa correspondiente al ejercicio 3 con los siguientes datos de entrada y anotar los resultados:
Datos de Entrada	Resultados
a = -3
b = 5
h = 10	m =
a = -3
b = 5
h = b	m =
¿Han observado algún resultado erróneo? ¿Es posible resolverlo utilizando únicamente la instrucción de control secuencial? 

#### 5 
¿Qué diferencias encuentran cuando quieren leer por teclado y escribir en pantalla datos de tipo real en simple y real en doble precisión utilizando las funciones printf y scanf de la biblioteca stdio.h?


#### 6 
¿Qué diferencias encuentran entre las funciones ceil y floor de la biblioteca math.h entre sí y  con la función interna trunc presentada en la notación de diseño?


#### 7
Indicar como se puede calcular en lenguaje de programación C el cociente (parte entera) y el resto (parte decimal) de la división entre dos números reales. 

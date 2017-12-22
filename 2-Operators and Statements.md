## Promoción Numérica en Java

La promoción numérica no es más que la acción que realiza Java de cambiar el tipo de dato a un valor cuando se utilizan los operadores aritméticos (suma +, resta -, multiplicación *, división /, modulo %, operadores unitarios como ++ o --, otros más). Para realizar esta promoción numérica (cambio del tipo de dato) Java cuenta con cuatro reglas que debemos de tener en la punta de la lengua:

    1. Si dos valores tienen diferente tipo de dato, Java automáticamente promoverá uno de los valores al más grande de los dos tipos de datos.

    2. Si uno de los valores es integral y el otro es un punto flotante, Java automáticamente promoverá el valor integral a un tipo de dato con valor de punto flotante.

    3. Los tipos de datos pequeños (byte, short, y char), se promueven primero a int siempre que sean utilizados con un operador aritmético binario en Java, incluso si ninguno de los operadores es un valor int.

    4. Después de que todas las promociones hayan ocurrido y los operadores tengan el mismo tipo de dato, los valores resultantes tendrán el mismo tipo de dato como sus operadores promovidos.


Puede que muchos desarrolladores hayan tenido problemas corriendo su código por la falta de conocimiento de estás reglas, o de la existencia de la promoción numérica y se hayan dado cuenta de que ocurre a prueba y error, pero sin saber exactamente la razón. Ahora exploremos cada una de las reglas con ejemplos prácticos.

```java
    int valorInt = 10;
    long valorLong = 5;

    long resultado = valorInt * valorLong;
```

En este fragmente de código tenemos dos variables, una de tipo entero llamada valorInt y otra de tipo long llamada valorLong, tenemos una tercera variable de tipo long llamada resultado donde se almacenará el resultado de la operación aritmética multiplicación entre ambos valores. ¿a qué se debe que la variable resultado sea de tipo long? ¿será que podemos definir resultado como un int? al final de cuentas el resultado de la operación será 50 y es un valor que cabe dentro de un int. Si nos remitimos a la primera regla de la promoción numérica obtendremos las respuestas a interrogantes como estas, "Java siempre promoverá los valores al tipo de dato más grande", en este caso long es un tipo de dato más grande que int. Al momento de ejecutar la operación valorInt es promovido a ser un tipo de dato long, pero también se aplica la regla número cuatro "los valores resultantes tendrán el mismo tipo de dato como sus operadores promovidos" por tanto el valor resultante será de tipo long.

```java
    long valorLong = 3;
    double valorDouble = 4.2;

    double resultado = valorLong * valorDouble;
```

En este fragmento de código tenemos dos variables, valorLong de tipo long, y valorDouble de tipo double, luego realizamos una operación aritmética de tipo multiplicación. En el momento de la multiplicación se aplica la regla numero dos "Java automáticamente promoverá el valor integral a un tipo de dato con valor de punto flotante" valorLong es promovido a double, luego es aplicada la regla número cuatro "los valores resultantes tendrán el mismo tipo de dato como sus operadores promovidos" por tanto la variable resultado donde es almacenado el mismo es de tipo double.

```java
    short valor1 = 4;
    short valor2 = 5;
      
    int resultado = valor1 + valor2;
```
En este fragmento de código tenemos dos variables de tipo short, valor1 y valor2, posteriormente realizamos la operación aritmética de suma y almacenamos en resultado en una variable de tipo int. Para este caso se aplica la regla número tres y cuatro, "Tipos de datos pequeños (byte, short, char) siempre son promovidos a int" esto significa que tanto valor1 como valor2 son del tipo de dato int al momento de la operación, pero también se aplica la regla numero cuatro "os valores resultantes tendrán el mismo tipo de datos como sus operadores promovidos" por tanto el valor resultante aunque sea nueve y esté dentro del valor soportado por un short, es promovido a ser un tipo de dato int.

Podemos concluir indicando que la promoción numérica es una acción que Java ejecuta cuando una operación aritmética se realiza, para poder tener compatibilidad en los tipos de datos.
(Fuente: https://community.oracle.com/blogs/aKnowledgeJourney/2016/11/24/javase8-oca-promoci%C3%B3n-num%C3%A9rica-en-java)
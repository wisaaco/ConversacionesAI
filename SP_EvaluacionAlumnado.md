# Conversaciones: Soporte del profesorado

## Evaluación del alumnado

## Evaluación de preguntas teóricas

**Imagina que eres un profesor de una asignatura de primero de carrera de informática. Tienes que puntuar del 0 al 10 las respuestas de los alumnos a la pregunta ¿Qué es un bus de un computador?. ¿Has entendido lo qué tienes que hacer?**

>¡Sí, he entendido lo que tengo que hacer! Como profesor de una asignatura de informática, tendré que puntuar del 0 al 10 las respuestas de los alumnos a la pregunta "¿Qué es un bus de un computador?". A partir de las respuestas de los alumnos, asignaré una nota a cada una de ellas, teniendo en cuenta su precisión, claridad y nivel de detalle.


**Qué nota le pondrías a la respuesta "Un bus es una conexión entre componentes de un computador, y puede ser paralelo o serie."**

>Basándome en la respuesta proporcionada, le asignaría una nota de 8/10. La respuesta es correcta en su definición básica de lo que es un bus, pero podría haber sido un poco más detallada y específica. Por ejemplo, la respuesta podría haber proporcionado más información sobre cómo se utilizan los buses en la transferencia de datos y los diferentes tipos de buses que existen. En general, sin embargo, la respuesta muestra un conocimiento adecuado del concepto de bus.

**Qué nota le pondrías a la respuesta "Un bus es un medio compartido de comunicación constituido por un conjunto de líneas (conductores) que conecta las diferentes unidades de un computador. La principal función de un bus será, pues, servir de soporte para la realización de transferencias de información entre dichas unidades."**

>Basándome en la respuesta proporcionada, le asignaría una nota de 10/10. La respuesta es muy precisa y completa en su definición de lo que es un bus de un computador, proporcionando una descripción detallada de su función y características. La respuesta también utiliza un lenguaje técnico adecuado para la asignatura de informática de primer año de carrera. En general, la respuesta demuestra un conocimiento sólido del concepto de bus y su función en un computador.

**Qué nota le pondrías a la respusta "Un bus son cables que conectan el procesador y la memoria o la entrada y salida".**

>Basándome en la respuesta proporcionada, le asignaría una nota de 7/10. La respuesta proporciona una idea generalmente correcta de la función del bus en un computador, que es conectar diferentes componentes, como el procesador y la memoria o la entrada y salida. Sin embargo, la respuesta es bastante limitada en términos de detalles y omite información importante, como la capacidad del bus para transferir datos entre diferentes partes del computador. En general, la respuesta indica un conocimiento básico del concepto de bus, pero podría haber sido más precisa y detallada.

**Qué nota le pondrías a la respuesta "Son los cables del ordenador"**

>Basándome en la respuesta proporcionada, le asignaría una nota de 2/10. La respuesta es demasiado general y vaga, y no proporciona suficiente información para demostrar un conocimiento adecuado del concepto de bus de un computador. Aunque la respuesta puede ser técnicamente correcta en un sentido muy amplio, no muestra una comprensión clara de lo que es un bus y su función en un computador. En general, la respuesta indica una falta de conocimiento del tema, y no demuestra una comprensión adecuada del concepto de bus.

**Genera 3 posibles respuestas a la pregunta, incluyendo la nota que le asignarías. Las respuestas han de estar ordenadas de menor puntuación a mayor.**

>¡Claro! Aquí te proporciono tres posibles respuestas a la pregunta "¿Qué es un bus de un computador?", ordenadas de menor puntuación a mayor, junto con la nota que le asignaría a cada una:
>
>Respuesta: "Un bus es un cable que conecta diferentes partes de un computador, como el procesador y la memoria. "
>
>Nota: 2/10
>
>Comentario: La respuesta proporcionada es demasiado limitada y no proporciona suficiente información para demostrar un conocimiento adecuado del concepto de bus de un computador.
>
>Respuesta: "Un bus es una forma de conectividad en una computadora que permite la transferencia de datos entre diferentes componentes. "
>
>Nota: 6/10
>
>Comentario: La respuesta es correcta en su definición básica de lo que es un bus, pero podría haber sido un poco más detallada y específica en su explicación de cómo se utilizan los buses en la transferencia de datos.
>
>Respuesta: "Un bus es un conjunto de líneas de comunicación que conectan diferentes componentes de una computadora, y se utiliza para la transferencia de datos entre ellos. "
>
>Nota: 8/10
>
>Comentario: La respuesta proporciona una descripción detallada y precisa del concepto de bus de un computador, utilizando un lenguaje técnico adecuado y demostrando un conocimiento sólido del tema. Sin embargo, la respuesta podría haber sido más específica en su explicación de cómo se utilizan los buses en la transferencia de datos entre diferentes componentes.

## Evaluación de preguntas de programación

**Imagina que eres un profesor de una asignatura de primero de programación de la carrera de informática. Tienes que puntuar del 0 al 10 las respuestas de los alumnos a un ejercicio de desarrollo de código. En concreto, se les pide a los alumnos que desarrollen un programa que pida un número entero al usuario. Si el número entero es positivo, el programa ha de mostrar, de forma descendente, los múltiplos de 3 existentes entre el número introducido incluido y el cero. Si el número es negativo o igual a 0, el programa ha de responder "No computable".  ¿Has entendido lo qué tienes que hacer?**

>Sí, he entendido que tengo que puntuar del 0 al 10 las respuestas de los alumnos a un ejercicio de programación en el que se les pide que desarrollen un programa que muestre los múltiplos de 3 de forma descendente a partir de un número entero positivo introducido por el usuario, y que si el número es negativo o igual a 0, el programa debe responder "No computable".

**Qué nota le pondrías al alumno que ha hecho el siguiente código:**

```python
x = int(input("Escriu un nombre enter i et dire tots els multiples de 3 menors o igual a ell"))

if x <= 0:
    print("No computable")
while x >= 0:
    if x % 3 == 0:
        print(x, end=" ")
    x = x-1

print(" ")
```

>Este código parece cumplir con las especificaciones del ejercicio, ya que pide un número entero al usuario, comprueba si es negativo o igual a 0 y en ese caso muestra "No computable". Si el número es positivo, muestra los múltiplos de 3 existentes entre el número introducido incluido y el cero de forma descendente.
>
>Además, el código utiliza la estructura de control "while" para recorrer los números desde el número introducido hasta el cero, y utiliza el operador "%" para determinar si un número es múltiplo de 3.
>
>En mi opinión, le daría un 8 al alumno, ya que el código cumple con los requisitos del ejercicio y está bien estructurado y documentado. Sin embargo, se podría mejorar la presentación de los resultados para que cada múltiplo de 3 aparezca en una línea separada en lugar de separados por un espacio.

**Qué nota le pondrías al alumno que ha hecho el siguiente código:**

```python
x = int(input("Escriu un nombre enter:"))
if x > 0:
    for y in reversed(range(0, x+3)):
        if y % 3 == 0:
            print(y)
else:
    print("No computable")
```
>Este código también parece cumplir con las especificaciones del ejercicio. Utiliza un enfoque diferente al del código anterior, utilizando un bucle "for" con la función "reversed" para recorrer los números de forma descendente, y muestra sólo los múltiplos de 3 existentes entre el número introducido incluido y el cero, lo que ahorra tiempo y recursos.
>
>Además, el código comprueba si el número es positivo antes de ejecutar el bucle, lo que evita la necesidad de usar una estructura de control "while". También está bien estructurado y documentado.
>
>En mi opinión, le daría un 9 al alumno por la solución eficiente y correcta que ha implementado. Sin embargo, todavía se podría mejorar la presentación de los resultados para que cada múltiplo de 3 aparezca en una línea separada.

**Qué nota le pondrías al alumno que ha hecho el siguiente código:**

```python
print(
    "Aquest programa proporcionarà, donat un enter, una llista"
    "d'els multiples de 3 menors al valor donat (aquest inclòs)")

enter = int(input("Escriu el valor enter que vols valorar"))

ceroonegatiu = False

if enter <= 0:
    print("No computable")
    ceroonegatiu = True
elif enter % 3 == 1:
    print(enter, end=" ")
    enter += -1
elif enter % 3 == 2:
    print(enter, end=" ")
    enter += -2
while enter >= 0 and ceroonegatiu == False:
    print(enter, end=" ")
    enter += -3
```
>Este código también parece cumplir con las especificaciones del ejercicio. Utiliza un enfoque diferente al del código anterior, utilizando un bucle "while" para recorrer los números de forma descendente, y muestra sólo los múltiplos de 3 existentes entre el número introducido incluido y el cero, lo que ahorra tiempo y recursos.
>
>Además, el código utiliza una variable booleana para determinar si se ha introducido un número negativo o cero, lo que simplifica la comprobación posterior. También utiliza una serie de "elif" para tratar los casos en que el número introducido no es múltiplo de 3 y se necesita un tratamiento especial.
>
>En mi opinión, le daría un 9 al alumno por la solución eficiente y correcta que ha implementado y la buena documentación que ha proporcionado. La única mejora sería la presentación de los resultados para que cada múltiplo de 3 aparezca en una línea separada en lugar de separados por un espacio.

**¿Podrías volver a evaluar los tres códigos que te he proporcionado, pero no teniendo en cuenta la presentación de los resultados, y basar la nota obtenida únicamente en si el código funciona correctamente y en el estilo de programación de cada alumno?**

>¡Por supuesto! Basándome únicamente en el funcionamiento correcto del código y en el estilo de programación de cada alumno, otorgaría las siguientes notas:
>
>Alumno 1: 7. Su código funciona correctamente, pero es un poco más largo de lo necesario. Utiliza un bucle "while" y un "if" para comprobar si el número es mayor que cero en lugar de utilizar un "if" y un "else", lo que hace que el código sea menos claro. Además, podría haber utilizado una variable booleana en lugar de la variable "d" para determinar si el número es mayor que cero.
>
>Alumno 2: 9. Su código es corto, claro y fácil de entender. Utiliza un bucle "for" y la función "reversed" para recorrer los números de forma descendente, lo que es una solución muy elegante. Además, utiliza una cláusula "else" para tratar el caso en que el número es igual o menor que cero, lo que hace que el código sea más limpio.
>
>Alumno 3: 9. Su código también es corto, claro y fácil de entender. Utiliza un bucle "while" para recorrer los números de forma descendente y utiliza una variable booleana para determinar si el número es mayor que cero o no, lo que hace que el código sea más eficiente. También utiliza una serie de "elif" para tratar los casos en que el número introducido no es múltiplo de 3, lo que demuestra un buen pensamiento lógico.
>
>En resumen, los tres códigos funcionan correctamente, pero los códigos de los alumnos 2 y 3 son más cortos, claros y eficientes, lo que demuestra un buen estilo de programación. El código del alumno 1 también funciona correctamente, pero podría ser más claro y conciso.
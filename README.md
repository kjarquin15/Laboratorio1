Laboratorio 1 – Modularización en Java

Descripción del programa

Este programa en Java funciona como un pequeño sistema para gestionar estudiantes. Permite agregar estudiantes con su calificación, mostrar la lista de estudiantes registrados, calcular el promedio de las calificaciones y mostrar cuál estudiante tiene la calificación más alta.

El objetivo del laboratorio fue analizar el código original proporcionado por el profesor, mejorarlo utilizando modularización y agregar validaciones para evitar errores en la entrada de datos.

Parte 1 – Análisis del Programa Original

Identificación de tareas repetitivas

En el código original se identificaron varias tareas que pueden convertirse en métodos para mejorar la organización del programa.

Las principales tareas son:

- Agregar estudiante
- Mostrar la lista de estudiantes
- Calcular el promedio de calificaciones
- Mostrar el estudiante con la calificación más alta
- Cada una de estas tareas realiza una función específica dentro del programa.

Separarlas en métodos mejora el programa porque el código queda más ordenado, es más fácil de leer y facilita hacer cambios en el futuro. También permite reutilizar partes del código si se necesitan nuevamente.

En el programa original todo estaba dentro del método main, lo que hacía que el programa fuera más difícil de entender cuando el código empieza a crecer.

Variables Locales vs Globales

En el programa existen dos listas que almacenan la información de los estudiantes:

- estudiantes
- calificaciones

Estas variables se declararon como globales utilizando static, porque se necesitan en varios métodos del programa.

Si estas variables fueran locales, solo funcionarían dentro de un método y no podrían utilizarse en otras partes del programa.

Las variables que deberían ser locales son las que solo se utilizan dentro de una función específica, por ejemplo:

- nombre
- calificacion
- suma
- promedio
- maxCalificacion

Estas variables solo se usan para cálculos o procesos temporales, por lo que no es necesario que estén disponibles en todo el programa.

Las variables globales permiten compartir información entre métodos, pero si se usan demasiado pueden causar errores porque cualquier método podría modificar su valor.

Parte 2 – Modularización del Programa

Para mejorar el programa se decidió dividir el código en varios métodos, donde cada método tiene una sola responsabilidad.

Los métodos que se implementaron fueron:

- agregarEstudiante()
- mostrarEstudiantes()
- calcularPromedio()
- mostrarMejorEstudiante()

Cada uno de estos métodos realiza una tarea específica dentro del programa y todos son llamados desde el método main.

Esto ayuda a que el programa esté más organizado, que el código sea más fácil de leer y que cada parte del programa tenga una función clara.

También facilita realizar modificaciones en el futuro sin tener que cambiar todo el programa.

Parte 3 – Validaciones y Manejo de Excepciones

En el programa original podían ocurrir errores si el usuario ingresaba datos incorrectos.

Por ejemplo:

* Si el usuario ingresaba texto cuando el programa esperaba un número.
* Si se ingresaba una calificación incorrecta.

Para evitar que el programa falle se agregaron validaciones y manejo de excepciones utilizando try-catch.

Esto permite capturar errores cuando el usuario ingresa datos incorrectos y mostrar un mensaje en lugar de que el programa se cierre.

También se agregó una validación para verificar que la calificación esté dentro de un rango válido antes de guardarla.

Estas validaciones son importantes porque hacen que el programa sea más seguro y evitan que el usuario provoque errores en la ejecución.

Parte 4 – Preguntas de Reflexión

¿Qué ventajas tiene dividir el código en métodos?

Dividir el código en métodos ayuda a que el programa esté mejor organizado, ya que cada método tiene una función específica. También permite reutilizar partes del código si se necesitan en otros lugares.

Además facilita el mantenimiento del programa porque si se necesita cambiar algo, solo se modifica el método correspondiente.

¿Por qué no es recomendable usar muchas variables globales?

No es recomendable usar muchas variables globales porque cualquier parte del programa puede modificar su valor, lo que puede provocar errores inesperados.

También hace que el programa sea más difícil de depurar y entender.

Por eso es mejor utilizar variables locales cuando solo se necesitan dentro de un método.

¿Cómo mejora la modularización la legibilidad del código?

La modularización mejora la legibilidad porque divide el programa en partes más pequeñas y fáciles de entender.

Cada método representa una tarea específica, lo que permite seguir la lógica del programa de una manera más clara.

Esto también facilita que otros programadores puedan entender el código con mayor facilidad.

Conclusión

La modularización permite organizar mejor el código y dividir las responsabilidades dentro del programa.

Separar las funciones en métodos hace que el código sea más fácil de leer, mantener y mejorar. Además, agregar validaciones ayuda a evitar errores cuando el usuario ingresa datos incorrectos.

Autor

Karen Lizzeth Jarquín Salguero
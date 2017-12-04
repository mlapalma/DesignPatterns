##Patrón de Diseño Mediator
===========================

Nombre: Mediator
Clasificación: De Comportamiento

###Introducción:

Supongamos que tenemos un sitio web compuesto de cuatro páginas, de esta forma, el usuario podrá navegar por todas las paginas y cada una de ellas tendrá que tener referencias a las otras tres. No es demasiado problema si hablamos de simplemente cuatro páginas, pero que pasaría si se tratara de decenas de ellas?

Implicaría tener muchísimo código duplicado en cada una de las páginas, entre otras cosas.

Se puede colocar un objeto mediator en el medio, con el objetivo de que referencie a todas las páginas del sitio, y todas las páginas deberán referenciar a él únicamente.

De esta forma, pero aplicado a objetos en lugar de sitios web es como trabaja el objeto mediator.


###Definición teórica:
Define un objeto que encapsula cómo una serie de objetos interactúan entre sí. Mediator promueve el desacoplamiento evitando que los objetos sean referenciados explícitamente entre sí y permite al desarrollador variar independiemente la interacción.


###Aplicabilidad:
Use el patron de diseño Mediator cuando:

    - Un conjunto de objetos se comunican entre sí en una forma bien definida pero compleja. Las interdependencias resultantes son no estructuradas y difíciles de entender.
    - Reutilizar un objeto es dificil por que referencia y se comunica con muchos otros objetos.
    - Se posee un comportamiento distribuído entre muchas clases que se desea personalizar sin usar muchas subclases.

###Ejemplos:
 - Todos los ejemplos de schedulexxx() de java.util.Timer http://docs.oracle.com/javase/8/docs/api/java/util/Timer.html
 - java.util.concurrent.Executor#execute() http://docs.oracle.com/javase/8/docs/api/java/util/concurrent/Executor.html#execute-java.lang.Runnable-
 - Métodos submit() e invokeXXX() de java.util.concurrent.ExecutorService http://docs.oracle.com/javase/8/docs/api/java/util/concurrent/ExecutorService.html
 - Métodos scheduleXXX() de java.util.concurrent.ScheduledExecutorService http://docs.oracle.com/javase/8/docs/api/java/util/concurrent/ScheduledExecutorService.html
 - java.lang.reflect.Method#invoke()http://docs.oracle.com/javase/8/docs/api/java/lang/reflect/Method.html#invoke-java.lang.Object-java.lang.Object...-




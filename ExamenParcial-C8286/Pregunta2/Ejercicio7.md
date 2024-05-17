Mejores al código para serlo más robusto (5 puntos)
¿Cómo podrías asegurarte de que el servidor se cierra correctamente al recibir una señal de
interrupción (por ejemplo, Ctrl+C)? Implementa un manejador de señales para limpiar
recursos y cerrar el servidor de manera ordenada.
- Es bueno utilizar with esto garantiza que el proceso continuo correctamente. Eso lo mas recomendable.
¿Cómo podrías utilizar funciones parciales para mejorar la legibilidad y la gestión de
parámetros en el código? Utiliza functools.partial para simplificar la creación de funciones
con múltiples parámetros predefinidos.
- 

:¿Cómo puedes inicializar adecuadamente los trabajadores y gestionar un pool de procesos,
asegurando que se ignoren ciertas señales en los trabajadores? Utiliza mp.Pool con un
inicializador que configure la gestión de señales apropiadamente en los procesos hijos.
- 
¿Cómo aseguras que los trabajadores terminan correctamente cuando se cierra el servidor?
Envia un trabajo especial (sentinela) a los trabajadores para indicarles que deben finalizar.
No te olvides de que los hilos trabajadores se unen adecuadamente antes de que el
programa principal termine.
-Podemos agregar agregar al final close(), esto garantiza de termine correctamente.
-En cuanto a hilos para empezar es necesario poner start() y joint(). Estas funciones garantizan de puedas empezar y terminar correctamente.

¿Cómo manejas adecuadamente las excepciones y errores para asegurarte de que el
servidor no falle de manera inesperada? Captura y maneja las excepciones en las funciones
asincrónicas y en los hilos trabajadores. Utiliza bloques try-except para manejar errores en la
comunicación entre el cliente y el servidor.
- 
¿Cómo puedes mejorar la estructura general y la legibilidad del código para hacerlo más
mantenible y robusto?. Refactoriza el código para separar claramente las responsabilidades
(por ejemplo, manejar trabajos, manejar resultados, aceptar solicitudes). Utiliza nombres de
variables y funciones descriptivos para mejorar la claridad del código
- 

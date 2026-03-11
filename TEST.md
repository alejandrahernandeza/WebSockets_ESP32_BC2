# Cuestionario de Evaluación: Comunicación por Sockets 📝

**Nombre del Estudiante:** Alejandra Hernández
**Fecha:** 11/3/2026

*Instrucciones: Responde a las siguientes preguntas basándote en la teoría de redes y en el análisis del código de nuestro proyecto. Sube este archivo con tus respuestas a tu repositorio como evidencia de trabajo.*

1. **¿Qué es una Dirección IP y para qué sirve en nuestro proyecto?**
   > *Tu respuesta aquí*
   Una dirección IP es el identificador numérico único que permite que los dispositivos se encuentren y se comuniquen en una red. En nuestro proyecto, sirve para conectar el software con el servidor o la base de datos de forma precisa.

2. **¿Qué es un Puerto de red? (Menciona qué puerto estamos usando en el código de la ESP32).**
   > *Tu respuesta aquí*
   > El puerdo de red es como un canal de conexión que permite que los datos lleguen a un proceso o servicio específico dentro de un dispositivo el puerto que se está utilizando es el puerto 80

3. **Define con tus propias palabras qué es un Servidor en informática.**
   > *Tu respuesta aquí*
   > Un servidor es una computadora o programa cuya única misión es estar siempre disponible para gestionar recursos y responder a las peticiones de otros dispositivos (clientes). En tu proyecto, es el "cerebro" que recibe los datos de la ESP32 y los procesa o almacena.

4. **¿Cuál es la diferencia entre un "Servidor" (Hardware/Software) y un "Servicio" (Service)?**
   > *Tu respuesta aquí*
    El Servidor es la herramienta y el Servicio es el trabajo que realiza
5. **Investigación: ¿Cuál es la diferencia técnica entre un "Socket TCP" normal y un "WebSocket"?**
   > *Tu respuesta aquí*
TCP es la carretera (infraestructura), WebSocket es el camión de mensajería (reglas de entrega) que corre sobre ella para que la web funcione en vivo
6. **Analizando nuestro código: ¿Quién actúa como Servidor y quién actúa como Cliente? (Justifica tu respuesta mencionando qué funciones del código lo demuestran, ej. `bind()`, `connect()`).**
   > *Tu respuesta aquí*
   > Si ves bind() y listen(), estás ante el Servidor.

Si ves connect() apuntando a una IP externa, estás ante el Cliente.

7. **En el código de la computadora (Python), importamos la librería `threading` (Hilos). ¿Qué pasaría con la ventana de Tkinter si no usáramos hilos para recibir los datos de la red?**
   > *Tu respuesta aquí*
Sin hilos, la red secuestra la interfaz. Con hilos, la interfaz y la red trabajan en paralelo.
8. **¿Por qué es necesario usar bloques `try...except` cuando trabajamos con conexiones de red e Internet?**
   > *Tu respuesta aquí*
Es necesario porque las conexiones de red son impredecibles por naturaleza. A diferencia de una operación matemática simple, el éxito de una conexión no depende solo de tu código, sino de factores externos que tú no controlas.
9. **En la función de encender el LED en Python, enviamos el comando así: `sock.send(b'ON')`. ¿Qué significa esa letra `b` antes de las comillas y por qué no enviamos un texto normal?**
   > *Tu respuesta aquí*
La b convierte tu comando en el lenguaje que la tarjeta de red y el microcontrolador (como un Arduino o ESP32) pueden procesar físicamente.
10. **Describe brevemente el flujo de datos: ¿Qué camino recorre la información desde que giras el potenciómetro físicamente hasta que la barra se mueve en la pantalla de la computadora?**
    > *Tu respuesta aquí*
    > Aquí tienes el resumen definitivo en dos líneas:

Infraestructura y Red: El Servidor es la máquina que aloja, el Servicio es la tarea que realiza, y los Sockets (TCP/Web) son las tuberías por donde viajan los datos.

Código y Flujo: Usamos Hilos y Bytes (b'') para que la red envíe el valor del potenciómetro a la interfaz (Tkinter) sin congelarla, protegiendo todo con try...except.


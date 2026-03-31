<h1 align="center">Node.js</h1>

---

## ¿Qué es?
Es un **entorno de ejecución de JavaScript** que te permite usar este lenguaje **fuera del navegador,** por ejemplo en tu computadora o en un servidor.

Antes, **JavaScript solo se ejecutaba dentro de un navegador web** (como Chrome o Firefox).
Con Node.js, ahora puedes usar JavaScript para crear:

- Servidores web
- Aplicaciones backend
Herramientas de línea de comandos
- APIs
- Y hasta programas de escritorio o apps IoT

---

## ¿Cómo funciona?
Está construido sobre el **motor V8 de Google Chrome,** el mismo que interpreta y ejecuta JavaScript en el navegador.
Pero además, le agrega módulos y herramientas del sistema operativo (archivos, red, procesos, etc.) que no existen en el navegador.

Esto hace posible cosas como:

```JavaScript
const fs = require('fs');
fs.writeFileSync('mensaje.txt', '¡Hola desde Node.js!');
```

Este código crea un archivo en tu computadora, algo imposible desde un navegador.

---

## Arquitectura y características principales
| Característica                | Explicación                                                                                              |
| ------------------------------| -------------------------------------------------------------------------------------------------------- |
| **Basado en módulos**         | Puedes importar y reutilizar código fácilmente (`require` o `import`).                                   |
| **Asíncrono y no bloqueante** | Node usa un solo hilo, pero maneja muchas tareas a la vez con un sistema basado en eventos (Event Loop). |
| **Rápido y eficiente**        | Gracias al motor V8 y su diseño orientado a I/O asíncrono.                                               |
| **Ideal para servidores**     | Permite crear servidores web muy ligeros y escalables.                                                   |
| **Integrado con npm**         | Viene con el gestor de paquetes npm, que te da acceso a millones de librerías.                           |

---

## Ejemplo práctico: servidor básico en Node.js
Crea un archivo llamado server.js:

```JavaScript
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('¡Hola desde mi primer servidor Node.js!');
});

server.listen(3000, () => {
  console.log('Servidor ejecutándose en http://localhost:3000');
});
```

Ejecuta:
```
node server.js
```

Abre tu navegador en `http://localhost:3000`
Y verás el mensaje:
**¡Hola desde mi primer servidor Node.js!**

---

## ¿Para qué se usa Node.js?
| Uso                               | Ejemplo                                       |
| --------------------------------- | --------------------------------------------- |
| **APIs y backend web**            | Express, NestJS, Fastify                      |
| **Aplicaciones en tiempo real**   | Chats, juegos, notificaciones (con Socket.IO) |
| **Herramientas de desarrollo**    | Webpack, ESLint, npm                          |
| **Bots y automatización**         | Bots de Discord, Telegram, etc.               |
| **Apps multiplataforma**          | Con frameworks como Electron o React Native   |

---

## Ventajas
- Usa el mismo lenguaje (JavaScript) en frontend y backend.
- Muy rápido para aplicaciones que manejan muchas conexiones.
- Gran comunidad y soporte.
-npm te da acceso a millones de paquetes.

---

## Desventajas
- No es ideal para tareas que requieren mucho procesamiento (como cálculos pesados).
- Su asincronía puede ser difícil al principio para programadores nuevos.

---

## ¿Qué es el Event Loop?
El Event Loop (bucle de eventos) es el mecanismo interno de Node.js que permite ejecutar muchas tareas al mismo tiempo, sin bloquear el programa, aunque solo use un único hilo (thread).

En palabras simples:
Mientras Node.js hace una tarea lenta (como leer un archivo o consultar una base de datos), no se queda esperando, sigue ejecutando otras cosas.
Cuando la tarea termina, el Event Loop recibe el resultado y lo procesa.

**Ejemplo básico**

```JavaScript
console.log("Inicio");

setTimeout(() => {
  console.log("Tarea con retardo");
}, 2000);

console.log("Fin");
```

Salida en consola:

Inicio
Fin
Tarea con retardo

¿Por qué “Tarea con retardo” se ejecuta al final, si aparece antes en el código?

Porque el Event Loop detecta que setTimeout() es una tarea asíncrona (tardará 2 segundos),
entonces la manda a otro lugar (la cola de tareas) y sigue adelante con el resto del programa.


¿Cómo funciona el flujo internamente?
1. Call Stack (pila de llamadas):
    Donde Node ejecuta el código JavaScript línea por línea.

2. Event Table:
    Donde se registran las tareas asíncronas (como timers, lecturas de archivos, peticiones HTTP, etc.).

3. Callback Queue (cola de espera):
    Cuando una tarea asíncrona termina, su “callback” se mueve aquí esperando ser ejecutado.

4. Event Loop:
    Es el vigilante.
    Constantemente pregunta:
    “¿El Call Stack está vacío?”
    Si sí, saca el siguiente callback de la cola y lo ejecuta.


🔁 Representación simple:
Código principal → Event Table → Callback Queue → Event Loop → Call Stack → Resultado
🔧 Ejemplo con tareas reales
const fs = require("fs");

console.log("Inicio");

fs.readFile("archivo.txt", "utf8", (err, data) => {
  console.log("Archivo leído");
});

console.log("Fin");

📤 Salida:

Inicio
Fin
Archivo leído

Mientras Node lee el archivo (operación lenta), el Event Loop deja que el programa continúe.
Cuando termina, ejecuta el callback console.log("Archivo leído").

🚀 Beneficio principal

Gracias al Event Loop:

Node.js no se bloquea con tareas lentas.

Puede atender miles de conexiones simultáneas con un solo hilo.

Es ideal para servidores web, APIs y aplicaciones en tiempo real (chats, sockets, etc.).

💡 En resumen
Componente	Función
Call Stack	Ejecuta el código principal
Event Table	Guarda tareas asíncronas
Callback Queue	Espera a que el Stack esté libre
Event Loop	Mueve las tareas completadas al Stack
Resultado	Flujo rápido y sin bloqueos


Este diagrama muestra cómo funciona el Event Loop en Node.js, que es el corazón de su sistema asíncrono. Vamos parte por parte 👇

## 1. Call Stack (Pila de llamadas)

Aquí se ejecuta el código principal de JavaScript, de arriba hacia abajo.
Cada vez que llamas una función, se “apila” aquí.
Cuando termina, se “desapila”.

🧩 Si algo toma mucho tiempo (como una petición HTTP), se delega fuera del stack para no bloquearlo.

## 2. Event Table (Tabla de eventos)

Cuando hay tareas que tardan (por ejemplo, setTimeout, lecturas de archivos o consultas a una API),
Node.js las manda a esta “mesa de trabajo”.

Aquí los eventos esperan a que el sistema operativo los complete.

## 3. Callback Queue (Cola de callbacks)

Una vez que una tarea asíncrona termina, su función callback pasa a esta cola.

Pero aún no se ejecuta, solo espera su turno.

## 4. Event Loop

El Event Loop es el encargado de revisar constantemente:

“¿Está libre el Call Stack?”

Si sí, toma el primer callback de la Callback Queue y lo ejecuta.

Si no, espera hasta que el stack quede vacío.

Así Node.js puede hacer muchas cosas al mismo tiempo sin bloquear el programa 💡

⚡ Ejemplo rápido:
console.log('1');
setTimeout(() => console.log('2'), 1000);
console.log('3');

🔹 Call Stack: ejecuta console.log('1') → muestra 1
🔹 Envía setTimeout al Event Table
🔹 Ejecuta console.log('3') → muestra 3
🔹 Cuando pasa 1 segundo, el callback (console.log('2')) vuelve a la Callback Queue
🔹 El Event Loop lo envía al Call Stack → muestra 2

🧠 Resultado final en consola:

1
3
2
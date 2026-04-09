<h1 align="center">MODELO CLIENTE - SERVIDOR</h1>

---

## ¿Qué es?
Es una arquitectura de red en la que las funciones de un sistema se dividen entre **clientes y servidores**.
- El **servidor** ofrece servicios, recursos o datos.
- El **cliente** solicita esos servicios o recursos para su uso.

Es como un restaurante: el **cliente** es quien pide la comida, y el **servidor** (el chef y el personal de cocina) prepara y entrega lo solicitado.

---

## Características Principales
1. **Centralización:** El servidor centraliza los recursos y servicios, lo que facilita la administración y seguridad.
2. **Interacción:** Los clientes dependen del servidor para obtener información o ejecutar funciones.
3. **Escalabilidad:** Se pueden agregar más clientes sin que afecte directamente al servidor (hasta cierto limite).
4. **Dependencia del servidor:** Si el servidor falla los clientes no pueden acceder a los recursos.

---

## Componentes
- **Cliente:** Computadora, aplicación o dispositivo que hace peticiones.
- **Servidor:** Computadora o programa que recibe peticiones y envia respuestas.
- **Red:** Medio de comunicación que conecta clientes y servidores, como internet o una red local (LAN).

---

## ¿Cómo Funciona?
- **Cliente**
    - Es quien **inicia la comunicación** enviando una **solicitud**. 
    - **Ejemplo:** tu navegador cuando escribes **www.google.com**
- **Solicitud o Petición**
    - El cliente pide un recurso o servicio al servidor. 
    - **Ejemplo:** el navegador solicita la página principal de Google.
- **Servidor**
    - Recibe la **solicitud**, la procesa y prepara la **respuesta**.
    - **Ejemplo:** El servidor de Google busca y arma la página de inicio para enviarla de vuelta.
- **Red**
    - Es el medio de comunicación entre cliente y servidor (Internet, WI-FI, LAN, etc).
    - Todos los datos viajan por esta red en mabas direcciones.
- **Flujo completo**
    1. El **cliente envía solicitud**.
    2. El **servidor procesa** la petición.
    3. El **servidor responde** (información, archivos, páginas web, etc).
    4. El **cliente recibe la respuesta** y la muestra al usuario.
---

## Tipos de Servidores
- **Servidor de archivos:** Almacena y comparte documentos o archivos.
- **Servidor web:** Proporciona páginas web y contenido en línea.
- **Servidor de correo:** Admnistra y entrega correos electrónicos.
- **Servidor de base de datos:** Maneja y proporciona acceso a bases de datos.

---

## Ventajas
- Administración centralizada.
- Mayor seguridad al controlar el acceso desde un punto central.
- Facilita el mantenimiento y actualización de aplicaciones.

---

## Desventajas
- **Dependencia del servidor:** Si falla, los clientes quedan intactos.
- **Costo:** Un servidor potente pude ser caro.
- **Escalabilidad limitada:** Demasiados clientes pueden saturar el servidor. 

---

## Ejemplos en la vida diaria
- **Navegar en internet:** Tu navegador (cliente) pide páginas a un servidor web.
- Aplicaciones de correo electrónico como Gmail.
- Juegos en línea donde los jugadores (clientes) se conectan a un servidor central que gestiona la partida. 

---

## Diagrama del funcionamiento del modelo cliente-servidor
<div align="center">
  <img src="/imgs/client-server-model.png" width="600" alt="Diagrama cliente-servidor" />
</div>

---

## Explicación del diagrama
1. **Cliente(laptop)**
    - Representado por una computadora portatil.
    - Es quien *inicia la comunicación* enviando una *solicitud*.
    - Ejemplo: tu navegador cuando escribes *www.google.com*.
2. **Solicitud (flecha hacia el servidor)**
    - El cliente pide un recurso o servicio al servidor.
    - Ejemplo: El navegador solicita la página principal de Google.
3. **Servidor**
    - Recibe la *solicitud*, la procesa y prepara la *respuesta*.
    - Ejemplo: El servidor de Google busca y arma la página de inicio para enviarla de vuelta.
4. **Red (línea con doble flecha)**
    - Es el medio de comunicación entre cliente y servidor (Internet, WI-FI, LAN).
    - Todos los datos viajan por esta red en ambas direcciones.
5. **Flujo completo**
    1. El *cliente envía solicitud*.
    2. El *servidor procesa* la petición.
    3. El *servidor responde* (información archivo, página web, etc).
    4. El *cliente recibe la respuesta* y la muestra al usuario.

---

## En resumen
El cliente **pide**, el servidor **responde**, y la red es el canal por donde viaja la información en ambas direcciones.  
<h1 align="center">CROSS-ORIGIN RESOURCE SHARING (CORS)</h1>

--- 

## ¿Qué es?
CORS significa **Cross-Origin Resource Sharing** (Compartición de Recursos entre Orígenes Cruzados).
Es un **mecanismo de seguridad** implementado por los navegadores para controlar qué recursos (APIs, imágenes, scripts, etc.) pueden ser solicitados desde **otro dominio diferente** al del sitio que hace la petición.

---

## En pocas palabras:
- Si tu frontend está en *http://midominio.com*
- Y tu backend está en *http://api.otrositio.com* 
  el navegador **bloqueará** la petición por seguridad...
  a menos que el **el servidor backend permita explicitamente** ese acceso usando CORS.

---

## ¿Por qué existe?
Para **proteger a los usuarios** de ataques como el **Cross-Site Request Forgery (CSRF)** o accesos no autorizados.
Sin CORS, cualquier página maliciosa podría hacer peticiones a tu API privada sin restricciones.

---

## ¿Cómo funciona?
Cuando haces una petición AJAX/Fetch desde un origen distinto, el navegador:
1. Envía una **petición preliminar** llamada **OPTIONS (Preflight request) al servidor.**
2. El servidor responde con cabeceras que dicen si permite esa petición.
    - **Ejemplo de cabeceras:**
      - **Access-Control-Allow-Origin:** *http://midominio.com*
      - **Access-Control-Allow-Methods:** GET, POST, PUT
      - **Access-Control-Allow-Headers:** Content-Type
3. Si el servidor **autoriza**, el navegador hace la petición real. 
4. Si no, el navegador la bloquea.

---

## Diagrama del funcionamiento de CORS
<div align="center">
  <img src="/imgs/cors.png" width="600" alt="Diagrama cliente-servidor" />
</div>

---

## En resumen:
- **CORS = reglas que el servidor define** para permitir o no peticiones desde otro dominios.
- Se controla con **cabeceras HTTP** (Access-Control-Allow-*).
- Evita riesgos de seguridad pero si no se configura bien puede bloquear tus peticiones aunque sean legítimas.
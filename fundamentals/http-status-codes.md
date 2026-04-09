<h1 align="center">CÓDIGOS DE ESTADO HTTP</h1>

---

## ¿Qué son?
Son respuestas de tres digitos que un servidor devuelve a un cliente (como puede ser un navegador web) para indicar si una solicitud ha sido procesada exitosamente, si hay un error o si se necesita más información. Se dividen en 5 clases principales.

---
## 1xx - Informativos
El servidor recibió la petición y sigue procesandola.
- **100 Continue:** El servidor recibió la petición, sigue el proceso.
- **101 Switching:** El servidor cambia a otro protocolo (ej. WebSocket).
- **102 Processing:** La petición esta en proceso (usado en WebDAV). 
- **103 Early Hints:** El servidor envía cabeceras preliminares antes de la respuesta final.
---

## 2xx - Éxito
La petición fue recibida, entendida y procesada correctamente.
- **200 OK:** La petición fue exitosa.
- **201 Created:** Se creo un recurso nuevo como resultado de la petición.
- **202 Accepted:** La petición fue aceptada pero aún no procesada. 
- **203 Non-Authoriative Information:** Información devuelta por una fuente diferente al servidor original.  
- **204 No Content:** La petición fue exitosa, pero no hay contenido que devolver.   
- **205 Reset Content:** La petición fue exitosa y se solicita que el cliente restablezca la vista.  
- **206 Partial Content:** La respuesta contiene solo una parte del recurso, según el rango solicitado.  
- **207 Multi-Status (WebDAV):** Respuesta con múltiples códigos para diferentes recursos.  
- **208 Already Reported (WebDAV):** Los recursos ya fueron reportados anteriormente.
- **226 IM Used (HTTP Delta encoding):** La petición fue exitosa y se aplicó el Delta Encoding.
---

## 3xx - Redirecciones
El cliente debe realizar otra acción para completar la petición.
- **300 Multiple Choices:** Hay varias opciones para el recurso solicitado.
- **301 Moved Permanently:** El recurso se movió permanentemente a otra URL.
- **302 Found:** Redirección temporal.
- **303 See Other:** La respuesta debe ser obtenida con un GET en otra URL. 
- **304 Not Modified:** El recurso no ha cambiado, usar la versión en caché.
- **305 Use Proxy:** Se debe acceder al recurso usando el proxy especificado (Deprecado por seguridad).
- **306 Switch Proxy:** Reservado no se usa actualmente.
- **307 Temporary Redirect:** Redirección temporal manteniendo el método HTTP.
- **308 Permanent Redirect:** Redirección permanente manteniendo el método HTTP.
---

## 4xx - Errores del cliente
Indican que el cliente hizo algo mal en la petición.
- **400 Bad Request:** La petición no pudo ser entendida por el servidor.     
- **401 Unauthorized:** Autenticación requerida o fallida.             
- **402 Payment Required:** Reservado para futuros usos.                   
- **403 Forbidden:** El servidor entendió la petición pero se niega a cumplirla.           
- **404 Not Found:** El recurso no existe.                                    
- **405 Method Not Allowed:** El método HTTP no está permitido para este recurso.                                     
- **406 Not Acceptable:** El recurso no puede generar contenido aceptable según las cabeceras del cliente.        
- **407 Proxy Authentication Required:** Se requiere autenticación con el proxy.                                                 
- **408 Request Timeout:** La petición tardó demasiado y fue cancelada.                                            
- **409 Conflict:** La petición no pudo completarse debido a un conflicto con el estado actual del recurso. 
- **410 Gone:** El recurso ya no está disponible y no volverá.                               
- **411 Length Required:** Se requiere el encabezado `Content-Length`.                                             
- **412 Precondition Failed:** Una precondición en la cabecera falló.                                                 
- **413 Payload Too Large** El cuerpo de la petición es demasiado grande.                                           
- **414 URI Too Long:** La URL es demasiado larga.                                                             
- **415 Unsupported Media Type:** El tipo de contenido de la petición no es soportado.                                    
- **416 Range Not Satisfiable:** El rango solicitado no puede ser cumplido.                                  
- **417 Expectation Failed:** El servidor no puede cumplir con la cabecera `Expect`.                                  
- **418 I'm a teapot:** [Broma de RFC 2324, Hyper Text Coffee Pot Control Protocol]                             
- **421 Misdirected Request:** La petición fue dirigida a un servidor que no puede producir la respuesta.              
- **422 Unprocessable Entity:** (WebDAV) La entidad está bien formada pero no se puede procesar.                        
- **423 Locked:** (WebDAV) El recurso está bloqueado.                                                     
- **424 Failed Dependency:** (WebDAV) Falló porque una petición anterior falló.                                      
- **425 Too Early:** Evita procesar la petición prematuramente.                                              
- **426 Upgrade Required:** Se requiere cambiar a un protocolo diferente.                                           
- **428 Precondition Required:** Se requiere una precondición para evitar actualizaciones concurrentes.                  
- **429 Too Many Requests:** El cliente envió demasiadas peticiones en poco tiempo.                                  
- **431 Request Header Fields Too Large:** Los encabezados de la petición son demasiado grandes.                                   
- **451 Unavailable For Legal Reasons:** El recurso no está disponible por motivos legales.                         
---

## 5xx - Errores del servidor
El problema esta del lado del servidor.
- **500 Internal Server Error:** Error génerico en el servidor.
- **501 Not Implemented:** El servidor no soporta la funcionalidad.
- **502 Bad Gateway:** El servidor recibió una respuesta inválida de otro servidor.
- **503 Service Unavailble:** El servidor no puede procesar la petición (sobrecarga o mantenimiento).
- **504 Gateway Timeout:** Tiempo agotado entre servidores.
- **505 HTTP Version Not Supported:** La versión de HTTP no es soportada.
- **506 Variant Also Negotiates:** Error de negociación de contenido.
- **507 Insufficient Storage (webDAV):** Espacio insuficiente para completar la operación.
- **508 Loop Detected (webDAV):** Bucle infinito detectado al procesar la petición.
- **510 No Extended:** La petición requiere extensiones adicionales.
- **511 Network Authentication Required:** Se requiere autenticación de red (ej. proxy de WI-FI corporativa).
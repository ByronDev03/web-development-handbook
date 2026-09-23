<h1 align="center">¿QUÉ ES UN ENDPOINT?</h1>

---

Un endpoint es una URL específica a la que puedes acceder para realizar una acción o solicitar datos en una API (Interfa de Programación de Aplicaciones).

> [!NOTE]
> En pocas palabras: un endpoint es una puerta de entrada a un recurso o funcionalidad en un servidor.

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/endpoint-diagram.avif" width="600" alt="Diagrama endpoint" />
</div>

---

## Partes de un Endpoint
<div align="center">
  <img src="/imgs/parts-endpoint.avif" width="600" alt="Partes de un endpoint" />
</div>

- <p style="text-align: left; color: green; font-weight: bold;">
    🟢 1.- Protocolo: 
    <span style="color: black; font-weight: normal;">Define cómo se realiza la comunicación. (HTTP o HTTPS)</span>
</p>

- <p style="text-align: left; color: purple; font-weight: bold;">
    🟣 2.- Dominio:
    <span style="color: black; font-weight: normal;">Es la dirección del servidor que aloja la API.</span>
</p>

- <p style="text-align: left; color: red; font-weight: bold;">
    🔴 3.- Versión:
    <span style="color: black; font-weight: normal;">Indica la version de la API. (Opcional, pero recomendado)</span>
</p>

- <p style="text-align: left; color: orange; font-weight: bold;">
    🟠 4.- Recurso:
    <span style="color: black; font-weight: normal;">El recurso al que quieres acceder. (ej, usuarios)</span>
</p>

- <p style="text-align: left; color: blue; font-weight: bold;">
    🔵 5.- Identificador:
    <span style="color: black; font-weight: normal;">ID o parámetro específico del recurso. (ej. 123)</span>
</p>
 
---

## Respuesta de un Endpoint
Los endpoints suelen devolver datos en formatos como JSON.

```JSON
{
    "id": 123,
    "nombre": "Ana Rosa",
    "email": "ana@example.com",
    "rol": "admin"
}
```

Tambíen pueden devolver códigos de estado HTTP:

- ✅ 200 OK - Exito
- ✅ 201 Created - Creado
- ⚠️ 400 Bad Request - Error en la petición
- ⚠️ 404 Not Found - No encontrado
- ❌ 500 Internal Server Error - Error del servidor

---

## Ejemplo práctico
Supongamos una API de usuarios: `https://api-ejemplo.com/v1/usuarios`

| Método                                                              | Endpoint             | Descripción                        | Ejemplo de Uso               |
| :---:                                                               | :---                 | :---                               | :---                         |
| <img src="/imgs/get.avif" width="115" alt="Método GET"/>            | /v1/usuarios         | Obtener todos los usuarios         | **GET** /v1/usuarios         |
| <img src="/imgs/getbyid.avif" width="115" alt="Método GET by ID"/>  | /v1/usuarios/123     | Obtener un usuario por ID          | **GET** /v1/usuarios/123     |
| <img src="/imgs/post.avif" width="115" alt="Método POST"/>          | /v1/usuarios         | Crear un nuevo usuario             | **POST** /v1/usuarios        |
| <img src="/imgs/put.avif" width="115" alt="Método PUT"/>            | /v1/usuarios/123     | Actualizar un usuario completo     | **PUT** /v1/usuarios/123     |
| <img src="/imgs/patch.avif" width="115" alt="Método PATCH"/>        | /v1/usuarios/123     | Actualizar parcialmente un usuario | **PATCH** /v1/usuarios/123   |
| <img src="/imgs/delete.avif" width="115" alt="Método DELETE"/>      | /v1/usuarios/123     | Eliminar un usuario                | **DELETE** /v1/usuarios/123  |
                       
---

## Métodos HTTP más comunes en endpoints REST



---

## ¿Para qué sirven los Endpoints?
- Permiten que diferentes aplicaciones se comuniquen entre sí.
- Facilitan el acceso a datos y funcionalidades de un sistema desde el exterior.
- Son la base para integrar servicios y construir aplicaciones modernas.

---

## Buenas Prácticas
- ✅ Usar nombres de recursos en plural ( */usuarios en lugar de /usuario* ). 
- ✅ Usar métodos HTTP adecuados para cada acción. 
- ✅ Incluye la versión de la API ( */v1/* ).
- ✅ Ser consistente en la estructura de los endpoints.
- ✅ Documentar los endpoints ( *ej. con OpenAPI/Swagger* ).

---

## En resumen
Un endpoint es una URL especifica que expone un recurso o funcionalidad de una API. A través de él, los clientes pueden enviar peticiones y obtener respuestas del servidor.
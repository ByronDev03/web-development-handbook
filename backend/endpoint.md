<h1 align="center">¿QUÉ ES UN ENDPOINT?</h1>

---

Un endpoint es una URL específica a la que puedes acceder para realizar una acción o solicitar datos en una API (Interfa de Programación de Aplicaciones).

> [!NOTE]
> En pocas palabras: un endpoint es una puerta de entrada a un recurso o funcionalidad en un servidor.

---

## ¿Cómo funciona?


---

## Partes de un Endpoint


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

---

## Ejemplo práctico


---

## Métodos HTTP más comunes en endpoints REST


---

## ¿Para qué sirven los Endpoints?
- Permiten que diferentes aplicaciones se comuniquen entre sí.
- Facilitan el acceso a datos y funcionalidades de un sistema desde el exterior.
- Son la base para integrar servicios y construir aplicaciones modernas.

---

## Buenas Prácticas
- Usar nombres de recursos en plural ( */usuarios en lugar de /usuario* ). 
- Usar métodos HTTP adecuados para cada acción. 
- Incluye la versión de la API ( */v1/* ).
- Ser consistente en la estructura de los endpoints.
- Documentar los endpoints ( *ej. con OpenAPI/Swagger* ).

---

## En resumen
Un endpoint es una URL especifica que expone un recurso o funcionalidad de una API. A través de él, los clientes pueden enviar peticiones y obtener respuestas del servidor.
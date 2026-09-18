<h1 align="center">¿QUÉ ES UNA API?</h1>

---

Una API (Interfaz de Programación de Aplicaciones) es un conjunto de reglas y protocolos que permite que difrentes aplicaciones se comuniquen entre sí para intercambiar datos y funcionalidades.

---

## En pocas palabras
Una **API** es un puente que permite que dos aplicaciones se entiendan y trabajen juntas sin que se necesite conocer cómo estan implementadas por dentro.

<div align="center">
  <img src="/imgs/api-diagram1.png" width="600" alt="Ejemplo API" />
</div>

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/api-diagram2.png" width="600" alt="¿Cómo funciona?" />
</div>

> [!NOTE]
> **FORMATO DE LOS DATOS**.
> Las APIs comúnmente utilizan formatos como JSON o XML para intercambiar información.

---

## Tipos de API
- **Públicas:** Son abiertas para que cualquier desarrollador pueda usarlas. 
    - **Ejemplo:** *API de clima pública OpenWeather*

- **Privadas:** Solo pueden ser usadas denteo de una empresa u organización.
    - **Ejemplo:** *API interna de una empresa para su app móvil.*

- **De socios:** Se comparten con socios estratégicos o empresas autorizadas.
    - **Ejemplo:** *API de pagos compartida con comercios afiliados.*

- **Compuestas:** Combina varias APIs para ofrecer una funcionalidad más compleja.
    - **Ejemplo:** *Una app que usa varias APIs (mapas, clima, tráfico) juntas.*

---

## Elementos de una API
- **Endpoint:** Es la **URL** específica donde se realiza la solicitud.
    - **Ejemplo:** `/usuarios`

- **Método HTTP:** Inidica la acción a realizar.
    - *GET, POST, PUT, DELETE, etc.*

- **Parámetros:** Filtros o datos que se envían para personalizar la solicitud.
    - **Ejemplo:** `?id=10`

- **Encabezados (Headers):** Información adicional como autenticación, tipo de contenido, etc.
    - **Ejemplo:** `Authorization`

- **Respuesta:** Datos devueltos por la API en un formato (Generalmente JSON).
    - *Código de estado HTTP (200 OK, 404, etc.)*

---

## Características principales
- **Interfaz:** Define los métodos y datos que se pueden solicitar y cómo hacerlo.
- **Independencia:** El cliente y el servidor pueden cambiar su implementación sin afectar al otro.
- **Reutilización:** Permite usar funcionalidades existentes sin reinventar la rueda.
- **Escalabilidad:** Facilita el crecimiento de aplicaciones integrando servicios externos.
- **Seguridad:** Permite controlar el acceso mediante autenticación y permisos.

---

## Ejemplo práctico
Supongamos que se usa una app del clima en tu celular:
<div align="center">
  <img src="/imgs/api-diagram3.png" width="600" alt="Ejemplo práctico" />
</div>

**Ejemplo de solicitud HTTP**
**GET** `https://api.openweatherapp.org/data/2.5/weather?q=MexicoCity&appid=TU_API_KEY`

```JSON
{
    "name": "Mexico City",
    "main": { "temp": 17.6, "humidity": 76 },
    "weather": { { "description": "nubes dispersas" } }
}
```

> [!IMPORTANT]
> La API responde en JSON con la información solicitada.

---

## Beneficios de usar APIs

- Aceleran el desarrollo al reutilizar servicios existentes.
- Reducen costos y esfuerzo de desarrollo.
- Permiten integrar servicios y sistemas diferentes.
- Mejoran la seguridad y el control de datos.
- Facilitan la innovación y la creación de nuevos productos.

---

## Ejemplos de APIs pupulares
- Google Maps API
- Stripe API (pagos)
- OpenWeather API (clima)
- <img src="https://cdn.simpleicons.org/github/ffffff" width="16"/> Github API (repositorios)
- Youtube Dats API (videos)

--- 

## En resumen
Una API es la forma en que las aplicaciones se comunican y comparten información de manera segura, eficiente y estandarizada. 

---

> [!IMPORTANT]
> **¡LAS APIS ESTAN EN TODAS PARTES!** <br>
> Desde redes sociales, mapas, pagos en línea, hasta en el clima que se consulta a diario. Son la base de muchas aplicaciones modernas. 


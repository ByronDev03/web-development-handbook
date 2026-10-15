<h1 align="center">¿QUÉ ES JWT?</h1>

<p align="center">
Permite autenticar usuarios mediante tokens sin almacenar sesiones.
</p>

---

## ¿Qué es?

JWT (JSON Web Token) es un estándar abierto (RFC 7519) para transmitir información de forma segura entre cliente y servidor mediante un token firmado digitalmente.

- **Seguro** firmado digitalmente.
- **Sin sesiones** Stateless (sin estado en el servidor).
- **Estándar abierto** usado por la mayoría de APIs.
- **Basado en JSON** ligero y fácil de usar.

---

## Estructura de un JWT
- **Un JWT tiene 3 partes, separadas por puntos( . )**
<div align="center">
  <img src="/imgs/jwt1.avif" width="600" alt="Estructura de un JWT" />
</div>

---

## Claims más comunes
Los claims en JWT (JSON Web Token) son los datos o afirmaciones que se guardan dentro del payload del token. Sirven para transportar información sobre el usuario, el emisor del token, su fecha de expiración y otros datos necesarios para la autenticación y autorización.
- `sub` Sujeto (ID del usuario)
- `iss` Emisor del token
- `aud` Audiencia (quién lo recibe)
- `exp` Fecha de expiración
- `iat` Fecha de emisión
- `nbf` No válido antes de
- `role` Bot o permisos
- `email` Correo del usuario

---

## Flujo de autenticación con JWT
<div align="center">
  <img src="/imgs/jwt2.avif" width="600" alt="Autenticación con JWT" />
</div>

---

## Ventajas
- ✅ Sin almacenamiento de sesiones en el servidor (stateless).
- ✅ Escalable (ideal para microservicios).
- ✅ Seguro (firma digital). 
- ✅ Funciona en múltiples plataformas
- ✅ Ligero y compacto.
- ✅ Perfecto para APIs y aplicaciones web/móviles.

---

## Ejemplo en Node.js
```Bash
// Generar un JWT
const jwt = require('jsonwebtoken');

const token = jwt.sign(
    {
        userId: 123,
        nombre: "Ana",
        rol: "admin"
    },
    process.env.JWT_SECRET,
    { expiresIn: '1h' }
);

console.log(token);
```

---

## Verificación
```Bash
// Verificar un JWT
try{
    const decoded = jwt.verify(
        token,
        process.env.JWT_SECRET
    );
    
console.log('Token válido:'; decoded);
} catch (error) {
    console.log('Token inválido');
}
```

---

## JWT vs Sesiones
| ASPECTO         | JWT                    | Sesiones                    | 
| :---:           | :---:                  | :---:                       | 
| Estado          | Stateless (sin estado) | Stateful (con estado)       | 
| Almacenamiento  | En el cliente (token)  | En el servidor (memoria/DB) | 
| Escalabilidad   | Alta                   | Limitada                    | 
| Rendimiento     | Mejor                  | Menor                       | 
| Uso típico      | APIs, SPA, Mobile      | Apps tradicionales          |

---

## ¿Dónde se usa?
- APIs REST y GraphQL
- Aplicaciones móviles
- Aplicaciones web SPA (Reacta, Vue, Angular)
- Microservicios
- Sistemas de Single Sign-On (SSO)

---

## En resumen
Autenticación segura, simple y escalable para la web moderna.
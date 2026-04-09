<h1 align="center">MÉTODOS DE PETICIÓN HTTP</h1>

---

## ¿Qué son?
Tambien llamados *"verbos HTTP"* son acciones que indican que operación se requiere realizar sobre un recurso en un servidor (una página, un archivo, un dato en una API, etc).

---
## Métodos HTTP principales
1. **GET:** Solicita datos de un recurso. No modifica nada.
    - **Ejemplo:** Enviar a *https://api.ejemplo.com/users* para obtener la lista de usuarios.
2. **POST:** Envia datos al servidor para **crear** un nuevo recurso.
    - **Ejemplo:** Enviar un formulario de registro para crear un usuario.
3. **PUT:** Envía datos para **reemplazar completamente** un recurso existente.
    - **Ejemplo:** Actualizar todo el perfil de un usuario.
4. **PATCH:** Modifica **solo una parte** de un recurso.
    - **Ejemplo:** Cambiar solo la contraseña de un usuario.
5. **DELETE:** Elimina un recurso en el servidor.
    - **Ejemplo:** Borra un usuario de la base de datos.
6. **HEAD:** Igual que GET, pero devuelve **solo los encabezados** (sin el cuerpo).
    - **Ejemplo:** Saber si una imagen existe, pero sin descargarla.
7. **OPTIONS:** Pregunta al servidor qué métodos estan permitidos sobre un recurso.
    - **Ejemplo:** Un navegador consulta si puede usar POST en una API (CORS).
8. **TRACE:** Devuelve la petición tal cual la recibió (para depuración, casi no se usa).
    - **Ejemplo:** Probar el camino que recorre la petición en la red.
9. **CONNECT:** Establece un túnel con el servidor (usado para HTTPS).
    - **Ejemplo:** Navegar seguro a través de un proxy.

---
## En resumen:
- **GET:** Leer 
- **POST** Crear
- **PUT** Reemplazar
- **PATCH** Modificar parcialmente
- **DELETE** Eliminar

<div align="center">
  <img src="/imgs/http-methods.png" width="600" alt="seo" />
</div>
<h1 align="center">¿QUÉ ES EL ARCHIVO .ENV?</h1>

---

El archivo **.env** (environment) se usa para guardar variable de entorno fuera del código fuente. Permite configurar la aplicacipin según el entorno (desarrollo, pruebas, producción) de forma segura y flexible.

---

## ¿Por qué es importante?
- ✅ Protege información sensible (claves, contraseñas).
- ✅ Facilita la configuración por entorno
- ✅ Evita cambiar código cuando cambian los datos.
- ✅ Hace tu aplicación más portable y escalable.

---

## ¿Cómo se ve un archivo .ENV?
```Bash
# Configuración de la aplicación
APP_NAME=MiApp
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost:8000

# Base de datos
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=mi_app
DB_USERNAME=root
DB_PASSWORD=secreto123
```

> [!NOTE]
> Cada línea tiene un formato CLAVE=valor
> Las líneas que comienzan con `#` son comentarios

---

- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css" width="20"/> Next.js
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css" width="20"/> Laravel
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css" width="20"/> Django


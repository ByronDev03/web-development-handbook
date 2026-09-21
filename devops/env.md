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

## ¿Para qué sirve?
- **Guardar credenciales:** Claves de API, contraseñas, tokens, etc.
- **Configurar la aplicación:** URLs, puertos, modos, características, etc.
- **Diferentes entornos:** Desarrollo, pruebas y producción sin cambiar el código. 
- **Trabajo en equipo:** Cada desarrollador usa su propio .env sin exponer datos.

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

## ¿Dónde y cómo se usa?
- **En frameworks populares**
    -  <img src="https://cdn.simpleicons.org/node.js" width="20"/> **Node.js:** `process.env.MI_CLAVE`
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/php/php-original.svg" width="20"/> **PHP:** `$_ENV['MI_CLAVE']`
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" width="20"/> **Python:** `os.getenv('MI_CLAVE')`
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" width="20"/> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original.svg" width="20"/> **Java (Spring):** `@Value("${mi.clave}")`

- **En frameworks populares**
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg" width="20"/> **Laravel:** `Usa el archivo .env para configuración de la app.`
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg" width="20"/> **Next.js:** `Variables disponibles en process.env.NEXT_PUBLIC_*`
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/django/django-plain.svg" width="20"/> **Django:** `Usa python-decouple o django-environ.`
    - <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vitejs/vitejs-original.svg" width="20"/> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" width="20"/> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original.svg" width="20"/> **Vite / React / Vue:** `Variables con VITE_(ej: VITE_API_URL)`

---

## Ejemplos de uso
- **Base de datos**
    - `DB_HOST=localhost`
    - `DB_DATABASE=mi_app`
    - `DB_USERNAME=root`
    - `DB_PASSWORD=secreto123`

- **APIs externas**
    - `API_URL=https://api.example.com`
    - `API_KEY=sk_live_xxxxxxxxxx`

- **Correo electrónico**
    - `MAIL_HOST=smtp.mail.com`
    - `MAIL_PORT=587`
    - `MAIL_USER=usuario@mail.com`
    - `MAIL_PASSWORD=secreto789`

- **General**
    - `APP_URL=https://miapp.com`
    - `APP_DEBUG=false`
    - `JWT_SECRET=secreto456`

---

## Buenas prácticas
- **Nunca subir el .env al repositorio:** Agregarlo al .gitignore. 
- **Usar variables descriptivas y consistentes:** Ej: DB_HOST en lugar de host
- **Usa archivos diferentes por entorno:** Ej: .env.local, .env.production
- **Proporcionar valores por defecto** cuando sea posible
- **Validar que las variables existan en producción:** Falla rápido si falta alguna
- **Usar secretos seguros en producción:** (Vault, AWS Secrets Manager, etc.)

**.gitignore**
```.gitignore
# Entorno
.env
.env.*
!.env.example
```

---

## Ejemplo: Distintos entornos


---

## Tips rápidos
- ⭐ Reiniciar el servidor después de cambiar el .env 
- ⭐ No poner espacios alrededor del `=`
- ⭐ Usar comillas solo si el valor lo necesita
- ⭐ Documentar tus variables en un .env.example 

---

## En resumen
El archivo .env es clave para mantener tu configuración segura, flexible y portable. Usarlo siempre y nunca exponer los secretos de una app.<br>

**Pequeño archivo, gran impacto**

---


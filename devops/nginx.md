<h1 align="center">¿QUÉ ES NGINX?</h1>

<p align="center">
Sirve aplicaciones, balancea tráfico y actuá como proxy inverso.
</p>

---

## ¿Qué es NGINX?
NGINX (pronunciado *"engine-x"*) es un servidor web de alto rendimiento, proxy inverso, balanceador de carga y caché HTTP.
Es ligero, escalable y se usa para mejorar el rendimiento, seguridad y disponibilidad de aplicaciones.

- **Alto rendimiento:** Maneja miles de conexiones con muy bajo consumo.
- **Confiable y estable:**  Diseñado para estar siempre activo.
- **Flexible:** Configuración potente y modular.
- **Open Source:** Gratuito y con grand comunidad.

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/nginx1.avif" width="600" alt="Funcionamiento de NGINX"/>
</div>

> [!NOTE]
> NGINX recibe las solicitudes de los clientes y decide a dónde enviarlas.
> Puede servir archivos estáticos, balancear entre servidores y mejorar la seguridad.

---

## Características principales
- Servidor web rápido y eficiente. 
- Proxy inverso y balanceador de carga.
- Soporte para HTTP y HTTP/2/3.
- Caché de contendido.
- Protección y control de acceso.
- Compresión de respuestas.
- Configuración simple y poderosa
- Alta disponibilidad y escalabilidad.

---

## ¿Para qué se usa?
- **Servidor web:** Sirve sitios web y archivos estáticos.
- **Balanceador de carga:** Distribuye el tráfico entre múltiples servidores.
- **Proxy inverso:** Protege servidores internos y mejora la seguridad.
- **Caché:** Acelera respuestas almacenamiento contenido.
- **API Gateway:** Gestiona y protege APIs y microservicios.
- **Alta disponibilidad:** Mejora la tolerancia a fallos.

---

## Ejemplo de configuración básica
```Bash
server {
    listen 80;
    server_name ejemplo.com;

    location / {
        proxy_pass http://backend_app;  # Proxy inverso
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }

    location /static/ {
        root /var/www/html;
        expires 30d;  # Caché de archivos estáticos
    }
}
```

---

## Flujo de una solicitud
<div align="center">
  <img src="/imgs/nginx2.avif" width="600" alt="Flujo de una solicitud NGINX"/>
</div>

---

## NGINX vs Otros
| ASPECTO         | NGINX                                       | APACHE                 | HAProxy                           |
| :---:           | :---:                                       | :---:                  | :---:                             |
| Tipos           | Servidor web / Proxy inverso / Balanceador  | Servidor web           | Balanceador de carga              |
| Rendimiento     | Muy alto (event-driven)                     | Alto (process/thread)  | Muy alto                          |
| Concurrencia    | Miles de conexiones con bajo consumo        | Menor eficiencia       | Optimizado para balanceo TCP/HTTP |
| Configuración   | Simple pero potente                         | Más compleja           | Media                             |
| Uso principal   | Web, APIs, Proxy, Balanceo, Caché           | Sitios web             | Balanceo de carga especializado   |

---

## ¿Dónde se usa NGINX?
- **En la nube** (AWS, GCP, Azure, etc.)
- **Contenedores** (Docker, Kubernetes)
- **Microservicios** y arquitecturas modernas
- **Grandes sitios web** y aplicaciones de alto tráfico

---

## Comandos útiles
```Bash
nginx -v         # Ver versión
nginx -t         # Probar configuración
nginx -s reload  # Recargar configuración
nginx -s stop    # Detener NGINX
nginx -s start   # Iniciar NGINX
```

---

## Beneficios clave
- ✅ Mejora el rendimiento de las aplicaciones que se crean
- ✅ Reduce la carga en servidores backend
- ✅ Aumenta la seguridad y control de acceso
- ✅ Escala fácilmente
- ✅ Optimiza el uso de recursos

---

## En resumen
NGINX es mucho más que un servidor web. Es una herramienta poderosa para entregar aplicaciones más rápidas, seguras y escalables.
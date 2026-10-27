<h1 align="center">
PREGUNTAS PARA ENTREVISTA<br>
(VERSIÓN DOCKER)
</h1>

---

1. **¿Qué es Docker y qué problema resuelve?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Docker es una <strong>plataforma</strong> que <strong>empaqueta</strong> una aplicación junto con todo lo que necesita para correr (runtime, librerías, configuración) en una unidad llamada contenedor.</li>
    <li>Resuelve el clásico "en mi máquina funciona": el mismo contenedor se comporta igual en tu laptop, y en diferentes ambientes como testing y en producción</li>
    </ul>

    ```docker
    docker run -p 8080:8080 mi-app
    # Corre tu app igual en cualquier entorno
    ```
    </details><br>

2. **¿Qué diferencia hay entre una imagen y un contenedor?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Una <strong>imagen</strong> es la plantilla inmutable (solo lectura) con todo lo necesario para correr una app.</li>
    <li>Un <strong>contenedor</strong> es una instancia en ejecución de esa imagen.</li>
    <li>De una misma imagen puedes levantar muchos contenedores.</li>
    </ul>

    ```docker
    # Crea la imagen
    docker build -t mi-app .

    # Crea y corre un contenedor ella
    docker run mi-app
    ```
    </details><br>

3. **¿Qué es un Dockerfile y qué instrucciones principales tiene?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es un archivo de texto con las instrucciones paso a paso para construir una imagen.</p>
    <ul>
    <li><strong>FROM</strong> (imagen base),</li>
    <li><strong>WORKDIR</strong> (directorio de trabajo),</li>
    <li><strong>COPY</strong> (copiar archivos),</li> 
    <li><strong>RUN</strong> (ejecutar comandos al construir),</li>
    <li><strong>EXPOSE</strong> (documentar el puerto) y</li>
    <li><strong>CMD / ENTRYPOINT</strong> (comando de arranque).</li>
    </ul>

    ```docker
    FROM eclipse-temurin:21-jre
    WORKDIR /app
    COPY target/app.jar app.jar
    EXPOSE 8080
    CMD ["java", "-jar", "app.jar"] 
    ```

    </details><br>

4. **¿Qué diferencia hay entre un contenedor y una máquina virtual?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Una <strong>VM virtualiza</strong> el hardware y trae un sistema operativo completo cada una: más pesada y lenta de arrancar.</li>
    <li>Un <strong>contenedor</strong> comparte el kernel del sistema operativo host y solo aisla la aplicación y sus dependencias: es más liviano y arranca en segundos.</li>
    <li>Por eso puedes correr decenas de contenedores en una máquina donde apenas caben unas pocas VMs.</li>
    </ul>
    </details><br>

5. **¿Cuál es la diferencia entre CMD y ENTRYPOINT?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Ambos definen qué se ejecuta al iniciar el contenedor.</p>
    <ul>
    <li><strong>CMD</strong> establece el comando por defecto y puede ser sobrescrito fácilmente al hacer <strong> docker run</strong>.</li>
    <li><strong>ENTRYPOINT</strong> define el ejecutable fijo del contenedor; lo que pases al <strong>docker run</strong> se agrega como argumentos.</li>
    </ul>

    ```docker
    # Siempre se ejecuta 
    ENTRYPOINT ["java", "-jar", "app.jar"]

    # Argumento por defecto, reemplazable
    CMD ["--spring.profiles.active=dev"]
    ```

    </details><br>

6. **¿Para qué sirven los volúmenes (volumes)?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Los datos dentro de un contenedor se <strong>pierden</strong> cuando este se elimina.</li>
    <li>Un volumen <strong>guarda datos fuera</strong> del ciclo de vida del contenedor, para que persistan (por ejemplo, los archivos de una base de datos).</li>
    </ul>

    ```docker
    docker run -v datos-pg:/var/lib/postgresql/data postgres
    # Aunque borres el contenedor, "datos-pg" sigue existiendo
    ```
    </details><br>

7. **¿Qué significa el mapeo de puertos (-p)?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>El contenedor tiene su <strong>propia red aislada,</strong> así que para acceder a él desde fuera debes mapearun puerto del host a uno del contenedor con el formato <strong>-p puertoHost:puertoContenedor</strong></li>
    </ul>

    ```docker
    docker run -p 9090:8080 mi-app
    # Accedes desde https://localhost:9090, internamente la app usa el 8080
    ```

    </details><br>

8. **¿Qué es Docker Compose y cuándo se usa?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es una herramienta para definir y levantar <strong>varios contenedores</strong> a la vez (por ejemplo, tu API + base de datos + Redis) desde un único archivo <strong>docker-compose.yml</strong> con un solo comando.</p>

    ```docker
    services:
        app:
            build: .
            ports: ["8080:8080"]
        db:
            image: postgres:16
    ```

    ```docker
    docker compose up  # Levanta todo el entorno
    ```

    </details><br>

9. **¿Qué es Docker Hub y qué es un registry?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Un registry <strong>es un repositorio</strong> donde se almacenan y distribuyen imágenes.</li>
    <li><strong>Docker Hub</strong> es el registry público más usad, de donde descargas imágenes como <strong>postrgres</strong> o <strong>redis</strong>.</li>
    <li>Las empresas suelen usar registries privados (AWS, ECR, GitHub Container Registry, etc.).</li>
    </ul>

    ```docker
    docker pull redis              # Descarga la imagen desde Docker Hub
    docker push mi-usuario/mi-app  # Publica tu imagen
    ```
    </details><br>

10. **¿Qué buenas prácticas existen al escribir un Dockerfile?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Usar imágenes base ligeras <strong>(-slim, alpine, jre en lugar de jdk)</strong></li>
    <li>Usar un archivo <strong>.dockerignore</strong> para no copiar archivos innecesarios.</li>
    <li>Aprovechar el <strong>caché de capas:</strong> poner primero lo que cambia poco (dependencias) y al final lo que cambia mucho (código).</li>
    <li>No guardar credenciales dentro de la imagen</li>
    <li>Usar <strong>multi-stage builds</strong> para que la imagen final no incluya herramientas de compilación.</li>
    </ul>

    ```docker
    # Multi-stage: compila como Maven, ejecuta solo con JRE
    FROM maven:3.9-eclipse-temurin-21 AS build
    COPY . .
    RUN mvn package
    FROM eclipse-temurin:21-jre
    COPY --from=build target/app.jar app.jar
    ```

    </details><br>
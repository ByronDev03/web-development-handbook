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

    </details><br>

5. **¿Cuál es la diferencia entre CMD y ENTRYPOINT?**
    <details>
    <summary>Solución</summary>

    </details><br>

6. **¿Para qué sirven los volúmenes (volumes)?**
    <details>
    <summary>Solución</summary>

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

    </details><br>

9. **¿Qué es Docker Hub y qué es un registry?**
    <details>
    <summary>Solución</summary>

    </details><br>

10. **¿Qué buenas prácticas existen al escribir un Dockerfile?**
    <details>
    <summary>Solución</summary>

    </details><br>
<h1 align="center">¿QUÉ ES GITHUB?</h1>

<p align="center">
Es una plataforma web para alojar proyectos que usan Git. Permite colaborar con otras personas, gestionar versiones de código y trabajar en equipo de forma eficiente.
</p>

---

## ¿Para qué sirve?
- **Alojar código:** Guardar proyectos en la nube de forma segura.
- **Colaborar:** Permite trabajar con otras personas en el mismo proyecto.
- **Control de versiones:** Lleva un historial de cambios y vuelve a versiones anteriores.
- **Ramas y fusiones:** Desarrollar nuevas funciones sin afectar el código principal.
- **Portafolio:** Mostrar los proyectos y contribuciones a los demás.

---

## Conceptos claves
- **Repositorio (Repo):** Es un proyecto que contiene todos los archivos y el historial de cambios.
- **Commit:** Es un *"guardado"* de los cambios realizados en el código.
- **Rama (Branch):** Es una línea de desarrollo independiente para trabajar en nuevas funciones o arreglos.
- **Pull Request (PR):** Es una solicitud para fusionar los cambios de una rama a otra (usualmente a main).
- **Merge:** Es unir los cambios de una rama a otra.
- **Issue:** Sirve para reportar errores, proponer mejoras o discutir tareas.

---

## Flujo de trabajo básico
1. **Clonar un repositorio:** Descarga una copia del repositorio a una computadora.
    ```Bash
    git clone https://github.com/usuario/repositorio.git
    ```

2. **Crear una rama:** Crea una rama nueva para trabajar.
    ```Bash
    git checkout -b mi-nueva-funcionalidad
    ```

3. **Hacer cambios:** Edita los archivos del proyecto.

4. **Agregar cambios (staging)** Prepara los cambios para el commit.
    ```Bash
    git add .
    ```

5. **Hacer commit:** Guarda los cambios con un mensaje.
    ```Bash
    git commit -m "mensaje descriptivo"
    ```

6. **Subir cambios (push):** Envía los cambios a Github.
    ```Bash
    got push origin mi-nueva-funcionalidad
    ```

7. **Abrir Pull Request:** Solicitar revisión y fusionar los cambios agregados.
> [!NOTE]
> En GitHub, para abrir un Pull Request se abre desde la rama que estas hacia main.

8. **Revisar y fusionar (merge):** Una vez aprobado, se fusiona la rama a main.
> [!NOTE]
> El código ahora forma parte del proyecto.

---

## ¿Cómo se ve en Github?
<div align="center">
  <img src="/imgs/repository-github.avif" width="600" alt="Repositorio en GitHub"/>
</div>

---

## Ramas: ejemplo visual
<div align="center">
  <img src="/imgs/branches.avif" width="600" alt="Ramas"/>
</div>

---

## Archivo README.md
Es la tarjeta de presentación de todo proyecto.<br>
Explica de qué trata y cómo usarlo.
<div align="center">
  <img src="/imgs/readme.avif" width="600" alt="README" />
</div>

---

## Comandos útiles de Git
- `git status:` Muestra el estado de los archivos.
- `git log:` Muestra el historial de commits.
- `git branch:` Lista las ramas existentes.
- `git checkout <rama>:` Cambia a otra rama.
- `git pull:` Descarga cambios del repositorio.

---

## Buenas prácticas
- ✅ Escribir commits claros y descriptivos.
- ✅ Trabajar en ramas para nuevas funciones.
- ✅ Mantener el repositorio organizado.
- ✅ Revisar el código antes de hacer merge.
- ✅ Actualizar la rama `main` con frecuencia

---

## ¿Dónde empezar?
1. Crear una cuenta en `github.com`
2. Crear un nuevo repositorio
3. Seguir el flujo de trabajo.
4. Colaborar y contruir nuevos proyectos.

---

## En resumen
GitHub + Git permiten colaborar, mantener un historial de cambios y construir mejores proyectos de software en equipo.
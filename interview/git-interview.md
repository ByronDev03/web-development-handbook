<h1 align="center">
PREGUNTAS PARA ENTREVISTA<br>
(VERSIÓN GIT)
</h1>

---

1. **¿Cuál es la diferencia entre git merge y git rebase?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>git merge</strong> combina dos ramas creando un nuevo commit de fusión, conservando el historial completo tal como ocurrió.</li>
    <li><strong>git rebase</strong> mueve tus commits para que parezca que se hicieron desde el punto más reciente de la otra rama, generando un historial más lineal y limpio.</li>
    </ul>

    ```Bash
    git merge feature-branch   # Conserva historial real, crea commit de merge
    git rebase main            # Reescribe historial, más lineal
    ```
    </details><br>

2. **¿Qué es un conflicto de merge y cómo se resuelve?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Ocurre cuando dos ramas <strong>modificaron la misma línea
   </strong> de un archivo de forma distinta, y Git no puede decidir cuál versión mantener. SE resuolve editando manualmente el archivo, eligiendo qué contenido conservar, y luego marcándolo como resuelto.</p>

    ```Bash
    # Git marca el conflicto asi en el archivo:
    <<<<<<< HEAD
    tu versión
    ======
    versión de la otra rama
    >>>>>>> feature-branch

    git add archivo.txt   # Después de resolver manualemnte
    git commit 
    ``` 
    </details><br>

3. **¿Qué diferencia hay entre git pull y git fetch?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>git fetch</strong> descarga los cambios del repositorio remoto, pero no los aplica a tu rama local, solo actualiza tu conocimiento de lo que hay en el remoto.</li>
    <li><strong>git pull</strong> hace lo mismo, pero además los fusiona automáticamente con tu rama actual.</li>
    </ul>

    ```Bash
    git fetch origin      # Descarga cambios, no los aplica
    git pull origin main  # Descarga y fusiona automáticamente
    ``` 
    </details><br>


4. **¿Qué es un .gitignore y por qué es importante?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es un archivo que le indica a Git qué archivos o carpetas debe<strong>ignorar y no rastrear</strong> (como archivos de configuración local, dependencias descargadas o credenciales). Evita que subas al repositorio archivos innecesarios o sensibles.</p>

    ```Bash
    # .gitignore
    target/
    .env
    *.log
    node_modules/
    ```
    </details><br>

5. **¿Qué es un branch (rama) y por qué se usan?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es una línea de desarrollo <strong>independiente</strong> dentro del repositorio que te permite trabajar en una funcionalidad o fix sin afectar el código principal (main) hasta que esté lista para integrarse.</p>

    ```Bash
    git branch feature-login       # Crea la rama
    git checkout feature-login     # Te mueves a ella
    git checkout -b feature-login  # Ambos pasos en uno
    ```
    </details><br>

6. **¿Qué diferencia hay entre git reset y git revert?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>git reset</strong> mueve el puntero de tu rama a un commit anterior, pusiendo eliminar commits del historial (peligroso si ya se compartió con otros).</li>
    <li><strong>git revert</strong> crea un nuevo commit que deshace los cambios de uno anterior, sin borrar el historial.</li>
    </ul>

    ```Bash
    git reset --hard HEAD-1     # Elimina el último commit por completo
    git revert HEAD             # Crea un commit nuevo que deshace el anterior
    ```

    <p align="justify">En ramas compartidas con el equipo, siempre es más seguro usar revert que reset.</p>
    </details><br>


7. **¿Qué es git stash y cuándo se usa?**
    <details>
    <summary>Solución</summary>
    <p align="justify"><strong>Guarda temporalmente</strong> los cambios no confirmados (sin hacer commit) para que puedas cambiar de rama sin perderlos ni tener que commitear algo incompleto.</p>
    </ul>

    ```Bash
    git stash           # Guarda los cambios pendientes
    git checkout main   # Cambios de rama limpio
    git stash pop       # Recuperas los cambios guardados
    ```
    </details><br>

8. **¿Qué diferencia hay entre HEAD, un commit y un branch?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Un <strong>commit</strong> es una "foto" del estado del código en un momento dado.</li>
    <li>Un <strong>branch</strong> es simplemente una etiqueta que apunta a un commit específico.</li>
    <li><strong>HEAD</strong> es un puntero que indica en qué branch (o commit) te encuentras parado actualmente.</li>
    </ul>

    <p align="justify">Cuando haces <strong>checkout</strong> a otro branch, en realidad estás moviendo dónde dónde apunta HEAD.</p>
    </details><br>

9. **¿Qué es un pull request (o merge request) y para qué sirve?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es una <strong>solicitud formal</strong> para fusionar los cambios de una rama hacia otra (normalmente hacia <strong>main</strong>), permitiendo que el equipo revise el código, deje comentarios y lo apruebe antes de integrarlo, evitando que cualquiera fusione cambios sin revisón.</p>
    <p align="justify">No es un comando de Git en sí, es una funcionalidad de plataforma como GitHub, GitLab o Bitbucket.</p>
    </details><br>

10. **¿Qué es un commit atómico y por qué se recomienda?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es un commit que <strong>representa un solo cambio</strong> lógico y completo (un fix, una funcionalidad específica), en vez de mezclar varios cambios no relacionados en un mismo commit.</p>
    <p align="justify">Facilita revisar el historial, revertir cambios puntuales y entender qué hizo cada commit sin ambigüedad.</p>

    ```Bash
    # ❌ Un commit mezclando todo
    git commit -m  # fix login, update readme, add tests"

    ✅ Commits atómicos, separados
    git commit -m "fix: corrige validación de login"
    git commit -m "docs: actualiza README"
    git commit -m "test: agrega test de login"
    ```
    </details><br>
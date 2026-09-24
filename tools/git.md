<h1 align="center">¿QUÉ ES GIT?</h1>

<p align="center">
Es un sistema de control de versiones distribuido. Permite registrar cambios en el código, volver a versiones anteriores, trabajar en equipo y gestionar proyectos de forma eficiente.
</p>

- **Historial:** Registra cada cambio realizado.
- **Colaboración:** Trabaja con otras personas fácilmente.
- **Seguridad:** Datos respaldados y confiables.
- **Rendimiento:** Ligero y rápido en operaciones.

---

## Conceptos clave
- **Repositorios (Repo):** Es el directorio donde Git guarda todo el historial del proyecto.
- **Commit:** Es una confirmación de cambios. Cada commit tiene un mensaje.
- **Rama (Branch):** Es una línea de desarrollo independiente.
- **Merge:** Es unir los cambios de una rama a otra.
- **Remote:** Es una versión del repositorio alojada en un servidor (ej. GitHub).
- **Clone:** Es una copia de un repositorio remoto en una máquina local.
- **Pull / Push:** Pull: trae cambios del remoto. Push: envía los cambios al remoto.

---

## Flujo de trabajo básico
1. **Modificar:** Editar archivos en el directorio de trabajo.
2. **Agregar:** Prepara los cambios para el commit.
3. **Commit:** Guardar los cambios en el repositorio local.
4. **Push:** Enviar los cambios al repositorio remoto.

---

## ¿Cómo funciona Git?
Git guarda la información como una serie de "instantáneas" de los proyectos. Cada vez que se hace un commit, almacena el estado de los archivos.

<div align="center">
  <img src="/imgs/work-git.avif" width="500" alt="¿Cómo funciona Git?" />
</div>

> [!IMPORTANT]
> Cada commit tiene un identificador único(SHA) forma un historial que se puede recorrer cuando lo necesites.

---

## Las 3 áreas de Git
<div align="center">
  <img src="/imgs/areas-git.avif" width="500" alt="¿Cómo funciona Git?" />
</div>

---

## Comandos básico de Git
| Comando                        | Descripción                           | 
| :---                           | :---                                  |   
| `git init`                     | Inicializa un nuevo repositorio Git.  |                        
| `git status`                   | Muestra el estado de los archivos.    | 
| `git add <archivo>`            | Agrega un archivo al área de staging. | 
| `git add .`                    | Agrega todos los cambios al staging.  | 
| `git commit -m "mensaje"`      | Guarda los cambios con un mensaje.    | 
| `git log`                      | Muestra el historial de commits.      | 
| `git branch`                   | Lista las ramas existentes.           | 
| `git branch <nombre>`          | Crea una nueva rama.                  | 
| `git checkout <rama>`          | Cambia a otra rama.                   | 
| `git merge <rama>`             | Fusiona la rama indicada a la actual. | 
| `git remote add origin <url>`  | Conecta un repo local con uno remoto. | 
| `git push origin <rama>`       | Envía los commits al remoto.          | 
| `git pull origin <rama>`       | Descarga cambios del remoto.          | 

---

## Buenas prácticas

- ✅ Hacer commits pequeños y con mensajes claros.
- ✅ Usar ramas para nuevas funcionalidades o arreglos.
- ✅ Sincronizar el código con frecuencia (pull & push).
- ✅ Revisa el código antes de hacer merge.
- ✅ No subir archivos innecesarios (usar .gitignore).

---

## Archivo .gitignore
Permite ignorar archivos o carpetas que no deben subirse al repositorio.
```Bash
# Ejemplos comunes
node_modules/
.env
*.log
dist/
.DS_Store
```

---

## Ramas (Branches)
<div align="center">
  <img src="/imgs/branches-git.avif" width="500" alt="¿Cómo funciona Git?" />
</div>

**Comando útiles**
- `git branch` → Lista las ramas.
- `git branch <nombre>` → Crea una nuevas rama.
- `git checkout <rama>` → Cambia de rama.
- `git merge <rama>` → Fusiona cambios de otra rama.
- `git branch -d <rama>` → Elimina una rama (ya fusionadas).

---

## En resumen
- ⭐ Git registra el historial de cambios del proyecto en el que se esta trabajando.
- ⭐ Permite trabajar en equipo sin sobrescribir el trabajo de otros.
- ⭐ Las rama ayudan a desarrollar nuevas ideas de forma segura.
- ⭐ Los comandos de Git dan el control total del código que se esta usando.

<h1 align="center">Git Commands Cheat Sheet</h1>

<p align="center">
Una referencia rápida de comandos esenciales de Git, organizados por categoría, con explicaciones y ejemplos.
</p>

---


## Inicialización

``` bash
git init                # Inicializa un nuevo repositorio Git.
git clone <repo-url>    # Clona un repositorio desde una URL.
```

---

## Desarrollo diario

``` bash
git status               # Muestra el estado de los cambios.
git add <archivo>        # Añade cambios al área de preparación.
git commit -m "Mensaje"  # Confirma los cambios con un mensaje.
```

---

## Gestión de ramas

``` bash
git branch                   # Lista las ramas.
git branch <nombre-rama>     # Crea una nueva rama.
git switch <nombre-rama>     # Cambia a una rama.
git branch -d <nombre-rama>  # Elimina una rama.
```

---

## Integración y colaboración

``` bash
git merge <rama>               # Fusiona los cambios de una rama.
git remote add <nombre> <url>  # Añade un repositorio remoto.
git push <remoto> <rama>       # Envía los cambios a un repositorio remoto.
git pull <remoto> <rama>       # Obtiene y fusiona cambios desde un repositorio remoto.
```

---

## Recuperación y limpieza

``` bash
git fetch                 # Recupera cambios sin fusionar.
git reset --hard HEAD     # Desecha todos los cambios locales.
git revert <hash-commit>  # Revierte los cambios de un commit.
```

---

## Avanzado y utilidades

``` bash
git diff <a> <b>          # Compara dos commits, ramas o archivos.
git show <hash>           # Muestra detalles de un commit.
git stash                 # Guarda cambios temporales y limpia el working tree.
git stash pop             # Restaura los cambios guardados del stash.
git cherry-pick <hash>    # Aplica un commit específico en la rama actual.
git rebase <base>         # Reaplica commits sobre otra base.
```
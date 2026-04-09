<h1 align="center">KANBAN</h1>

---

## ¿Qué es?
Un método ágil *visual* que usa tableros con columnas (ej. **"Por hacer** → **En progreso** → **Terminado"**).

---

## ¿Cómo funciona?
Cada tarea es una tarjeta que avanza en el tablero.

---

## Reglas importantes:
- Visualizar el flujo de trabajo.
- Limitar el número de tareas en progreso (WIP = Work In Progress).
- Mejorar continuamente.

---

## Ejemplo práctico:
- "Ticket nuevo" → "Atendiendo" → "Resuelto".
- Si hay más de 5 tickets en "Atendiendo", nadie toma uno nuevo hasta resolver los pendientes.

**NOTA:** Se busca flujo constante, menos bloqueos y menos tareas acumuladas.

---

## ¿Qué es un ticket?
Un ticket es básicamente una tarea que hay que realizar.
- Puede ser un bug (error que arreglar).
- Una mejora (agregar un botón nuevo).
- Una tarea de mantenimiento (actualizar librerías).

En Kanban cada tarea se convierte en un ticket individual que se mueve por el tablero:

**To Do** → **In Progress** → **Done**

---

## Ejemplo en la vida real
Imagina que trabajas en el soporte de una tienda online.
Un cliente manda un correo diciendo **"No puedo entrar a mi cuenta"**.
- El sistema de soporte genera un **ticket #21** con el titulo: **"Cliente no puede iniciar sesión"**.
- Ese ticket entra a la columna **To Do**.
- Un desarrollador lo toma, lo mueve a **In Progress**.
- Cuando lo arregla, pasa a **Done**.

El ticket es como un *"papelito"* o *"nota digital"* que representa esa tarea específica que viaja por el tablero hasta terminarse.

**Ticket #21 - Error al inicar sesión**

- **Título:** Cliente no puede iniciar sesión en su cuenta.
- **Descripción:** El cliente reporta que al ingresar su correo y contraseña aparece el mensaje *"usuario no encontrado"*, aunque la cuenta existe en la base de datos.
- **Prioridad:** 🔴 Alta
- **Estado Actual:** To Do
- **Asignado a:** Juan Pérez (Desarrollador Backend)
- **Fecha de Creación:** 10/03/2026
- **Fecha Límite:** 12/03/2026

**Checklist dentro del ticket:**
- [  ] Revisar logs de autenticación.
- [  ] Verificar conexión con base de datos.
- [  ] Probar flujo de login con cuentas de prueba.
- [  ] Subir fix al repositorio.

**Comentarios:**
- **Soporte:** "Cliente afectado: ID-1234, email: cliente@ejemplo.com"
- **Desarrollador:** "Ya revisé logs y encontré error en la validación del token".

**Este ticket pasaríapor las columnas de Kanban así:**
- **To Do:** Recién creado, nadie lo toca aún.
- **In Progress:** Juan lo empieza a trabajar.
- **Done:** El bug se corrige y se despliega la solución.

**NOTA:**
- Cada ticket suele tener un ID, un título y detalles (quién lo reporto, prioridad, fecha, etc).
- Se pueden añadir comentarios, adjuntar imágenes o marcar checklist dentro del ticket.

---

## Diferencia clave:
- **SCRUM:** Trabaja en *bloques de tiempo (sprints)* → ideal para proyectos ccon entregas incrementales.
- **KANBAN:** Trabaja en *flujo continuo* → ideal para soporte, mantenimiento o entornos cambiantes.

---

## Demostración de SCRUM y KANBAN
<div align="center">
  <img src="imgs/scrum-kanban.png" width="600" alt="Demostración de SCRUM y KANBAN"/>
</div>
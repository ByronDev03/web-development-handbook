<h1 align="center">SCRUM</h1>

---

## ¿Qué es?
Es un *marco de trabajo ágil* para desarrollar proyectos complejos (software, marketing, etc).

---

## ¿Cómo funciona?
Se organiza el trabajo en ciclos cortos llamadas *sprints* (normalmente de 2 a 4 semanas).

---

## Roles principales
- **Prooduct Owner (PO):** Prioriza qué se debe hacer.
- **Scrum Master:** Guía al equipo, elimina obstáculos.
- **Equipo de desarrollo:** Construye el producto.

---

## Eventos clave:
- **Sprint Planning:** Planificación del sprint. 
- **Daily Scrum:** Reunión diaria de 15 min.
- **Sprint Review:** Revisar el resultado del sprint.
- **Sprint Retrospective:** Analizar cómo mejorar.

---

## ¿Qué es un Sprint?
Es un periodo corto de tiempo en Scrum donde el equipo trabaja para completar un conjunto específico de tareas o funcionalidades del proyecto.

Normalmente dura entre 1 y 4 semanas, aunque lo más común son 2 semanas.

**Explicación simple**

Un Sprint es como decir:

*“Durante las próximas 2 semanas vamos a trabajar solo en estas tareas y al final debemos tener algo funcionando”.*

Es decir, es un ciclo de trabajo con inicio y fin definidos.

---

## Ejemplo práctico
Imagina que tu equipo está desarrollando una tienda online de ropa.

Antes del sprint hay un **Product Backlog** (lista de todas las tareas posibles).
| ID | Historia de usuario                    | Prioridad |
| -- | -------------------------------------- | --------- |
| 1  | Como usuario quiero iniciar sesión     | Alta      |
| 2  | Como usuario quiero ver productos      | Alta      |
| 3  | Como usuario quiero agregar al carrito | Alta      |
| 4  | Como usuario quiero pagar con tarjeta  | Media     |
| 5  | Como usuario quiero ver mis pedidos    | Baja      |

---

## Sprint Planning
El equipo decide qué tareas sí puede completar en este sprint.

Supongamos que el sprint dura 2 semanas.
**Sprint 1 Backlog**
| Sprint   | Tarea                | Desarrollador |
| -------- | -------------------- | ------------- |
| Sprint 1 | Login                | Ana           |
| Sprint 1 | Listado de productos | Carlos        |
| Sprint 1 | Carrito de compras   | Luis          |

Estas tareas son las historias de usuario del sprint.

---

## Ejemplo de Historia de Usuario (Ticket Scrum)

Una historia realista de Scrum se ve así:

**Historia de usuario**

**ID:** US-01
**Título:** Sistema de Login

Como usuario
Quiero iniciar sesión con mi correo y contraseña
Para poder acceder a mi cuenta.

**Criterios de aceptación**
- El usuario puede ingresar email y contraseña.
- El sistema valida credenciales.
- Si los datos son incorrectos aparece error.
- Si son correctos redirige al dashboard.

**Tareas técnicas dentro del Sprint**
1. Crear formulario de login
2. Crear API `/login`
3. Validar credenciales en backend
4. Manejar errores de autenticación

---


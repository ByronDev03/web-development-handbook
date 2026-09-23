<h1 align="center">¿QUÉ ES UN ORM?</h1>

<p align="center">
Permite trabajar con una base de datos utilizando objetos y código en lugar de escribir todo el SQL manualmente.
</p>

---

## ¿Qué es un ORM?
Un ORM (Object Relational Mapping) es una técnica de programación que convierte datos entre sistemas incompatibles utilizando un lenguaje orientado a objetos.

- **Menos SQL manual:** Evita escribir consultas SQL complejas y repetitivas.
- **Más productividad:** Permite enfocarte en la lógica de negocio.
- **Menos errores:** Reduce errores comunes en consultas SQL.
- **Portabilidad:** Cambia de base de datos con menos esfuerzo.
- **Mantenible:** Código más limpio, legible y fácil de matener.

---

## ¿Cómo funciona?
1. **Definir modelo:**  Se representan las tablas de la base de datos como clases u objetos.
    ```Bash
    class Usuario {
        id:      number
        nombre:  string
        email:   string
    }
    ```

2. **Usar el ORM:** Interactúas con los datos usando métodos del ORM, no SQL directo.
    ```Bash
    const usuario = await Usuario
        .findUnique({
            where: { id: 1 }
        })
    ```

3. **El ORM traduce:** El ORM convierte tu código en cosnultas SQL optimizadas.
    ```SQL
    SELECT * 
    FROM usuarios
    WHERE id = 1;
    ```

4. **Se obtienen los resultados:** El ORM convierte el resultado de la consulta en objetos del lenguaje que se esta usando.
    ```Bash
    Usuario {
        id: 1,
        nombre: "Ana",
        email: "ana@ej.com"
    }
    ```

<div align="center">
  <img src="/imgs/work-orm.avif" width="600" alt="¿Cómo funciona un ORM?" />
</div>

---

## ORM populares
- <img src="https://cdn.simpleicons.org/prisma/ffffff" width="20"/> Prisma
- <img src="https://cdn.simpleicons.org/typeorm" width="20"/> TypeORM
- <img src="https://cdn.simpleicons.org/sequelize" width="20"/> Sequelize
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/hibernate/hibernate-original.svg" width="20"/> Hibernate
- Entity Framework

---

## Ejemplo práctico con Prisma
**Modelo (schema.prisma)**
```Bash
model Usuario {
    id        Int         @id @default(autoincrement())
    nombre    String   
    email     String      @unique
    creadoEn  DateTime    @default(now())
}
```

**Uso en código (TypeScript)**
```TypeScript
// Crear usuario
await prisma.usuario.create({
    data: {
        nombre: "Ana",
        email: "ana@ej.com"
    }
})

// Obtener usuario
const usuario = await prisma.usuario.findUnique({
    where: { id: 1 }
})

// Actualizar usuario
await prisma.usuario.update({
    where: { id: 1 },
    data: { nombre: "Ana Gómez" }
})

// Eliminar usuario
await prisma.usuario.delete({
    where: { id: 1 }
})

```

---

## SQL manual vs ORM
- **Con SQL manual**
    ```SQL
    SELECT u.id, u.nombre, u.email 
    FROM usuarios u
    WHERE u.email = 'anaej.com';
    ```

    - ❌ Se escribe más código
    - ❌ Más propenso a errores
    - ❌ Difícil de mantener
    - ❌ Menos portátil

- **Con ORM**
    ```Bash
    const usuario = await Usuario
      .findUnique({
        where: { email: 'ana@ej.com' }
      })
    ```

    - ✅ Menos código
    - ✅ Menos errores
    - ✅ Facil de mantener
    - ✅ Más portátil

---

## ¿Cuándo usar un ORM?
- **Proyectos medianos y grandes:** Mejora la productividad del equipo.
- **Equipos con diferentes niveles de SQL:** Permite a todos trabajar sin ser expertos en SQL.
- **Desarrollo ágil:** Itera más rapido y enfócate en la lógica de negocio.
- **Bases de datos relacionales:** Ideal para MySQL, PostgreSQL, SQL Server, etc.


---

## Ventajas
- ✅ Productividad
- ✅ Seguridad (menos inyección SQL)
- ✅ Abstracción de la BD
- ✅ Consultas más legibles
- ✅ Relaciones entre modelos
- ✅ Migraciones y seeders
- ✅ Comunidad y soporte

---

## Tener en cuenta 
- ⚠️ Puede ocultar lo que ocurre por debajo.
- ⚠️ Menos control en consultas muy complejas.
- ⚠️ Curva de aprendizaje inicial.
- ⚠️ No siempre es la mejor opción para proyectos muy pequeños.

---

## En resumen
Un ORM actúa como un puente entre tu aplicación y la base de datos, permitiendo trabajar con datos de forma más eficiente, segura y productiva.
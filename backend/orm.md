<h1 align="center">¿QUÉ ES UN ORM?</h1>

<p align="center">
Permite trabajar con una base de datos utilizando objetos y código en lugar de escribir todo el SQL manualmente.
</p>

---

## ¿Qué es un ORM?
Un ORM (Object Relational Mapping) es una técnica de programación que convierte datos entre sistemas incompatibles utilizando un lenguaje orientado a objetos.

---

## ¿Cómo funciona?


---

## ORM populares
- Prisma
- TypeORM
- Sequelize
- Hibernate
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


---

## ¿Cuándo usar un ORM?
- 
-
- 
-


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
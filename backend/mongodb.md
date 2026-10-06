<h1 align="center">¿QUÉ ES MONGODB?</h1>

<p align="center">
Almacena información en documentos flexibles en lugar de las tradicionales filas y columnas.
</p>

---

## ¿Qué es MongoDB?
Es una base de datos NoSQL orientada a documentos, diseñada para ser escalable, flexible y fácil de usar.
Guarda los datos en documentos similares a JSON en lugar de tablas y filas.

- **Esquema flexible:** Cada documento puede tener campos diferentes.
- **Escalable:** Escala horizontalmente de forma sencilla.
- **Alto rendimiento:** Optimizado para grandes volúmnes de datos.
- **Open Source:** Código abierto y con una gran comunidad.

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/mongodb1.avif" width="600" alt="¿Cómo funciona?" />
</div>

**¿Qué sucede por dentro?**
1. La aplicación envía una consulta (CRUD: Crear, Leer, Actualizar, Eliminar).
2. MongoDB interpreta y ejecuta la consulta.
3. Busca los documentos en la colección correspondiente.
4. Devuelve los resultados en formato JSON/BSON.

- **Consultas rápidas**
- **Documentos JSON/BSON**
- **índices optmizados**
- **Sharding (escalabilidad)**
- **Replica Set (alta disponibilidad)**

---

## Características clave
- **Modelo de documentos:** Almacena datos en documentos BSON (similar a JSON).
- **Esquema flexible:** No requiere estructura fija. Cada documento es único.
- **Consultas potentes:** Lenguaje de consulta rico y flexible.
- **Índices:** Mejora el rendimiento de las consultas.
- **Escalabilidad horizontal:** Con sharding puedes distribuir datos en múltiples servidores.
- **Alta disponibilidad:** Replica sets para tolerancia a fallos.

---

## Ejemplo de documento (JSON)
```JSON
{
  "_id": ObjectId("6649c1..."),
  "nombre": "Ana Pérez",
  "email": "ana@example.com",
  "edad": 28,
  "roles": ["admin", "editor"],
  "activo": true,
  "dirección": {
    "ciudad": "Morelos",
    "país": "México"
  },
  "creado_en": ISODate("2026-10-05T10:00:003")
}
```

---

## Ejemplo: consulta

**Obtener todos los usuarios activos:**
```Bash
db.usuarios.find({activo: true})
```

**Actualizar un documento**
```Bash
db.usuarios.updateOne(
  { _id: ObjectId("6649c1...") },
  { $set: { edad: 29 } },
)
```

**Eliminar un documento:**
```Bash
db.usuarios.deleteOne({
  { _id: ObjectId("6649c1...") })
```

---

## Estructura: Base de datos
<div align="center">
  <img src="/imgs/mongodb2.avif" width="600" alt="Estructura MongoDB" />
</div>

---

## MongoDB Compass
Herramienta oficial de MongoDB para explorar, visualizar y administrar datos de forma sencilla y gráfica.
<div align="center">
  <img src="/imgs/mongodb3.avif" width="600" alt="MongoDB Compass" />
</div>

---

## Casos de uso
- Aplicaciones Web y Móviles
- Catálogos de productos
- Gestión de contenido (CMS)
- IoT y Big Data
- Logs y analítica en tiempo real

---

## Ventajas
- ✅ Muy flexible
- ✅ Desarrollo más rápido
- ✅ Escala fácilmente
- ✅ Gran comunidad
- ✅ Integración nativa con JSON

---

## ¿Dónde se usa?
- 
- 
- 
- 
-
-
- y muchas más...

---

## En resumen
MongoDB es una base de datos NoSQL orientada a documentos que te permite guardar datos de forma flexible, escalar fácilmente y desarrollar aplicaciones modernas de manera más rápida y eficiente.
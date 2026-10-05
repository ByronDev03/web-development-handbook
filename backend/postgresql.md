<h1 align="center">¿QUÉ ES POSTGRESQL?</h1>

<p align="center">
Una de las bases de datos relacionales más utilizadas para construir aplicaciones modernas.
</p>

---

## ¿Qué es PostgreSQL?
Es un sistema de gestión de bases de datos relacional, robusto, confiable y de código abierto. Soporta SQL, ACID, integridad referencial y muchas características avanzadas.

- **Confiable y robusto:** Diseñado para la integridad y la durabilidad de los datos.
- **Alto rendimiento:** Optimizado para cargas de trabajo complejas y grandes volúmenes.
- **Extensible:** Permite agregar funciones, tipos de datos y operadores propios.
- **Comunidad activa:** Miles de contribuidores en todo el mundo.

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/postgresql1.avif" width="600" alt="Diagrama endpoint" />
</div>

**¿Qué sucede por dentro?**
1. El servidor recibe y analiza la consulta SQL.
2. El optimizador de consultas elige el mejor plan de ejecución.
3. El motor de almacenamiento lee o escribe los datos en disco.
4. Los resultados son devueltos al cliente.

- **ACID:** Transacciones seguras
- **Índices:** Búsquedas rápidas
- **Claves foráneas:** Integridad referencial
- **Vistas:** Consultas simplificadas
- **Funciones:** Lógica del lado de la base de datos

---

## Características destacadas
- **SQL Completo:** Soporta la mayoría de características del estándar SQL.
- **Tipos de datos avanzados:** JSONB, Array, UUID, HSTORE, rangos, geometría y más.
- **Extensiones:** PostGIS, pgTrgm, hstore, citext, entre muchas otras.
- **Seguridad:** Roles, permisos granulares, cifrado y autenticación avanzada.
- **Replicación:** Replica tus datos para alta disponibilidad y escalabilidad.
- **Copias de seguridad:** Herramientas integradas para respaldos y recuperación.

---

## Ejemplo: Crear tabla y consultar
```sql
CREATE TABLE usuarios (
    id        SERIAL        PRIMARY KEY,
    nombre    VARCHAR(100)  NOT NULL,
    email     VARCHAR(100)  UNIQUE,
    creado_en TIMESTAMP     DEFAULT NOW()
);

-- Insertar datos
INSERT INTO usuarios (nombre, email)
VALUES ('Ana Perez', 'ana@email.com');

-- Consultar datos
SELECT id, nombre, email
FROM usuarios;

```

## Tipos de datos populares
- **INTEGER:** Números enteros
- **VARCHAR(n):** Cadenas de texto 
- **TEXT:** Texto Largo
- **BOOLEAN:** Verdadero / Falso
- **TIMESTAMP:** Fecha y hora
- **JSONB:** Datos JSON (binario)
- **UUID:** Identificador único
- **ARRAY:** Arreglos de valores

---

## Ejemplo: JSONB
```sql
CREATE TABLE productos (
  id        SERIAL PRIMARY KEY,
  nombre    TEXT,
  atributos JSONB
);
INSERT INTO productos (nombre, atributos)
VALUE (
  'Laptop',
  '{"marca": "Dell", "ram": "16GB", 
    "almacenamiento": "512 GB SSD"}'
);

-- Consultar por un atributo JSON
SELECT * FROM productos
WHERE atributos->>'marca' = 'Dell';

```

---

## Herramientas ecosistema
- **pgAdmin:** Interfaz gráfica para administrar las bases de datos.
- **psql:** CLI oficial para interactuar con PostgreSQL.
- **Docker:** Ejecuta PostgreSQL fácilmente en contenedores.
- **ORMs:** Compatible con cualquier ORM: *Prisma, TypeORM, Sequelize, etc.*

---

## Casos de uso
- Aplicaciones Web y Móviles
- Sistemas Financieros
- Análisis de Datos y BI
- IoT y Big Data
- GIS (con PostGIS)

---

## Ventajas
- ✅ 100% Open Source
- ✅ Confiable y probado en producción
- ✅ Muy escalable
- ✅ Comunidad y documentación excelentes
- ✅ Actualización constantes

---

## ¿Dónde se usa?
- <img src="https://cdn.simpleicons.org/instagram" width="20"/> Instagram
- <img src="https://cdn.simpleicons.org/spotify" width="20"/> Spotify
- <img src="https://cdn.simpleicons.org/youtube" width="20"/> YouTube
- <img src="https://cdn.simpleicons.org/reddit" width="20"/> Reddit
- <img src="https://cdn.simpleicons.org/airbnb" width="20"/> Airbnb
- <img src="https://cdn.simpleicons.org/discord" width="20"/> Discord
- y muchas más...

--- 

## En resumen
PostgreSQL es una base de datos potente, flexible y de código abierto que te brinda seguridad, escalabilidad y características avanzadas para construir aplicaciones modernas y de misión crítica.

---
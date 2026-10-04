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


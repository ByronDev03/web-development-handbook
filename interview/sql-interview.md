<h1 align="center">
PREGUNTAS PARA ENTREVISTA JUNIOR-MID<br>
(VERSIÓN SQL)
</h1>

---

1. **¿Cuál es la diferencia entre INNER JOIN, LEFT JOIN y RIGHT JOIN?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>INNER JOIN</strong> devuelve solo las filas que coinciden en ambas tablas.</li>
    <li><strong>LEFT JOIN</strong> devuelve todas las filas de la tabla izquierda, aunque no haya coincidencia en la derecha (con NULL en esos campos).</li>
    <li><strong>RIGHT JOIN</strong> hace lo mismo pero priorizando la tabla derecha.</li>
    </ul>

    ```sql
    SELECT u.nombre, p.total
    FROM usuarios u
    LEFT JOIN pedidos p ON u.id = p.usuario_id;
    -- Trae TODOS los usuarios, tengan o no pedidos
    ```
    </details><br>

2. **¿Qué diferencia hay entre WHERE y HAVING?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>WHERE</strong> filtra filas antes de agrupar.</li>
    <li><strong>HAVING</strong> filtra después de aplicar.</li>
    <li><strong>GROUP BY</strong> filtra sobre los resultados ya agregados.</li>
    </ul>

    ```sql
    SELECT departamento, COUNT(*) AS total
    FROM empleados
    WHERE activo = true           -- Filtra ANTES de agrupar
    GROUP BY departamento
    HAVING COUNT(*) > 5;          -- Filtra DESPUÉS de agrupar
    ``` 
    </details><br>

3. **¿Qué es una clave clave primaria (Primary Key) y una foránea (Foreign Key)?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Una <strong>clave primaria</strong> identifica de forma única cada fila de una tabla, no puede repetirse ni ser nula.</li>
    <li>Una <strong>clave foránea</strong> es un campo que referenci la clave primaria de otra tabla, estableciendo una relación entre ambas.</li>
    </ul>

    ```sql 
    CREATE TABLE pedidos (
        id          INT PRIMARY KEY,
        usuario_id  INT REFERENCES usuarios(id)  -- Foreign Key
    );
    ``` 
    </details><br>


4. **¿Qué hace GROUP BY y qué funciones de agregación existen?**
    <details>
    <summary>Solución</summary>
    <p align="justify"><strong>GROUP BY</strong> agrupa filas que comparten un valor en común para aplicarles funciones de agregación como <strong> COUNT(), SUM(), AVG(), MAX(), MIN().</strong></p>

    ```sql 
    SELECT departamento, AVG(salario) AS promedio
    FROM empelados
    GROUP BY departamento;
    ```
    </details><br>

5. **¿Qué es una subquery (subconsulta)?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es una <strong>consulta anidada</strong> dentro de otra consulta, usada como si fuera un valor o una tabla temporal.</p>

    ```sql 
    SELECT departamento FROM empleados
    WHERE salario > (
        SELECT AVG(salario) FROM empleados
    ); -- Empleados con salario sobre el promedio
    ```
    </details><br>

6. **¿Qué es la normalización de una base de datos?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es el <strong>proceso</strong> de organizar los datos para <strong>para reducir redundancia y evitar inconsistencias,</strong> dividiendo la información en tablas relacionadas en vez de repetirla en un solo lugar.</p>
    <ul>
    <li><strong>Ejemplo:</strong> en vez de repetir el nombre de un cliente en cada pedido, guardas su ID y lo relacionas con una tabla clientes aparte.</li>
    </ul>
    </details><br>

7. **¿Cuál es la diferencia entre DELETE, TRUNCATE y DROP?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>DELETE</strong> elimina filas específicas (se puede revertir con rollback, y se puede filtrar con WHERE).</li>
    <li><strong>TRUNCATE</strong> elimina todas las filas de una tabla de golpe, más rápido, pero sin poder filtrar.</li>
    <li><strong>DROP</strong> elimina la tabla completa, estructura incluida.</li>
    </ul>

    ```sql
    DELETE FROM usuarios WHERE activo = false;     -- Filas específicas
    TRUNCATE TABLE logs;                           -- Todas las filas, tabla se mantiene 
    DROP TABLE logs_antiguos;                      -- Elimina la tabla completa
    ```
    </details><br>

8. **¿Qué es un índice y para qué sirve?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Es una <strong>estructura que acelera</strong>  las búsquedas en una tabla, similar al índice de un libro: en vez de revisar fila por fila, la base de datos "salta" directo a donde está el dato.</p>

    ```sql 
    CREATE INDEX idx_email ON usuarios(email);
    -- Búsquedas por email serán mucho más rápidas
    ```
    </details><br>

9. **¿Cuál es la diferencia entre UNION y UNION ALL?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Ambos <strong>combinan</strong> los resultados de dos consultas.</p>
    <ul>
    <li><strong>UNION ALL</strong> elimina filas duplicadas automáticamente.</li>
    <li><strong>UNION ALL</strong> las mantiene todas, sin filtrar, por lo que es más rápido.</li> 
    </ul>
    
    ```sql 
    SELECT nombre clientes_2024
    UNION ALL
    SELECT nombre FROM clientes_2025;     -- Mantiene duplicados
    ```
    </details><br>

10. **¿Qué es una transacción y qué significa ACID?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Una <strong>transacción</strong> agrupa varias operaciones para que se ejecuten todas o ninguna.</p>
    <p align="justify"><strong>ACID</strong> son las 4 propiedades que garantizan su confiabilidad:</p>
    <ul>
    <li><strong>Atomicidad:</strong> todo o nada.</li>
    <li><strong>Consistencia:</strong> la BD pasa de un estado válido a otro</li> 
    <li><strong>Aislamiento (Isolation):</strong> transacciones no interfieren entre sí.</li>
    <li><strong>Durabilidad:</strong> una vez confirmada, el cambio persiste aunque el sistema falle.</li>
    </ul>
    </details><br>
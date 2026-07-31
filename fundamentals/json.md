<h1 align="center">JAVASCRIPT OBJECT NOTATION (JSON)</h1>

---

## ¿Qué es JSON?
JSON significa **JavaScript Object Notation** (Notación de Objetos de JavaScript). Es un **formato ligero de intercambio de datos**, que es fácil de leer para los humanos y fácil de analizar para las computadoras. Aunque viene de JavaScript, hoy en día se usa en casi todos los lenguajes de programación.

Se usa mucho para **enviar datos entre un cliente (por ejemplo, un navegador) y un servidor**, o para guardar configuraciones.

---

## Estrcutura Básica
Un JSON se basa en **dos estructuras principales:**
1. **Objeto:** Colecciones de pares **claves-valor**, delimitadas por `{}`.
    - Ejemplo:
        ```Bash
        {
            "nombre": "Byron",
            "edad": 23,
            "activo": true
        }
        ```
        - **"nombre"** es la clave, **"Byron"** es el valor.
        - Los valores pueden ser: **números, cadenas, booleanos, nulos, objetos o arreglos**.

2. **Arreglos (Arrays):** Listas de valores delimitadas por `[]`.
    - Ejemplo:
        ```Bash
        [
            "Manzana",
            "Pera",
            "Plátano"
        ]
        ```

Los objetos y arreglos pueden **anidarse:**
- Ejemplo: 
    ```Bash
    {
        "usuario": {
            "nombre": "Byron",
            "edad": 23
        },
        "hobbies": ["futbol", "lectura", "programación"]
    }
    ```
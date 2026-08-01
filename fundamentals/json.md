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

---

## Reglas Importantes
- Las **claves siempre deben ir entre comillas dobles `" "`**.
- Los valores pueden ser:
    - **Número:** 42, 3.14
    - **Cadena de texto:** "Hola Mundo"
    - **Booleano:** true o false
    - **Nulo:** null
    - **Objeto:** {"clave":"valor"}
    - **Arreglo:** [1, 2, 3]
- No se permiten **comentarios** en JSON (a diferencia de otros formatos como YAML).

----

## ¿Para qué se usa JSON?
- Intercambio de datos entre **frontend** y **backend.**
- Guardar configuraciones de aplicaciones.
- APIs modernas devuelven datos en JSON casi siempre.
- Serialización de datos: convertir un objeto de un lenguaje a texto JSON para enviarlo o almacenarlo.

---

## Ejemplo Práctico
Supongamos que quieres guardar información de varios usuarios:
```Bash
[
    {
        "nombre": "Byron",
        "edad": 25,
        "activo": true   
    },
    {
        "nombre": "Ana",
        "edad": 30,
        "activo": false  
    }
]
```
Aqui tenemos un **arreglo de objetos**, cada uno representando un usuario.

---

## Nota Importante
- JSON solo **almacena datos.**
- Necesitas un lenguaje que lo lea y haga algo  con esos datos.

---

## Entonces...
La función principal de un JSON es **almacenar y transmitir datos de manera estructurada y legible,** no ejecutar acciones por sí mismo.
Dicho de otra forma: **JSON es un formato de datos, no un programa.**

**Se resume así:**
1. **Intercambio de datos:** JSON se usa para **enviar información entre sistemas,** por ejemplo:
    - Un navegador y un servidor y un servidor web (frontend⭤ backend).
    - Diferentes servicios o APIs entre sí.

**Ejemplo:** Una app de clima pide los datos al servidor y recibe:
```Bash
{
    "ciudad": "Ciudad de México",
    "temperatura": 25°,
    "condición": "soleado"
}
```
El servidor envía datos y la aplicación los interpreta para mostrar la información al usuario.

2. **Almacenamiento de datos:** Se puede usar para **guardar información de manera organizada,** como:
    - Configuración de una app.
    - Datos de usuarios. 
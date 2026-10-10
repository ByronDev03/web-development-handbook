<h1 align="center">
PREGUNTAS PARA ENTREVISTA JUNIOR<br>
(VERSIÓN JAVA)
</h1>

---

1. **¿Cuál es la última versión de Java?**
    <details>
    <summary>Solución</summary>
    <p align="justify">A diciembre de 2025, la última versión estable es JDK 25.</p>
    </details><br>

2. **¿Qué diferencia hay entre JDK y JRE?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>JDK (Java Development Kit):</strong> Herramienta para desarrollar y ejecutar aplicaciones en Java.</li>
    <li><strong>JRE (Java Runtime Environment):</strong> Herramienta SOLO para ejecutar aplicaciones en Java, pero no trae las herramientas de desarrollo.</li>
    </ul>
    </details><br>

3. **¿Cuál es el proyecto más completo que hiciste? ¿Por qué? ¿Qué tecnologías usaste?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Esta pregunta busca evaluar tu experiencia práctica, cómo resuelves problemas y qué tecnologías dominas. Siempre cuenta EL PROBLEMA que resolvía el proyecto, qué hacía exactamente y qué tecnologías usaste.</p>
    </details><br>

4. **¿Qué diferencia hay entre programación funcional e imperativa?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>La <strong>programación imperativa</strong> es el estilo más clásico y tradicional. En este enfoque, el programador le indica a la computadora exactamente qué
    pasos debe seguir para llegar a un resultado. Es como dar una receta paso a paso.</li>
    <li>La <strong>programación funcional</strong> se centra más en describir qué se quiere lograr, en lugar de detallar cómo hacerlo paso a paso (trabajando más con
    funciones puras). Podríamos compararlo con pedir un servicio que se encargue del trabajo: no te preocupas por los pasos intermedios, solo dices
    qué resultado buscas.</li>
    </ul>
    </details><br>

5. **En POO: ¿Cuál es la diferencia entre interfaz y clase abstracta?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Una <strong>interfaz</strong> es un tipo "especial" de clase que establece qué métodos puede implementar una clase sin especificar el código de su lógica interna.</li>
    <li>Una <strong>clase abstracta</strong> es un punto intermedio entre una interfaz y una clase común. No se puede instanciar directamente, pero sí puede contener tanto
    métodos abstractos (sin código) como métodos ya implementados.</li>
    </ul>
    </details><br>

6. **¿A partir de qué versión de Java se implementó la programación funcional?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Desde Java 8 (2014) se incorporaron expresiones lambda, interfaces funcionales y Streams, dando inicio al paradigma funcional en Java.</p>
    </details><br>

7. **¿Cuáles son las propiedades de la POO?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Las 4 propiedades principales son Abstracción, Encapsulamiento, Herencia y Polimorfismo.</p>
    <p align="justify"><strong>Ejemplo:</strong></p>
    <ul>
    <li><strong>Encapsulamiento:</strong> ocultar atributos y acceder a ellos solo con getters/setters.</li>
    <li><strong>Herencia:</strong> una clase hija puede reutilizar el código de la clase padre.</li> 
    </ul>
    </details><br>

8. **¿Qué diferencia hay entre Spring y Spring Boot?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>Spring:</strong> es un framework extenso para aplicaciones Java.</li>
    <li><strong>Spring Boot:</strong> simplifica Spring, permitiendo crear apps con menos configuración, usando starters y servidor embebido.</li>
    </ul>
    </details><br>

9. **Diferencia HashMap de LinkedList**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>HashMap:</strong> almacena pares clave-valor, ideal para búsquedas rápidas. Ej: guardar usuarios por nro de cliente.</li>
    <li><strong>LinkedList:</strong> lista doblemente enlazada, buena para insertar/eliminar elementos. Ej: cola de atención de clientes.</li>
    </ul>
    </details><br>

10. **¿Cómo puedes hacer pruebas en un BACKEND si no tienes un FRONTEND?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Puedes usar herramientas como Postman, cURL o armar pruebas automatizadas con JUnit + MockMVC, enviando requests al backend y validando las respuestas sin necesidad de un frontend.</p>
    </details><br>

11. **¿Qué diferencias hay entre una clase y un objeto?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li>Una <strong>clase</strong> es el molde o plantilla que define cómo serán los objetos (sus atributos o características y métodos o comportamientos).</li>
    <li>Un <strong>objeto</strong> es una instancia concreta de esa clase, es decir, a partir de ese molde creamos un objeto que tiene "esa forma" y la guardamos en memoria.</li>
    </ul>
    </details><br>

12. **¿Conoces la diferencia entre MONOLITO y MICROSERVICIO?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>Monolito:</strong> toda la app funciona como un único bloque; si algo falla, puede afectar a todo el sistema.</li>
    <li><strong>Microservicio:</strong> la app se divide en módulos independientes (servicios) que se comunican entre sí, facilitando el mantenimiento y la escalabilidad. 
    Si uno deja de funcionar, generalmente no afecta a los otros.</li>
    </ul>
    </details><br>

13. **¿Qué es una annotation? Da un ejemplo de uso**
    <details>
    <summary>Solución</summary>
    <p align="justify">Una <strong>annotation</strong> es una forma de agregar "info extra" o etiquetas al código para indicar comportamientos especiales al compilador o framework.</p>
    <p align="justify"><strong>Ejemplo:</strong></p>
    <ul>
    <li>Override indica que un método está sobrescribiendo otro de su clase padre.</li>
    </ul>
    </details><br>

14. **¿Qué diferencia hay entre Hibernate y JPA?** **¿Son lo mismo?**
    <details>
    <summary>Solución</summary>
    <ul>
    <li><strong>JPA</strong> es un ORM, especificación o tecnología para utilizar bases de datos en Java (es quien establece ciertas reglas).</li>
    <li><strong>Hibernate</strong> es una implementación de JPA (básicamente una forma de hacerlo funcionar).</li>
    <li>En resumen: JPA dice qué hacer, Hibernate lo hace.</li>
    </ul>
    </details><br>

15. **¿Qué es un endpoint en una API?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Un <strong>endpoint</strong> es una URL específica donde una API recibe y responde peticiones/requests.</p>
    <p align="justify"><strong>Ejemplo:</strong></p>
    <ul>
    <li><strong>GET</strong> /api/usuarios devuelve la lista de usuarios desde el servidor.</li>
    </ul>
    </details><br>
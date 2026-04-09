<h1 align="center">
PREGUNTAS PARA ENTREVISTA JUNIOR<br>
(VERSIÓN JAVA)
</h1>

---

1. **¿Cuál es la última versión de Java?**
A diciembre de 2025, la última versión estable es JDK 25.

2. **¿Qué diferencia hay entre JDK y JRE?**
    - ***JDK (Java Development Kit):*** Herramienta para desarrollar y ejecutar
      aplicaciones en Java.
    - ***JRE (Java Runtime Environment):*** Herramienta SOLO para ejecutar
      aplicaciones en Java, pero no trae las herramientas de desarrollo.

3. **¿Cuál es el proyecto más completo que hiciste? ¿Por qué? ¿Qué tecnologías usaste?**
Esta pregunta busca evaluar tu experiencia práctica, cómo resuelves problemas y qué tecnologías dominas. Siempre cuenta EL PROBLEMA que resolvía el proyecto, qué hacía exactamente y qué tecnologías usaste.

4. **¿Qué diferencia hay entre programación funcional e imperativa?**
    - La ***programación imperativa*** es el estilo más clásico y tradicional. En este enfoque, el programador le indica a la computadora exactamente qué
      pasos debe seguir para llegar a un resultado. Es como dar una receta paso a paso.
    - La ***programación funcional*** se centra más en describir qué se quiere lograr, en lugar de detallar cómo hacerlo paso a paso (trabajando más con
      funciones puras). Podríamos compararlo con pedir un servicio que se encargue del trabajo: no te preocupas por los pasos intermedios, solo dices
      qué resultado buscas.

5. **En POO: ¿Cuál es la diferencia entre interfaz y clase abstracta?**
    - Una ***interfaz*** es un tipo "especial" de clase que establece qué métodos puede implementar una clase sin especificar el código de su lógica interna.
    - Una ***clase abstracta*** es un punto intermedio entre una interfaz y una clase común. No se puede instanciar directamente, pero sí puede contener tanto
      métodos abstractos (sin código) como métodos ya implementados.

6. **¿A partir de qué versión de Java se implementó la programación funcional?**
Desde Java 8 (2014) se incorporaron expresiones lambda, interfaces funcionales y Streams, dando inicio al paradigma funcional en Java.

7. **¿Cuáles son las propiedades de la POO?**
Las 4 propiedades principales son Abstracción, Encapsulamiento, Herencia y Polimorfismo.
    - ***Ejemplo:***
      - ***Encapsulamiento:*** ocultar atributos y acceder a ellos solo con getters/setters.
      - ***Herencia:*** una clase hija puede reutilizar el código de la clase padre.

8. **¿Qué diferencia hay entre Spring y Spring Boot?**
    - ***Spring:*** es un framework extenso para aplicaciones Java.
    - ***Spring Boot:*** simplifica Spring, permitiendo crear apps con menos configuración, usando starters y servidor embebido.

9. **Diferencia HashMap de LinkedList**
    - ***HashMap:*** almacena pares clave-valor, ideal para búsquedas rápidas. Ej: guardar usuarios por nro de cliente.
    - ***LinkedList:*** lista doblemente enlazada, buena para insertar/eliminar elementos. Ej: cola de atención de clientes.

10. **¿Cómo puedes hacer pruebas en un BACKEND si no tienes un FRONTEND?**
Puedes usar herramientas como Postman, cURL o armar pruebas automatizadas con JUnit + MockMVC, enviando requests al backend y validando las respuestas sin necesidad de un frontend.

11. **¿Qué diferencias hay entre una clase y un objeto?**
     - Una ***clase*** es el molde o plantilla que define cómo serán los objetos (sus atributos o características y métodos o comportamientos).
     - Un ***objeto*** es una instancia concreta de esa clase, es decir, a partir de ese molde creamos un objeto que tiene "esa forma" y la guardamos en memoria.

12. **¿Conoces la diferencia entre MONOLITO y MICROSERVICIO?**
     - ***Monolito:*** toda la app funciona como un único bloque; si algo falla, puede afectar a todo el sistema.
     - ***Microservicio:*** la app se divide en módulos independientes (servicios) que se comunican entre sí, facilitando el mantenimiento y la escalabilidad. 
       Si uno deja de funcionar, generalmente no afecta a los otros.

13. **¿Qué es una annotation? Da un ejemplo de uso**
Una ***annotation*** es una forma de agregar "info extra" o etiquetas al código para indicar comportamientos especiales al compilador o framework.
     - ***Ejemplo:***
       Override indica que un método está sobrescribiendo otro de su clase padre.

14. **¿Qué diferencia hay entre Hibernate y JPA?** **¿Son lo mismo?**
     - ***JPA*** es un ORM, especificación o tecnología para utilizar bases de datos en Java (es quien establece ciertas reglas).
     - ***Hibernate*** es una implementación de JPA (básicamente una forma de hacerlo funcionar). 
     - En resumen: JPA dice qué hacer, Hibernate lo hace.

15. **¿Qué es un endpoint en una API?**
Un ***endpoint*** es una URL específica donde una API recibe y responde peticiones/requests.
    - ***Ejemplo:***
      GET /api/usuarios devuelve la lista de usuarios desde el servidor.
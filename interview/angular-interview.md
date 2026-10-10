<h1 align="center">
PREGUNTAS PARA ENTREVISTA JUNIOR<br>
(VERSIÓN ANGULAR)
</h1>

---

1. **¿Conoces las diferencias entre las versiones de Angular?**
    <details>
    <summary>Solución</summary>
    <p align="justify"> AngularJS (la primera versión) fue lanzada en 2010 y estaba basado en JavaScript. 
    En 2016, Google presentó Angular 2, una reescritura completa del framework usando TypeScript como base.
    Cada versión de Angular trajo mejoras en rendimiento, compatibilidad, herramientas y simplicidad en el desarrollo. 
    Por ejemplo: Angular 15 y 16 mejoraron la detección de cambios, el rendimiento y la compatibilidad con standalone components.</p>
    </details><br>

2. **Explica el concepto de *“Two Way Data Binding”***
    <details>
    <summary>Solución</summary>
    <p align="justify">El <strong>Two Way Data Binding</strong> permite que los datos del modelo y la vista estén sincronizados automáticamente.
    Si el usuario cambia algo en la interfaz, el modelo se actualiza, y viceversa.
    En Angular se usa con <strong>[(ngModel)]</strong>.</p>
    </details><br>

3. **¿Qué es un componente? ¿Qué se puede hacer con ellos?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Un componente es una parte reutilizable de la interfaz gráfica que contiene su propia lógica, vista y estilos. 
    Con los componentes se puede dividir una app en secciones como encabezado, menú o lista de productos.</p>
    </details><br>
  
4. **¿Qué son los Pipes en Angular y para qué se utilizan?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Los Pipes son funciones que permiten transformar los datos antes de mostrarlos en la vista, sin modificar el valor original del modelo. 
    Por ejemplo, convertir texto a mayúsculas, dar formato a fechas o números o incluso crear pipes con formatos personalizados.</p>
    </details><br>

5. **¿Qué es TypeScript y qué ventajas tiene respecto a utilizar solamente JavaScript?**
    <details>
    <summary>Solución</summary>
    <p>TypeScript es un superconjunto de JavaScript que agrega <strong>tipado estático</strong> y características avanzadas. Permite:</p>    
    <ul>
    <li>Detectar errores antes de ejecutar el código.</li>
    <li>Mejorar el autocompletado y la mantenibilidad de un proyecto.</li>
    </ul>
    </details><br>
    
6. **¿Sabes qué es y para qué sirve RXJS?**
    <details>
    <summary>Solución</summary>
    <p align="justify">RxJS (Reactive Extensions for JavaScript) es una librería que permite trabajar con programación reactiva, basada en el uso de Observables. 
    Con RxJS puedes manejar fácilmente eventos asíncronos, como peticiones HTTP o actualizaciones de datos en tiempo real. Angular la usa internamente, 
    por ejemplo, en HttpClient y en los formularios reactivos.</p>
    </details><br>

7. **¿Cómo creas un componente en Angular? ¿De qué archivos generalmente se compone?**
    <details>
    <summary>Solución</summary>
    <p>Puedes crear un componente con el comando: <strong>ng generate component nombre-del-componente</strong>. Cada componente suele tener 4 archivos
    principales:</p>
    <ul>
    <li><strong>.ts (la lógica)</strong></li>
    <li><strong>.html (plantilla o vista)</strong></li>
    <li><strong>.css (los estilos)</strong></li>
    <li><strong>.spec.ts (pruebas unitarias)</strong></li>
    </ul>
    </details><br>

8. **¿Puedo tener un conjunto de componentes adentro de otro componente? Dame ejemplos**
    <details>
    <summary>Solución</summary>
    <p>Sí, es una práctica muy común. Un componente padre puede contener varios componentes hijos para dividir la interfaz en partes más pequeñas y reutilizables.</p>
    <p>Ejemplo: Un componente AppComponent que contiene dentro:</p>
    <ul>
    <li><strong>NavbarComponent</strong></li>
    <li><strong>SidebarComponent</strong></li>
    <li><strong>UserListComponent</strong></li>
    </ul>
    </details><br>

9. **¿Qué es un servicio en Angular?**
    <details>
    <summary>Solución</summary>
    <p align="justify">Un servicio es una clase que se utiliza para centralizar lógica o datos que se comparten entre componentes, como peticiones a una API o funciones reutilizables.</p>
    </details><br>

10. **¿Qué papel cumple la inyección de dependencias con los servicios?**
    <details>
    <summary>Solución</summary>
    <p align="justify">La inyección de dependencias (DI) es el mecanismo que permite que Angular cree y proporcione instancias de servicios de forma automática alos componentes que las necesiten. 
    En lugar de crear manualmente un nuevo servicio con new, Angular lo “inyecta” donde lo necesitas usando el constructor.</p>
    </details>
<h1 align="center">¿QUÉ ES UN TEST UNITARIO?</h1>

<p align="center">
Comprueban pequeñas partes del código de forma aislada para detectar errores rápidamente.
</p>

---

## ¿Qué es?
Es una prueba automática que verifica que una **unidad pequeña** de **código** (función, método, componente, etc.) hace exactamente lo que debe hacer.

---

## ¿Cómo funcionan?
<div align="center">
  <img src="/imgs/unit-testing1.avif" width="600" alt="¿Cómo funciona un unit testing?" />
</div>

---

## Beneficios clave
- **Menos bugs:** Detecta problemas desde el inicio. 
- **Mejor diseño:** Fomenta funciones pequeñas y responsables.
- **Confianza:** Sabes que tu código sigue funcionando.
- **Ahorra tiempo:** Se encuntran errores rápido y barato.

---

## ¿Dónde encajan en TDD?
<div align="center">
  <img src="/imgs/unit-testing2.avif" width="600" alt="¿Dónde encajan en TDD?" />
</div>

---

## ¿Porqué son importantes?
- **Detectan errores:** Encuentran fallos antes de que lleguen a producción.
- **Código más confiable:** Facilitan refactorizar sin miedo a romper funcionalidad.
- **Desarrollo más rapido:** Automatizan la verificación del código.
- **Mejor colaboración:** Dan seguridad a todo el equipo.

---

## Ejemplo práctico (JavaScript + Jest)
- **Código a probar**
    ```javascript
    // sum.js
    function suma(a, b) {
        return a + b;
    }

    module.exports = suma;
    ```

- **Test unitario**
    ```javascript
    // sum.test.js
    const suma = require('./sum');

    test('suma 2 + 3 debe ser 5', () => {
        const resultado = suma(2, 3);
        expect(resultado).toBe(5);
    });

    test('suma con números negativos', () => {
        expect(suma(-2, -3)).toBe(-5);
    });
    ```

- **Resultado al ejecutar**
    ```javascript
    Resultado al ejecutar

    PASS sum.test.js
        ✓ suma 2 + 3 debe ser 5 (2 ms)
        ✓ suma con números negativos (1 ms)

    Test Suites: 1 passed, 1 total
    Tests:       2 passed, 2 total
    Snapshots:   0 total
    Time:        0.345 s
    Ran all test suites.
    ```

---

## Tipos de tests
- **Unitarios:** Prueban unidades pequeñas de código de forma aislada.
- **Integración:** Verifican que varias partes funcionen juntas.
- **E2E (End to End):** Simulan el uso real de la aplicación completa.

---

## Herramientas populares
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jest/jest-plain.svg" alt="Jest" width="28"/> Jest
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vitest/vitest-original.svg" alt="Vitest" width="28"/> Vitest
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mocha/mocha-original.svg" alt="Mocha" width="28"/> Mocha
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jasmine/jasmine-original.svg" alt="Jasmine" width="28"/> Jasmine
- <img src="https://testing-library.com/img/octopus-64x64.png" alt="Testing Library" width="28"/> Testing Library

---

## En resumen
Los tests unitarios ayudan a escribir código más limpio, confiable y fácil de mantener.
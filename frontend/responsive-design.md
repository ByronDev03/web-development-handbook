<h1 align="center">RESPONSIVE DESIGN EN CSS</h1>

<p align="center">
Diseña una sola vez, adapta tu sitio a cualquier dispositivo.
</p>

---

## ¿Qué es?
Es una técnica que permite que todo sitio web se vea y funcione bien en cualquier dispositivo: computadoras, tablets y smartphones.

<div align="center">
    <img src="/imgs/responsive-design1.avif" width="600" alt="Dispositivos"/>
</div>
---

## ¿Cómo funciona?
Usa CSS para detectar el tamaño de la pantalla y aplicar estilos diferentes según el dispositivo.

<div align="center">
    <img src="/imgs/responsive-design2.avif" width="600" alt="Funcionamiento de Responsive Design"/>
</div>

> [!NOTE]
> Una experiencia óptima en todos los dispositivos.

---

## 1. Meta Viewport (Esencial)
Indica al navegador cómo controlar las dimensiones y el escalado de la página en dispositivos móviles.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
```
> [!NOTE]
> Siempre se debe incluir esta etiqueta en el `head` de archivo HTML.

---

## 2. Media Queries
Permiten aplicar estilos CSS según el ancho de la pantalla.
```css
/* Celulares (hasta 576px) */
@media (max-width: 576px) {
    .menu { display: none; }
}

/* Tablets (577px - 992px) */
@media (min-width: 577px) and (max-width: 992px) {
    .menu { display: block; }
}

/* Escritorio (desde 993px) */
@media (min-width: 993px) {
    .menu { display: flex; }
}
```

> [!NOTE]
> Puedes usar `min-width`, `max-width` o un rango con `min-width` y `max-width`.

---

## 3. Unidades flexibles
Se recomienda usar unidades relativas para que los elementos se adapten al tamaño de la pantalla.

- `$`   Relativo al contenedor padre.
- `em`  Relativo al tamaño de fuente del elemento.
- `rem` Relativo al tamaño de fuente `<html>`
- `vw`  1% del ancho de la ventana (viewport width).
- `vh`  1% del alto de la ventana (viewport heigth).

```css
.titulo { font-size: 2rem; }
.contenedor { width: 90%; margin: 0 auto; }
.banner { height: 80vh; }
```

---

## 4. Ejemplo práctico
Navegación que cambia según el dispositivo.
<div align="center">
    <img src="/imgs/responsive-design3.avif" width="600" alt="Ejemplo práctico de Responsive Design"/>
</div>

- **HTML**
```html
<nav class="navbar">
    <div class="logo">MiSitio</div>
    <ul class="menu">
        <li>Inicio</li>
        <li>Servicios</li>
        <li>Sobre nosotros</li>
        <li>Contacto</li>
    </ul>
    <div class="toggle">☰</div>
</nav>
```
- **CSS**
```css
.menu {
    display: flex;
    list-style: none;
}

@media (max-width: 992px) {
    .menu {
        display: none;
    }

    .toggle {
        display: block;
    }
}

@media (max-width: 576px) {
    .menu {
        position: absolute;
        top: 60px;
        left: 0;
        width: 100%;
        flex-direction: column;
        background: #333;
    }
}
```

---

## Buenas prácticas
- ✅ Diseñar mobile-first (empezar por móviles).
- ✅ Usar breakpoints comunes (576px, 768px, 992px, 1200px).
- ✅ Usar imágenes y videos fluidos.
- ✅ Pruebas en diferentes dispositivos y navegadores.
- ✅ Mantén tu diseño simple y consistente.

---

## Breakpoints comunes
| Dispositivo        | Ancho de pantalla |
|--------------------|-------------------|
| Móvil              | ≤ 576px           |
| Tablet             | 577px - 992px     |
| Escritorio         | ≥ 993px           |
| Escritorio Grande  | ≥ 1200px          |

---

## En resumen
El objetivo del Responsive Design es ofrecer la mejor experiencia de usuario posible, sin importar el dispositivo.
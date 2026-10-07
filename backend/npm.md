<h1 align="center">¿QUÉ ES NPM?</h1>

<p align="center">
Permite instalar y admnistrar las dependencias que se utilizan en un proyecto.
</p>

---

## ¿Qué es?
NPM (Node Package Manager) es el gestor de paquetes oficial de Node.js. Permite encontrar, instalar, compartir y reutilizar código de terceros fácilmente.

- **Gigantesco ecosistema:** Más de 2 milones de paquetes reutilizables.
- **Comunidad activa:** Miles de desarrolladores contribuyendo cada día.
- **Gratuito y open source:** Cualquier persona puede usar y publicar paquetes.
- **Sencillo y rápido:** Un solo comando para instalar lo que se necesita.

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/npm1.avif" width="600" alt="¿Cómo funciona?" />
</div>

---

## Flujo de instalación
<div align="center">
  <img src="/imgs/npm2.avif" width="600" alt="Flujo de instalación"/>
</div>

---

## Ejemplo en terminal
```Bash
$ npm install express

added 57 packages, and audited 58 packages in: 2s

found 0 vulnerabilities

```

---

## ¿Dónde se guarda?
```Bash
mi-projecto/
│
├── node_modules/        # Paquetes instalados
├── package.json         # Información del proyecto
└── package-lock.json    # Versiones exactas 
```
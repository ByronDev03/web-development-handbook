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

---

## Comandos más utiles
- `npm install <paquete>`: Instala un paquete y lo guarda en dependencias.
- `npm i -D <paquete>`: Instala un paquete solo para desarrollo (devDependencies).
- `npm uninstall <paquete>`: Desinstala un paquete.
- `npm update`: Actualiza todos los paquetes.
- `npm init`: Crea un nuevo package.json.
- `npm list`: Lista los paquetes instalados.

---

## ¿Qué es package.json?
Define las dependencias y scripts de cualquier proyecto.
```Bash
{
  "name": "mi-proyecto",
  "version": "1.0.0",
  "dependencies": {
    "express": "^4.18.2"
  },
  "devDependencies": {
    "nodemon": "^3.0.1"
  }
}
```

---

## ¿Porqué es importante?
- **Ahorra tiempo:** no reinventes la rueda.
- **Código de calidad:** usa librerías probadas.
- **Fácil de entender:** versiones y actualizaciones controladas.
- **Escalable:** ideal para proyectos pequeños y grandes.

---

## Ejemplos de paquetes populares
- <img src="https://expressjs.com/images/logos/logo-express-white.svg" alt="express" width="25"/> Framework web rápido y minimalista.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original-wordmark.svg" alt="react" width="25"/> Librería para construir interfaces de usuario.
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/axios/axios-plain-wordmark.svg" alt="axios" width="25"/> Cliente HTTP basado en promesas.
- <img src="https://cdn.simpleicons.org/lodash/fff" alt="lodash" width="25"> Utilidades para trabajar con JavaScript.
- <img src="https://cdn.jsdelivr.net/npm/@dev.icons/core@latest/export-files/icons/chalk.svg" alt="chalk" width="25"> Colorea texto en la terminal.
- <img src="https://cdn.jsdelivr.net/npm/@dev.icons/core@latest/export-files/icons/moment-js.svg" alt="moment" width="25"> Manipula y formatea fechas.

---

## En resumen
NPM es el corazón del ecosistema JavaScript.
Conecta con millones de paquetes para construir mejores proyectos, más rápido.
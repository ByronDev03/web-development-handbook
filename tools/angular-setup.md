<h1 align="center">GUÍA DE INSTALACIÓN DE ANGULAR</h1>

---

## ¿CÓMO INSTALAR *nvm* EN WINDOWS?
1. **Descargar el instalador**
   - Ve al repositorio oficial: nvm-windows releases (https://github.com/coreybutler/nvm-windows/releases).
   - Descarga el archivo nvm-setup.exe (el instalador).

2. **Ejecutar el instalador**
   - Haz doble clic en nvm-setup.exe.
   - Te pedirá una carpeta de instalación (por defecto C:\Program Files\nvm).
   - También pedirá dónde se instalarán las versiones de Node (ej. C:\Program Files\nodejs).
   - Acepta y sigue el asistente.

3. **Verificar instalación**
   - Abre CMD o PowerShell y escribe:
     ```Bash
     nvm -v
     ```
      
Si ves un número de versión, está funcionando.

---

## ¿CÓMO INSTALAR Y DESINSTALAR *Node.js* DESDE *nvm* EN WINDOWS?
**NOTA:**
No instalar Node.js directamente desde nodejs.org, porque puede interferir con nvm.

**¿Por qué?**
- El instalador oficial de Node.js para Windows agrega Node y npm directamente al PATH del sistema.
- Eso significa que cuando en la terminal escribas node, Windows usará esa instalación fija.
- Luego, si instalas nvm-windows, va a entrar en conflicto porque NVM también quiere controlar el PATH para que apunte a la versión que elijas.

**CON *nvm*, ¿QUÉ PASA?**
- nvm se encarga de descargar Node.js desde el mismo sitio oficial (https://nodejs.org/dist), pero en vez de instalarlo fijo, lo guarda en su propia carpeta y ajusta el PATH dinámicamente.
- Así tú decides cuál versión de Node usar, y no hay conflicto.

**EN RESUMEN:**
Node.js oficial + NVM al mismo tiempo = choques y confusión.
1. **Ver qué versiones de Node.js hay disponibles online**
   ```Bash
   nvm list available
   ```

2. **Instalar una versión específica de Node.js**
   ```Bash
   nvm install <versión>
   ```
   - **Ejemplo:** *nvm install 22.19.0*

3. **Activar (usar) una versión instalada**
   ```Bash
   nvm use <versión>
   ```
   - **Ejemplo:** *nvm use 22.19.0*

4. **Ver la versión activa de Node.js y npm**
   - Versión de Node.js
     ```Bash
     node -v
     ```
   - Versión de npm
     ```Bash
     npm -v  
     ```
    
5. **Listar versiones instaladas en tu máquina**
   ```Bash
   nvm list
   ```
   - **IMPORTANTE:** *La versión activa tendrá un asterisco al lado.*

6. **Establecer una versión por defecto**
   ```Bash
   nvm alias default <versión>
   ```
   - **Ejemplo:** *nvm alias default 22.19.0*
   
7. **Desinstalar una versión**
   ```Bash
   nvm uninstall <versión>
   ```
   - **Ejemplo:** *nvm uninstall 18.17.0*

**TIPS:**
  - Tras un nvm use, cierra y vuelve a abrir la terminal para que tome efecto.
  - Usa siempre las versiones LTS (ej. 22.x) para proyectos estables.

---

## ¿CÓMO INSTALAR ANGULAR PARA WINDOWS?
1. **Verifica que tienes *Node.js* y *npm* en la terminal (CMD, POWERSHELL o la de VS Code), escribe:** 
   ```Bash
   node -v
   ```
   ```Bash
   npm -v
   ```
   - Si te aparece la versión de Node (ej. v20.x.x) y la de npm (ej. 10.x.x), estás listo.

2. **Instalar *Angular CLI* (herramienta de interfaz de línea de comandos)**
   ```Bash
   npm install -g @angular/cli
   ```
   - **NOTA:**
      - -g significa que se instala globalmente, para que lo uses en cualquier proyecto.
      - Esto instalará el comando ng (el que se usa para trabajar con Angular).

3. **Para comprobar que se instaló bien:**
   ```Bash
   ng version
   ```

---

## ¿CÓMO CREAR UN PROYECTO DESDE CERO EN ANGULAR PARA WINDOWS?
1. **Crear un nuevo proyecto**
    - **Ve a la carpeta donde quieras tu proyecto, por ejemplo:**
      ```Bash
      cd C:\Users\Dell\Documents
      ```
    - **Crea el proyecto**
      ```Bash
      ng new nombre-del-proyecto
      ```
   - **El CLI te preguntará**
        - Which stylesheet format would you like to use? → **SCSS**
        - Do you want to enable Server-Side Rendering (SSR) and Static Site Generation (SSG/Prerendering)? → **Yes**
        - Do you want to create a 'zoneless' application without zone.js? → **Yes**
        - Which AI tools do you want to configure with Angular best practices? → **None**
        Esto generará una carpeta "nombre-del-proyecto" con toda la estructura Angular.

2. **Entra al proyecto**
   ```Bash
   cd nombre-del-proyecto
   ```

3. **Levantar el servidor de desarrollo**
   ```Bash
   ng serve -o
   ```
   - Esto abre en tu navegador `http://localhost:4200/` con tu app corriendo.
      
      **NOTA:**
      - **ng serve:** Inicia el servidor, tú abres el navegador.
      - **ng serve -o:** Inicia el servidor y abre el navegador automáticamente.

---

## ¿CÓMO ELIMINAR UN PROYECTO EN ANGULAR PARA WINDOWS?
1. **Sal de la carpeta del proyecto en la terminal:**
   - ***cd..***
   (esto te regresara a la carpeta superior)

2. **Borra la carpeta del proyecto**
   - **En Windows**
     ```Bash
     rmdir /s /q nombre-del-pryecto
     ```
     (borra toda la carpeta y su contenido sin pedir confirmación).

      **NOTA:** 
     	- **rmdir:** Significa remove directory, es decir, “eliminar directorio” (carpeta).
     	- **/s:** Significa “delete all subdirectories and files”, o sea borra todo el contenido dentro de la carpeta, incluyendo subcarpetas y archivos.
         Sin /s, solo eliminaría la carpeta si está vacía.
     	- **/q:** Significa quiet mode (modo silencioso): es decir, no pide confirmación. Borra sin preguntar “¿Está seguro? (Y/N)”.

---

## COMANDOS BÁSICOS DE NPM
- **Ver versión de npm:**
  ```Bash
  npm -v
  ```

- **Inicializar un proyecto (crear package.json):**
  ```Bash
  npm init -y 
  ```

- **Listar paquetes instalados:**
  ```Bash
  npm list
  ```

- **Instalar un paquete:**
  ```Bash
  npm install <paquete>
  ```

- **Instalar un paquete global (para usarlo en todo el sistema):**
  ```Bash
  npm install -g <paquete>
  ```

- **Desinstalar un paquete:**
  ```Bash
  npm uninstall <paquete>
  ```

- **Actualizar un paquete:**
  ```Bash
  npm update <paquete>
  ```
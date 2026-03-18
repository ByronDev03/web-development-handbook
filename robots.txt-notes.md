<h1 align="center">robots.txt</h1>

---

## ¿Qué es?
Es un ***archivo de texto*** que se coloca en la raíz de un sitio web (ejemplo: ***tusitio.com/robots.txt***).
Sirve para ***indicar a los motoresde búsqueda (Google, Bing, etc.) que partes del sitio pueden o no pueden rastrear.***

No bloquea el acceso real a la información (si alguien tiene el link directo la puede ver), solo da ***instrucciones a los bots*** de los buscadores.

---

## ¿Cómo funciona?
**Cuando un buscador entra a tu web:**
1. Primero revisa el archivo ***robots.txt.***
2. Lee las reglas.
3. Decide que páginas rastrear y cuáles ignorar.

---

## Ejemplo de robots.txt
#Permitir que todos los robots accedan a todo
user_agent: *
Disallow: 

#Bloquear una carpeta llamda /privado/
user_agent: *
Disallow: /privado/

#Bloquear solo a Googlebot de entrar en /test/
user_agent: Googlebot
Dissallow: /test/

---

## Cosas importantes
- **user_agent:** Identifica a qué bot se aplica (ejemplo: Googlebot para Google, Bingbot para Bing).
- **Disallow:** Ruta que no quieres que no rastreen.
- Si quieres permitir todo, basta con:
    - **user_agent:** *
    - **Disallow:**

---

## Uso práctico
- **Si conviene:** Para carpetas como ***/admin/, /login/, /tmp/*** que no aportan nada a Google.
- **No conviene:** Bloquear contenido importante, porque Google no lo indexara.

---

## En resumen
***robots.txt es un semáforo para los buscadores*** sobre qué partes de tu web pueden recorrer y cuáles no.
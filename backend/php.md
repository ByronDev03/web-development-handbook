<h1 align="center">¿QUÉ ES PHP?</h1>

---

**PHP (Hypertext Preprocessor)** es un lenguaje de programación del lado del servidor, diseñado para el desarrollo web dinámico. Se ejecuta en el servidor y genera HTML que se envía al navegador.

---

## Ventajas de PHP
- ✅ Software libre y de código abierto.
- ✅ Fácil de aprender y usar.
- ✅ Gran comunidad y mucha documentación.
- ✅ Funciona en la mayoría de servidores (Windows, Linux y Mac).
- ✅ Ideal para el desarrollo web dinámico.

---

## 1. ¿Para qué sirve?
- Desarrollo de sitios web dinámicos.
- Procesamiento de formularios.
- Conexión y manipulación de bases de datos.
- Sistemas de autenticación.
- Tiendas en línea, blogs, CMS y mucho más.

---

## 2. ¿Cómo funciona?
<div align="center">
  <img src="/imgs/php1.avif" width="600" alt="¿Cómo funciona PHP?" />
</div>

---

## 3. Sintaxis básica
Todo el código PHP va entre las etiquetas `<?php ?>`.
```php
<?php
// Esto es un comentario
$mensaje = "¡Hola, PHP!";
$numero = 10;

echo $mensaje;     // Imprime: ¡Hola, PHP!
echo "<br>";
echo $numero + 5;  // Imprime: 15
?>
```

---

## 4. Variables en PHP
Las variables empiezan con `$`.
```php
<?php
$nombre = "Ana"; // String
$edad = 25;      // Entero
$precio = 19.99; // Decimal
$activo = true;  // Booleano
?>
```

PHP es un lenguaje de **tipado dinámico**.

---

## 5. Estructuras de control
- **Condicionales**
    ```php
    <?php
    $edad = 18;
    if ($edad >= 18) {
        echo "Eres mayor de edad";
    } else {
        echo "Eres menor de edad";
    }
    ?>
    ```

- **Bucles**
    ```php
    <?php
    for ($i = 1; $i <= 5; $i++) {
        echo "Número: $i<br>";
    }
    $j = 1;
    while ($j <= 3) {
        echo "Contador: $j<br>";
        $j++;
    }
    ?>
    ```

---

## 6. Funciones
Las funciones permiten reutilizar código.
```php
<?php
function saludar($nombre) {
    return "¡Hola, $nombre!";
}
echo saludar("Carlos");
// ¡Hola, Carlos!
?>
```

---

## 7. Arrays (arreglos)
Almacenan múltiples valores en una sola variable.
```php
<?php
$frutas = ["Manzana", "Pera", "Uva"];
echo $frutas[0]; // Manzana
foreach ($frutas as $fruta) {
    echo $fruta . "<br>";
}
?>
```

---

## 8. Conexión a base de datos (MySQL)
PHP se integra fácilmente con bases de datos.
```php
<?php
$conexion = new mysqli("localhost", "usuario", "clave", "mi_db");
if ($conexion->connect_error) {
    die("Error de conexión: " . $conexion->connect_error);
}
$sql = "SELECT * FROM usuarios";
$resultado = $conexion->query($sql);
while ($fila = $resultado->fetch_assoc()) {
    echo $fila['nombre'] . " - " . $fila['email'] . "<br>";
}
?>
```

---

## 9. Formularios en PHP
Procesar datos de formularios.
- **HTML (formulario)**
    ```html
    <form method="POST" action="procesar.php">
        <input type="text" name="nombre" placeholder="Tu nombre">
        <input type="submit" value="Enviar">
    </form>
    ```

- **PHP (`procesar.php`)**
    ```php
    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $nombre = $_POST["nombre"];
        echo "Hola, $nombre";
    }
    ?>
    ```

---

## 10. Integración con HTML
Se puede mezclar PHP y HTML fácilmente.
```php
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi sitio con PHP</title>
</head>
<body>
    <h1>Bienvenido <?php echo $nombre; ?></h1>
    <p>La fecha actual es: <?php echo date("d/m/Y"); ?></p>
</body>
</html>
```

---

## Ejemplo completo
```php
<?php
$tareas = ["Aprender PHP", "Hacer ejercicio", "Leer un libro"];
?>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Tareas</title>
</head>
<body>
    <h2>Lista de Tareas</h2>
    <ul>
        <?php foreach ($tareas as $tarea): ?>
            <li><?php echo $tarea; ?></li>
        <?php endforeach; ?>
    </ul>
</body>
</html>
```

- **Resultado**
<div align="center">
  <img src="/imgs/php2.avif" width="250" alt="Ejemplo PHP"/>
</div>

---

## Frameworks populares
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg" alt="Laravel" width="28"/> Laravel
- <img src="https://cdn.simpleicons.org/symfony/ffffff" alt="Symfony" width="28"/> Symfony
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/codeigniter/codeigniter-plain.svg" alt="CodeIgniter" width="28"/> CodeIgniter
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/yii/yii-original.svg" alt="Yii" width="28"> Yii

## Herramientas útiles
- <img src="https://cdn.simpleicons.org/xampp" alt="XAMPP" width="28"/> XAMPP
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg" alt="VSCode" width="28"/> Visual Studio Code
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/composer/composer-original.svg" alt="Composer" width="28"/> Composer
- <img src="https://cdn.simpleicons.org/phpmyadmin" alt="phpMyAdmin" width="28"/> phpMyAdmin
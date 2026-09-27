<h1 align="center">¿QUÉ ES SSH?</h1>

<p align="center">
Permite conectarte y administrar servidores remotos mediante una conexión cifrada.
</p>

---

## ¿Qué es?
SSH (Secure Shell) es un protocolo de red que permite conectarse a un servidro remoto de forma segura. <br>
Cifra toda la comunicación para proteger credenciales, comandos y datos.

- **Seguro:** Cifra la conexión y protege contra la interceptación de datos.
- **Remoto:** Accede y administra servidores desde cualquier lugar.
- **Versátil:** Útil para administración, automatización y DevOps.

---

## ¿Cómo funciona?
<div align="center">
  <img src="/imgs/ssh-diagram1.avif" width="600" alt="Funcionamiento de SSH" />
</div>

- **¿Qué sucede?**
    1. El cliente inicia una conexión SSH al servidor (puerto 22). 
    2. Se realiza una autenticación segura (contraseña o llave pública).
    3. Se establece un canal cifrado.
    4. Todos los datos viajan cifrados entre cliente y servidor.
    5. Se pueden ejecutar comandos y administrar el servidor de forma segura.

<div align="center">
  <img src="/imgs/ssh-diagram2.avif" width="600" alt="Funcionamiento de SSH" />
</div>

---

## Autenticación
- **Contraseña:** El método más común. Menos seguro si la contraseña es débil.
<div align="center">
  <img src="/imgs/ssh-diagram3.1.avif" width="100" alt="Llave pública" />
</div>

- **Llave pública (Recomendado):** Más seguro. Usa un par de llaves: pública (en el servidor) y privada (en la máquia).
<div align="center">
  <img src="/imgs/ssh-diagram3.2.avif" width="600" alt="Llave pública" />
</div>

> [!NOTE]
> Usar llaves SSH para mayor seguridad y automatización.

---

## Comandos básicos
```Bash
# Conectarse a un servidor
ssh usuario@ip_del_servidor

# Conectarse usando un puerto distinto
ssh -p 2222 usuario@ip_del_servidor

# Conectarse con una llave privada
ssh -i ~/.ssh/id_rsa usuario@servidor

# Copiar archivos usando SCP
scp archivo.txt usuario@servidor:/ruta/

# Copiar carpetas usando SCP
scp -r carpeta/ usuario@servidor:/ruta/
```

---

## Ejemplo de conexión
```Bash
ssh usuario@192.168.1.10
The authenticity of host '192.168.1.10 (192.168.1.10)'
can't be established.
ED25519 key fingerprint is SHA256:ABcd1234...
Are you sure you want to continue connecting (yes/no)?
yes
Warning: Permanently added '192.168.1.10' (ED25519)
to the list of known hosts.
usuario@192.168.1.10's password:
[usuario@servidor ~]$
```

> [!NOTE]
> **¡Conexión establecida!**
> Ahora ya se puede ejecutar comandos en el servidor.

---

## Casos de uso
- Administración de servidores Linux
- Despliegue de aplicaciones (DevOps)
- Transferencia segura de archivos
- Acceso a bases de datos seguras remotas
- Automatización con scripts

---

## Puerto por defecto
<div align="center">
  <img src="/imgs/ssh-diagram4.avif" width="600" alt="Puerta por defecto SSH" />
</div>

> [!NOTE]
> Se puede cambiar en el servidor editando */etc/ssh/ssh_config* (Puerto recomendado: 2222)

---

## Flujo de una conexión SSH
<div align="center">
  <img src="/imgs/ssh-diagram5.avif" width="600" alt="Flujo de una conexión SSH" />
</div>

---

## En resumen
- SSH = Secure Shell
- Conexión cifrada y segura
- Autenticación por contraseña o llave
- Ideal para administración y DevOps
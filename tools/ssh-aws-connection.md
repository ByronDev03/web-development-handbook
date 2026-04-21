<h1 align="center">
CONEXIÓN POR SSH A UN SERVIDOR<br>
REMOTO (AWS)
</h1>

---

#### Usar SSH  nativo de Windows

Windows 11 incluye *OpenSSH Client* por defecto.
- **Abrir Powershell y ejecutar:**
```Bash
ssh
```

- **Deberá responder lo siguiente:**
![[IMG-20260410-WA0065.jpg]]

---
#### ¿Cómo conectarse a AWS?

Supon que tú instancia EC2 tiene:
- **IP pública:** `18.222.xx.xx`
- **Usuario:** `ec2-user` (Amazon Linux)
- **Clave:** `mi-clave.pem`
Haz esto:

1. **Guardar el`.pem` en una carpeta**
```Bash
C:\Users\TuUsuario\.ssh
```

2. **En Powershell:**
```Bash
cd $env:USERPROFILE\.ssh
```

3. **Conectarse**
```Bash
ssh -i mi-clave.pem ec2-user@18.222.xx.xx
```

> [!IMPORTANT]
> **Permisos de la clave**
> Si da error de permisos, ejecutar:
> ```Bash
> icacls mi-clave.pem /inheritance:r
   icacls mi clave.pem/ grant:r"$($env:USERNAME):(R)"
> ```
> Con esto corrigue permisos estilo Linux.

> [!NOTE]
> **Usuario según sistema**
> - En AWS cambia según AMI:
> 	- **Amazon Linux:** `ec2-user`
> 	- **Ubuntu:** `ubuntu`
> 	- **Debían:** admin
> 	- **CentOS:** `centos`

---
#### Instalar Nginx en EC2

- **Ejecutar:**
```Bash
sudo apt install nginx -y
```

- **Verificar:**
```Bash
sudo systemctl status nginx
```
Debera decir `active (running)`

- **Abrir navegador:**
```
http://TU-IP-PUBLICA
```
Deberás aparecer la página de bienvenida de Nginx.

---
#### Instalar MySQL en EC2

- **Ejecutar:**
```Bash
sudo apt install mysql-server -y
```

- **Cuando termine de instalar, ejecutar:** 
```Bash
sudo mysql_secure_installation
```

- **Responder así (recomendado):**
	- *VALIDATE PASSWORD:* `Y`
	- *Nivel:* `2`
	- *Cambiar contraseña root:* `Y`
	- *Quitar usuarios anónimos:* `Y`
	- *Deshabilitar root remoto:* `Y`
	- *Eliminar base test:* `Y`
	- *Recargar privilegios:* `Y`

- **Verificar instalación:**
```Bash
sudo systemctl status mysql
```
Debera decir `active (running)`

Entrar al cliente MySQL

- **Ejecuta:**
```Bash
sudo mysql
```

- **Al entrar se deberá ver algo como:** 
```
mysql>
```
Funciona correctamente.

- **Para salir:**
```sql
exit;
```

Ver versión instalada

- **Dentro de MySQL escribe:**
```sql
SELECT VERSION();
```

- **Devolverá algo como:**
```
0.0.xx
```

Ver puerto escuchado
- **Ejecuta:**
```Bash
sudo ss -tulpn | grep 3306
```

- 3306 es el puerto de MySQL.
- Debe aparecer algo escuchando en 127.0.0.1:3306.

> [!Important]
> En AWS normalmente **NO** debes abrir puerto 3306 al mundo.
> Solo que tú app Node se conecte localmente.

---
#### Instalar Node.js en EC2
**No usar `apt install nodejs` directo.**
- **Usa NodeSource para agregar el repositorio oficial de Node.js:**
```Bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
```

- **Instala Node.js desde ese repositorio**
```Bash
sudo apt install -y nodejs
```

- **Verificar instalación:**
```Bash 
node -v
npm -v
```

- **Deberá mostrar:**
```
v20.20.x
10.x.x
```

---
#### Instalar PM2 en EC2

- **Ejecutar:**
```Bash
sudo npm install -g pm2
```

- **Verificar:**
```Bash
pm2 -v
```

- **Hacer que PM2 arranque al reiniciar**
```Bash
pm2 startup
```
Dará un comando 
Copiarlo y ejecutarlo

- **Después:**
```Bash
pm2 save
```
---
#### Instalar Docker en EC2

- **Instalar Docker:**
```Bash
sudo apt install -y docker.io
```

- **Verificar:**
```Bash
sudo systemctl status docker
```

- **Ver versión:**
```Bash
docker --version
```

- **Iniciar Docker:**
```Bash
sudo systemctl start docker
```

- **Activar Docker al reiniciar:**
```Bash
sudo systemctl enable docker
```

- **Instalar Docker Compose:**
```Bash
sudo apt install -y docker-compose
```

> [! Important]
> **Para evitar usar `sudo` siempre y dar permisos:**
> ```Bash
> sudo usermod -aG docker $USER
> ```
> **Aplicar inmediatamente el cambio de grupo (docker) SIN reiniciar sesión**
> ```Bash
> newgrp docker 
> ```
> **Luego:**
> ```Bash
> exit
> ```
> **Volver a entrar:**
> ```Bash
> ssh ec2-user@TU_IP
> ```
> 



 

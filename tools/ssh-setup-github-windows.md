<h1 align="center">
CONFIGURACIÓN DE SSH PARA GITHUB<br>
EN WINDOWS 11
</h1>

---

#### 1. Configurar GIT
```Bash
  git config --global user.name "Juanito Pérez"
  git config --global user.email "tu_correo@ejemplo.com"
  ```
**Verificar:**
```Bash
git config --global --list
```
---
#### 2. Crear nueva llave SSH
```Bash
ssh-keygen -t ed25519 -C "tu_correo@ejemplo.com"
```
- *Enter file in which to save the key → ENTER*
- *Enter passphrase → opcional (se puede dejar vacio)*

**RESULTADO**
- *Se crea:*
```
C:\Users\tu-usuario\.ssh\
```

- con:
```
id_ed25519
id_ed25519.pub
```

**Verifica:**
```Bash
dir $env:USERPROFILE\.ssh
```
Se verán los archivos

---
#### 3. Iniciar SSH Agent
1. **Ejecutar Powershell como Admin**
2. **Habilitar servicio:**
	```Bash
	Set-Service -Name ssh-agent -StartupType Automatic
	```
3. **Iniciar servicio:**
	```Powershell
	Start-Service ssh-agent
	```
4. **Validar:**
	```Powershell
	Get-Service ssh-agent
	```
Debe decir:
*Status: Running*

---
#### 4. Agregar llave
```Bash
ssh-add $env:USERPROFILE\.ssh\id_ed25519
```
Pedirá contraseña si es que se creo alguna

---
#### 5. Copiar llave pública 
```Bash
cat $env:USERPROFILE\.ssh\id_ed25519.pub
```
Copiar todo lo que salga

---
#### 6. Agregar en GitHub
- **Dirigirse a:**
	- HTTPS://github.com/settings/keys
- Click ***New SSH key***
- Title: ***Cualquiera***
- Key type: ***Authentication Key***
	- Porqué está es para:
		- Conectarse a GitHub
		- Hacer git push / git pull
		- Autenticar tu maquina
	- En cambio ***Signing Key***
		- Firmar Commits (GPG/SSH signing)
- Key: ***Pegar la llave pública***

---
#### 7. Probar Conexion
> [!Warning]
> **Si al ejecutar:**
> ```Bash
> ssh -T git@github.com
> ```
> **Salta este mensaje**
> ```
> ssh: connect to host github.com port 22: Conection timed out
> ```
> **Significa:**
> Tu red está bloqueando el puerto 22 (SSH)

> [!Important]
> **¿Porqué pasa?**
> Muy común en:
> - redes de universidad 
> - redes de trabajo 
> - algunos proveedores de internet 
> - firewalls de Windows

**Usar SSH por puerto 443 (HTTPS) en lugar de 22**
1. **Crear config SSH**
	```Bash
	notepad $env:USERPROFILE\.ssh\config
	```
2. **Escribir:**
	```
	Host github.con
      HostName ssh.github.com
      User git
      Port 443
	```
		
	Guardar y cerrar
	
	3. **Probar otra vez:**
		```Bash
		ssh -T git@github.com
		```
		- **Preguntara:**
			- *Are you sure you want yo continue connecting (yes/no/[fingerprint])?* **yes**
		- **Deberías de ver:**
			```
			Hi user_name! You've successfully authenticated
			```


> [!Note]
> **Ya puedes hacer:**
> ```Bash
> git clone git@github.com:usuario/repo.git
> git pull
> git push
> ```
> 	

---
#### 8. Verificar repositorios
- **Dentro del proyecto:**
	```Bash
	git remote -v
	```
- **Deberías de ver:**
	```
	git@github.com:usuario/repo.git
	```

> [!Warning]
> - **Si ves HTTPS**
> ```
> https://github.com/...
> ```
> - **Cámbialo:**
> ```Bash
> git remote set-url origin git@github.com:TU_USUARIO/TU_REPO.git
> ```

---

> [!Tip]
> ESTE PROCESO SOLO SE HACE UNA VEZ POR EQUIPO
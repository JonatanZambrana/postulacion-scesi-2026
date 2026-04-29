# GIT HUB CON LA SCESI

## DIA 1 

### INTRODUCCION
- COMO NACIO GIT
Lo creo un sujeto que necesitaba el programa
- ARCHIVOS IMPORTANTES EN GIT 
1 README.md 
Una pequeña documentacion del Repositorio
2 .gitignore
Para no subir 1000 lineas de codigo de solo paquetes o de node


## DIA 2 
### STATES AND COMMITS
- LOS ESTADOS DE GIT
1 Directorio de Trabajo (Modificado)
Para restaurar archivo
git restore <archivoNombre>
2 Stage Area (Preparado)
Agregar al area de Staging
git add . 
git <Archivo>
Para restaurar 
git restore --staged <archivo>

3 Repositorio Local (Confirmado)
Para confirmar el Commit 
git commit -m "mensaje"
Deshacer el ultimo commit 
git reset --soft HEAD~1 

### BUENAS PRACTICAS 
Prefijos 

* **feat:** Nueva caracteristica para el Usuario
* **fix:** Reparar bug o Arregar errores
* **perf:** Cambios que mejoran el Rendimiento
* **build:** Cambios en el sistema Build
* **ci:** Cambios de Integracion Continua 
* **docs:** Cambios en Documetacion
* **refactor:** Refactorizacion de Codigo
* **style:** Cambios de Formato o estilos
* **test:** test o refactorizacion 

## DIA 3
### GITHUB Y SSH

1 QUE ES GITHUB
Plataforma en la nube que permite alojar, gestionar y colaborar en proyectos de SW utilizando Git

2 GIT VS GIT HUB
Git es el sistema de control de versiones y Github es el servidor donde estos se almacenan

3 SSH Y HTTP 
SSH conexion segura mediante una key y HTTPs clonar el repositorio

4CONFIGURACION SSH 


ssh-keygen -t ed25519 -C ""


5 CREAR REPOSITORIO EN GITHUB  

6 CLONAR REPOSITORIO EN GIT

7 CAMBIOS

* Subir Cambios 
* Bajar Cambios 


##DIA 4

# Día 4: Git Avanzado y Repositorios Remotos

En esta sesión aprendimos a conectar nuestro trabajo local con la nube y a navegar por la historia del proyecto.

## 1. Repositorios Remotos (`git remote`)
Sirven para conectar tu computadora con servidores como GitHub.
* `git remote add <nombre> <url>`: Conecta tu carpeta local con un repositorio en línea.
* `git remote -v`: Lista las conexiones actuales.
* `git remote set-url <nombre> <url>`: Cambia la dirección del repositorio remoto.

## 2. Configuración de SSH
Para manejar varias cuentas de GitHub en una misma PC:
* Se crean llaves únicas con `ssh-keygen`.
* Se configuran en un archivo `config` asignando alias a cada cuenta.
* **Prioridad:** Las configuraciones locales del repositorio siempre mandan sobre las globales.

## 3. Navegación con `git checkout`
Sirve para "viajar en el tiempo" a commits anteriores o cambiar de rama.
* **Detached HEAD:** Estado que ocurre al apuntar directamente a un commit y no a una rama. 
* **Regla de oro:** No trabajes mucho tiempo en "Detached HEAD"; si vas a hacer cambios reales, mejor crea una rama nueva para no perder tu progreso.

# Día 5





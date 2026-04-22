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




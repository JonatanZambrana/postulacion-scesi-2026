# GIT HUB CON LA SCESI

## DÍA 1: INTRODUCCIÓN

*   **Origen de Git:** Creado por Linus Torvalds después de que la comunidad de Linux perdiera el acceso gratuito a BitKeeper.
*   **Configuración Inicial:** Es esencial configurar la identidad con `git config --global user.name` y `user.email`.
*   **Archivos Esenciales:**
    1.  **README.md:** Documentación del repositorio.
    2.  **.gitignore:** Define qué archivos o carpetas (como `node_modules` o `.env`) Git debe ignorar para no ensuciar el repositorio.


## DÍA 2: ESTADOS Y BUENAS PRÁCTICAS

### Los 3 Estados de Git
1.  **Directorio de Trabajo (Modified):** Archivos editados pero no guardados aún en la historia. Comando para deshacer: `git restore <archivo>`.
2.  **Stage Area (Staging):** Área de espera para los cambios que se incluirán en el próximo commit. Comandos: `git add <archivo>` o `git add .`. Para sacar del área: `git restore --staged <archivo>`.
3.  **Repositorio Local (Committed):** Cambios confirmados con un ID (hash) único. Comando: `git commit -m "mensaje"`.

### Buenas Prácticas de Commits
*   **Commits Atómicos:** Cada commit debe representar un único cambio lógico y pequeño.
*   **Mensajes Semánticos:** Usar verbos imperativos y prefijos para mayor claridad:
    *   `feat`: Nueva funcionalidad.
    *   `fix`: Corrección de errores.
    *   `docs`: Cambios en documentación.
    *   `refactor`: Mejora de código sin cambiar funcionalidad.
    *   `style`: Formato y estilos (no afecta lógica).



## DÍA 3: GITHUB Y SSH

*   **Git vs GitHub:** Git es la herramienta local; GitHub es la plataforma en la nube para alojar y colaborar en proyectos.
*   **SSH (Secure Shell):** Método recomendado para conectar tu PC con GitHub sin pedir contraseña constantemente. Se genera con `ssh-keygen -t ed25519`.
*   **Flujo Remoto Básico:**
    *   `git remote add origin <url>`: Conecta el repo local con el remoto.
    *   `git push`: Sube tus cambios al servidor.
    *   `git pull`: Trae y fusiona los cambios del servidor a tu PC.



## DÍA 4: GIT AVANZADO Y MULTI-SSH
*   **Gestión de Remotos:** `git remote -v` para ver conexiones y `git remote set-url` para cambiarlas.
*   **Multi-SSH:** Uso de un archivo `config` en `~/.ssh/` para gestionar múltiples cuentas de GitHub en una misma máquina mediante alias.
*   **Navegación (Checkout):** Permite "viajar en el tiempo" a commits anteriores. Evitar trabajar mucho tiempo en estado **Detached HEAD** (punto fijo sin rama); si vas a hacer cambios, crea una rama nueva con `git checkout -b <nombre>`.



## DÍA 5: RAMAS (BRANCHING)
*   **¿Qué son?:** Bifurcaciones que permiten desarrollar funciones en paralelo sin afectar el código principal.
*   **Comandos:** `git branch` (listar), `git branch <nombre>` (crear), `git branch -D` (borrar).
*   **Switch vs Checkout:** `git switch` es el comando moderno (2019) especializado exclusivamente en cambiar de ramas para evitar errores accidentales.

## DÍA 6: GITFLOW Y FUSIONES
*   **Gitflow:** Flujo de trabajo organizado con ramas específicas: `main` (producción), `develop` (desarrollo), `feature` (nuevas funciones), `hotfix` (arreglos urgentes).
*   **Fusiones (Merge):** `git merge --no-ff <rama>` une los cambios. El flag `--no-ff` (no fast-forward) es crucial para mantener un historial visual de la rama fusionada aunque esta sea borrada.
*   **Actualización:** Usar `git fetch` para revisar cambios remotos sin mezclarlos todavía.



## DÍA 7: PULL REQUESTS (PR) Y SEGURIDAD
*   **¿Qué es un PR?:** Es la forma profesional de proponer cambios. Crea una solicitud para que el equipo revise tu código antes de integrarlo a la rama principal (`main` o `develop`).
*   **Ventajas:**
    *   **Seguridad:** Evita que cualquiera suba código malicioso o erróneo directamente.
    *   **Revisión por Pares:** Fomenta el debate y la mejora del código antes de lanzarlo.
*   **Protección del Repo:** GitHub permite bloquear ramas para obligar a que todo cambio pase por una revisión de PR antes de ser aceptado.



## DÍA 8: CONTRIBUCIÓN A OPEN SOURCE
*   **El Fork:** Si no eres colaborador directo de un proyecto, realizas un **Fork** (copia a tu propia cuenta de GitHub) desde la web.
*   **Flujo de Contribución:**
    1.  **Clonar:** `git clone` de tu fork personal.
    2.  **Rama Nueva:** Crear una rama específica para tu mejora (ej. `docs/mejora-readme`).
    3.  **Cambios y Commits:** Realizar las mejoras y hacer commit semántico.
    4.  **Push:** Subir la rama a *tu* fork: `git push -u origin <rama>`.
    5.  **PR Final:** Desde GitHub, abrir un Pull Request hacia el repositorio original.
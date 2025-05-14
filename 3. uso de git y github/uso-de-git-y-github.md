## USO DE GIT Y GITHUB

### Fundamentos de Git: commits, branches, merges

<div style="text-align: center;">
  <img src="ramas.png" alt="ramas" width="500"/>
</div>

**¿Qué es Git?**

Es un software de control de versiones distribuido que permite administrar y gestionar los cambios en la información de un proyecto con código. Estos proyectos se guardan en **repositorios**. El funcionamiento de Git se basa en unas líneas de desarrollo conocidas como **ramas** (o ***branches***), que almacenan copias independientes de los archivos de trabajo contenidos en el repositorio.

Mediante estas ramas, cada usuario tiene la facilidad de modificar su código de forma aislada. Estos cambios pasan momentáneamente al área de preparación o *staging area* y son confirmados a través de confirmaciones o ***"commits"***, sin afectar al código principal almacenado en la rama principal. Posteriormente, estas ramas son fusionadas en dicha rama principal, donde se consolida la versión definitiva del proyecto.

Los ***merges*** hacen referencia a la fusión de una rama paralela, cuyos cambios realizados independientemente son transferidos a la rama principal.

**git init:** inicializar repositorio local nuevo

**git add archivo:** añade un archivo específico al área de preparación

**git add .:** añade todos los archivos del repositorio al área de preparación

**git branch rama-nueva:** crear una rama

**git checkout rama-nueva:** cambiar la rama de trabajo

**git commit -m "Comentario que explica tu commit":** confirma los cambios hechos en el repositorio

**git status:** muestra el estado del repositorio

**git log:** muestra el historial de commits

**git branch:** gestiona ramas

**git merge:** fusiona ramas

### Sincronización con GitHub

Los repositorios de Git pueden ser sincronizados a la nube, mediante el portal GitHub. Para esta acción, utilizaremos la terminal de Git Bash, en donde usaremos algunos comandos.

**git remote add origin `https://github.com/usuario/repositorio.git`:** vincular el repositorio a Git

**git branch -M main**: cambiar la rama de trabajo a la principal

**git push -u origin main**: enviar tu rama principal por primera vez

**git pull origin main:** obtiene y fusiona cambios desde un repositorio remoto

**git push origin main:** envía tus commits al repositorio remoto

### Uso de Git en el entorno GitHub

GitHub proporciona una interfaz web muy útil para trabajar con repositorios y colaborar.

**Fork**: Es una copia personal de un repositorio público que puedes modificar libremente.

**Pull Request (PR)**: Es una solicitud para que el propietario del repositorio original revise y acepte tus cambios.

Pasos típicos para colaborar:

- Hacer un fork del repositorio a tu cuenta.

- Clonar tu fork localmente.

- Crear una rama para tu cambio.

- Hacer commits y push a tu fork.

- Desde GitHub, abrir un *Pull Request* hacia el repositorio original.

**Issues:** Sirven para reportar errores, solicitar mejoras o anotar ideas. Puedes asignarlos, etiquetarlos y comentarlos.

**GitHub Actions:** Automatización CI/CD (por ejemplo, ejecutar pruebas automáticamente al hacer push).

**Projects:** Tableros de tareas estilo Kanban. Útiles para visualizar el avance del proyecto.
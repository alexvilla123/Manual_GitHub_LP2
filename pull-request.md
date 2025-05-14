## Pull Requests

## Pull Requests

### ¿Qué es un Pull Request?

Un **Pull Request (PR)** permite a los desarrolladores proponer cambios a un proyecto. Es una solicitud para que el propietario del repositorio revise y fusione los cambios en la rama principal.

![Pull Request en GitHub](https://docs.github.com/assets/cb-87213/images/help/pull_requests/pull-request-review-edit-branch.png)

### Revisión, Comentarios y Merge

1. Accede al repositorio y crea un nuevo branch:

```bash
git checkout -b feature/nueva-funcionalidad
```

2. Realiza los cambios y súbelos:

```bash
git add .
git commit -m "Añadir nueva funcionalidad"
git push origin feature/nueva-funcionalidad
```

3. En GitHub, crea un nuevo Pull Request y selecciona la rama principal para la fusión.
4. Solicita revisiones y realiza los ajustes necesarios.

### Resolución de Conflictos

Si el PR tiene conflictos, GitHub los señalará. Puedes resolverlos directamente en la interfaz web o mediante la línea de comandos:

```bash
git fetch origin

git checkout main
git merge feature/nueva-funcionalidad
# Resolver conflictos manualmente
git add .
git commit -m "Resolver conflictos"

git push origin main
```


---

## Gestión de Proyectos con GitHub Projects

### Creación de Tableros y Tarjetas

GitHub Proyects permite gestionar el trabajo mediante tableros y tarjetas:

1. Haz clic en **Projects** en el repositorio.
2. Crea un nuevo proyecto y define las columnas (To Do, In Progress, Done).
3. Asocia issues y PRs a las tarjetas.

![Tableros de Proyectos en GitHub](https://misovirtual.virtual.uniandes.edu.co/codelabs/tableros-proyecto-github/img/8ee1e4d39b396c36.png)

### Flujos de Trabajo Integrados con Issues y PRs

Los issues y PRs pueden vincularse automáticamente a tarjetas del proyecto. Esto facilita la gestión del flujo de trabajo y el seguimiento del progreso.

Ejemplo de integración de un issue en un proyecto:

```bash
gh project card add 1 --content-url https://github.com/usuario/repo/issues/123
```

---
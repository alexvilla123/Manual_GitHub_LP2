## Automatización y Despliegue

### GitHub Actions: Conceptos Básicos

GitHub Actions permite automatizar flujos de trabajo mediante la creación de acciones personalizadas y workflows basados en eventos. Es ideal para integraciones continuas (CI) y despliegues continuos (CD).

![GitHub Actions](https://miro.medium.com/v2/resize:fit:679/1*_7mJjD1resPodxT7agk16w.png)

Ejemplo de un workflow básico en `.github/workflows/ci.yml`:

```yaml
name: CI Workflow

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '16'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
```

### Workflows para CI/CD

Los workflows permiten definir procesos automáticos para pruebas, compilación y despliegue.

Ejemplo de despliegue en GitHub Pages mediante un workflow:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Build site
        run: npm run build

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          publish_dir: ./build
```

![Despliegue GitHub Pages](https://miro.medium.com/v2/resize:fit:2000/1*clSGFb4fWjIakZ0ewv6keg.png)

### Automatización en GitHub Projects

GitHub Projects permite crear tableros Kanban y flujos de trabajo personalizados para gestionar tareas de forma ágil.

Ejemplo de automatización usando GitHub CLI:

```bash
# Crear un proyecto
gh project create --title "Sprint 1" --owner usuario

# Agregar un issue al proyecto
gh project item add 1 --issue 123
```


### GitHub Pages

GitHub Pages permite desplegar sitios web estáticos directamente desde un repositorio. Es ideal para documentación, blogs o portfolios.

Para activar GitHub Pages:

1. Accede a **Settings** del repositorio.
2. Desplázate a **Pages**.
3. Selecciona la rama y carpeta de origen.
4. Haz clic en **Save**.

Ejemplo de un archivo `index.html` para GitHub Pages:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Mi Sitio en GitHub Pages</title>
</head>
<body>
  <h1>Bienvenido a mi sitio web desplegado con GitHub Pages</h1>
</body>
</html>
```

---
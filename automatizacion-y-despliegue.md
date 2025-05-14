## Automatización y Despliegue

### GitHub Actions: Conceptos Básicos

**GitHub Actions** permite automatizar tareas como compilación, pruebas y despliegue mediante workflows definidos en archivos YAML.

![GitHub Actions](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQpQy91HRXhmeB3bPt20n1h48p5rPQ3nHVIrA&s)

Ejemplo de workflow básico:

```yaml
name: CI Workflow

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Ejecutar pruebas
        run: npm test
```

### Workflows para CI/CD

Los workflows se configuran para ejecutar pruebas, compilaciones y despliegues automáticamente.

```yaml
name: Deploy Workflow

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          publish_dir: ./public
```

![Workflow CI/CD](https://docs.github.com/assets/images/help/actions/workflow.png)

---

### Automatización en GitHub Projects

- Los workflows pueden integrarse con **GitHub Projects** para actualizar automáticamente el estado de issues y PRs.

Ejemplo:

```yaml
name: Update Project Board

on:
  issues:
    types: [opened, closed]

jobs:
  update-board:
    runs-on: ubuntu-latest
    steps:
      - name: Update Project Board
        run: echo "Issue actualizado en el tablero"
```

![GitHub Projects](https://docs.github.com/assets/images/help/projects/project-board.png)

---

### GitHub Pages

GitHub Pages permite alojar sitios estáticos directamente desde un repositorio.

1. Habilita GitHub Pages desde las **Settings** del repositorio.
2. Selecciona la rama y carpeta para desplegar el sitio.

Ejemplo de configuración en `gh-pages`:

```bash
git checkout -b gh-pages
npm run build
git add .
git commit -m "Deploy site"
git push origin gh-pages
```

![GitHub Pages](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRlBEhcnZfEiCZBr0bb0uCDjR7RA9TX_HOBGA&s)

---


# 4. Colaboración en Proyectos

## Gestión de Issues

### ¿Qué es un Issue?

Un **issue** en GitHub es una herramienta para reportar errores, solicitar nuevas funciones o hacer un seguimiento del progreso de tareas en un proyecto. Los issues permiten a los colaboradores comunicarse, discutir problemas y organizar el trabajo de manera efectiva.

### Creación, Asignación y Seguimiento

Para crear un issue, sigue estos pasos:

1. Accede al repositorio donde quieres crear el issue.
2. Haz clic en la pestaña **Issues**.
3. Haz clic en **New Issue**.
4. Rellena el título y la descripción del issue.
5. Opcionalmente, asigna el issue a un colaborador, etiqueta el issue y asocia un milestone.
6. Haz clic en **Submit new issue**.

Ejemplo de creación de un issue usando la línea de comandos:

```bash
# Crear un issue utilizando GitHub CLI
gh issue create --title "Error al cargar imágenes" --body "Las imágenes no se cargan en la página de inicio."
```

### Etiquetas y Milestones

- **Etiquetas (Labels):** Permiten clasificar los issues según su prioridad, tipo o estado (bug, enhancement, documentation, etc.).
- **Milestones:** Agrupan issues relacionados para indicar su progreso en un proyecto específico.

Ejemplo de asignación de etiqueta y milestone:

```bash
# Asignar una etiqueta a un issue
gh issue edit 123 --add-label "bug"

# Asociar un milestone
gh issue edit 123 --milestone "Sprint 1"
```

---
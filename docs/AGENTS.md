# Estándar de Gestión de Proyecto y Documentación

**Versión:** 1.0
**Propósito:** Este documento describe la metodología, herramientas y flujos de trabajo a seguir durante el ciclo de vida del desarrollo. Su objetivo es asegurar la consistencia, claridad y trazabilidad en todas las fases.

---

## 1. Filosofía General

1.  **Docs-First (La Documentación Primero):** La planificación y documentación preceden a la implementación. Se definen el "qué", "porqué" y "cómo" antes de escribir código.
2.  **GitHub como Única Fuente de Verdad (SSOT):** Todo lo relacionado con el proyecto —código, documentación, tareas y discusiones— vive dentro del ecosistema de GitHub.
3.  **Claridad sobre Brevedad:** Las descripciones de tareas (Issues) deben ser explícitas, detallando el objetivo y los criterios de aceptación para eliminar suposiciones.
4.  **Documentación Viva:** Los documentos en `/docs/` son dinámicos y se actualizan si las decisiones de arquitectura o diseño cambian.

---

## 2. Estructura de Documentación (`/docs/`)

La carpeta `/docs/` es el cerebro del proyecto.

* **`/docs/01-manifest.md`**: La "Constitución" del proyecto. Define la visión, objetivos y alcance.
* **`/docs/02-design-system.md`**: La fuente de verdad para la UI. Traduce Figma a tokens de diseño.
* **`/docs/03-database-schema.md`**: El plano arquitectónico de los datos, con un diagrama Mermaid.
* **`/docs/04-user-stories.md`**: El backlog completo de funcionalidades. Es la fuente para crear Issues.
* **`/docs/sprints/[sprint-number]-[sprint-name].md`**: La bitácora de cada sprint. Registra el alcance, decisiones, bloqueos y resultados.

---

## 3. Flujo de Trabajo en GitHub

### A. GitHub Projects (Kanban)

El tablero Kanban es la representación visual del trabajo.

* `Backlog`: Almacén de todas las tareas (Issues) no priorizadas para el sprint actual.
* `To Do (Sprint Actual)`: Tareas seleccionadas y comprometidas para el sprint en curso.
* `In Progress`: La tarea en la que se está trabajando activamente.
* `Done`: Tareas completadas y cerradas.

### B. Estructura de Issues: Épicas y Tareas

El trabajo se organiza en dos niveles:

1.  **Épicas (Issues "Padre"):**
    * **Qué son:** Issues de alto nivel que agrupan un conjunto de funcionalidades (ej. `Épica: Módulo 2 - Gestión de Citas`).
    * **Cómo se identifican:** Usan la etiqueta `Epic` 📚.
    * **Propósito:** Agrupar y ver el progreso general de un área a través de su checklist de tareas. **No se añaden al Kanban.**

2.  **Tareas (Sub-issues / Historias de Usuario):**
    * **Qué son:** Issues accionables que implementan una única historia de usuario (ej. `[Citas] Agendar una nueva cita`).
    * **Cómo se identifican:** Usan etiquetas de `Type`, `Module` y `Priority`.
    * **Propósito:** Es el trabajo real. **Estas son las issues que se añaden al Kanban** y se mueven a través de las columnas.

### C. La Plantilla de Issue Maestra

Cada `sub-issue` de tipo Tarea **debe** seguir esta estructura en su descripción:

```markdown
**Descripción:**
> [Aquí se pega una descripción para identificar el propósito de la tarea."]

---

### Criterios de Aceptación (AC)
*Se considera completada esta tarea CUANDO:*
- [ ] Criterio 1 (Define una condición medible y verificable).
- [ ] Criterio 2 (Ej: La acción A resulta en el efecto B).
- [ ] Criterio 3 (Ej: El usuario ve el mensaje C).

---

### Tareas Técnicas (Checklist de Implementación)
- [ ] Tarea técnica 1 (Ej: Crear el archivo de migración...).
- [ ] Tarea técnica 2 (Ej: Implementar el método X en el Controlador Y).
- [ ] Tarea técnica 3 (Ej: Escribir la prueba de funcionalidad Z).
````

### D. Sistema de Etiquetas (Labels)

Un sistema de etiquetas consistente es crucial para la organización.

#### Tipo de Tarea (Type)

*Indica la naturaleza del trabajo.*

  * `Type: Feature`: Nueva funcionalidad para el usuario.
  * `Type: Chore`: Tareas de mantenimiento, configuración o refactorización.
  * `Type: Bug`: Corrección de un error en el código existente.
  * `Type: Documentation`: Creación o actualización de la documentación.

#### Módulo de la Aplicación (Module)

*Asocia la tarea a un área específica del proyecto.*

  * `Module: Auth`: Autenticación, registro, perfiles de usuario.
  * `Module: Database`: Migraciones, seeders, cambios de esquema.
  * `Module: UI/UX`: Tareas de frontend, estilos, componentes visuales.
  * `Module: Citas`: Flujo de reserva, calendario, gestión de citas.
  * `Module: Lealtad`: Sellos, recompensas, cupones.
  * `Module: Admin (Nova)`: Tareas relacionadas con el panel de Laravel Nova.
  * `Module: Core`: Lógica de negocio principal, modelos, servicios.

#### Prioridad (Priority)

*Indica la urgencia de la tarea.*

  * `Priority: Critical` 🔴: Debe ser atendido inmediatamente.
  * `Priority: High` 🟠: Importante, para el sprint actual si es posible.
  * `Priority: Medium` 🟡: Prioridad normal.
  * `Priority: Low` 🟢: Tarea de baja urgencia.

#### Etiquetas Especiales

  * `Epic` 📚: Para identificar las Issues "Padre" que agrupan tareas.
  * `Sprint: 1`, `Sprint: 2`, etc. 🚀: Para agrupar todas las tareas de un sprint.
  * `Status: Blocked` 🚧: La tarea no puede continuar.
  * `Status: Needs Review` 👀: La tarea está completa y tiene un Pull Request abierto.

-----

## 4\. Ciclo de Vida de un Sprint

Un sprint es un ciclo de trabajo con un objetivo claro.

1.  **Planificación del Sprint:**

      * Se revisa el `Backlog` del Kanban y `/docs/04-user-stories.md`.
      * Se seleccionan las `Tareas` para el nuevo sprint.
      * Se crea una `Épica Maestra` para el sprint, enlazando todas las `Tareas` seleccionadas.
      * Se mueven las `Tareas` seleccionadas del `Backlog` a la columna `To Do (Sprint Actual)`.

2.  **Creación del Diario del Sprint:**

      * Se crea un nuevo archivo en `/docs/sprints/` (ej. `02-appointment-booking.md`).
      * El archivo **debe** crearse utilizando la siguiente plantilla para asegurar la consistencia:

      ```markdown
      # Diario del Sprint [Número]: [Nombre del Sprint]

      **Periodo:** [Fecha de Inicio] - [Fecha de Fin]

      **Épica Maestra en GitHub:** [Enlace a la Épica Maestra del Sprint]

      ---

      ## 1. Objetivo del Sprint

      [Describe aquí el objetivo principal y el resultado esperado del sprint en 1-2 frases.]

      ## 2. Alcance y Tareas Incluidas

      [Lista aquí, en formato de checklist, todas las issues/tareas que forman parte del sprint.]

      - [ ] `#IssueID - [Título de la Issue]`
      - [ ] `#IssueID - [Título de la Issue]`

      ---

      ## 3. Registro de Decisiones Técnicas

      *Esta sección es un log vivo. Se actualiza a medida que se toman decisiones durante el sprint.*

      *   **[FECHA]:** [Descripción de la decisión técnica.]
          *   **Razón:** [Justificación clara y concisa de por qué se tomó esa decisión.]

      ---

      ## 4. Registro de Bloqueos y Soluciones

      *Esta sección documenta los problemas inesperados y cómo se resolvieron.*

      *   **[FECHA]:**
          *   **Problema:** [Descripción del bloqueo.]
          *   **Solución:** [Cómo se resolvió el problema.]

      ---

      ## 5. Resultado del Sprint (A completar al final)

      *   **Tareas Completadas:** [ ] X de Y
      *   **Resumen:** [Escribe un resumen ejecutivo del resultado del sprint. ¿Se cumplió el objetivo?]
      *   **Aprendizajes / Retrospectiva:**
          *   **Qué funcionó bien:** [Anota los puntos positivos y las prácticas exitosas.]
          *   **Qué se puede mejorar:** [Identifica áreas de mejora para futuros sprints.]
      ```

3.  **Ejecución del Sprint:**

      * Se mueven las `Tareas` a través del Kanban.
      * Se documentan en vivo las decisiones y bloqueos en el diario del sprint.

4.  **Cierre y Retrospectiva:**

      * Al completar todas las `Tareas`, se cierra la `Épica Maestra`.
      * Se completa la sección "Resultado del Sprint" en el diario, anotando resúmenes y aprendizajes.
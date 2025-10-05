# Manifest del Proyecto: edd n'dev Portfolio

**Versión:** 1.0
**Fecha de Creación:** 2025-10-04
**Última Actualización:** 2025-10-04

---

## 1. Visión del Proyecto

**edd n'dev** es un portafolio web y plataforma de marca personal diseñada para establecer presencia digital, construir identidad de marca y compartir conocimiento con la comunidad de desarrollo web y marketing digital.

**No es:** Un funnel de conversión o generador de leads tradicional.

**Es:** Una huella digital auténtica que combina:
- Muestra de proyectos profesionales y open source
- Plataforma de contenido educativo (blog + recursos de aprendizaje)
- Expresión de identidad técnica y creativa
- Punto de contacto profesional

---

## 2. Objetivos Principales

1. **Construir Marca Personal:** Establecer edd n'dev como un estudio independiente reconocible en desarrollo web y marketing
2. **Compartir Conocimiento:** Crear contenido educativo de valor a través de tutoriales, experiencias y recursos
3. **Mostrar Expertise:** Presentar proyectos realizados (cliente + open source) con storytelling técnico
4. **Networking Profesional:** Facilitar conexiones profesionales auténticas sin presión comercial
5. **Experimentación Técnica:** Servir como playground para implementar animaciones avanzadas y tecnologías modernas

---

## 3. Alcance del Proyecto

### 3.1 Características Incluidas (MVP)

#### Sección: Hero / Landing
- Presentación visual impactante con animaciones GSAP + Lenis
- Branding claro de edd n'dev
- Call-to-action suave hacia contenido principal

#### Sección: Sobre Mí / Mi Historia
- Narrativa personal y filosofía de trabajo
- Skills y tecnologías visualizadas de forma creativa
- Timeline de experiencia (opcional)

#### Sección: Lo Que Hago
- Descripción de servicios/áreas de expertise (desarrollo web, marketing)
- Sin estructura de "paquetes" o precios (enfoque en capacidades)

#### Sección: Proyectos
- **Categoría 1:** Proyectos de Cliente
- **Categoría 2:** Proyectos Personales / Open Source
- **Información por proyecto:**
  - Descripción y contexto
  - Stack tecnológico usado
  - Screenshots/imágenes
  - Links a demo/repositorio (cuando aplique)
- **Filtros:** Por tecnología, tipo de proyecto, tags

#### Sección: Blog
- **Tipos de contenido:**
  - Tutoriales técnicos
  - Experiencias de desarrollo
  - Opinión técnica
  - Reflexiones sobre la industria
- Sistema de tags/categorías
- Buscador de contenido
- Formato: Markdown con syntax highlighting
- **NO incluye:** Sistema de comentarios, suscripción a newsletter

#### Sección: Aprendizaje / Recursos
- Cursos y guías educativas
- Recursos descargables (templates, cheatsheets, etc.)
- Organización por categorías/tags
- Posible integración futura con plataforma de cursos

#### Sección: Contacto
- Formulario de contacto simple
- Links a redes sociales/GitHub
- Información profesional (email, LinkedIn, etc.)

#### Características Técnicas
- **Smooth Scroll:** Implementado con Lenis
- **Animaciones:** Controladas por scroll usando GSAP + ScrollTrigger
- **Dark/Light Mode:** Dual theme completo
- **Responsive:** Mobile-first design
- **Performance:** Optimizado para Core Web Vitals
- **SEO:** Meta tags, Open Graph, Schema.org

### 3.2 Características NO Incluidas (Fuera del Alcance Inicial)

- Panel de administración (será un proyecto separado en subdominio)
- Sistema de comentarios en blog
- Newsletter/Email marketing
- E-commerce o venta de servicios
- Sistema de autenticación de usuarios
- Chat en vivo
- Traducción multiidioma (solo español en MVP)

### 3.3 Fases Futuras (Backlog Estratégico)

**Fase 2: CMS Headless**
- Panel admin en subdominio (admin.eddn.dev)
- API para gestión de contenido
- Editor Markdown con preview

**Fase 3: Plataforma de Aprendizaje**
- Sistema de cursos completo
- Progreso de usuario
- Certificados de finalización

**Fase 4: Comunidad**
- Comentarios en blog
- Foro de discusión
- Newsletter integrada

---

## 4. Stack Tecnológico

### Frontend
- **Framework:** Laravel 11 (Blade templating)
- **CSS:** Tailwind CSS 4.x
- **Animaciones:** GSAP 3.13 + Lenis 1.x
- **Build Tool:** Vite 7.x

### Backend (Fase Actual)
- **Framework:** Laravel 11
- **Base de Datos:** MySQL 8.x (para contenido dinámico futuro)
- **Storage:** Sistema de archivos local (para Markdown en MVP)

### Infraestructura
- **Hosting:** Apache (local dev), TBD para producción
- **Control de Versiones:** Git + GitHub
- **CI/CD:** TBD

---

## 5. Usuarios y Audiencia

### Perfil de Usuario Principal
- **Quién:** Desarrolladores, diseñadores, empresarios tech-savvy, reclutadores técnicos
- **Nivel Técnico:** Medio a avanzado
- **Motivación:** Conocer el trabajo de edd n'dev, aprender de contenido técnico, explorar proyectos
- **Comportamiento:** Navegación exploratoria, lectura profunda de artículos, revisión de código en proyectos

### Usuarios Secundarios
- Clientes potenciales evaluando capacidades
- Estudiantes/juniors buscando recursos de aprendizaje
- Peers buscando networking

---

## 6. Principios de Diseño

### Identidad Visual
- **Paleta de Colores:**
  - **Primarios:** Morados (violetas) y azules metálicos
  - **Requisito:** Deben funcionar perfectamente en light mode y dark mode
  - **Inspiración:** konpo.studio (como referente, no copia directa)
- **Tipografía:** TBD (System fonts vs custom fonts)
- **Estilo:** Moderno, limpio, con personalidad técnica pero creativa

### Experiencia de Animación
- **Filosofía:** Animaciones sutiles que mejoran la narrativa, no distraen
- **Técnicas:**
  - Scroll-triggered reveals
  - Parallax suave
  - Transiciones de estado fluidas
  - Micro-interacciones significativas
- **Performance:** 60fps garantizados, optimización mobile

### UX Core Principles
1. **Claridad sobre Creatividad:** Las animaciones no deben obstaculizar la lectura
2. **Accesibilidad:** Respeto a `prefers-reduced-motion`
3. **Speed:** Carga rápida, interacción inmediata
4. **Navegación Intuitiva:** Estructura clara sin necesidad de instrucciones

---

## 7. Métricas de Éxito

Dado que no es un sitio de conversión, las métricas son diferentes:

### Métricas Principales
- **Engagement:** Tiempo promedio en sitio (objetivo: >3 min)
- **Content Performance:** Páginas vistas en blog y recursos
- **Bounce Rate:** <50% en artículos de blog
- **Returning Visitors:** Tasa de retorno >20%

### Métricas Técnicas
- **Core Web Vitals:**
  - LCP: <2.5s
  - FID: <100ms
  - CLS: <0.1
- **Lighthouse Score:** >90 en todas las categorías

### Métricas de Contenido
- Artículos publicados por mes
- Recursos descargados
- Proyectos showcaseados

---

## 8. Restricciones y Consideraciones

### Restricciones Técnicas
- Debe funcionar en Apache (entorno actual)
- Compatible con navegadores modernos (últimas 2 versiones)
- Mobile-first (mayoría de tráfico esperado en móvil)

### Restricciones de Contenido
- Todo el contenido debe ser creado/curado manualmente (no generativo)
- Propiedad intelectual respetada en proyectos showcaseados
- GDPR-friendly (aunque no es el target principal)

### Restricciones de Tiempo
- MVP debe estar funcional para demostración de capacidades
- El CMS admin es un proyecto separado (no bloquea el lanzamiento)

---

## 9. Riesgos y Mitigaciones

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| Animaciones pesadas afectan performance | Media | Alto | Testing continuo, lazy loading, optimización progresiva |
| Contenido estático difícil de mantener | Alta | Medio | Markdown con estructura clara, documentación de proceso |
| Scope creep en diseño/animaciones | Alta | Medio | Definir límite de animaciones por sección en design system |
| Falta de contenido para blog | Media | Medio | Crear calendario editorial, tener 5 artículos pre-escritos para launch |

---

## 10. Roadmap de Alto Nivel

### Sprint 0: Fundación (Actual)
- [x] Instalación de dependencias (GSAP, Lenis)
- [ ] Documentación base (Manifest, Design System, Database Schema, User Stories)
- [ ] Setup de proyecto y estructura de archivos

### Sprint 1: Core Layout & Animations
- [ ] Sistema de design tokens en Tailwind
- [ ] Layout base con dark/light mode
- [ ] Navegación principal + footer
- [ ] Sistema de smooth scroll configurado
- [ ] Primeras animaciones de scroll

### Sprint 2: Home & About
- [ ] Hero section con animaciones
- [ ] Sección "Sobre mí" completa
- [ ] Sección "Lo que hago"
- [ ] Skills visualization

### Sprint 3: Proyectos
- [ ] Sistema de showcase de proyectos
- [ ] Filtros y búsqueda
- [ ] Páginas de detalle de proyecto
- [ ] Integración con GitHub API (para repos open source)

### Sprint 4: Blog Engine
- [ ] Sistema de parseo Markdown
- [ ] Listado de artículos
- [ ] Página de artículo individual
- [ ] Tags y categorías
- [ ] Buscador

### Sprint 5: Aprendizaje & Contacto
- [ ] Sección de recursos/cursos
- [ ] Formulario de contacto funcional
- [ ] Integración de redes sociales

### Sprint 6: Polish & Launch
- [ ] Optimización de performance
- [ ] SEO completo
- [ ] Testing cross-browser/device
- [ ] Deploy a producción

---

## 11. Definición de "Hecho" (Definition of Done)

Una feature se considera completa cuando:

- [ ] Código implementado y funcional
- [ ] Responsive en mobile, tablet, desktop
- [ ] Dark mode y light mode probados
- [ ] Animaciones optimizadas (60fps)
- [ ] Accesible (WCAG AA mínimo)
- [ ] Sin errores en consola
- [ ] Documentado (si es componente reutilizable)
- [ ] Testeado en Chrome, Firefox, Safari
- [ ] Merged a rama principal

---

## 12. Contacto y Stakeholders

**Owner del Proyecto:** Eduardo (edd n'dev)
**Rol:** Desarrollador, Diseñador, Content Creator
**Decisiones Finales:** Eduardo

---

**Última Revisión:** 2025-10-04
**Próxima Revisión:** Al completar Sprint 0

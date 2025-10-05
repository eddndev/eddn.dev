# Sistema de Diseño: edd n'dev Portfolio

**Versión:** 1.0
**Fecha de Creación:** 2025-10-04
**Inspiración Visual:** konpo.studio (adaptado a identidad propia)

---

## 1. Paleta de Colores

### Filosofía de Color

El sistema de colores de edd n'dev se construye sobre una base de **morados vibrantes** y **azules metálicos**, diseñado para funcionar perfectamente tanto en modo claro como oscuro. La paleta transmite modernidad, profesionalismo técnico y creatividad.

**Principios:**
- Contraste WCAG AA en todos los pares texto/fondo
- Transición fluida entre light/dark mode
- Colores saturados pero no agresivos
- Metallic sheen en azules para profundidad

### Colores Primarios: Purple (Morado)

Uso principal: Branding, CTAs, elementos destacados, links

```
- purple-50:  #faf5ff
- purple-100: #f3e8ff
- purple-200: #e9d5ff
- purple-300: #d8b4fe
- purple-400: #c084fc
- purple-500: #a855f7  ← Color principal de marca
- purple-600: #9333ea
- purple-700: #7e22ce
- purple-800: #6b21a8
- purple-900: #581c87
- purple-950: #3b0764
```

![purple-500](https://img.shields.io/badge/purple--500-a855f7?style=for-the-badge&logoColor=white&color=a855f7)

### Colores Secundarios: Blue Metallic (Azul Metálico)

Uso principal: Acentos técnicos, código, elementos interactivos

```
- blue-50:  #eff6ff
- blue-100: #dbeafe
- blue-200: #bfdbfe
- blue-300: #93c5fd
- blue-400: #60a5fa
- blue-500: #3b82f6  ← Azul base
- blue-600: #2563eb
- blue-700: #1d4ed8
- blue-800: #1e40af
- blue-900: #1e3a8a
- blue-950: #172554
```

![blue-600](https://img.shields.io/badge/blue--600-2563eb?style=for-the-badge&logoColor=white&color=2563eb)

### Colores de Acento: Cyan (Para highlights técnicos)

```
- cyan-400: #22d3ee  ← Highlights de código
- cyan-500: #06b6d4
- cyan-600: #0891b2
```

### Colores Neutrales: Slate (Textos y fondos)

Escala para textos, fondos, bordes y elementos estructurales

```
- slate-50:  #f8fafc  ← Fondo light mode
- slate-100: #f1f5f9
- slate-200: #e2e8f0
- slate-300: #cbd5e1  ← Bordes light
- slate-400: #94a3b8
- slate-500: #64748b  ← Texto secundario
- slate-600: #475569
- slate-700: #334155  ← Texto principal light
- slate-800: #1e293b
- slate-900: #0f172a  ← Fondo dark mode
- slate-950: #020617  ← Fondo dark profundo
```

### Colores Semánticos

- **Éxito (`success`):** ![Success](https://img.shields.io/badge/success-10b981?style=for-the-badge&logoColor=white&color=10b981) `#10b981` (green-500)
- **Peligro (`danger`):** ![Danger](https://img.shields.io/badge/danger-ef4444?style=for-the-badge&logoColor=white&color=ef4444) `#ef4444` (red-500)
- **Advertencia (`warning`):** ![Warning](https://img.shields.io/badge/warning-f59e0b?style=for-the-badge&logoColor=white&color=f59e0b) `#f59e0b` (amber-500)
- **Información (`info`):** ![Info](https://img.shields.io/badge/info-3b82f6?style=for-the-badge&logoColor=white&color=3b82f6) `#3b82f6` (blue-500)

### Mapeo: Modo Claro vs Modo Oscuro

| Uso Semántico | Modo Claro (`light`) | Modo Oscuro (`dark`) |
|---------------|----------------------|----------------------|
| **Fondo Principal** | `bg-slate-50` | `bg-slate-900` |
| **Fondo Secundario** | `bg-white` | `bg-slate-950` |
| **Fondo Tarjetas** | `bg-white` con `shadow-md` | `bg-slate-800/50` con `border border-slate-700` |
| **Texto Principal** | `text-slate-700` | `text-slate-100` |
| **Texto Secundario** | `text-slate-500` | `text-slate-400` |
| **Texto Terciario** | `text-slate-400` | `text-slate-500` |
| **Links** | `text-purple-600 hover:text-purple-700` | `text-purple-400 hover:text-purple-300` |
| **Bordes** | `border-slate-300` | `border-slate-700` |
| **Botón Primario** | `bg-purple-600 text-white hover:bg-purple-700` | `bg-purple-500 text-white hover:bg-purple-600` |
| **Botón Secundario** | `border-2 border-purple-600 text-purple-600` | `border-2 border-purple-400 text-purple-400` |
| **Code Background** | `bg-slate-100` | `bg-slate-950` |

---

## 2. Tipografía

### Fuentes

- **Fuente Principal:** `Inter` (Google Fonts)
  - Uso: Toda la UI, navegación, cuerpo de texto
  - Características: Moderna, legible, excelente para pantallas

- **Fuente Monoespaciada:** `JetBrains Mono` o `Fira Code`
  - Uso: Bloques de código, snippets técnicos
  - Características: Ligaduras de código, clara distinción de caracteres

### Escala Tipográfica

**Desktop:**
- **h1:** `text-6xl font-bold` (60px) - Títulos hero
- **h2:** `text-5xl font-bold` (48px) - Títulos de sección principal
- **h3:** `text-4xl font-semibold` (36px) - Subsecciones importantes
- **h4:** `text-3xl font-semibold` (30px) - Títulos de tarjetas
- **h5:** `text-2xl font-medium` (24px) - Subtítulos
- **h6:** `text-xl font-medium` (20px) - Encabezados menores
- **p (body):** `text-base font-normal leading-relaxed` (16px, line-height: 1.75)
- **small:** `text-sm` (14px) - Metadatos, labels
- **caption:** `text-xs` (12px) - Timestamps, disclaimers

**Mobile:**
- **h1:** `text-4xl font-bold` (36px)
- **h2:** `text-3xl font-bold` (30px)
- **h3:** `text-2xl font-semibold` (24px)
- **h4:** `text-xl font-semibold` (20px)
- **p (body):** `text-base` (16px)

### Pesos de Fuente

- `font-normal` (400) - Texto de cuerpo
- `font-medium` (500) - Énfasis suave
- `font-semibold` (600) - Subtítulos, labels
- `font-bold` (700) - Títulos, CTAs
- `font-extrabold` (800) - Hero text (uso ocasional)

---

## 3. Espaciado y Rejilla

### Sistema de Espaciado (Tailwind scale)

- `space-1`: 4px (0.25rem)
- `space-2`: 8px (0.5rem)
- `space-3`: 12px (0.75rem)
- `space-4`: 16px (1rem) ← Base unit
- `space-6`: 24px (1.5rem)
- `space-8`: 32px (2rem)
- `space-12`: 48px (3rem)
- `space-16`: 64px (4rem)
- `space-24`: 96px (6rem)
- `space-32`: 128px (8rem)

### Contenedores

- **Max Width Container:** `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`
- **Narrow Content:** `max-w-3xl mx-auto` (para artículos de blog)
- **Wide Content:** `max-w-screen-2xl mx-auto` (para galerías)

### Grid System

- **Grid de Proyectos:** `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8`
- **Grid de Blog:** `grid grid-cols-1 md:grid-cols-2 gap-6`
- **Grid de Skills:** `grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4`

### Breakpoints

```
sm: 640px   - Móviles grandes / Tablets pequeñas
md: 768px   - Tablets
lg: 1024px  - Laptops / Desktop pequeño
xl: 1280px  - Desktop
2xl: 1536px - Pantallas grandes
```

**Estrategia:** Mobile-first. Diseñar primero para móvil y escalar hacia arriba.

---

## 4. Componentes Clave

### Botones

**Primario:**
- **Uso:** Acciones principales (enviar formulario, CTA principal)
- **Estilo:**
```html
<button class="px-6 py-3 bg-purple-600 text-white font-semibold rounded-lg
               hover:bg-purple-700 active:bg-purple-800
               transition-colors duration-200
               focus:outline-none focus:ring-4 focus:ring-purple-300 dark:focus:ring-purple-800">
  Call to Action
</button>
```

**Secundario:**
- **Uso:** Acciones alternativas
- **Estilo:**
```html
<button class="px-6 py-3 border-2 border-purple-600 text-purple-600
               dark:border-purple-400 dark:text-purple-400
               font-semibold rounded-lg
               hover:bg-purple-50 dark:hover:bg-purple-950/30
               transition-all duration-200">
  Acción Secundaria
</button>
```

**Tertiary/Ghost:**
- **Uso:** Navegación, acciones sutiles
- **Estilo:**
```html
<button class="px-4 py-2 text-slate-700 dark:text-slate-300
               hover:text-purple-600 dark:hover:text-purple-400
               transition-colors duration-200">
  Ver más
</button>
```

### Links

```html
<a href="#" class="text-purple-600 dark:text-purple-400
                   hover:text-purple-700 dark:hover:text-purple-300
                   underline decoration-purple-300 dark:decoration-purple-600
                   underline-offset-4 hover:decoration-purple-500
                   transition-colors duration-200">
  Link de ejemplo
</a>
```

### Inputs de Formulario

**Input de Texto:**
```html
<input type="text"
       class="w-full px-4 py-3
              bg-white dark:bg-slate-800
              border-2 border-slate-300 dark:border-slate-600
              rounded-lg
              text-slate-700 dark:text-slate-200
              placeholder:text-slate-400
              focus:outline-none focus:border-purple-500 focus:ring-4 focus:ring-purple-200 dark:focus:ring-purple-900
              transition-all duration-200"
       placeholder="Escribe aquí...">
```

**Estado de Error:**
```html
<input class="border-red-500 focus:border-red-500 focus:ring-red-200">
<p class="mt-2 text-sm text-red-600 dark:text-red-400">Mensaje de error</p>
```

**Textarea:**
```html
<textarea rows="5" class="[mismas clases que input] resize-none"></textarea>
```

### Tarjetas (Cards)

**Card Base:**
```html
<div class="bg-white dark:bg-slate-800/50
            border border-slate-200 dark:border-slate-700
            rounded-xl p-6
            shadow-md hover:shadow-xl
            transition-all duration-300">
  <h3 class="text-xl font-semibold text-slate-800 dark:text-slate-100 mb-3">
    Título de la Tarjeta
  </h3>
  <p class="text-slate-600 dark:text-slate-300">
    Contenido de la tarjeta...
  </p>
</div>
```

**Card Interactiva (Proyecto):**
```html
<article class="group bg-white dark:bg-slate-800
                border border-slate-200 dark:border-slate-700
                rounded-xl overflow-hidden
                hover:border-purple-400 dark:hover:border-purple-500
                hover:shadow-2xl hover:scale-[1.02]
                transition-all duration-300 cursor-pointer">
  <div class="aspect-video bg-gradient-to-br from-purple-100 to-blue-100 dark:from-slate-900 dark:to-slate-800">
    <!-- Imagen del proyecto -->
  </div>
  <div class="p-6">
    <h3 class="text-xl font-semibold mb-2 group-hover:text-purple-600 dark:group-hover:text-purple-400">
      Nombre del Proyecto
    </h3>
    <p class="text-slate-600 dark:text-slate-400 text-sm">
      Descripción breve...
    </p>
  </div>
</article>
```

### Badges/Tags

```html
<!-- Tag de categoría -->
<span class="inline-block px-3 py-1
             bg-purple-100 dark:bg-purple-900/30
             text-purple-700 dark:text-purple-300
             text-xs font-medium rounded-full">
  React
</span>

<!-- Tag de tecnología -->
<span class="inline-block px-3 py-1
             bg-blue-100 dark:bg-blue-900/30
             text-blue-700 dark:text-blue-300
             text-xs font-medium rounded-full">
  Laravel
</span>
```

### Code Blocks

```html
<pre class="bg-slate-900 dark:bg-slate-950
            border border-slate-700
            rounded-lg p-6 overflow-x-auto">
  <code class="text-sm font-mono text-slate-100">
    // Código aquí
  </code>
</pre>
```

**Inline Code:**
```html
<code class="px-2 py-1 bg-slate-100 dark:bg-slate-800
             text-purple-600 dark:text-purple-400
             font-mono text-sm rounded">
  variable
</code>
```

---

## 5. Navegación

### Navbar Principal

```html
<nav class="sticky top-0 z-50
            bg-white/80 dark:bg-slate-900/80
            backdrop-blur-lg
            border-b border-slate-200 dark:border-slate-800">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">
      <!-- Logo -->
      <a href="/" class="text-2xl font-bold text-purple-600 dark:text-purple-400">
        edd n'dev
      </a>

      <!-- Nav Links -->
      <div class="hidden md:flex space-x-8">
        <a href="#" class="text-slate-700 dark:text-slate-300
                           hover:text-purple-600 dark:hover:text-purple-400
                           transition-colors">
          Proyectos
        </a>
        <!-- Más links... -->
      </div>

      <!-- Theme Toggle -->
      <button class="p-2 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800">
        <!-- Icon -->
      </button>
    </div>
  </div>
</nav>
```

### Footer

```html
<footer class="bg-slate-100 dark:bg-slate-950
               border-t border-slate-200 dark:border-slate-800
               py-12">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <!-- Contenido del footer -->
  </div>
</footer>
```

---

## 6. Iconografía

- **Librería:** Heroicons (outline style)
- **Tamaño por defecto:** `w-6 h-6` (24px)
- **Tamaño pequeño:** `w-4 h-4` (16px) - Para badges, inline
- **Tamaño grande:** `w-8 h-8` (32px) - Para features
- **Color:** Hereda del texto padre

### Iconos Comunes

| Contexto | Icono | Uso |
|----------|-------|-----|
| Menú móvil | `Bars3Icon` | Abrir menú hamburguesa |
| Cerrar | `XMarkIcon` | Cerrar modales, menú |
| Búsqueda | `MagnifyingGlassIcon` | Campo de búsqueda |
| Usuario | `UserIcon` | Perfil (si aplica) |
| GitHub | `CodeBracketIcon` | Link a repositorios |
| LinkedIn | Custom SVG | Link a LinkedIn |
| Email | `EnvelopeIcon` | Contacto |
| External Link | `ArrowTopRightOnSquareIcon` | Links externos |
| Código | `CommandLineIcon` | Sección de desarrollo |
| Diseño | `PaintBrushIcon` | Sección de diseño |

---

## 7. Sombras (Shadows)

```
- shadow-sm:  0 1px 2px 0 rgb(0 0 0 / 0.05)
- shadow:     0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1)
- shadow-md:  0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1)
- shadow-lg:  0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1)
- shadow-xl:  0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1)
- shadow-2xl: 0 25px 50px -12px rgb(0 0 0 / 0.25)
```

**Uso:**
- Tarjetas: `shadow-md` (normal), `shadow-xl` (hover)
- Modales: `shadow-2xl`
- Botones elevados: `shadow-lg`
- Navbar: `shadow-sm`

---

## 8. Bordes y Esquinas

### Border Radius

```
- rounded-none: 0px
- rounded-sm:   0.125rem (2px)
- rounded:      0.25rem (4px)
- rounded-md:   0.375rem (6px)
- rounded-lg:   0.5rem (8px)    ← Default para botones/inputs
- rounded-xl:   0.75rem (12px)  ← Default para cards
- rounded-2xl:  1rem (16px)     ← Para secciones grandes
- rounded-full: 9999px          ← Para badges circulares, avatares
```

### Border Width

```
- border:   1px (default)
- border-2: 2px (para inputs focus, botones secundarios)
- border-4: 4px (para focus rings)
```

---

## 9. Animaciones y Transiciones

### Duraciones

```css
- duration-150: 150ms  (micro-interacciones)
- duration-200: 200ms  (hover, cambios de color)
- duration-300: 300ms  (transiciones estándar)
- duration-500: 500ms  (cambios de estado grandes)
```

### Easing

```css
- ease-in:     cubic-bezier(0.4, 0, 1, 1)
- ease-out:    cubic-bezier(0, 0, 0.2, 1)     ← Preferido para UI
- ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)   ← Default
```

### Propiedades Comunes

```html
<!-- Hover en botones -->
<button class="transition-colors duration-200">

<!-- Cards con escala -->
<div class="transition-all duration-300 hover:scale-105">

<!-- Fade in/out -->
<div class="transition-opacity duration-300">
```

### Animaciones GSAP (Scroll-triggered)

**Fade Up:**
```javascript
gsap.from('.fade-up', {
  scrollTrigger: '.fade-up',
  y: 50,
  opacity: 0,
  duration: 0.8,
  ease: 'power2.out'
});
```

**Stagger Grid:**
```javascript
gsap.from('.project-card', {
  scrollTrigger: {
    trigger: '.projects-grid',
    start: 'top 80%'
  },
  y: 100,
  opacity: 0,
  duration: 0.6,
  stagger: 0.1,
  ease: 'power3.out'
});
```

**Parallax Suave:**
```javascript
gsap.to('.parallax-element', {
  scrollTrigger: {
    trigger: '.parallax-element',
    scrub: 1
  },
  y: -100,
  ease: 'none'
});
```

---

## 10. Accesibilidad (A11y)

### Directrices Obligatorias

1. **Contraste de Colores:**
   - Texto normal: Mínimo 4.5:1 (WCAG AA)
   - Texto grande (18px+): Mínimo 3:1
   - Validar con: https://contrast-ratio.com

2. **Focus States:**
   - Todos los elementos interactivos: `focus:outline-none focus:ring-4 focus:ring-purple-300`
   - Nunca quitar focus sin proveer alternativa visual

3. **Motion Preferences:**
```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

4. **Tamaños Touch:**
   - Mínimo 44x44px para elementos táctiles (botones, links)

5. **Semántica HTML:**
   - Usar `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`
   - Headings jerárquicos (no saltar niveles)

6. **Textos Alternativos:**
   - Todas las imágenes con `alt` descriptivo
   - Iconos decorativos: `aria-hidden="true"`

---

## 11. Responsive Design

### Estrategia: Mobile-First

**Principios:**
1. Diseñar primero para móvil (320px+)
2. Escalar progresivamente hacia desktop
3. Touch-first en móvil, hover en desktop
4. Content prioritization en pantallas pequeñas

### Patrones Responsivos

**Tipografía:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
  Título Responsive
</h1>
```

**Espaciado:**
```html
<section class="py-12 md:py-20 lg:py-32">
```

**Grid:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 lg:gap-8">
```

**Navegación:**
```html
<!-- Móvil: Hamburger menu -->
<!-- Desktop: Horizontal nav -->
<div class="md:hidden"> <!-- Mobile menu --> </div>
<div class="hidden md:flex"> <!-- Desktop nav --> </div>
```

---

## 12. Design Tokens (Tailwind Config)

```javascript
// tailwind.config.js
export default {
  theme: {
    extend: {
      colors: {
        purple: {
          // Escala completa definida arriba
        },
        blue: {
          // Escala completa definida arriba
        }
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', 'sans-serif'],
        mono: ['JetBrains Mono', 'Fira Code', 'monospace'],
      },
      animation: {
        'fade-in': 'fadeIn 0.5s ease-out',
        'slide-up': 'slideUp 0.6s ease-out',
      },
      keyframes: {
        fadeIn: {
          '0%': { opacity: '0' },
          '100%': { opacity: '1' },
        },
        slideUp: {
          '0%': { transform: 'translateY(20px)', opacity: '0' },
          '100%': { transform: 'translateY(0)', opacity: '1' },
        }
      }
    }
  }
}
```

---

## 13. Recursos

- **Paleta de Colores:** https://uicolors.app (para generar variantes)
- **Contraste:** https://contrast-ratio.com
- **Fuentes:**
  - Inter: https://fonts.google.com/specimen/Inter
  - JetBrains Mono: https://www.jetbrains.com/lp/mono/
- **Iconos:** https://heroicons.com
- **Inspiración:** konpo.studio (referencia visual)

---

**Notas Finales:**

Este design system es un documento vivo. Se actualizará conforme se descubran nuevos patrones durante la implementación. Todos los componentes deben seguir estos lineamientos para mantener consistencia visual y de código.

**Próximos Pasos:**
1. Implementar tokens en Tailwind config
2. Crear componentes Blade reutilizables
3. Configurar dark mode con `class` strategy
4. Documentar componentes adicionales conforme se creen

# edd n'dev Portfolio

![Status](https://img.shields.io/badge/status-in%20development-yellow)
![Laravel](https://img.shields.io/badge/Laravel-12-red)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-4.x-38bdf8)
![License](https://img.shields.io/badge/license-MIT-green)

**Portafolio web y plataforma de marca personal** para edd n'dev, un estudio independiente de desarrollo web y marketing digital.

Este proyecto combina un portafolio profesional, blog técnico y plataforma de recursos educativos con animaciones avanzadas controladas por scroll.

---

## 🎯 Visión del Proyecto

**edd n'dev** no es un funnel de conversión tradicional. Es una **huella digital auténtica** que:

- 🚀 Muestra proyectos profesionales y open source
- 📝 Comparte conocimiento a través de blog y recursos educativos
- 💼 Establece presencia profesional sin presión comercial
- ✨ Experimenta con animaciones modernas y tecnologías de vanguardia

---

## 🛠️ Stack Tecnológico

### Frontend
- **Framework:** Laravel 12 (Blade Templating)
- **CSS:** Tailwind CSS 4.x
- **Animaciones:** GSAP 3.13 + ScrollTrigger
- **Smooth Scroll:** Lenis 1.x
- **Build Tool:** Vite 7.x

### Backend
- **Framework:** Laravel 12
- **Base de Datos:** MySQL 8.x
- **ORM:** Eloquent
- **Cache:** Redis (producción) / File (desarrollo)

### Infraestructura
- **Dev Server:** Apache (XAMPP/Local)
- **Control de Versiones:** Git + GitHub
- **Metodología:** Docs-First Development

---

## 🎨 Características Principales

### ✨ Experiencia Visual
- Animaciones suaves controladas por scroll (GSAP + Lenis)
- Dark/Light mode completo
- Diseño responsive mobile-first
- Performance optimizado (Core Web Vitals)

### 📄 Secciones del Sitio
- **Hero/Landing:** Presentación impactante con animaciones
- **Sobre Mí:** Historia personal, skills, experiencia
- **Servicios:** Desarrollo web y marketing
- **Portafolio:** Proyectos de cliente y open source
- **Blog:** Tutoriales, experiencias, opinión técnica
- **Recursos:** Cursos, guías, templates descargables
- **Contacto:** Formulario simple + links sociales

### 🔧 Funcionalidades Técnicas
- Sistema de tags unificado para blog/proyectos/recursos
- Buscador de contenido fulltext
- Filtros por tecnología y categoría
- Integración con GitHub API (repos open source)
- Sistema de caché robusto
- SEO optimizado (meta tags, Open Graph, Schema.org)

---

## 📚 Documentación

El proyecto sigue la metodología **Docs-First**. Toda la documentación vive en `/docs/`:

- **[01-manifest.md](docs/01-manifest.md)**: Visión, objetivos y alcance del proyecto
- **[02-design-system.md](docs/02-design-system.md)**: Paleta de colores, tipografía, componentes
- **[03-database-schema.md](docs/03-database-schema.md)**: Esquema de base de datos completo
- **[04-user-stories.md](docs/04-user-stories.md)**: Historias de usuario y backlog
- **[AGENTS.md](docs/AGENTS.md)**: Estándar de gestión de proyecto

### Paleta de Colores

El diseño se basa en **morados vibrantes** y **azules metálicos**, optimizados para light y dark mode:

- **Primary:** Purple (#a855f7)
- **Secondary:** Blue (#2563eb)
- **Neutral:** Slate (textos y fondos)

---

## 🚀 Instalación Local

### Requisitos Previos

- PHP 8.2+
- Composer
- Node.js 18+ y npm
- MySQL 8.x
- Apache/Nginx

### Pasos de Instalación

1. **Clonar el repositorio**
```bash
git clone https://github.com/tuusuario/eddn.dev.git
cd eddn.dev
```

2. **Instalar dependencias PHP**
```bash
composer install
```

3. **Instalar dependencias JavaScript**
```bash
npm install
```

4. **Configurar variables de entorno**
```bash
cp .env.example .env
php artisan key:generate
```

Editar `.env` con tus credenciales de base de datos:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=eddn_dev
DB_USERNAME=root
DB_PASSWORD=
```

5. **Crear base de datos**
```bash
# En MySQL
CREATE DATABASE eddn_dev CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

6. **Ejecutar migraciones y seeders**
```bash
php artisan migrate --seed
```

7. **Crear symlink para storage**
```bash
php artisan storage:link
```

8. **Compilar assets**
```bash
# Desarrollo
npm run dev

# Producción
npm run build
```

9. **Levantar servidor de desarrollo**
```bash
php artisan serve
```

El sitio estará disponible en: `http://localhost:8000`

---

## 📦 Estructura del Proyecto

```
eddn.dev/
├── app/
│   ├── Http/Controllers/      # Controladores
│   ├── Models/                 # Modelos Eloquent
│   └── View/Components/        # Componentes Blade
├── database/
│   ├── migrations/             # Migraciones
│   ├── seeders/                # Seeders
│   └── factories/              # Factories para testing
├── docs/                       # 📚 Documentación del proyecto
│   ├── 01-manifest.md
│   ├── 02-design-system.md
│   ├── 03-database-schema.md
│   ├── 04-user-stories.md
│   └── AGENTS.md
├── resources/
│   ├── css/                    # Estilos Tailwind
│   ├── js/
│   │   └── app.js             # Entry point (GSAP + Lenis)
│   └── views/                  # Vistas Blade
├── public/
│   └── storage/                # Symlink a storage/app/public
├── routes/
│   └── web.php                 # Rutas del sitio
├── tailwind.config.js          # Configuración de Tailwind
├── vite.config.js              # Configuración de Vite
└── package.json                # Dependencias Node
```

---

## 🎯 Roadmap

### ✅ Sprint 0: Fundación (Actual)
- [x] Instalación de GSAP y Lenis
- [x] Documentación base completa
- [ ] Setup de estructura de archivos

### 📋 Sprint 1: Core Layout & Animations
- [ ] Sistema de design tokens en Tailwind
- [ ] Layout base con dark/light mode
- [ ] Navegación principal + footer
- [ ] Smooth scroll configurado
- [ ] Primeras animaciones de scroll

### 📋 Sprint 2: Home & About
- [ ] Hero section con animaciones
- [ ] Sección "Sobre mí" completa
- [ ] Sección "Lo que hago"
- [ ] Skills visualization

### 📋 Sprint 3: Proyectos
- [ ] Sistema de showcase de proyectos
- [ ] Filtros y búsqueda
- [ ] Páginas de detalle
- [ ] Integración con GitHub API

### 📋 Sprint 4: Blog & API
- [ ] Modelos y migraciones
- [ ] Listado y detalle de posts
- [ ] Tags y categorías
- [ ] Buscador
- [ ] Sistema de caché

### 📋 Sprint 5: Recursos & Contacto
- [ ] Sección de recursos/cursos
- [ ] Formulario de contacto
- [ ] Integración de redes sociales

### 📋 Sprint 6: Polish & Launch
- [ ] Optimización de performance
- [ ] SEO completo
- [ ] Testing cross-browser
- [ ] Deploy a producción

---

## 🧪 Testing

```bash
# Ejecutar tests
php artisan test

# Con coverage
php artisan test --coverage

# Tests específicos
php artisan test --filter=BlogTest
```

---

## 📈 Performance Targets

- **LCP (Largest Contentful Paint):** < 2.5s
- **FID (First Input Delay):** < 100ms
- **CLS (Cumulative Layout Shift):** < 0.1
- **Lighthouse Score:** > 90 en todas las categorías
- **Animaciones:** 60fps garantizados

---

## 🔐 Seguridad

- ✅ Validación de inputs con FormRequests
- ✅ Sanitización de contenido HTML (HTMLPurifier)
- ✅ Rate limiting en formulario de contacto
- ✅ CSRF protection (Laravel default)
- ✅ XSS protection con Blade escaping
- ✅ SQL Injection prevention (Eloquent ORM)

---

## 🤝 Contribuciones

Este es un proyecto personal de portafolio, pero si encuentras bugs o tienes sugerencias:

1. Abre un **Issue** describiendo el problema/sugerencia
2. Si quieres contribuir código:
   - Fork el proyecto
   - Crea una rama (`git checkout -b feature/amazing-feature`)
   - Commit tus cambios (`git commit -m 'Add amazing feature'`)
   - Push a la rama (`git push origin feature/amazing-feature`)
   - Abre un Pull Request

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Ver el archivo [LICENSE](LICENSE) para más detalles.

---

## 👤 Autor

**Eduardo (edd n'dev)**
- Portfolio: [eddn.dev](https://eddn.dev) (en construcción)
- GitHub: [@tu-usuario](https://github.com/tu-usuario)
- LinkedIn: [Tu LinkedIn](https://linkedin.com/in/tu-perfil)
- Email: [tu@email.com](mailto:tu@email.com)

---

## 🙏 Agradecimientos

- **Inspiración Visual:** [konpo.studio](https://konpo.studio)
- **Animaciones:** GSAP + Lenis
- **Framework:** Laravel Team
- **Comunidad:** Todos los que comparten conocimiento

---

## 📝 Notas de Desarrollo

### Comandos Útiles

```bash
# Limpiar caché
php artisan cache:clear
php artisan config:clear
php artisan view:clear

# Regenerar autoload
composer dump-autoload

# Optimizar para producción
php artisan config:cache
php artisan route:cache
php artisan view:cache

# Compilar assets para producción
npm run build
```

### Convenciones de Código

- **Branches:** `feature/nombre`, `fix/nombre`, `docs/nombre`
- **Commits:** Mensajes descriptivos en inglés
- **Código:** PSR-12 coding standard
- **Base de Datos:** Snake_case para tablas y columnas
- **Rutas:** Kebab-case para URLs (`/blog/mi-articulo`)

---

**Construido con ❤️ usando Laravel, Tailwind, GSAP y mucho café ☕**

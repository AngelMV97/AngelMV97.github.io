# Sistema de Doble Portafolio - LuAng's

## Descripción General

Sitio oficial con **dos versiones del portafolio** que conviven en el mismo repositorio:

1. **Data Science Portfolio** (`index.html`) - Versión original
2. **Game Development Portfolio** (`gamedev.html`) - Versión con diseño moderno

## Estructura de Archivos

```
AngelMV97.github.io/
├── index.html                    # Portafolio Data Science (original)
├── gamedev.html                  # Portafolio Game Development
├── css/
│   └── style.css                # Estilos compartidos + componentes personalizados
├── js/
│   └── main.js                  # JavaScript con carrusel de portfolio
├── images/
│   └── gamedev/                 # Imágenes específicas de Game Dev
│       ├── hero-bg.gif
│       ├── WOBBLEHEAD.png
│       ├── 3d-design.jpeg
│       ├── cattle-herding.png
│       ├── plane-programming.png
│       ├── gamedev-about.jpg
│       ├── unity-logo.png
│       ├── csharp-logo.png
│       ├── blender-logo.png
│       └── git-logo.png
└── ... (otros archivos)
```

## Cómo Funciona

### Toggle Button

Ambas versiones incluyen un **botón circular compacto** (42px) en la esquina superior derecha para cambiar entre portafolios:

- **En index.html**: Ícono de caja 📦 → "Switch to Data Science Portfolio"
- **En gamedev.html**: Ícono de control de juego 🎮 → "Switch to Game Dev Portfolio"

### Características del Toggle

- **Tamaño compacto**: 42px de diámetro (encaja en navbar)
- **Posición fija**: Top: 18px, Right: 20px
- **Estilo moderno**: Fondo rojo (#d63447) con sombra
- **Responsive**: 38px en móviles
- **Efecto hover**: Elevación y escala con sombra intensificada

## URLs de Acceso

- **Data Science**: https://angelmv97.github.io/ (o index.html)
- **Game Development**: https://angelmv97.github.io/gamedev.html

## Características de Diseño

### Portafolio de Game Development (gamedev.html)

#### 🎨 Hero Section
- **Fondo animado**: GIF de videojuego (hero-bg.gif)
- **Iconos sociales con efecto luminoso**: 
  - GitHub, LinkedIn, Itch.io, WhatsApp
  - Contorno brillante con sombra gradiente azul/morado
  - Efecto hover que intensifica el brillo
  - Diseño similar a los skill badges

#### 📁 Portfolio Section (Carrusel Elegante)
- **Diseño de carrusel** con Owl Carousel:
  - Imagen grande del proyecto a la izquierda (col-lg-6)
  - Descripción detallada a la derecha (col-lg-6)
  - 4 proyectos: WOBBLEHEADS Game Jam, 3D Environment Design, Cattle Herding, Plane Programming
  - Botones de enlace (GitHub/Itch.io) que aparecen al hacer hover
  - Navegación personalizada con botones circulares
  - Transiciones suaves con fade in/out
  - Dots indicadores personalizados

**Proyectos destacados:**
1. **WOBBLEHEADS (Game Jam)**: Juego multijugador 3D con mecánica de insultos
2. **3D Environment Design**: Pipeline completo de diseño de entorno (~61k a <19k triángulos)
3. **Cattle Herding**: Implementación custom con Unity Learn assets (2-player multiplayer)
4. **Plane Programming**: Extensión de Unity Learn challenge con física mejorada

#### 🎯 Skills Section
- **Logo carousel**: Unity, C#, Blender, Git
- **Skills badges con diseño moderno**:
  - Low-poly Modeling, Modular Environment Design, Level Design
  - UV Mapping, Material Authoring
  - Unity Input System, Game State Management, Physics-Based Gameplay
  - Gradiente morado/azul, sombras, efectos hover
  - Diseño responsive

#### 📐 About Me Section
- **Proporción ajustada**: Imagen 5 columnas / Descripción 6 columnas
- **Imagen optimizada**: 512x384px
- **Descripción extendida** con enfoque en game development

#### 🧭 Navegación
- **Secciones**: Home, About, Portfolio, Skills
- **Eliminado**: Contact section (completa)
- **Menú limpio** y consistente

#### 📏 Footer Compacto
- **Altura reducida**: 200px (antes 400px)
- **Enlaces sociales**: GitHub, LinkedIn, Itch.io, WhatsApp
- **Copyright**: Colorlib template attribution

### Optimizaciones de Diseño

- **Espaciado reducido**: Padding de secciones de 3.5rem a 2rem
- **Títulos consistentes**: Todos con mismo formato (heading-h2 + divider)
- **Carrusel responsive**: Ajusta diseño en tablets y móviles
- **Sin errores de sintaxis**: HTML y CSS validados

## Recursos Compartidos

Ambos portafolios comparten:
- **CSS**: Archivo único con estilos base + componentes personalizados
- **JavaScript**: Funciones compartidas + inicialización del carrusel
- **Vendor Libraries**: Bootstrap, Owl Carousel, jQuery, AOS, Jarallax
- **Iconos**: Icons8 CDN + Icomoon font icons

## Tecnologías Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript (ES6)
- **Framework CSS**: Bootstrap 4
- **Carrusel**: Owl Carousel 2
- **Animaciones**: AOS (Animate On Scroll), GSAP
- **Parallax**: Jarallax
- **Iconos**: Icons8, Icomoon
- **Hosting**: GitHub Pages

## Componentes Personalizados CSS

### Portfolio Carousel
```css
.portfolio-carousel-wrapper
.portfolio-slide
.portfolio-image-wrapper
.project-links
.portfolio-content
.portfolio-nav
```

### Skills Badges
```css
.skills-list
.skill-badge (con gradiente y hover effects)
```

### Social Icons
```css
.hero-social-icons
.social-icon (con efecto luminoso)
```

### Toggle Button
```css
.portfolio-toggle (42px, responsive)
```

## Deployment

### Actualizar GitHub Pages

1. **Verificar cambios:**
```bash
git status
```

2. **Agregar archivos:**
```bash
git add .
```

3. **Hacer commit:**
```bash
git commit -m "Actualización de portfolio con carrusel y mejoras de diseño"
```

4. **Push a GitHub:**
```bash
git push origin main
```

GitHub Pages se actualiza automáticamente en 1-2 minutos.

## Mantenimiento

### Agregar Nuevo Proyecto al Carrusel

Edita `gamedev.html` y agrega un nuevo slide dentro de `.owl-carousel.portfolio-carousel`:

```html
<div class="portfolio-slide">
  <div class="row align-items-center">
    <div class="col-lg-6 mb-4 mb-lg-0">
      <div class="portfolio-image-wrapper">
        <img src="images/gamedev/tu-proyecto.png" alt="Proyecto" class="img-fluid">
        <div class="project-links">
          <a href="TU_URL" target="_blank" class="project-link">
            <span class="icon-link2"></span> Ver Proyecto
          </a>
        </div>
      </div>
    </div>
    <div class="col-lg-6">
      <div class="portfolio-content">
        <span class="project-number">05</span>
        <h3 class="project-title">Nombre del Proyecto</h3>
        <p class="project-intro">Descripción...</p>
        <p class="project-tech"><em>Technologies: ...</em></p>
      </div>
    </div>
  </div>
</div>
```

### Actualizar Skills

Edita la sección `.skills-list` en `gamedev.html`:

```html
<span class="skill-badge">Nueva Habilidad</span>
```

## Testing Local

Prueba localmente antes de hacer push:

```bash
# Windows
start gamedev.html

# O usa Live Server extension en VS Code
```

## Contacto y Links

- **Portfolio Data Science**: https://angelmv97.github.io/
- **Portfolio Game Dev**: https://angelmv97.github.io/gamedev.html
- **GitHub**: https://github.com/AngelMV97
- **LinkedIn**: https://www.linkedin.com/in/luangmv-developer/
- **Itch.io**: https://angelmv97.itch.io/

---

**Template original**: Colorlib (Licensed under CC BY 3.0)  
**Personalización y desarrollo**: Luis Angel Motta Valero  
**Última actualización**: 2026-07-01

## Mantenimiento

### Actualizar Información de Contacto
Si cambias tu información de contacto, actualiza **ambos archivos**:
- `index.html` (líneas ~566-588)
- `gamedev.html` (líneas ~566-588)

### Agregar Nuevo Proyecto

**Para Data Science (index.html)**:
1. Localiza la sección `<div id="posts" class="row...">`
2. Duplica un `<div class="item web branding...">`
3. Actualiza contenido e imagen

**Para Game Dev (gamedev.html)**:
1. Mismo proceso que arriba
2. Usa imágenes relevantes a videojuegos

### Cambiar Estilos

Los estilos del toggle se encuentran al final de `css/style.css` (líneas ~1971+):
```css
/* Portfolio Toggle Switch */
.portfolio-toggle { ... }
```

## Compatibilidad

- ✅ Responsive design (mobile, tablet, desktop)
- ✅ Compatible con GitHub Pages
- ✅ Sin dependencias adicionales
- ✅ Usa los mismos recursos que la versión original

## SEO Considerations

Ambas páginas tienen meta tags diferenciados:
- **index.html**: "data science, AI, machine learning"
- **gamedev.html**: "unity, blender, game development, 3d modeling"

## Notas Finales

- Los estilos del toggle son responsive y se adaptan a móviles
- El CV enlazado es el mismo en ambas versiones (puedes crear uno específico para Game Dev)
- Las redes sociales en el footer se comparten (actualiza según prefieras)
- Ambas versiones mantienen el mismo estilo visual y diseño

# 🔄 Continuation Guide - Pasión Frutos Secos

## 📋 **Template para Nuevas Conversaciones con Claude**

### **🎯 Contexto Inicial Obligatorio**
```markdown
Hola Claude! Estoy continuando el desarrollo de la tienda Shopify "Pasión Frutos Secos".

**Proyecto:** Tienda premium frutos secos gourmet
**GitHub:** https://github.com/KnuppeArt/pasion-frutos-secos-shopify
**Estado actual:** [Consultar DEVELOPMENT_LOG.md]
**Última sesión:** 2025-07-20 (GitHub setup completado)

**Necesito continuar con:** [Especificar componente/tarea]

¿Puedes revisar los archivos del repositorio para ponerte al día con el proyecto?
```

### **📁 Archivos de Referencia Obligatorios**
1. **README.md** - Overview completo del proyecto
2. **DEVELOPMENT_LOG.md** - Log detallado de cada sesión
3. **sections/hero-integrated.liquid** - Componente principal desarrollado
4. **Este archivo** - Guía de continuidad

---

## 🎯 **Información Clave del Proyecto**

### **Identidad de Marca**
- **Nombre:** Pasión Frutos Secos
- **Valores:** Premium, natural, confiable  
- **Propuesta:** "Excelencia en materia prima"
- **Estilo:** Minimalista mediterráneo, UX impecable

### **Stack Técnico**
- **Plataforma:** Shopify
- **Tema:** Dawn (personalizado)
- **Approach:** Custom sections + admin controls
- **Responsive:** Mobile-first
- **Performance:** Optimizado velocidad

### **Estructura Páginas**
```
Homepage: Hero + Categorías + Productos + Banner + Instagram + Footer
Tienda: Banner + Filtros + Grid productos + Footer
Sobre Nosotros: [Pendiente]
Contacto: [Pendiente]  
Blog: [Pendiente]
```

---

## ✅ **Estado Actual Desarrollo**

### **🎉 COMPLETADO:**

#### **Hero Integrado (v1.0)**
- ✅ **Navegación:** Transparente integrada + sticky glassmorphism
- ✅ **Overlay:** Sistema gradientes 7 direcciones + sólido
- ✅ **Responsive:** Mobile-first perfecto
- ✅ **Admin:** 68 controles configurables
- ✅ **Performance:** Optimizado + accessibility

**📁 Archivo:** `sections/hero-integrated.liquid` (902 líneas)
**🏷️ Tag:** `v1.0-hero`

#### **GitHub Repository (v1.0)**
- ✅ **Estructura:** Repositorio profesional completo
- ✅ **Documentación:** README + Log + Guía continuidad
- ✅ **Templates:** Issues, PRs, bug reports
- ✅ **Workflow:** Commits semánticos establecido

### **⏳ PENDIENTE:**

#### **Próxima Prioridad: Sección Categorías**
- ❌ Análisis referencias + diseño
- ❌ Grid responsive 3 columnas
- ❌ Hover effects + animaciones  
- ❌ Admin controls (imagen, título, enlace)
- ❌ Mobile optimization

#### **Siguientes Componentes:**
- ❌ Productos destacados con beneficios salud
- ❌ Banner anuncio personalizable
- ❌ Instagram feed integration
- ❌ Footer premium completo

---

## 📋 **Templates para Desarrollo**

### **🔥 Template Nueva Sección**
```markdown
## Nueva Sección: [NOMBRE]

### Contexto
**Objetivo:** [Descripción funcionalidad necesaria]
**Referencia:** [Enlaces o descripción estilo deseado]
**Prioridad:** [Alta/Media/Baja]

### Requisitos Técnicos
- [ ] Responsive mobile-first
- [ ] Admin controls configurables
- [ ] Performance optimized
- [ ] Accessibility compliant
- [ ] Consistent con hero style

### Funcionalidades Específicas
- [ ] [Lista funcionalidades necesarias]
- [ ] [Una por línea para tracking]

### Admin Controls Deseados
- [ ] [Especificar controles Shopify admin necesarios]
- [ ] [Colores, textos, imágenes, etc.]

### Archivos Afectados
- **Nuevo:** `sections/[nombre-seccion].liquid`
- **Modificar:** `templates/index.json` (si es homepage)
```

### **🐛 Template Reporte Bug**
```markdown
## Bug: [DESCRIPCIÓN CORTA]

### Problema
**Síntoma:** [Qué está pasando]
**Esperado:** [Qué debería pasar]
**Dispositivo:** [Mobile/Desktop/Ambos]

### Reproducción
1. [Pasos para reproducir]
2. [Uno por línea]
3. [Incluir screenshots si es posible]

### Contexto Técnico
**Archivo:** [Archivo donde probablemente está el bug]
**Sección:** [Líneas aproximadas si se conoce]
**Navegador:** [Chrome/Safari/Firefox/etc.]

### Urgencia
- [ ] 🔴 Crítico (rompe funcionalidad)
- [ ] 🟡 Alto (impacta UX)
- [ ] 🟢 Bajo (mejora visual)
```

### **💡 Template Nueva Feature**
```markdown
## Feature Request: [NOMBRE]

### Descripción
**Qué:** [Descripción de la funcionalidad]
**Por qué:** [Justificación/beneficio]
**Dónde:** [En qué página/sección]

### Especificaciones
- **Design:** [Como debería verse]
- **Interaction:** [Como debería comportarse]
- **Mobile:** [Consideraciones mobile específicas]
- **Admin:** [Qué debería ser configurable]

### Referencias
- [Links a ejemplos similares]
- [Screenshots o mockups si hay]

### Prioridad & Timeline
**Prioridad:** [1-5, siendo 1 más urgente]
**Timeline:** [Cuándo se necesita]
**Dependencias:** [Si depende de otros componentes]
```

---

## 🔧 **Información Técnica Crítica**

### **Estructura Z-index Establecida**
```css
/* NUNCA cambiar sin documentar */
.hero-bg-image: 1          /* Background image */
.hero-bg-overlay: 2        /* Overlay gradients */  
.hero-content: 3           /* Text content */
.hero-nav: 100             /* Navigation normal */
.hero-nav.scrolled: 1000   /* Sticky navigation */
.mobile-menu-overlay: 9999 /* Mobile menu */
```

### **Variables CSS Principales**
```css
/* Mantener consistencia */
--primary-color: #8b4513     /* Brown principal */
--text-color: #2c3e37        /* Text dark */
--nav-text-color: #2c3e37    /* Navigation text */
--nav-hover-color: #8b4513   /* Navigation hover */
```

### **Breakpoints Responsive**
```css
/* Mobile first approach */
@media (max-width: 480px)  /* Mobile small */
@media (max-width: 768px)  /* Mobile + tablet */
@media (min-width: 769px)  /* Desktop */
```

### **Convenciones Naming**
```liquid
<!-- Secciones: kebab-case -->
sections/hero-integrated.liquid
sections/categories-section.liquid
sections/featured-products.liquid

<!-- CSS Classes: kebab-case con prefijo componente -->
.hero-nav, .hero-content, .hero-bg-overlay
.categories-grid, .categories-card
.products-featured, .products-card

<!-- Admin Settings: snake_case -->
section.settings.bg_color
section.settings.overlay_type  
section.settings.gradient_direction
```

---

## 📝 **Workflow de Commits**

### **Estructura Commits Semánticos**
```
feat: add [component] with [main-features]
fix: resolve [issue] in [component]  
docs: update [documentation-type]
style: improve [visual-aspect] in [component]
refactor: optimize [code-section] for [reason]
test: add tests for [functionality]
```

### **Ejemplos Reales**
```
feat: add categories-section with hover effects and admin controls
fix: resolve mobile nav overlay z-index in hero-integrated  
docs: update README with categories section documentation
style: improve gradient transitions in overlay system
refactor: optimize CSS variables for better performance
```

### **Tags de Versión**
```
v1.0-hero           # Hero integrado completo
v1.1-categories     # + Sección categorías
v1.2-products       # + Productos destacados  
v1.3-content        # + Banner + Instagram
v2.0-homepage       # Homepage completa
v2.1-shop           # + Página tienda
v3.0-launch         # Versión lanzamiento
```

---

## 🎯 **Checklist Pre-Sesión**

### **✅ Antes de Empezar Nueva Sesión:**
- [ ] GitHub repo actualizado
- [ ] DEVELOPMENT_LOG.md leído por Claude
- [ ] Objetivo de sesión claramente definido
- [ ] Referencias/mockups preparados si es necesario
- [ ] Backup de archivos críticos hecho

### **✅ Durante Desarrollo:**
- [ ] Documentar decisiones importantes
- [ ] Hacer commits incrementales
- [ ] Testear en mobile + desktop
- [ ] Verificar admin controls funcionan
- [ ] Mantener performance optimizado

### **✅ Final de Sesión:**
- [ ] Actualizar DEVELOPMENT_LOG.md
- [ ] Crear tag de versión
- [ ] Backup archivos modificados
- [ ] Documentar próximos pasos
- [ ] Push a GitHub repo

---

## 🔗 **Links y Referencias Importantes**

### **Proyecto Actual**
- **GitHub Repo:** https://github.com/KnuppeArt/pasion-frutos-secos-shopify
- **Shopify Store:** [URL cuando esté público]
- **Admin Shopify:** [Acceso privado]

### **Referencias de Diseño**
- **Estilo principal:** Botánica theme reference
- **Imágenes:** Estilo mediterráneo natural
- **Gradientes:** Cinematográficos + elegant

### **Documentación Técnica**
- **Shopify Liquid:** https://shopify.dev/docs/themes/liquid
- **Theme Architecture:** https://shopify.dev/docs/themes/architecture
- **CSS Custom Properties:** Para admin controls
- **Mobile-first:** Responsive design patterns

---

## 🚨 **Información Crítica - NO OLVIDAR**

### **⚠️ Elementos que NO se deben tocar:**
1. **Z-index hierarchy** del hero (funciona perfecto)
2. **Sticky navigation** JavaScript (optimizado)
3. **Mobile menu** structure (tested extensively)
4. **CSS variables** naming convention
5. **Admin schema** structure del hero

### **⚠️ Problemas Conocidos Resueltos:**
1. **Overlay no funcionaba** → Usar CSS calc() nativo
2. **Logo cortado** → Eliminar max-height restrictions  
3. **Header duplicado** → CSS .template-index específico
4. **Z-index conflictos** → Jerarquía documentada arriba

### **⚠️ Testing Obligatorio:**
- ✅ Mobile responsive (375px, 768px, 1200px)
- ✅ Admin controls (todos los sliders/selects)
- ✅ Performance (PageSpeed insights)
- ✅ Cross-browser (Chrome, Safari, Firefox)

---

**📅 Creado:** 2025-07-19
**📝 Última actualización:** 2025-07-20
**👤 Para usar por:** Cualquier sesión futura con Claude
**🎯 Objetivo:** Continuidad perfecta sin pérdida contexto
**🔗 GitHub:** https://github.com/KnuppeArt/pasion-frutos-secos-shopify
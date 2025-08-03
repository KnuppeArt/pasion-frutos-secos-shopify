# 🛠️ VS Code Setup Guide - Pasión Frutos Secos

## 🎯 **Configuración Completa VS Code + Shopify CLI**

Esta guía documenta la configuración completa del entorno de desarrollo local para el proyecto **Pasión Frutos Secos**.

---

## 📋 **Prerequisitos**

### **🔧 Software Requerido:**
```bash
# 1. Node.js (v18+)
node --version

# 2. Shopify CLI (v3.0+)
shopify version

# 3. Git
git --version

# 4. VS Code
code --version
```

### **📦 Instalación Shopify CLI:**
```bash
# macOS/Linux
curl -s https://shopify.dev/shopify-cli.sh | bash

# Windows (PowerShell)
iwr https://shopify.dev/shopify-cli.ps1 | iex

# Verificar instalación
shopify version
```

---

## 🚀 **Setup Inicial del Proyecto**

### **1️⃣ Clonar Repositorio:**
```bash
git clone https://github.com/KnuppeArt/pasion-frutos-secos-shopify.git
cd pasion-frutos-secos-shopify
```

### **2️⃣ Estructura de Directorios:**
```
pasion-frutos-secos-shopify/
├── 📁 .vscode/                 # ← Configuración VS Code
│   ├── settings.json          # ← Settings workspace
│   └── extensions.json        # ← Extensions recomendadas
├── 📁 sections/               # ← Secciones custom Liquid
│   ├── hero-integrated.liquid
│   └── categories-section.liquid
├── 📁 templates/              # ← Templates Shopify
├── 📁 assets/                 # ← CSS, JS, images
├── 📁 snippets/               # ← Snippets reutilizables
├── 📁 layout/                 # ← Layout principal
├── 📁 docs/                   # ← Documentación
│   ├── VS_CODE_SETUP.md       # ← Esta guía
│   └── AI_AGENTS_PROMPTS.md   # ← Prompts AI
├── 📄 .shopifyignore          # ← Archivos a ignorar
├── 📄 README.md               # ← Documentación principal
└── 📄 DEVELOPMENT_LOG.md      # ← Log desarrollo
```

### **3️⃣ Configurar VS Code:**
```bash
# Abrir proyecto en VS Code
code .

# VS Code instalará automáticamente las extensions recomendadas
# (Si no, instalar manualmente desde .vscode/extensions.json)
```

---

## ⚙️ **Configuración VS Code**

### **📄 .vscode/settings.json:**
```json
{
  "liquid.format.enable": true,
  "shopifyLiquid.snippetFormat": "tabstop",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  "files.associations": {
    "*.liquid": "liquid"
  },
  "emmet.includeLanguages": {
    "liquid": "html"
  },
  "liquid.engine": "shopify",
  "shopifyLiquid.formatterBinary": "theme check",
  "editor.quickSuggestions": {
    "strings": true
  },
  "github.copilot.enable": {
    "*": true,
    "liquid": true,
    "yaml": true,
    "json": true,
    "plaintext": false,
    "markdown": true
  },
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.wordWrap": "on",
  "editor.lineNumbers": "on",
  "editor.rulers": [80, 120],
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true
}
```

### **📄 .vscode/extensions.json:**
```json
{
  "recommendations": [
    "shopify.theme-check-vscode",
    "shopify.shopify-liquid",
    "github.copilot",
    "github.copilot-chat",
    "ms-vscode.vscode-json",
    "bradlc.vscode-tailwindcss",
    "formulahendry.auto-rename-tag",
    "christian-kohler.path-intellisense",
    "ms-vscode.vs-keybindings",
    "vsls-contrib.gistfs",
    "ms-vscode.theme-predawn",
    "ms-vscode.live-server"
  ]
}
```

---

## 🏪 **Configuración Shopify CLI**

### **1️⃣ Autenticación:**
```bash
# Login en Shopify
shopify auth login

# Verificar autenticación
shopify auth status
```

### **2️⃣ Conectar con Tienda de Desarrollo:**
```bash
# Conectar con store
shopify theme dev --store tu-tienda-dev.myshopify.com

# O usar store ID si ya está configurado
shopify theme dev
```

### **3️⃣ Comandos Útiles:**
```bash
# Desarrollo con hot reload
shopify theme dev

# Ver archivos remotos
shopify theme list

# Pull theme remoto
shopify theme pull

# Push cambios locales
shopify theme push

# Deploy a producción
shopify theme push --store tu-tienda-prod.myshopify.com
```

---

## 🤖 **Integración AI Agents**

### **🔧 GitHub Copilot Setup:**

1. **Instalación:**
   - Extension ya incluida en `extensions.json`
   - Activar desde VS Code: `Ctrl+Shift+P` → "GitHub Copilot: Enable"

2. **Configuración Específica Shopify:**
   ```json
   // En settings.json
   "github.copilot.enable": {
     "liquid": true,
     "yaml": true,
     "json": true
   }
   ```

3. **Uso Optimizado:**
   ```liquid
   <!-- Copilot activará autocompletado inteligente -->
   <!-- Ejemplo: escribir "section" + Tab autocompleta estructura -->
   <div class="hero-section">
     <!-- Copilot sugiere HTML semántico -->
   </div>
   ```

### **🎯 Gemini Coder Assistant:**

1. **Acceso:** Browser-based o VS Code extension
2. **Prompt Templates:** Ver `docs/AI_AGENTS_PROMPTS.md`
3. **Uso:** Debugging profundo y análisis de código

---

## 📁 **Archivos de Configuración**

### **📄 .shopifyignore:**
```gitignore
# Development files
.vscode/
.git/
.github/
node_modules/
.env
.env.local

# Documentation
README.md
DEVELOPMENT_LOG.md
CONTINUATION_GUIDE.md
docs/
design/

# Backup files
*.backup
*.bak
*.tmp
*~

# OS files
.DS_Store
Thumbs.db
```

---

## 🔄 **Workflow de Desarrollo**

### **📅 Flujo Diario:**

```bash
# 1. Iniciar desarrollo
cd pasion-frutos-secos-shopify
shopify theme dev

# 2. Abrir VS Code
code .

# 3. Desarrollar con hot reload automático
# - Editar archivos .liquid
# - Cambios se reflejan inmediatamente en browser
# - Copilot asiste con autocompletado

# 4. Testing y debugging
# - Usar browser dev tools
# - Theme Check automático en VS Code
# - Gemini para debugging profundo

# 5. Commit cambios
git add .
git commit -m "feat: descripción cambios"
git push origin main
```

### **🎯 Comandos VS Code Útiles:**

| Comando | Shortcut | Función |
|---------|----------|---------|
| Command Palette | `Ctrl+Shift+P` | Acceso a todos los comandos |
| Quick Open | `Ctrl+P` | Abrir archivo rápidamente |
| Copilot Suggestions | `Tab` | Aceptar sugerencia Copilot |
| Theme Check | `Ctrl+Shift+E` | Ver errores Liquid |
| Format Document | `Shift+Alt+F` | Formatear código |
| Toggle Terminal | `Ctrl+` | Abrir/cerrar terminal |

---

## 🐛 **Debugging y Testing**

### **🔍 Debugging Liquid:**

```liquid
<!-- Debugging variables -->
{{ variable | json }}

<!-- Conditional debugging -->
{% if settings.debug_mode %}
  <pre>{{ some_object | json }}</pre>
{% endif %}

<!-- Theme Check warnings -->
<!-- Automáticamente detecta errores de sintaxis -->
```

### **📱 Testing Responsive:**

```bash
# Shopify CLI provee múltiples URLs:
# Desktop: https://localhost:9292
# Mobile: https://[ip]:9292 (accesible desde móvil)
```

### **⚡ Performance Testing:**

```bash
# Theme Check performance automático
# Lighthouse integration
# Core Web Vitals monitoring
```

---

## 🚀 **Tips y Optimizaciones**

### **💡 VS Code Pro Tips:**

1. **Multi-cursor editing:** `Ctrl+Alt+Down`
2. **Duplicate line:** `Shift+Alt+Down`
3. **Block comment:** `Shift+Alt+A`
4. **Go to definition:** `F12`
5. **Peek definition:** `Alt+F12`

### **🎯 Shopify Development Tips:**

```liquid
<!-- Usar snippets para reutilización -->
{% render 'icon', icon: 'arrow-right' %}

<!-- Optimizar imágenes -->
{{ product.featured_image | image_url: width: 600 }}

<!-- Lazy loading -->
<img loading="lazy" src="{{ image | image_url }}" alt="">

<!-- Responsive images -->
{{ image | image_url: width: 600 }} 600w,
{{ image | image_url: width: 1200 }} 1200w
```

### **🔧 Performance Optimizations:**

```css
/* CSS custom properties para admin controls */
:root {
  --primary-color: {{ section.settings.primary_color }};
  --spacing: {{ section.settings.spacing }}px;
}

/* Lazy loading animations */
.fade-in {
  opacity: 0;
  animation: fadeIn 0.6s ease forwards;
}

@keyframes fadeIn {
  to { opacity: 1; }
}
```

---

## 📊 **Métricas y Monitoring**

### **📈 Performance Tracking:**

```javascript
// Core Web Vitals
// Automatically tracked by Shopify
// Monitor through Shopify Admin → Analytics

// Custom performance tracking
const perfObserver = new PerformanceObserver((list) => {
  list.getEntries().forEach((entry) => {
    console.log('Performance:', entry);
  });
});
```

### **🎯 Development Metrics:**

- **Hot reload speed:** < 1 second
- **Theme Check:** Real-time linting
- **Build time:** Optimized for speed
- **Code quality:** Copilot + Gemini assisted

---

## 🔗 **Enlaces Útiles**

### **📚 Documentación:**
- [Shopify CLI Docs](https://shopify.dev/docs/themes/tools/cli)
- [Liquid Reference](https://shopify.dev/docs/api/liquid)
- [Theme Development](https://shopify.dev/docs/themes)
- [VS Code Shopify Extensions](https://marketplace.visualstudio.com/shopify)

### **🤖 AI Tools:**
- [GitHub Copilot](https://github.com/features/copilot)
- [Gemini Code Assist](https://cloud.google.com/products/ai)

### **🛠️ Development Tools:**
- [Theme Check](https://shopify.dev/docs/themes/tools/theme-check)
- [Shopify Partners](https://partners.shopify.com)

---

## 🚨 **Troubleshooting**

### **❌ Problemas Comunes:**

| Problema | Solución |
|----------|----------|
| Shopify CLI no conecta | `shopify auth login` |
| Hot reload no funciona | Verificar puerto 9292 libre |
| Extensions no cargan | Reinstalar desde extensions.json |
| Copilot no sugiere | Verificar autenticación GitHub |
| Liquid syntax errors | Usar Theme Check automático |

### **🔧 Comandos de Reset:**

```bash
# Reset completo Shopify CLI
shopify auth logout
shopify auth login

# Reset VS Code workspace
rm -rf .vscode/
# Recrear archivos de configuración

# Reset tema local
shopify theme pull --force
```

---

**🎯 Setup completado correctamente cuando:**
- ✅ `shopify theme dev` funciona sin errores
- ✅ VS Code abre proyecto con extensions activas
- ✅ Hot reload funciona en browser
- ✅ GitHub Copilot sugiere código Liquid
- ✅ Theme Check detecta errores automáticamente

---

*Guía creada: 2025-08-03*  
*Para uso en: Pasión Frutos Secos development*  
*Workflow: VS Code + Shopify CLI + AI Agents*
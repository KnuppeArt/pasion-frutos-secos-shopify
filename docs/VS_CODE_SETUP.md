# 🔧 VS Code Setup Guide - Pasión Frutos Secos

## 📋 **Quick Setup Overview**

Este proyecto está optimizado para desarrollo con **VS Code + Shopify CLI + AI Agents**. Sigue esta guía para configurar tu entorno perfectamente.

---

## 🚀 **Instalación Rápida**

### **1️⃣ Prerequisitos:**
```bash
# Node.js (v18+)
node --version

# Shopify CLI
npm install -g @shopify/cli @shopify/theme

# Git configurado
git --version
```

### **2️⃣ Clone & Setup:**
```bash
# Clone del repositorio
git clone https://github.com/KnuppeArt/pasion-frutos-secos-shopify.git
cd pasion-frutos-secos-shopify

# Abrir en VS Code
code .

# Instalar extensiones recomendadas
# VS Code te preguntará automáticamente
```

### **3️⃣ Iniciar Desarrollo:**
```bash
# Conectar con tu store
shopify theme dev --store tu-store.myshopify.com

# URLs automáticas generadas:
# Preview: https://tu-store.myshopify.com/?preview_theme_id=XXXXX
# Editor: https://tu-store.myshopify.com/admin/themes/XXXXX/editor
```

---

## ⚙️ **Configuración Detallada**

### **📦 Extensiones Recomendadas (Auto-instalación):**

#### **Esenciales Shopify:**
- `sissel.shopify-liquid` - Syntax highlighting Liquid
- `shopify.theme-check-vscode` - Linting Shopify
- `github.copilot` - AI autocompletado
- `github.copilot-chat` - AI chat integration

#### **Desarrollo General:**
- `esbenp.prettier-vscode` - Formateo código
- `bradlc.vscode-tailwindcss` - Tailwind CSS
- `formulahendry.auto-rename-tag` - Rename tags automático
- `christian-kohler.path-intellisense` - Path autocompletado

#### **Productividad:**
- `eamodio.gitlens` - Git supercharged
- `pkief.material-icon-theme` - Iconos bonitos
- `gruntfuggly.todo-tree` - TODO tracking
- `wayou.vscode-todo-highlight` - Highlight TODOs

### **🔧 Settings.json Automático:**

El archivo `.vscode/settings.json` se configura automáticamente con:

```json
{
  "liquid.format.enable": true,
  "shopifyLiquid.snippetFormat": "tabstop",
  "editor.formatOnSave": true,
  "github.copilot.enable": {
    "*": true,
    "liquid": true
  }
}
```

---

## 🤖 **AI Agents Integration**

### **✅ GitHub Copilot (Incluido):**
- **Activación:** Automática al abrir VS Code
- **Shortcuts:** 
  - `Ctrl/Cmd + I` - Inline suggestions
  - `Tab` - Accept suggestion
  - `Alt + ]` - Next suggestion

### **💬 Copilot Chat:**
```bash
# En VS Code, abrir chat:
Ctrl/Cmd + Shift + P > "GitHub Copilot: Open Chat"

# Prompts útiles:
"Fix this Shopify Liquid error"
"Make this responsive mobile-first"
"Add accessibility to this section"
```

### **🧠 Gemini Assistant (Externo):**
- Usar web interface para debugging profundo
- Ver `docs/AI_AGENTS_PROMPTS.md` para prompts específicos

---

## 📁 **Estructura de Archivos**

```
pasion-frutos-secos-shopify/
├── .vscode/
│   ├── settings.json          # ✅ Configuración automática
│   └── extensions.json        # ✅ Extensiones recomendadas
├── .shopifyignore             # ✅ Optimización deploys
├── sections/
│   ├── hero-integrated.liquid # ✅ Disponible en repo
│   └── categories-section.liquid # ✅ Disponible en repo
├── docs/
│   ├── AI_AGENTS_PROMPTS.md   # ✅ Guía prompts AI
│   └── VS_CODE_SETUP.md       # ✅ Esta guía
├── DEVELOPMENT_LOG.md         # ✅ Log desarrollo completo
├── CONTINUATION_GUIDE.md      # ✅ Guía continuidad
└── README.md                  # ✅ Documentación proyecto
```

---

## 🔥 **Workflow de Desarrollo**

### **🏃‍♂️ Desarrollo Rápido:**

```bash
# 1. Start development server
shopify theme dev

# 2. Open VS Code with project
code .

# 3. Edit files with AI assistance:
#    - Copilot autocompletado
#    - Theme Check linting en tiempo real
#    - Hot reload automático
```

### **⚡ Hot Reload Mágico:**
- **Cambios CSS:** Instantáneo
- **Cambios Liquid:** ~2 segundos
- **Nuevos archivos:** ~5 segundos
- **Schema changes:** Reload manual necesario

### **🎯 Testing en Vivo:**
- **Preview URL:** Cambios en tiempo real
- **Admin URL:** Configurar settings
- **Mobile testing:** Usar dev tools

---

## 🐛 **Debugging & Troubleshooting**

### **🔧 Problemas Comunes:**

#### **Shopify CLI no conecta:**
```bash
# Logout y re-login
shopify auth logout
shopify auth login

# Verificar store
shopify theme list
```

#### **VS Code no reconoce Liquid:**
```bash
# Instalar manualmente extensión Liquid
Ctrl/Cmd + Shift + X
Buscar: "Shopify Liquid"
Instalar: sissel.shopify-liquid
```

#### **Copilot no funciona:**
```bash
# Verificar login GitHub
Ctrl/Cmd + Shift + P
> "GitHub Copilot: Sign in"
```

#### **Hot reload no funciona:**
```bash
# Restart development server
Ctrl + C (stop)
shopify theme dev (restart)
```

### **🚨 Errores Específicos:**

#### **Error: "Theme not found"**
```bash
# Verificar store URL
shopify theme dev --store [correcto-store-name].myshopify.com
```

#### **Error: "Permission denied"**
```bash
# Verificar permisos de la app
# Ir a Shopify Admin > Apps > Shopify CLI
# Verificar permisos de themes
```

#### **Error: "Port already in use"**
```bash
# Cambiar puerto
shopify theme dev --port 9293
```

---

## 🚀 **Optimización Performance**

### **⚡ VS Code Optimizations:**

#### **Mejorar velocidad:**
```json
// .vscode/settings.json (ya incluido)
{
  "files.watcherExclude": {
    "**/.shopify/**": true,
    "**/node_modules/**": true
  },
  "search.exclude": {
    "**/.shopify": true,
    "**/node_modules": true
  }
}
```

#### **Linting inteligente:**
```json
{
  "themeCheck.checkOnSave": true,
  "themeCheck.checkOnOpen": true
}
```

### **🔧 Shopify CLI Optimizations:**

#### **Deploy más rápido:**
```bash
# Solo archivos modificados
shopify theme push --development

# Ignorar archivos innecesarios (.shopifyignore activo)
shopify theme push --ignore=docs/**
```

---

## 📊 **Comandos Útiles**

### **🎯 Desarrollo Diario:**
```bash
# Iniciar día
shopify theme dev

# Subir cambios
git add .
git commit -m "feat: add new section"
git push origin main

# Deploy a staging
shopify theme push --development

# Deploy a production
shopify theme push --live
```

### **🔍 Debugging:**
```bash
# Ver themes disponibles
shopify theme list

# Descargar theme actual
shopify theme pull

# Verificar archivos modificados
shopify theme check

# Ver logs detallados
shopify theme dev --verbose
```

### **📦 Gestión de Themes:**
```bash
# Crear nuevo theme
shopify theme init

# Copiar theme existente
shopify theme pull --theme [THEME_ID]

# Publicar theme
shopify theme publish
```

---

## 🎯 **Next Steps después del Setup**

### **✅ Verificar Todo Funciona:**

1. **VS Code abierto** con project
2. **Extensions instaladas** (popup automático)
3. **Shopify CLI conectado** (`shopify theme dev`)
4. **Hot reload funcionando** (editar CSS y ver cambios)
5. **Copilot activo** (icon en status bar)
6. **Theme Check working** (ver problemas en panel)

### **🚀 Comenzar Desarrollo:**

1. **Copiar archivos existentes:**
   - `sections/hero-integrated.liquid`
   - `sections/categories-section.liquid`

2. **Configurar en Shopify Admin:**
   - Añadir secciones al homepage
   - Configurar settings básicos

3. **Empezar nueva sección:**
   - Ver `docs/AI_AGENTS_PROMPTS.md`
   - Usar prompts de Claude para desarrollo

### **📚 Recursos Adicionales:**
- **Documentation:** `DEVELOPMENT_LOG.md`
- **AI Prompts:** `docs/AI_AGENTS_PROMPTS.md`
- **Continuity:** `CONTINUATION_GUIDE.md`
- **Project Overview:** `README.md`

---

## 💡 **Pro Tips**

### **🔥 Productivity Hacks:**

1. **Snippet personalizados:** Crear snippets Liquid comunes
2. **Multi-cursor:** `Alt + Click` para ediciones múltiples
3. **Command Palette:** `Ctrl/Cmd + Shift + P` para todo
4. **Quick Open:** `Ctrl/Cmd + P` para abrir archivos rápido

### **🎨 Aesthetic Improvements:**
```json
// Opcional en settings.json
{
  "workbench.colorTheme": "Default Dark Modern",
  "workbench.iconTheme": "material-icon-theme",
  "editor.fontFamily": "JetBrains Mono, Consolas, monospace",
  "editor.fontSize": 14,
  "editor.lineHeight": 1.5
}
```

### **🚀 AI-Powered Development:**
- **Copilot para autocompletado** de Liquid
- **Claude para arquitectura** de secciones
- **Gemini para debugging** complejo
- **Combined power** = 5x velocidad desarrollo

---

**🎯 Objetivo:** Setup perfecto para desarrollo Shopify acelerado  
**⏱️ Tiempo setup:** ~15 minutos  
**🚀 Resultado:** Environment productivo 5x más rápido  
**📅 Actualizado:** 2025-08-03  

¡Happy coding! 🚀✨
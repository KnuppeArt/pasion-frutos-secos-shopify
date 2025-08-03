# 🤖 AI Agents Prompts Guide - Pasión Frutos Secos

## 📋 **Overview del Workflow AI**

Este proyecto utiliza **múltiples AI agents** para desarrollo acelerado:

```
Claude (Arquitectura) → VS Code (Implementación) → Copilot (Refinamiento) → Gemini (Validación)
```

### **🎯 Roles de cada AI:**
- **Claude:** Desarrollo de secciones completas, arquitectura, debugging complejo
- **GitHub Copilot:** Autocompletado, fixes rápidos, optimizaciones
- **Gemini:** Debugging profundo, testing, validación de código

---

## 🚀 **GitHub Copilot - Quick Fixes & Autocompletado**

### **🔧 Prompts para Fixes Rápidos:**

#### **Shopify Liquid Syntax:**
```
Fix this Shopify Liquid syntax error in sections/[archivo]:
[pegar error exacto del terminal]
```

#### **Responsive Mobile-First:**
```
Make this component responsive mobile-first following our breakpoints:
- Mobile: 480px
- Tablet: 768px  
- Desktop: 769px+
```

#### **Accessibility Improvements:**
```
Add accessibility improvements to this Shopify section:
- ARIA labels
- Screen reader support
- Keyboard navigation
- High contrast support
```

#### **Performance Optimization:**
```
Optimize this code for performance:
- Lazy loading
- Reduce DOM queries
- Optimize animations
- Minimize CSS
```

### **💡 Autocompletado Específico:**

#### **Schema Settings:**
```
// Prompt: "Add admin settings for"
{
  "type": "header",
  "content": "t:sections.[section].name"
},
{
  "type": "color",
  "id": "bg_color",
  "label": "t:sections.[section].settings.bg_color.label",
  "default": "#ffffff"
}
```

#### **CSS Variables:**
```
/* Prompt: "Create CSS custom properties for" */
:root {
  --primary-color: {{ section.settings.primary_color }};
  --text-color: {{ section.settings.text_color }};
  --border-radius: {{ section.settings.border_radius }}px;
}
```

---

## 🧠 **Gemini - Deep Analysis & Debugging**

### **🔍 Prompts para Debugging Profundo:**

#### **Bug Analysis Completo:**
```
Act as a Shopify theme expert. Debug this section:

Context: Premium nuts store, Dawn theme customization
Error: [descripción específica del error]
Expected behavior: [qué debería pasar]
Current behavior: [qué está pasando]

File: sections/[archivo].liquid
Lines: [rango de líneas si conocido]

Code:
[pegar código completo de la sección]

Analyze and provide:
1. Root cause of the issue
2. Step-by-step fix
3. Prevention strategies
4. Alternative approaches
```

#### **Performance Analysis:**
```
Analyze this Shopify section for performance issues:

Store type: Premium e-commerce nuts
Target: Mobile-first, Core Web Vitals optimization
Current section: [nombre sección]

Code:
[pegar código]

Provide analysis on:
1. Loading performance
2. Runtime performance  
3. CSS optimization
4. JavaScript efficiency
5. Image optimization
6. Shopify-specific best practices
```

#### **Security & Best Practices:**
```
Review this Shopify liquid code for security and best practices:

Context: Production e-commerce store
Code:
[pegar código]

Check for:
1. XSS vulnerabilities
2. Input sanitization
3. Shopify API usage
4. Performance implications
5. Accessibility compliance
6. SEO optimization
```

### **🧪 Testing & Validation:**

#### **Cross-Browser Testing:**
```
Create a testing checklist for this Shopify section:

Section: [nombre]
Features: [listar funcionalidades]

Generate tests for:
1. Chrome/Safari/Firefox/Edge
2. iOS Safari/Android Chrome
3. Desktop breakpoints: 1920px, 1366px, 1024px
4. Mobile breakpoints: 768px, 480px, 375px
5. Accessibility: Screen readers, keyboard nav
6. Performance: Page load, animations
```

---

## 💻 **VS Code Integration Prompts**

### **🔧 Workspace Setup:**

#### **Debugging Specific Errors:**
```
// Para el terminal de VS Code
Act as VS Code expert. Fix this error:

Error: [error exacto del terminal]
Context: Shopify theme development, Dawn base
Current file: [archivo actual]
Shopify CLI version: [versión]

Provide:
1. Immediate fix
2. Root cause explanation  
3. Prevention for future
```

#### **IntelliSense Improvements:**
```
Improve VS Code IntelliSense for this Shopify project:

Current settings.json:
[pegar settings actuales]

Add configurations for:
1. Better Liquid autocompletion
2. Shopify objects intellisense
3. CSS custom properties
4. File path completion
```

---

## 🎨 **Desarrollo de Secciones - Prompts Específicos**

### **🛍️ Our Best Seller Section:**

#### **Para Claude (Desarrollo Completo):**
```
Develop a complete "Our Best Seller" section for Shopify:

Store: Premium nuts and gourmet products
Style: Mediterranean minimalist, consistent with hero section
Base: Dawn theme customization

Requirements:
1. Grid layout: 3 productos desktop, 1 mobile
2. Each card includes:
   - Product image
   - Product name
   - Health benefits (highlight)
   - Price display
   - "Add to cart" button
3. Hover effects: Premium feel, smooth animations
4. Admin controls: 60+ settings for full customization
5. Responsive: Mobile-first approach
6. Performance: Lazy loading, optimized CSS
7. Accessibility: WCAG 2.1 AA compliant
8. SEO: Structured data ready

Visual style:
- Colors: Earth tones, premium feel
- Typography: Clean, modern
- Spacing: Generous whitespace
- Animations: Subtle, professional

Provide complete .liquid file with schema.
```

#### **Para Copilot (Refinamiento):**
```
Optimize this Our Best Seller section:
- Add missing accessibility attributes
- Improve mobile touch targets
- Optimize CSS for performance
- Add loading states for images
```

#### **Para Gemini (Validación):**
```
Validate this Our Best Seller section:

Requirements compliance:
1. Mobile responsiveness
2. Admin controls functionality
3. Performance benchmarks
4. Cross-browser compatibility
5. Accessibility standards
6. SEO optimization

Code:
[pegar código]
```

### **📢 Banner Anuncio Section:**

#### **Para Claude:**
```
Create promotional banner section for Shopify:

Purpose: Announcements, offers, shipping info
Placement: Between hero and categories
Style: Subtle, non-intrusive

Features:
1. Multiple banner types:
   - Free shipping
   - Discount codes
   - General announcements  
   - Seasonal offers
2. Dismissible option
3. Animation entrance
4. Call-to-action button
5. Admin controls: colors, text, links
6. Responsive design
7. Performance optimized

Provide complete implementation.
```

---

## 🔄 **Workflow Específico por Tarea**

### **🐛 Cuando hay un Error:**

1. **Identificar error** (Terminal/Console)
2. **Copilot quick fix:** `Fix this Shopify Liquid error: [error]`
3. **Si persiste → Gemini analysis:** `Debug this section: [context + code]`
4. **Si es complejo → Claude:** `Redesign this problematic section`

### **✨ Nueva Funcionalidad:**

1. **Claude:** Desarrollo inicial completo
2. **Copilot:** Refinamiento y optimizaciones
3. **Gemini:** Testing y validación final
4. **Claude:** Documentación y commit

### **🚀 Optimización Performance:**

1. **Gemini:** `Analyze performance of [section]`
2. **Copilot:** Implementar optimizaciones sugeridas
3. **Claude:** Refactoring si es necesario

---

## 📊 **Templates por Caso de Uso**

### **🔧 Quick Fix (Copilot):**
```
Fix this [type] issue in sections/[file]:
Error: [error]
Expected: [expected behavior]
```

### **🧠 Deep Analysis (Gemini):**
```
Analyze this Shopify section for [specific aspect]:
Context: [project context]
Code: [full code]
Requirements: [specific requirements]
```

### **🏗️ Full Development (Claude):**
```
Develop complete [section name] for Shopify:
Store: Premium nuts gourmet products
Requirements: [detailed requirements]
Style: [style guidelines]
Technical: [technical constraints]
```

---

## 💡 **Best Practices para Prompts**

### **✅ DO:**
- Ser específico con el contexto del proyecto
- Incluir código completo cuando sea necesario
- Mencionar errores exactos del terminal
- Especificar breakpoints responsive
- Incluir requisitos de accesibilidad

### **❌ DON'T:**
- Prompts genéricos sin contexto
- Omitir información de errores
- Asumir conocimiento del proyecto previo
- Pedir múltiples tareas en un prompt

---

## 🎯 **Shortcuts Rápidos**

### **Copilot en VS Code:**
- `Ctrl/Cmd + I`: Inline suggestions
- `Alt + ]`: Next suggestion
- `Alt + [`: Previous suggestion
- `Tab`: Accept suggestion

### **Prompts de Emergencia:**

#### **Error Crítico:**
```
URGENT: Fix this breaking error in production theme:
[error exacto]
File: [archivo]
Context: [context mínimo]
```

#### **Deploy Rápido:**
```
Prepare this section for immediate deployment:
- Validate all admin controls
- Check responsive breakpoints
- Verify accessibility
- Test browser compatibility
```

---

**📅 Creado:** 2025-08-03  
**🎯 Propósito:** Acelerar desarrollo con AI agents  
**🔄 Actualizar:** Según nuevas necesidades del proyecto  
**📝 Usar con:** VS Code + Shopify CLI + GitHub Copilot + Gemini
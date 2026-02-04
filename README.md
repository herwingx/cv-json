# 🚀 CV JSON - Portfolio Minimalista

> **Portfolio/CV profesional** — Construido con Astro y datos en JSON, con soporte bilingüe (ES/EN).

[![Astro](https://img.shields.io/badge/Astro-BC52EE?style=flat-square&logo=astro&logoColor=fff)](https://astro.build)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=fff)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE.txt)

---

## ✨ Características

| Característica | Descripción |
|:--|:--|
| 🌐 **Bilingüe** | Soporte completo para Español e Inglés con selector de idioma |
| 📄 **Basado en JSON** | Esquema [jsonresume.org](https://jsonresume.org/schema/) para fácil edición |
| 🖨️ **Listo para PDF** | Optimizado para impresión con `Ctrl/Cmd + P` |
| ⌨️ **Paleta de comandos** | Atajos de teclado con `Ctrl/Cmd + K` |
| 🎨 **Iconos Skill** | Integración con [skillicons.dev](https://skillicons.dev) |
| 📱 **Responsive** | Diseño adaptable a cualquier dispositivo |

---

## 🚀 Inicio Rápido

### 1. Clonar el repositorio

```bash
git clone https://github.com/herwingx/cv-json.git
cd cv-json
```

### 2. Instalar dependencias

```bash
# Usar pnpm (recomendado)
pnpm install

# O usar npm
npm install
```

### 3. Personalizar tu CV

Edita los archivos JSON con tu información:

| Archivo | Idioma |
|:--|:--|
| `cv.json` | Español |
| `cv_english.json` | Inglés |

### 4. Iniciar servidor de desarrollo

```bash
pnpm dev
```

Abre [http://localhost:4321](http://localhost:4321) para ver tu portfolio.

---

## 📁 Estructura del Proyecto

```
cv-json/
├── cv.json                    # CV en Español
├── cv_english.json            # CV en Inglés
├── src/
│   ├── components/
│   │   ├── sections/          # Componentes ES
│   │   │   └── en/            # Componentes EN
│   │   ├── en/                # KeyboardManager EN
│   │   ├── KeyboardManager.astro
│   │   ├── LanguageSwitcher.astro
│   │   └── Section.astro
│   ├── icons/                 # Iconos SVG (contacto)
│   ├── layouts/
│   │   ├── Layout.astro       # Layout ES
│   │   └── LayoutEN.astro     # Layout EN
│   └── pages/
│       ├── index.astro        # Página ES (/)
│       └── en/
│           └── index.astro    # Página EN (/en)
└── public/
    └── me.webp                # Tu foto de perfil
```

---

## 🧞 Comandos

| Comando | Descripción |
|:--|:--|
| `pnpm dev` | Inicia servidor de desarrollo en `localhost:4321` |
| `pnpm build` | Compila para producción en `./dist/` |
| `pnpm preview` | Vista previa de la compilación |

---

## 🌐 URLs

| Ruta | Idioma |
|:--|:--|
| `/` | Español |
| `/en` | English |

---

## ⌨️ Atajos de Teclado

| Atajo | Acción |
|:--|:--|
| `Ctrl/Cmd + K` | Abrir paleta de comandos |
| `Ctrl/Cmd + P` | Imprimir / Guardar como PDF |
| `Ctrl/Cmd + L` | Ir a LinkedIn |
| `Ctrl/Cmd + G` | Ir a GitHub |
| `Ctrl/Cmd + X` | Ir a X (Twitter) |

---

## 🛠️ Stack Tecnológico

| Capa | Tecnologías |
|:--|:--|
| **Framework** | [Astro](https://astro.build/) |
| **Lenguaje** | TypeScript |
| **Iconos** | [skillicons.dev](https://skillicons.dev), SVG custom |
| **Atajos** | [hotkeypad](https://github.com/AdrianCarreno/hotkeypad) |

---

## 📝 Personalización del CV

El archivo `cv.json` sigue el esquema de [jsonresume.org](https://jsonresume.org/schema/):

```json
{
  "basics": {
    "name": "Tu Nombre",
    "label": "Tu título profesional",
    "email": "tu@email.com",
    "summary": "Tu resumen profesional..."
  },
  "work": [...],
  "education": [...],
  "skills": [...],
  "projects": [...]
}
```

---

## 🔧 Agregar Nuevas Skills

1. Agrega la skill en `cv.json` y `cv_english.json`
2. Busca el ID del icono en [skillicons.dev](https://skillicons.dev)
3. Agrega el mapeo en `src/components/sections/Skills.astro`:

```javascript
const SKILL_ICON_IDS = {
  // ...
  "Nueva Skill": "iconid",
}
```

---

## 🚀 Deploy en Vercel

Este proyecto está configurado para desplegarse en [Vercel](https://vercel.com).

### Opción 1: CLI

```bash
npx vercel
```

### Opción 2: Conectar repositorio

1. Sube tu código a GitHub
2. Ve a [vercel.com/new](https://vercel.com/new)
3. Importa tu repositorio
4. ¡Listo! Vercel detectará automáticamente que es un proyecto Astro

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/herwingx/cv-json)

---

## 🔑 Licencia

[MIT](LICENSE.txt) - Basado en el proyecto de [midudev](https://github.com/midudev/minimalist-portfolio-json).

---

## 👤 Autor

**Herwing Eduardo Vázquez Macías**

- 🌐 [herwingx.dev](https://herwingx.dev)
- 💼 [LinkedIn](https://linkedin.com/in/herwingx)
- 🐙 [GitHub](https://github.com/herwingx)
- 🐦 [X](https://x.com/herwingx)

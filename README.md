# Pet Verde 🐾

> Sitio web oficial de **Pet Verde**, tienda de mascotas y servicio de grooming profesional ubicada en Itagüí, Antioquia, Colombia.

[![Hugo](https://img.shields.io/badge/Hugo-0.157+-FF4088.svg)](https://gohugo.io)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3.svg)](https://getbootstrap.com)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-success.svg)](https://pages.github.com)

---

## 🚀 Vista Rápida

```powershell
# Instalar Hugo (si no lo tienes)
winget install Hugo.Hugo.Extended

# Clonar el repositorio
git clone https://github.com/handresc1127/petverde-web.git
cd petverde-web

# Ejecutar localmente
hugo server

# Acceder
# http://localhost:1313/petverde-web/
```

---

## ✨ Características

### 🎨 Diseño Profesional
- **Tipografía de marca**: Campton Bold y Campton Extrabold (con Montserrat como fallback)
- **Paleta de colores oficial**: 4 verdes corporativos (#0f5534, #47833f, #86b357, #e6edd9)
- **Bootstrap 5.3** con diseño responsive
- **Bootstrap Icons** para iconografía consistente
- **Cards con efectos hover** y sombras profesionales
- **Hero section** con gradiente verde corporativo

### 📱 Secciones del Sitio
- **Inicio**: Presentación de Pet Verde con logo y branding
- **Servicios**: Cards visuales mostrando:
  - 🪒 Grooming profesional
  - 🛒 Tienda de productos
  - 💧 Spa para perros
  - ❤️ Cuidado especializado
- **Ubicación**: Mapa embebido de Google Maps + enlace directo
- **Contacto**: Botón directo de WhatsApp para reservas

### 🔧 Optimizaciones
- **Favicons completos**: 16x16, 32x32, Apple Touch Icon, Android Chrome
- **PWA Ready**: Web manifest para instalar como app
- **SEO Friendly**: Meta tags y descripción optimizados
- **GitHub Actions**: Deploy automático a GitHub Pages

---

## 📁 Estructura del Proyecto

```
PetVerde/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions workflow para deploy
├── content/
│   └── _index.md             # Página principal
├── layouts/
│   └── index.html            # Template principal con Bootstrap
├── static/
│   ├── fonts/                # Tipografía de marca (Campton)
│   │   └── README.md         # Instrucciones para agregar Campton
│   ├── images/               # Logos y favicons
│   │   ├── Logo.png          # Logo oficial de la marca
│   │   ├── android-chrome-192x192.png
│   │   ├── android-chrome-512x512.png
│   │   ├── apple-touch-icon.png
│   │   ├── favicon-16x16.png
│   │   └── favicon-32x32.png
│   ├── colors.md             # Paleta de colores oficial
│   └── site.webmanifest      # PWA manifest
├── hugo.toml                 # Configuración de Hugo
├── .gitignore
└── README.md
```

---

## 🛠️ Tecnologías

- **[Hugo Extended 0.157+](https://gohugo.io)** - Generador de sitios estáticos
- **[Bootstrap 5.3](https://getbootstrap.com)** - Framework CSS
- **[Bootstrap Icons](https://icons.getbootstrap.com)** - Iconografía
- **[Montserrat Font](https://fonts.google.com/specimen/Montserrat)** - Tipografía (similar a Campton)
- **[GitHub Pages](https://pages.github.com)** - Hosting gratuito
- **[GitHub Actions](https://github.com/features/actions)** - CI/CD

---

## 💻 Desarrollo Local

### Prerrequisitos
- Hugo Extended 0.157 o superior

### Instalación

**Windows (WinGet):**
```powershell
winget install Hugo.Hugo.Extended
```

**macOS (Homebrew):**
```bash
brew install hugo
```

**Linux (Snap):**
```bash
snap install hugo
```

### Ejecutar el sitio

```powershell
# Clonar repositorio
git clone https://github.com/handresc1127/petverde-web.git
cd petverde-web

# Iniciar servidor de desarrollo
hugo server

# O con live reload
hugo server --navigateToChanged
```

El sitio estará disponible en: `http://localhost:1313/`

### Construir para producción

```powershell
hugo
```

Los archivos de salida estarán en la carpeta `public/`.

---

## 🚢 Desplegar a GitHub Pages

### 1️⃣ Configuración Inicial

El repositorio ya incluye el workflow de GitHub Actions en `.github/workflows/hugo.yml`.

### 2️⃣ Activar GitHub Pages

1. Ve a tu repositorio en GitHub
2. **Settings** → **Pages**
3. En **Source**, selecciona **GitHub Actions**

### 3️⃣ Hacer Push

```powershell
git add .
git commit -m "Update Pet Verde website"
git push origin main
```

Esto activará automáticamente:
- ✅ Build del sitio con Hugo
- ✅ Deploy a GitHub Pages
- ✅ Sitio publicado temporalmente en: `https://handresc1127.github.io/petverde-web/`

### 4️⃣ Configurar Dominio Personalizado

1. Ve a tu repositorio en GitHub
2. **Settings** → **Pages**
3. En **Custom domain**, ingresa: `petverde.co`
4. Click en **Save**
5. Marca la opción **Enforce HTTPS** (después de que se valide el dominio)

### 5️⃣ Configurar DNS

En tu proveedor de dominio (donde compraste `petverde.co`), agrega estos registros DNS:

**Opción A - Usando registros A (Recomendado):**
```
Tipo: A
Nombre: @
Valor: 185.199.108.153

Tipo: A
Nombre: @
Valor: 185.199.109.153

Tipo: A
Nombre: @
Valor: 185.199.110.153

Tipo: A  
Nombre: @
Valor: 185.199.111.153

Tipo: CNAME
Nombre: www
Valor: handresc1127.github.io
```

**Opción B - Usando CNAME (Alternativa):**
```
Tipo: CNAME
Nombre: @
Valor: handresc1127.github.io.
```

⚠️ **Nota**: La propagación DNS puede tomar entre 1-48 horas.

Una vez configurado, tu sitio estará disponible en: **`https://petverde.co`**

---

## 🎨 Personalización

### Modificar Contenido

Edita el archivo `content/_index.md`:

```markdown
---
title: "Tu Título"
---

Tu contenido aquí en **Markdown**.
```

### Cambiar Colores

La paleta de colores oficial está documentada en [`static/colors.md`](static/colors.md).

Variables CSS en `layouts/index.html`:

```css
:root {
    --color-primary: #0f5534;      /* Verde oscuro principal */
    --color-secondary: #47833f;    /* Verde medio */
    --color-tertiary: #86b357;     /* Verde claro */
    --color-light: #e6edd9;        /* Verde muy claro / crema - fondo */
}
```

### Usar Tipografía Campton (Marca Oficial)

**Por defecto**, el sitio usa **Montserrat** (similar a Campton) desde Google Fonts.

**Si tienes la licencia de Campton:**

1. Coloca los archivos de fuente en `static/fonts/`:
   - `Campton-Bold.woff2` (peso 700)
   - `Campton-ExtraBold.woff2` (peso 800)

2. Descomenta las reglas `@font-face` en `layouts/index.html`

3. Actualiza la variable CSS:
   ```css
   :root {
       --font-primary: 'Campton', sans-serif;
   }
   ```

Ver [`static/fonts/README.md`](static/fonts/README.md) para instrucciones completas.

### Actualizar Logo

El logo oficial de la marca está en `static/images/Logo.png`.

Para reemplazar los favicons (iconos del navegador):
- `android-chrome-192x192.png`
- `android-chrome-512x512.png`  
- `apple-touch-icon.png`
- `favicon-16x16.png`
- `favicon-32x32.png`

El logo principal se muestra en:
- Navbar (30px de altura)
- Hero section (200px de ancho máximo)

---

## 📞 Información de Contacto

- **Ubicación**: Itagüí, Antioquia, Colombia
- **WhatsApp**: [Reservar cita](https://wa.me/573332272604)
- **Sitio Web**: https://petverde.co

---

## 📝 Próximas Mejoras

- [ ] Agregar galería de fotos de servicios
- [ ] Integrar sistema de reservas online
- [ ] Agregar sección de productos en venta
- [ ] Implementar blog con consejos para mascotas
- [x] Conectar dominio personalizado `petverde.co`
- [ ] Agregar testimonios de clientes
- [x] Integrar mapa de Google Maps
- [ ] Agregar certificado SSL (HTTPS)

---

## 📄 Licencia

Este proyecto es privado y de uso exclusivo de **Pet Verde**.

---

## 🤝 Créditos

**Desarrollado por:** [handresc1127](https://github.com/handresc1127)

Desarrollado con 💚 para **Pet Verde** - Tu tienda de mascotas de confianza en Itagüí.

Diseño inspirado en el sistema POS Green de Pet Verde.

&copy; 2026 Pet Verde. Todos los derechos reservados.
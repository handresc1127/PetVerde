# Tipografía Pet Verde

La tipografía oficial de la marca Pet Verde es **Campton**:

- **Campton Bold** (700) - Texto general
- **Campton Extrabold** (800) - Títulos y elementos destacados

## 🔤 Cómo agregar Campton

**Campton es una fuente premium** que requiere licencia de [MyFonts](https://www.myfonts.com/collections/campton-font-rene-bieder).

### Si tienes la licencia de Campton:

1. **Coloca los archivos de fuente en este directorio:**
   ```
   static/fonts/
   ├── Campton-Bold.woff2
   └── Campton-ExtraBold.woff2
   ```

2. **Descomenta las reglas @font-face en `layouts/index.html`:**
   ```css
   @font-face {
       font-family: 'Campton';
       src: url('/fonts/Campton-Bold.woff2') format('woff2');
       font-weight: 700;
       font-style: normal;
       font-display: swap;
   }
   
   @font-face {
       font-family: 'Campton';
       src: url('/fonts/Campton-ExtraBold.woff2') format('woff2');
       font-weight: 800;
       font-style: normal;
       font-display: swap;
   }
   ```

3. **Actualiza la variable CSS:**
   ```css
   :root {
       --font-primary: 'Campton', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
   }
   ```

## 📝 Alternativa actual

Actualmente el sitio usa **Montserrat** (Bold 700 y ExtraBold 800) como alternativa similar a Campton, disponible gratuitamente desde Google Fonts.

Montserrat es una fuente geométrica sans-serif que comparte características visuales similares con Campton:
- Formas redondas y amigables
- Excelente legibilidad
- Múltiples pesos disponibles

## 🎨 Uso de pesos

- **Body text**: Font weight 700 (Bold)
- **Títulos (h1-h6)**: Font weight 800 (ExtraBold)
- **Navbar brand**: Font weight 800 (ExtraBold)
- **Botones**: Font weight 800 (ExtraBold)
- **Links de navegación**: Font weight 700 (Bold)

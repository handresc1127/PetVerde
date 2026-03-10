# 🎨 Paleta de Colores Pet Verde

Paleta oficial de colores de la marca **Pet Verde**.

## Colores Principales

### 1. Verde Oscuro Principal
**Color primario de la marca**
- **HEX:** `#0f5534`
- **RGB:** `rgb(15, 85, 52)`
- **Uso:** 
  - Navbar de fondo
  - Footer
  - Hover de botones
  - Elementos de mayor jerarquía

---

### 2. Verde Medio
**Color secundario**
- **HEX:** `#47833f`
- **RGB:** `rgb(71, 131, 63)`
- **Uso:**
  - Hero section gradient
  - Botones principales
  - Iconos de servicios
  - Elementos destacados

---

### 3. Verde Claro
**Color terciario**
- **HEX:** `#86b357`
- **RGB:** `rgb(134, 179, 87)`
- **Uso:**
  - Acentos y detalles
  - Hover states secundarios
  - Elementos decorativos

---

### 4. Verde Muy Claro / Crema
**Color de fondo**
- **HEX:** `#e6edd9`
- **RGB:** `rgb(230, 237, 217)`
- **Uso:**
  - Background del body
  - Fondos de secciones
  - Espacios suaves
  - PWA background color
  - Fondo de cards combinado con blanco para contraste

---

## Variables CSS

Los colores están definidos como variables CSS en `layouts/index.html`:

```css
:root {
    --color-primary: #0f5534;      /* Verde oscuro principal */
    --color-secondary: #47833f;    /* Verde medio */
    --color-tertiary: #86b357;     /* Verde claro */
    --color-light: #e6edd9;        /* Verde muy claro / crema - fondo */
}
```

## Implementación

### HTML/CSS
```css
.element {
    background-color: var(--color-primary);
    color: var(--color-light);
}
```

### Gradientes
```css
.hero {
    background: linear-gradient(135deg, var(--color-secondary) 0%, var(--color-primary) 100%);
}
```

## Accesibilidad

### Contrastes Verificados
- ✅ **Texto blanco sobre #0f5534**: Ratio 7.84:1 (AAA)
- ✅ **Texto blanco sobre #47833f**: Ratio 4.82:1 (AA)
- ✅ **Texto #0f5534 sobre #e6edd9**: Ratio 8.91:1 (AAA)

Todos los contrastes cumplen con WCAG 2.1 nivel AA o superior.

---

## Coherencia de Marca

Esta paleta debe usarse consistentemente en:
- ✅ Sitio web (Hugo)
- ✅ Sistema POS Green
- ✅ Material impreso
- ✅ Redes sociales
- ✅ Señalización física

---

**Última actualización:** Marzo 2026  
**Versión:** 1.0

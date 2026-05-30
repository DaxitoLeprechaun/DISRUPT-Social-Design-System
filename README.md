# DISRUPT — Social Media Design System

> **"at DISRUPT"** — Agencia de estrategia y creatividad digital.  
> Este repositorio documenta el sistema de diseño extraído del *Bundle de Identidad Redes Sociales* (53 assets, 2026).

---

## COMPANY / PRODUCT CONTEXT

| Campo | Detalle |
|---|---|
| **Marca** | at DISRUPT |
| **Categoría** | Agencia de Marketing / Creatividad Digital |
| **Producto documentado** | Bundle de Identidad Redes Sociales |
| **Alcance** | Social Media Posts — Instagram, Facebook, LinkedIn |
| **Formatos cubiertos** | 1:1 (Square), 4:5 (Portrait), 9:16 (Stories), 1.91:1 (Landscape) |
| **Idioma visual** | Glassmorphism · Gradient blobs · Ultra-bold type · Dark/Light duality |
| **Fuente de assets** | `Bundle de Identidad Redes Sociales/` — 53 JPGs |

### Sources
- `assets/brand/` — 53 imágenes originales del Bundle
- `colors_and_type.css` — tokens de color, tipo, espaciado y efectos
- `preview/` — cards HTML de referencia visual
- `ui_kits/social_media/` — UI kit completo para posts
- `SKILL.md` — skill para agentes AI

---

## CONTENT FUNDAMENTALS

### Voz y Tono
DISRUPT comunica con **autoridad editorial** y **provocación inteligente**. Sus posts son declaraciones, no descripciones.

| Dimensión | Estilo |
|---|---|
| **Registro** | Directo · Culto · Seguro |
| **Tono** | Afirmativo. Nunca defensivo |
| **Longitud** | Titulares cortos + una línea de contexto. Sin relleno |
| **Idioma** | Inglés para posts de agencia (posicionamiento global) |
| **Voz** | Primera persona plural → "We build." / Tercera provocadora → "The large-agency model has a structural flaw" |

### Tipografías de Contenido

| Rol | Familia | Peso | Tamaño aprox. |
|---|---|---|---|
| **Display / Hero** | Inter | Black 900 | 80–128 px |
| **Headline de post** | Inter | Bold 700 | 48–80 px |
| **Body editorial** | Inter | Regular 400 | 16–22 px |
| **Label / Tag** | Inter | Medium 500 + Uppercase | 11–13 px |
| **Wordmark "at DISRUPT"** | Inter | Black 900 (`at` small, `DISRUPT` grande) | variable |

### Patrones narrativos observados
1. **Contraste conceptual** — "Authority vs. Presence"  
2. **Afirmación disruptiva** — "The large-agency model has a structural flaw"  
3. **Reencuadre de tecnología** — "AI does not replace editorial thinking. In the right hands, it amplifies it."  
4. **Identidad de categoría** — Sticker del logo + fondos de color (4 variantes)

---

## VISUAL FOUNDATIONS

### Sistema de Color

```
PRIMARIOS
  Blanco puro       #FFFFFF   — fondo claro canónico
  Negro profundo    #0A0A0A   — fondo oscuro canónico
  Off-white cálido  #F0EFED   — superficie secundaria luz
  Gris claro        #EAEAE8   — bordes y fondos neutros
  Dark Purple       #1C1228   — editorial oscuro (posts premium)

FAMILIA AZUL (brand core)
  Azul 100   #D9EEFF  
  Azul 300   #7BBFF7   ← pétalo de flor (light)
  Azul 500   #2B6FD4   ← azul principal
  Azul 600   #1A4FA8   ← confianza / profundidad

ACENTOS (blobs / gradients)
  Rosado    #F7A8A8 → #E8687A
  Violeta   #C4B0F7 → #9B78E8
  Verde     #85E89C → #3EC96B
  Durazno   #F7C49A → #E8A87C
  Sky       #A8D8F0 → #7BBFF7

TEXTO
  Primario  #1A1A1A
  Secundario #4A4A4A
  Label     #6B6B6B
  On Dark   #FFFFFF
```

### Paleta de la Flor (Logo)
El ícono de DISRUPT es una **flor de 4 pétalos** en gradiente ice-blue/white:

| Pétalo | Color |
|---|---|
| Superior | `#B9DCF5` |
| Derecho | `#A8CEF0` |
| Inferior | `#C5E0F7` |
| Izquierdo | `#D0E8F8` |
| Centro (overlap) | `#DAEEFA` |

**Variantes cromáticas del logo:** Azul (default), Rosado, Violeta, Verde, Durazno, Monocromático oscuro, Blanco.

### Texturas y Efectos Visuales

| Efecto | Descripción | Uso |
|---|---|---|
| **Gradient blobs** | Manchas de color suaves y desenfocadas | Fondos de posts, acento decorativo |
| **Glassmorphism** | `backdrop-filter: blur(20px)` + borde semitransparente + sombra sutil | Cards sobre gradientes |
| **Grain / noise** | Textura granulada sutil en fondos | Posts con gradientes sólidos |
| **Rounded glass card** | Radio 36px + borde blanco translúcido | Frame para imagen de post |
| **Shadow card blanca** | Card blanca opaca, sombra suave, radio 24px | Tag de texto + datos secundarios |
| **Sticker peel** | Logo sobre fondo blanco con borde curvo y sombra | Brand stamp en posts de color |

### Composición de Posts

```
ESTRUCTURA LIGHT
┌─────────────────────────────┐
│ Agency (label, top-left)    │   at DISRUPT (logo, top-right)
│ ─────────────────────────── │   ← hairline separator
│                             │
│   [BLOB DECORATOR top-left] │
│                             │
│   [GLASS CARD — content]    │
│                             │
│   [WHITE SHADOW CARD]       │   ← overlapping bottom-right
└─────────────────────────────┘

ESTRUCTURA TYPOGRAPHIC (editorial)
┌─────────────────────────────┐
│ Agency      at DISRUPT      │
│ ─────────── ─────────────── │
│                             │
│  MASSIVE HEADLINE           │   ← Inter Black, full-bleed
│  (2–3 lines)                │
│                             │
│  Body text, lighter weight  │   ← bottom quarter
└─────────────────────────────┘

ESTRUCTURA PHOTO (dark)
┌─────────────────────────────┐
│ Agency      at DISRUPT      │   ← white text on dark
│ ─────────── ─────────────── │
│                             │
│  [FULL-BLEED PHOTO]         │
│                             │
│  BIG HEADLINE (white bold)  │
└─────────────────────────────┘
```

### Espaciado y Márgenes
- **Margen de contenido:** `5–6%` del ancho del canvas
- **Header bar height:** ~80px (label + logo + separador)
- **Separador:** línea de 1px, negro/gris sobre blanco, blanco sobre negro
- **Radio de cards:** 24–36px
- **Gap entre elementos:** 24–48px

---

## ICONOGRAFÍA

### El Símbolo "Flor DISRUPT"

El ícono es una abstracción de **4 pétalos redondeados** organizados en cruz, con superposición central translúcida. Representa innovación orgánica y conectividad.

**Variantes documentadas:**
- `1.jpg` — Logo blanco sobre fondo blanco (versión limpia)
- `2.jpg` — Logo blanco sobre negro (versión oscura)
- `3.jpg` — Logo negro sobre off-white
- `8.jpg` — Logo negro con flor azul-violeta (variante púrpura)
- `10.jpg` — Logo negro con flor azul-violeta (variante violeta sola)
- `7.jpg` — Stickers × 4 colores (azul, rosa, violeta, verde)

**Reglas de uso:**
1. La flor siempre acompaña al wordmark "at DISRUPT" — nunca va sola en posts
2. En fondos de color, el logo aparece como sticker blanco opaco con sombra
3. En dark mode: flor en gradiente ice-blue, wordmark en blanco
4. La flor se escala al 60–80% del alto del wordmark

### Sistema de Stickers
Los stickers (imagen `7.jpg`) muestran el logo sobre fondo blanco con esquinas redondeadas + sombra de despegado. Versiones: Azul, Rosa, Violeta, Verde.

---

## FILE INDEX / MANIFEST

```
DISRUPT-Social-Design-System/
├── README.md                          ← Este archivo
├── colors_and_type.css                ← Tokens CSS completos
├── SKILL.md                           ← Skill para agentes AI
│
├── fonts/                             ← (Inter via Google Fonts CDN)
│
├── assets/
│   └── brand/                         ← 53 JPGs originales del Bundle
│       ├── 1.jpg  → Logo light (white bg)
│       ├── 2.jpg  → Logo dark (black bg)
│       ├── 3.jpg  → Logo light (off-white bg)
│       ├── 4.jpg  → Color blobs light — Blue/Pink/Purple/Green
│       ├── 5.jpg  → Color blobs dark — Blue/Pink/Purple/Green
│       ├── 6.jpg  → Color blobs medium — Blue/Pink/Purple/Green
│       ├── 7.jpg  → Stickers × 4 colores con bandas de color
│       ├── 8.jpg  → Logo variante Purple flower
│       ├── 9.jpg  → Textura blob verde-amarillo (landscape)
│       ├── 10.jpg → Logo variante Purple/Lilac flower
│       ├── 11.jpg → [asset adicional]
│       ├── 12–19 → Fondos gradient templates
│       ├── 20–29 → Post templates — frame glass (light variants)
│       ├── 25.jpg → Post template frame glass black/pink
│       ├── 30.jpg → Post template frame glass green
│       ├── 31–34 → Typographic post templates
│       ├── 35–39 → Editorial posts (text-heavy, agency positioning)
│       ├── 40.jpg → Post con blob pink, texto editorial negro
│       ├── 41–49 → Posts editorial dark / photo + headline
│       ├── 50.jpg → Photo post dark purple + rose + headline
│       └── 51–53 → [assets adicionales]
│
├── preview/
│   └── index.html                     ← Cards de preview del sistema
│
└── ui_kits/
    └── social_media/
        └── index.html                 ← UI Kit completo Social Media
```

---

## QUICK START

```html
<!-- 1. Importar tokens -->
<link rel="stylesheet" href="../../colors_and_type.css">

<!-- 2. Usar variables en tu CSS -->
<style>
  .post-card {
    background: var(--bg-off-white);
    font-family: var(--font-sans);
    border-radius: var(--radius-xl);
    color: var(--text-primary);
  }
  .post-headline {
    font-size: var(--text-5xl);
    font-weight: var(--weight-black);
    letter-spacing: var(--tracking-tight);
  }
</style>
```

---

*Generado por Antigravity IDE · Mayo 2026*

---
name: disrupt-social-design-system
description: >
  Design system completo para la agencia "at DISRUPT". Extrae, documenta y aplica
  los tokens de identidad visual (colores, tipografía, efectos, componentes) del
  Bundle de Identidad de Redes Sociales. Úsalo cuando necesites crear posts,
  templates, o cualquier asset de comunicación visual alineado con la marca DISRUPT.
---

# DISRUPT Social Media Design System — SKILL

## CUÁNDO USAR ESTE SKILL

Activa este skill cuando:
- Necesitas crear o editar posts para las redes sociales de DISRUPT
- Quieres generar nuevos templates HTML fieles a la identidad visual
- Necesitas tokens de color, tipo o espaciado exactos de la marca
- Debes documentar nuevos assets o actualizar el sistema
- Quieres crear variaciones de posts (paleta azul, rosada, violeta, verde, dark)

---

## IDENTIDAD VISUAL RÁPIDA

### Logotipo
- **Wordmark**: `at` (pequeño, peso 500) + `DISRUPT` (grande, peso 900)
- **Símbolo**: Flor de 4 pétalos en gradiente ice-blue/white
- **Variantes**: Light (negro sobre blanco), Dark (blanco sobre negro), Color (pétalos en colores de acento)

### Paletas
| Nombre | BG | Blob principal | Blob secundario |
|---|---|---|---|
| **Blue** (default) | `#F0EFED` | `rgba(123,191,247,0.6)` | `rgba(43,111,212,0.4)` |
| **Pink** | `#FFF5F5` | `rgba(247,168,168,0.6)` | `rgba(232,104,122,0.45)` |
| **Violet** | `#F3F0FF` | `rgba(196,176,247,0.6)` | `rgba(155,120,232,0.45)` |
| **Green** | `#F2FFF5` | `rgba(133,232,156,0.6)` | `rgba(62,201,107,0.45)` |
| **Dark** | `#0A0A0A` | `rgba(123,191,247,0.35)` | `rgba(43,111,212,0.25)` |

### Tipografía
- **Familia**: Inter (Google Fonts)
- **Hero / Headline**: Black 900, tracking -0.04em, leading 1.0–1.1
- **Body**: Regular 400, leading 1.65
- **Label**: Medium 500, uppercase, tracking 0.14em

---

## ESTRUCTURA DE ARCHIVOS

```
DISRUPT-Social-Design-System/
├── README.md               # Documentación completa
├── colors_and_type.css     # Todos los tokens CSS (importar primero)
├── SKILL.md                # Este archivo
├── assets/brand/           # 53 JPGs del Bundle original (1.jpg – 53.jpg)
├── preview/index.html      # Cards de colores, tipo, componentes, assets
└── ui_kits/social_media/
    └── index.html          # UI Kit interactivo + Post Builder
```

---

## TEMPLATES DE POST HTML

### Template Base — Post Frame Glass

```html
<!DOCTYPE html>
<html>
<head>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
  <style>
    /* Importa desde el design system */
    /* O copia las variables críticas: */
    :root {
      --bg: #F0EFED;
      --blob1: rgba(123,191,247,0.6);
      --blob2: rgba(43,111,212,0.4);
      --text: #1A1A1A;
      --glass: rgba(255,255,255,0.55);
    }
    body { margin: 0; font-family: 'Inter', sans-serif; }
    
    .post {
      width: 1080px; height: 1350px; /* 4:5 */
      position: relative; overflow: hidden;
      background: var(--bg);
    }
    /* Blob superior izquierdo */
    .post::before {
      content: '';
      position: absolute; width: 55%; height: 50%;
      top: -10%; left: -10%;
      border-radius: 50%;
      background: radial-gradient(ellipse, var(--blob1) 0%, transparent 70%);
      filter: blur(50px);
    }
    /* Blob inferior derecho */
    .post::after {
      content: '';
      position: absolute; width: 50%; height: 45%;
      bottom: -5%; right: -5%;
      border-radius: 50%;
      background: radial-gradient(ellipse, var(--blob2) 0%, transparent 70%);
      filter: blur(45px);
    }

    /* Header */
    .header {
      position: relative; z-index: 10;
      display: flex; justify-content: space-between; align-items: center;
      padding: 54px 65px 36px;
      border-bottom: 1px solid rgba(0,0,0,0.12);
    }
    .label { font-size: 22px; font-weight: 400; color: #666; }
    .wordmark { font-size: 36px; font-weight: 900; letter-spacing: -0.03em; color: #1a1a1a; }
    .wordmark .at { font-size: 22px; font-weight: 500; }

    /* Glass Frame */
    .frame {
      position: relative; z-index: 10;
      margin: 54px 65px 0;
      border-radius: 36px;
      background: var(--glass);
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255,255,255,0.45);
      box-shadow: 0 8px 40px rgba(0,0,0,0.08);
      min-height: 700px;
      display: flex; align-items: center; justify-content: center;
    }

    /* White Tag Card */
    .tag-card {
      position: absolute; z-index: 20;
      bottom: 280px; right: 65px;
      background: white;
      border-radius: 24px;
      box-shadow: 0 8px 40px rgba(0,0,0,0.12);
      padding: 36px 42px;
      width: 420px;
    }
    
    /* Headline */
    .headline {
      position: relative; z-index: 10;
      padding: 48px 65px;
      font-size: 120px; font-weight: 900;
      letter-spacing: -0.04em; line-height: 1.0;
      color: var(--text);
    }
  </style>
</head>
<body>
  <div class="post">
    <div class="header">
      <span class="label">Agency</span>
      <span class="wordmark"><span class="at">at </span>DISRUPT</span>
    </div>
    <div class="frame">
      <!-- Imagen o contenido principal -->
    </div>
    <div class="tag-card">
      <!-- Texto secundario, datos, CTA -->
    </div>
    <div class="headline">
      Tu headline<br>aquí
    </div>
  </div>
</body>
</html>
```

### Template — Post Tipográfico Editorial

```html
<!-- Post con texto grande, sin frame glass -->
<div class="post" style="background:#F0EFED;">
  <div class="header">
    <span class="label">Agency</span>
    <span class="wordmark"><span class="at">at </span>DISRUPT</span>
  </div>
  <div class="headline" style="font-size:140px;padding-top:80px;">
    Authority vs.<br>Presence
  </div>
  <div style="padding:0 65px;font-size:26px;line-height:1.65;color:#4a4a4a;max-width:800px;">
    When you lead through presence, your formal authority is 
    amplified because people respect <u>who</u> is leading, 
    not just the <strong>position</strong> they hold.
  </div>
</div>
```

---

## REGLAS DE COMPOSICIÓN

1. **Header siempre visible**: `Agency` label top-left + `at DISRUPT` top-right, separados por hairline 1px
2. **Blob decorativo**: esquina opuesta al contenido principal
3. **Glass frame**: radio 36px, blur 20px, borde `rgba(white, 0.4)`, sombra `0 8px 40px rgba(0,0,0,0.08)`
4. **White tag card**: posición bottom-right superpuesta al frame, radio 24px, sombra suave
5. **Headline**: Inter Black 900, tracking -0.04em, leading 1.0
6. **Dark mode**: texto blanco, border del header `rgba(white, 0.15)`, glass oscuro `rgba(30,30,30,0.6)`

---

## VARIANTES DISPONIBLES

| Ref. Imagen | Variante | Paleta |
|---|---|---|
| `1.jpg` | Logo minimal | White |
| `2.jpg` | Logo dark | Black |
| `4–6.jpg` | Color blobs | Blue/Pink/Violet/Green |
| `7.jpg` | Sticker × 4 | Multicolor |
| `20–34.jpg` | Frame glass | 5 paletas × light/dark |
| `35–47.jpg` | Editorial text | 5 paletas × light/dark |
| `48–53.jpg` | Photo + headline | Dark + acentos |

---

## CÓMO ACTUALIZAR EL SISTEMA

1. Agrega nuevos assets en `assets/brand/`
2. Actualiza el número máximo en `preview/index.html` (variable en el loop JS)
3. Agrega el template en `ui_kits/social_media/index.html` → array `templates`
4. Si hay nuevos colores, agrega variables en `colors_and_type.css`
5. Actualiza el manifest en `README.md`

---

*Skill generado por Antigravity IDE · Mayo 2026*

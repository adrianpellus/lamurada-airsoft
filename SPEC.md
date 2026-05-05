# La Murada Airsoft — Sunday Match Web

## 1. Concept & Vision

Landing page para el evento "Sunday Match" de La Murada Airsoft (10 mayo 2026). Web con estética militar/táctica, oscuro y directo — transmite urgencia, accion y hermandad. El usuario debe sentir que esto es un evento real donde quiere estar.

## 2. Design Language

**Aesthetic:** Militar moderno, gritty, nocturno. Piensa operador especial pero accesible.

**Colors:**
- Background: `#0a0a0a` (negro profundo)
- Primary: `#b8952b` (dorado militar)
- Secondary: `#1a1a1a` (gris oscuro)
- Accent: `#c9393b` (rojo tactico)
- Text: `#f0f0f0` (blanco humo)
- Text muted: `#888888`

**Typography:**
- Headings: `Oswald` (bold, condensed, militar)
- Body: `Roboto Condensed`
- Monospace accents: `Share Tech Mono`

**Motion:**
- Entrance: fade-in + slide-up, staggered 80ms
- Hover buttons: scale 1.03, border glow
- Scroll reveals con IntersectionObserver
- Scan line animation sutil en hero

**Visual assets:**
- Iconos: Font Awesome 6 (solid)
- Imagen del poster como hero principal
- Estampado de camo como textura SVG inline

## 3. Layout & Structure

```
[NAV] Logo | Fecha destaque
[HERO] Poster event image + overlay + titulo principal
[INFO] CardGrid: Horario / Location / What to bring
[MAP] Google Maps embed (La Murada, Orihuela)
[CTA] Boton "Apuntate" grande
[FOOTER] Logo + redes + derechos
```

**Responsive:** Mobile-first, stack en mobile, 3-col grid en desktop para cards.

## 4. Features & Interactions

- **Hero parallax** sutil en scroll
- **Countdown timer** al evento (falta countdown.js, se simula con CSS)
- **Cards con hover lift** y borde dorado
- **Boton CTA** con pulse animation
- **Smooth scroll** a secciones
- **Map iframe** de La Murada, Orihuela

## 5. Component Inventory

### Hero Section
- Full viewport height
- Background image del poster con overlay oscuro
- Badge superior: "EVENTO PRESENCIAL"
- Titulo: "SUNDAY MATCH" en Oswald XXL
- Sub: "La Murada Airsoft"
- Fecha: "10 de Mayo 2026"
- Flecha animada bajando

### Info Cards
- 3 cards: Horario / Normas / Equipamiento
- Icono + titulo + lista
- Hover: lift + border glow dorado

### CTA Section
- Fondo con textura camo
- Titulo motivacional
- Boton grande dorado

### Footer
- Minimalista, oscuro

## 6. Technical Approach

- **Single HTML file** con CSS inline y JS vanilla
- No frameworks, no build step
- Google Fonts via CDN
- Font Awesome via CDN
- Google Maps iframe embedido
- IntersectionObserver para animaciones on-scroll

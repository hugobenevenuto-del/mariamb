# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Landing page for **Maria Bonita Estética** — a beauty salon in Rio Bonito/RJ, Brazil. Static HTML + CSS + vanilla JS, no build step or dependencies.

## Client Brand

- **Name:** Maria Bonita Estética
- **Address:** Av. Sete de Maio, 349 – Loja 2, Rio Bonito/RJ
- **WhatsApp:** (21) 96932-3119 → `https://wa.me/5521969323119`
- **Instagram:** @m.ariabonitaestetica → `https://www.instagram.com/m.ariabonitaestetica`
- **Slogan:** *Bonita é ser você na sua melhor versão.*
- **Brand colors:** dark green `#1a3a2a`, gold `#c9a84c`, cream (logo text) `#ddd3be`
- **Logo file:** `fotos/LOGO.jpg`
- **Services:** Lash Designer, Manicure, Pedicure, Alongamento de Unhas, Harmonização Facial, Preenchimento Facial, Peelings Químicos

## Architecture

| File | Purpose |
|---|---|
| `index.html` | All markup + vanilla JS (gallery filters, lightbox) |
| `style.css` | All styles via CSS custom properties. Mobile breakpoint at 768px. |
| `fotos/` | All images used in the gallery and logo |

**Fonts (Google Fonts):**
- `Josefin Sans` thin/light — header logo name, watermark MB
- `Cormorant Garamond` — headings, slogan, decorative text
- `Montserrat` — body, buttons, labels

**CSS variables (`:root`):**
- `--verde` `#1a3a2a` — primary dark green
- `--dourado` `#c9a84c` — gold accent
- `--creme-logo` `#ddd3be` — cream, matches logo text color

## Page Structure (top → bottom)

1. **Header** — fixed, logo text ("maria bonita" in Josefin Sans thin) + nav + WhatsApp CTA button
2. **Hero** — full-height, dark green background, large MB watermark, headline + slogan + CTAs
3. **Serviços** — 6 service cards in responsive grid (cream background)
4. **Sobre** — "Nossa história" text about the three sisters who founded the studio
5. **Galeria** — 7 photos with category filters (Lash, Unhas, Facial, Corporal) + lightbox
6. **CTA** — full-width band with WhatsApp button
7. **Contato** — address, WhatsApp, Instagram
8. **Footer**
9. **WhatsApp float button** — fixed bottom-right

## Gallery photos (`fotos/`)

| File | Category |
|---|---|
| `foto 2.JPG` | Lash Designer |
| `576030837_...webp` | Lash Designer |
| `524566758_...jpg` | Unhas |
| `foto 7.JPG` | Unhas |
| `foto 4.JPG` | Facial |
| `619900521_...jpg` | Corporal |
| `foto 6.JPG` | Corporal |

To add more photos: place the file in `fotos/` and add a new `.gallery-item` block in the gallery grid inside `index.html`.

## Development

Open `index.html` directly in a browser — no server required.

```bash
npx serve .
# or
python -m http.server 8000
```

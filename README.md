# Haanie Hashim — Portfolio Website

A personal portfolio website for **Haanie Hashim**, inspired by the design language of [therishithakor.com](https://therishithakor.com/). Built as a single-page experience with interactive room pages, smooth animations, and a dark/light mode toggle.

## 🌐 Live Structure

```
haanie-site/
├── index.html                  # Main page — hero, doors, about, contact
├── fonts/
│   ├── onest-latin.woff2       # Onest font (latin)
│   └── onest-latin-ext.woff2   # Onest font (latin extended)
├── web-developer/
│   └── index.html              # Web Development room
├── app-developer/
│   └── index.html              # App Development room
├── ui-ux-designer/
│   └── index.html              # UI/UX Design room
├── graphic-designer/
│   └── index.html              # Graphic Design room
└── photographer/
    └── index.html              # Photography room (draggable photo wall)
```

## 🚀 How It Works

### Main Page (`index.html`)
- **Loader** — Colored bars stack up on page load, then slide apart
- **Hero** — Name, tagline, and portrait with a liquid-reveal cursor trail (color ↔ B&W); photo embedded inline as a data URI (no external image file)
- **Doors** — 5 interactive doors (Web Dev, App Dev, UI/UX, Graphic Design, Photography) that open with a walk-through animation into embedded iframe rooms
- **Pull-cord** — Dark/light mode toggle styled as a wall cord
- **Smooth scrolling** — Powered by Lenis
- **About section** — Story timeline with scroll animations
- **Contact** — Modal with a step-by-step questionnaire form

### Room Pages
Each room page is a self-contained HTML file loaded via iframe when a door is opened. They share:

- **Sticky stacking cards** with 3D mockups (monitors for web/UI, iPhones for apps)
- **Scroll-triggered reveal animations** — text slides up, mockups slide in from the side
- **Sticky navigation bar** with live clock, menu button, and back-to-doors button
- **Full-screen mobile menu** with staggered item animations
- **Dark/light mode sync** — rooms follow the main page's mode toggle
- **Back-to-top button** with SVG progress ring
- **Footer** with name marquee, navigation columns, and availability status

### Room-specific features

| Room | Design |
|------|--------|
| **Web Developer** | 7 project cards with 3D perspective monitor mockups, alternating left/right layout |
| **App Developer** | iPhone mockups with Dynamic Island, status bar, app icons |
| **UI/UX Designer** | Monitor mockups for design showcases |
| **Graphic Designer** | Horizontal-scrolling "clotheslines" with hanging prints, brand worlds with unique color palettes, lightbox |
| **Photographer** | Infinite draggable photo wall with star-field parallax canvas, 3D tilt on drag, lightbox with keyboard nav |

## 🛠 Tech Stack

- **Pure HTML/CSS/JavaScript** — No frameworks, no build step
- **Onest** typeface (variable weight 100–900)
- **Lenis** smooth scroll (main page)
- **CSS custom properties** for theming (light/dark mode)
- **IntersectionObserver** for scroll animations
- **Canvas API** for the photographer's star field
- **postMessage API** for iframe ↔ parent communication
- **View Transitions API** (photographer page)

## 📱 Responsive

- Desktop: full navigation bar, floating back button, wide layouts
- Tablet: condensed nav, adapted card layouts
- Mobile: hamburger menu, stacked cards, touch-friendly drag on photo wall

## 🌗 Dark Mode

Toggle via the pull-cord on the main page. Mode persists via `localStorage` and syncs across all iframe rooms in real time.

## 📄 License

This is a personal portfolio site. Content and identity belong to **Haanie Hashim**.

---

**Contact:** haaniehashim@gmail.com

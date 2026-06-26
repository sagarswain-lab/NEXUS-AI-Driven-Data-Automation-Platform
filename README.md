# NEXUS - AI-Driven Data Automation Platform

> **FrontEnd Battle 3.0 - Phase 1 Submission**
> *Next-Gen AI Platform Speed Run - 26 June 2026*

---

## Live Demo

| Resource | Link |
|---|---|
| **Live Deployment** | [https://sagarswain-lab.github.io/NEXUS-AI-Driven-Data-Automation-Platform/](https://sagarswain-lab.github.io/NEXUS-AI-Driven-Data-Automation-Platform/) |

### Walkthrough Video
<video src="video.mp4" width="100%" autoplay loop muted playsinline controls></video>

---

## Project Overview

**NEXUS** is a premium, high-converting, fully responsive landing page for a next-generation AI-driven data automation platform. Built under a strict 4-hour competitive countdown for **FrontEnd Battle 3.0 - Phase 1**, the page demonstrates enterprise-grade motion choreography, architectural integrity, engineering speed, and full SEO hygiene.

The design challenge: build a page that feels like a real SaaS product — complete with animated data workflows, live performance counters, GPU-rendered 3D particles, and pixel-perfect responsive behaviour across desktop, tablet, and mobile.

---

## Key Highlights

- **Single-file architecture** — entire project in one index.html (HTML + embedded CSS + embedded JS)
- **Premium dark-mode design** — custom gold/teal/midnight color palette, glassmorphism cards, micro-animations
- **Three.js hero canvas** — GPU-rendered 3D particle field with mouse-reactive drift
- **Animated workflow builder** — SVG path animations with animated data-pulse dots
- **Live performance dashboard** — real-time fluctuating counters for throughput, latency, connectors, automation rate
- **Dynamic pricing** — multi-currency support (INR / USD / EUR), annual/monthly toggle with live price recalculation
- **Fully responsive** — adaptive layouts from 320px mobile to 4K desktop
- **Accessible** — ARIA roles, keyboard navigation, focus management, reduced-motion support
- **SEO-complete** — Open Graph, Twitter Cards, JSON-LD schema, canonical, meta robots

---

## Tech Stack

| Layer | Technology |
|---|---|
| Structure | Semantic HTML5 |
| Styling | Vanilla CSS (custom properties, grid, flexbox, animations, @property) |
| Scripting | Vanilla JavaScript (ES2022) |
| 3D Rendering | Three.js r128 (via CDN) |
| Typography | JetBrains Mono + Inter (Google Fonts) |
| Framework | None — pure browser-native |

---

## Page Sections

| # | Section | Description |
|---|---|---|
| 1 | **Hero** | Animated headline with glitch effect, Three.js particle canvas, scroll-reveal CTAs |
| 2 | **Platform Stats** | Key metrics — 99.9% uptime, <10ms latency, 500+ integrations, SOC2 |
| 3 | **Features** | 6-card Bento Grid (desktop) / accordion (mobile) showcasing core modules |
| 4 | **Workflow Builder** | Interactive node canvas with animated SVG flow paths and data pulses |
| 5 | **Performance** | Live-updating metric cards — throughput, latency, connectors, automation rate |
| 6 | **Pricing** | 3-tier cards (Starter / Pro / Enterprise) with currency toggle and annual savings |
| 7 | **FAQ** | Accessible accordion with smooth expand/collapse |
| 8 | **Footer CTA** | Call-to-action banner + full site footer with brand, platform, company, and legal links |

---

## Feature Modules (Bento Grid)

| Module | Tag | Description |
|---|---|---|
| **AI Pipeline Engine** | CORE MODULE | Self-healing data pipelines with schema-drift adaptation and auto-scaling |
| **Real-time Analytics** | ANALYTICS | Sub-10ms stream analytics, anomaly detection, predictive dashboards |
| **500+ Integrations** | CONNECTIVITY | Native connectors for every major warehouse, CRM, and API |
| **Workflow Automation** | AUTOMATION | Zero-code automation chains with AI-suggested optimizations |
| **Semantic AI Search** | SEARCH | Natural language queries across all data — no SQL required |
| **Growth Intelligence** | AI INTELLIGENCE | Revenue forecasting, churn prediction, market signal detection |

---

## Design & Motion Details

### Custom Cursor
Two-layer cursor (gold dot + expanding ring) follows pointer with requestAnimationFrame lerp. Ring scales on interactive elements.

### Page Loader
Staggered spinning cube animation (ldSpin keyframe) runs until DOM is ready, then fades out smoothly.

### Hero Animation
- Three.js BufferGeometry point cloud with 3,000 vertices forming a drifting particle field
- Mouse-reactive — particles gently follow cursor in 3D space
- Headline reveal using sequential opacity + translateY via the Web Animations API
- NEXUS glitch effect via CSS ::before/::after pseudo-elements and clip-path keyframes

### Scroll-Reveal
IntersectionObserver watches .rv (reveal) elements with stagger delays via .d1–.d4 utility classes.

### Workflow Canvas
- Six nodes across three columns: Triggers → Processing → Outputs
- SVG <path> connectors with stroke-dasharray + stroke-dashoffset animated flow
- Animated SVG <circle> dots travel paths using CSS offset-path
- Active nodes pulse with a 
odeActGlow drop-shadow keyframe
- **Mobile fallback**: vertical golden gradient line + gold left-border on active nodes

### Performance Counters
JS random-walk loop updates four live metrics every 1,200ms:
- **Pipeline Throughput** — ~94,204 events/sec
- **Query Latency** — ~6.8 ms
- **Active Connectors** — ~512
- **Automation Rate** — ~96.7%

### Pricing Engine
- PRICING config object holds base INR prices + per-currency conversion tariffs
- Toggle between Monthly / Annual (20% discount applied live)
- Currency <select> (INR / USD / EUR) updates all displayed prices instantly

---

## Responsive Behaviour

| Breakpoint | Layout Changes |
|---|---|
| > 1024px | Full desktop — bento grid, side-by-side workflow, 3-column pricing |
| <= 1024px | Tablet — bento hidden (accordion shown), single-column workflow, 1-column pricing |
| <= 640px | Mobile — hamburger nav overlay, centred header CTA, stacked footer, vertical workflow nodes |

### Mobile Navigation Overlay
- Hamburger button (top-right) opens a full-viewport dark overlay (z-index: 200)
- Same 3-line icon inside the overlay acts as the close toggle
- Header is fully hidden while overlay is open to prevent bleed-through
- Clicking any nav link closes the overlay and scrolls to the target section
- Keyboard accessible — Escape key closes the overlay

---

## SEO Implementation

`html
<!-- Title & Meta Description -->
<title>NEXUS | AI-Driven Data Automation Platform</title>
<meta name="description" content="...">

<!-- Open Graph (Facebook / LinkedIn) -->
<meta property="og:title"       content="...">
<meta property="og:description" content="...">
<meta property="og:image"       content="...">
<meta property="og:type"        content="website">

<!-- Twitter Card -->
<meta name="twitter:card"        content="summary_large_image">
<meta name="twitter:title"       content="...">
<meta name="twitter:description" content="...">

<!-- Canonical & Robots -->
<link rel="canonical" href="...">
<meta name="robots" content="index, follow">

<!-- JSON-LD Structured Data -->
<script type="application/ld+json">
  {
    "@type": "SoftwareApplication",
    "name": "NEXUS",
    "applicationCategory": "BusinessApplication",
    "offers": { "@type": "AggregateOffer", "priceCurrency": "INR" }
  }
</script>
`

Additional SEO practices:
- Single <h1> per page with proper heading hierarchy
- Semantic HTML5 landmarks (<header>, <main>, <section>, <footer>, <nav>)
- All SVGs carry ria-hidden="true" or a descriptive ria-label
- All interactive elements have unique, descriptive id attributes

---

## Accessibility

- All interactive elements keyboard-focusable with visible focus indicators
- ARIA roles used: 
avigation, dialog, list, listitem, utton, switch, rticle
- Dynamic attributes: ria-modal, ria-label, ria-live, ria-checked, ria-expanded
- @media (prefers-reduced-motion: reduce) disables all transitions and animations globally
- Mobile menu focus-trap — mobClose.focus() is called on open

---

## Easter Egg

Type the **Konami Code** on any keyboard:

`
↑  ↑  ↓  ↓  ←  →  ←  →  B  A
`

A golden particle burst explosion fires from the centre of the screen.

---

## Project Structure

`
FrontEnd Battle 3.0/
├── index.html     <- Entire project (HTML + embedded CSS + embedded JS, ~3,700 lines)
└── README.md      <- This file
`

All styles are in a <style> block inside <head>.  
All scripts are in a <script> block before </body>.  
**No build step. No bundler. No npm. Open in any browser.**

---

## Running Locally

`ash
# Option 1 — Open directly in browser
start index.html

# Option 2 — VS Code Live Server
# Install the "Live Server" extension
# Right-click index.html -> "Open with Live Server"

# Option 3 — Python HTTP server
python -m http.server 3000
# Visit http://localhost:3000
`

---

## Competition Requirements Checklist

| Requirement | Status |
|---|---|
| Premium responsive landing page | Done |
| Vanilla JS (no framework) | Done |
| Custom CSS (no Tailwind) | Done |
| SEO hygiene (meta, OG, schema, canonical) | Done |
| Motion choreography | Done |
| Mobile responsive | Done |
| Public GitHub repository | Done |
| Live deployment link | Done (see top of README) |
| Demo video (<=100MB) | Done (see top of README) |

---

## Author

**Sagar** — FrontEnd Battle 3.0 Participant

> Built entirely during the 4-hour competitive window: **2:00 PM – 6:00 PM, 26 June 2026**

---

## License

This project was created for the **FrontEnd Battle 3.0** hackathon. All rights reserved.

---

*Built with code, caffeine, and a countdown timer.*
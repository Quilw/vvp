# Växjö Vattenpolering AB - Website Project

## Company Info
- **Name**: Växjö Vattenpolering AB
- **Service**: Water polishing (vattenpolering) - surface finishing process for hard material parts
- **Clients**: Custom parts, car parts, industrial parts, marine parts
- **Address**: Rådjursvägen 15, 352 45 Växjö
- **Phone**: 0470-74 86 90
- **Location**: Växjö, Sweden

## Project Decisions
- **Language**: Swedish only
- **Theme**: Dark & metallic - industrial premium feel
- **Logo**: Create a simple text-based/minimal logo (SVG)
- **Style**: "Alive" - smooth animations, parallax, subtle motion
- **Hosting**: Cloudflare Pages at quilw.pages.dev
- **GitHub**: Push to github.com/Quilw (repo name TBD)
- **Tech Stack**: Astro + Tailwind CSS (static site, fast, perfect for Cloudflare Pages)
- **Photos**: 15 images in /Photos/ folder showing equipment, polished parts (aluminum, brass, steel)

## Website Sections (Planned)
- Hero with video/animated background
- Om oss (About us)
- Tjänster (Services) - water polishing explanation
- Galleri (Gallery) - showcase the 15 photos
- Kontakt (Contact) - address, phone, map embed
- Footer

## Design Direction
- Dark backgrounds (#0a0a0a, #1a1a1a)
- Metallic silver/steel accents
- Subtle blue tones (water reference)
- High-contrast typography
- Smooth scroll animations (intersection observer / GSAP)
- Photo showcase with hover effects

## Research Findings

### About Vattenpolering (Process)
- Water + fine abrasive media (glass beads) propelled under high pressure in a closed-loop system
- Water dampens impact → satin-smooth finish, no media embedding, only 1-2 μm material removal
- One-step: cleans, degreases, and polishes simultaneously
- Dustless, environmentally friendly, safe for precision parts
- Works on: aluminum, steel, stainless, brass, bronze, chrome
- Applications: automotive, industrial, marine, custom/restoration
- Key advantage over dry blasting: superior finish, no dust, no dimensional impact, surface sealing

### Swedish Copy Snippets (Ready to Use)

**Hero tagline:**
"Precision i varje yta" (subtitle: "Vi ger metall nytt liv genom vattenpolering — den skonsamma ytbehandlingen som levererar resultat i världsklass.")

**Om oss:**
"Växjö Vattenpolering AB är specialister på vattenpolering — en avancerad ytbehandlingsmetod som återställer och förädlar metallytor med enastående precision. Med vår teknik avlägsnar vi smuts, oxidering och slitage utan att påverka detaljens mått eller form. Resultatet? En slät, blank yta som både ser ut och presterar som ny."

**Tjänster:**
"Vattenpolering är en effektiv och miljövänlig metod för ytbehandling av metall. Genom att kombinera vatten med fint slipmedel under högt tryck uppnår vi en jämn, satinblank yta som är svår att nå med traditionella metoder. Processen rengör, avfettar och polerar i ett enda steg — helt utan damm, kemikalier eller risk för materialpåverkan."

**Process (4 steg):**
1. Förberedelse — "Vi inspekterar varje detalj noggrant och väljer rätt slipmedel och inställningar baserat på material och önskat resultat."
2. Vattenpolering — "Detaljen behandlas i vår maskin där en blandning av vatten och fint slipmedel under högt tryck skonsamt avlägsnar smuts, oxidering och ojämnheter."
3. Kvalitetskontroll — "Efter behandlingen inspekteras ytan för att säkerställa att resultatet möter våra höga krav."
4. Leverans — "Detaljen skyddas och förpackas omsorgsfullt, redo för montering eller vidare behandling."

**Galleri:**
"Se skillnaden med egna ögon. Våra före- och efterbilder visar kraften i vattenpolering."

**Material:**
"Vi behandlar aluminium, stål, rostfritt, mässing, brons, krom och andra hårda material."

### Design Inspiration Notes

**Color palette (confirmed):**
- Backgrounds: #0a0a0a (hero), #111111, #1a1a1a (alternating sections)
- Metallic accents: #C0C0C0 (silver), #71797E (steel gray)
- Water accent: #0ea5e9 (sky blue) or #3b82f6 (electric blue) for CTAs
- Text: #ffffff (headings), #a1a1aa (body text)

**Layout patterns from industry leaders:**
- Single-page scroll with full-viewport hero (video or animated background)
- Sticky transparent nav → solid on scroll
- Alternating dark section backgrounds for visual rhythm
- Before/After imagery is a MUST (strongest pattern in competitor sites)
- Three-column grids for services/features
- Split layouts for about/contact sections

**Animation approach:**
- GSAP ScrollTrigger for scroll-reveal animations (fade-in, slide-up)
- Parallax on background images
- Hover effects on gallery (scale + brightness + overlay)
- Subtle water/particle effects in hero (keep lightweight)
- Counter animations for stats if applicable
- Smooth scrolling via CSS scroll-behavior or Lenis

**Key differentiator opportunity:**
Swedish competitors (Bålsta, OSSO, Vattenpolerat) all use basic WordPress themes with light backgrounds. A dark, premium, animated site will immediately stand out in this market.

See `/research-notes.md` for full detailed research including sources.

## Project Structure
```
src/
  layouts/Layout.astro    — Base layout with dark theme, Inter font, Swedish meta tags
  pages/index.astro       — Single-page with section placeholders (hero, om-oss, tjanster, galleri, kontakt, footer)
  styles/global.css       — Tailwind v4 config with custom theme (@theme block)
  components/             — Empty, ready for section components
public/
  images/                 — 15 renamed photos (see Photo Mapping below)
  logo.svg                — Metallic gradient SVG text logo
```

## Tailwind v4 Custom Theme (in global.css @theme block)
- Dark: dark-950 (#0a0a0a), dark-900 (#111111), dark-800 (#1a1a1a), dark-700 (#222222), dark-600 (#2a2a2a)
- Silver: silver-300 (#c0c0c0), silver-200 (#d4d4d4), silver-100 (#e0e0e0)
- Steel: steel-500 (#71797E), steel-400 (#848884)
- Water: water-700 (#1e3a5f), water-500 (#2563eb), water-400 (#3b82f6)
- Font: Inter (Google Fonts)

## Photo Mapping (Photos/ → public/images/)
| Original filename | Renamed | Content |
|---|---|---|
| 594163691_... | blasting-cabinet.jpg | Blasting/polishing cabinet (equipment) |
| 610828752_... | husqvarna-engine-cover-before.jpg | Husqvarna engine cover – BEFORE polishing |
| 611068885_... | husqvarna-engine-cover-after.jpg | Husqvarna engine cover – AFTER polishing |
| 611576275_... | brass-marine-intake-strainers.jpg | Polished brass marine intake strainers |
| 611590408_... | steel-thermostat-housing-before.jpg | Steel thermostat housing – BEFORE polishing |
| 612318791_... | edelbrock-intake-manifold.jpg | Edelbrock Performer aluminum intake manifold |
| 612325640_... | steel-thermostat-housing-after.jpg | Steel thermostat housing – AFTER polishing |
| 613720896_... | dark-steel-cylinder-block.jpg | Dark steel/iron cylinder block |
| 614138207_... | aluminum-differential-cover.jpg | Aluminum differential cover |
| 616031342_... | aluminum-steering-knuckle.jpg | Aluminum steering knuckle |
| 620080150_... | motorcycle-throttle-assembly.jpg | Motorcycle throttle grip assembly |
| 622638534_... | bing-carburetor-polished.jpg | Bing carburetor (polished aluminum) |
| 629270895_... | aluminum-bearing-housing.jpg | Aluminum bearing/mounting plate |
| 632023406_... | brake-caliper-installed.jpg | Brake caliper installed on motorcycle wheel |
| 632197914_... | brake-caliper-halves.jpg | Brake caliper halves (polished aluminum) |

### Before/After Pairs (great for showcasing results)
- Husqvarna engine cover: `husqvarna-engine-cover-before.jpg` → `husqvarna-engine-cover-after.jpg`
- Steel thermostat housing: `steel-thermostat-housing-before.jpg` → `steel-thermostat-housing-after.jpg`

## Team Log
- [Team Lead] Initial setup: git init, CLAUDE.md created, tech stack chosen
- [Researcher] Water polishing process research, Swedish copy, and design analysis completed
- [Scaffolder] Astro + Tailwind v4 initialized, 15 photos renamed, SVG logo created, Layout + index with section placeholders built, build verified
- [Crow] Team architect — assembled vvp-build team for implementation phase
- [Forge] Built all 7 components (Nav, Hero, About, Services, Gallery, Contact, Footer), updated index.astro + Layout.astro with GSAP CDN. All sections filled with real Swedish content, responsive mobile-first design, before/after gallery, photo grid, Google Maps embed, mobile hamburger menu, sticky nav. Build passes clean.
- [Flux] Added GSAP animations: hero entrance timeline (staggered fade-in of heading/subtitle/CTAs/scroll indicator), scroll-triggered section reveals for all sections (headings, text, cards, images with staggered delays), hero + about image parallax, service timeline connecting line draw animation, gallery hover glow + before/after card lift, active nav link tracking via ScrollTrigger, prefers-reduced-motion guard. All in a single <script> block in Layout.astro + CSS enhancements in global.css. Build passes clean.

## Build Team (vvp-build) — Assembled by Crow
- **Forge** — Lead frontend developer. Builds all components, sections, content, gallery, responsive design
- **Flux** — Animation & UX specialist. Adds GSAP ScrollTrigger, scroll animations, parallax, hover effects, "alive" feel
- **Crow** — Project lead. Coordinates team, handles deployment to GitHub + Cloudflare Pages

### Build Plan
1. Forge builds complete site with all sections and real content (Phase 1) — DONE
2. Flux adds animations and interactive polish (Phase 2) — DONE
3. Crow deploys to GitHub + Cloudflare Pages (Phase 3) — GitHub DONE, Cloudflare needs manual setup

## Deployment
- **GitHub**: https://github.com/Quilw/vvp (public repo, main branch)
- **Cloudflare Pages**: Needs one-time setup via Cloudflare dashboard
  - Connect GitHub repo `Quilw/vvp`
  - Framework preset: Astro
  - Build command: `npm run build`
  - Output directory: `dist`
  - Then every push to `main` auto-deploys

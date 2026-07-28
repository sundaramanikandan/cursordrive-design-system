# CursorDrive Design System v1.0

50-theme design system for all CursorDrive properties. Single HTML file — zero build step, zero CDN dependency.

## Usage

Set `data-theme` on `<body>` or the root element:

```html
<body data-theme="midnight-cyan">
```

Switch theme at runtime:

```js
document.body.setAttribute('data-theme', 'aurora');
```

## 50 Themes

| # | Theme ID | Category | Accent | Mode |
|---|----------|----------|--------|------|
| 1 | `midnight-cyan` | Dark SaaS · parsemind / VYNE | `#22D3EE` | Dark |
| 2 | `nova-amber` | Dark Agency · cursordrive.com | `#FBBF24` | Dark |
| 3 | `arctic` | Light Tech SaaS | `#0891B2` | Light |
| 4 | `jade` | Healthcare / Wellness · billsense | `#059669` | Light |
| 5 | `saffron` | Heritage Food serif · sathyakitchen | `#D4AF37` | Light |
| 6 | `crimson` | Real Estate · primesquare | `#DC2626` | Light |
| 7 | `ocean` | Business Commerce · excelbills | `#2563EB` | Light |
| 8 | `twilight` | Enterprise SaaS | `#6366F1` | Dark |
| 9 | `scholar` | Ed-Tech Purple × Gold · riwardz | `#7C3AED` | Light |
| 10 | `ember` | Dark F&B · kallidaipappads | `#F97316` | Dark |
| 11 | `neon-lime` | Gaming / Dev Tools | `#84CC16` | Dark |
| 12 | `rose-gold` | Luxury Beauty | `#C2799A` | Light |
| 13 | `deep-navy` | Corporate Finance Dark | `#60A5FA` | Dark |
| 14 | `mint-fresh` | Health & Wellness Light | `#14B8A6` | Light |
| 15 | `obsidian` | Premium Minimal Dark | `#E5E5E5` | Dark |
| 16 | `sunset` | Warm Creative Light | `#EA580C` | Light |
| 17 | `forest` | Eco / Nature | `#166534` | Light |
| 18 | `coral` | Startup Energy | `#FF6B6B` | Light |
| 19 | `slate-minimal` | Neutral B2B | `#334155` | Light |
| 20 | `gold-rush` | Premium Dark Luxury | `#F59E0B` | Dark |
| 21 | `ice` | Ultra Cool Minimal | `#67E8F9` | Light |
| 22 | `violet-dusk` | Dark Creative Studio | `#A855F7` | Dark |
| 23 | `copper` | Artisan / Industrial | `#B45309` | Light |
| 24 | `sakura` | Japanese Aesthetic | `#EC4899` | Light |
| 25 | `terra` | Earthy Warm | `#C2522A` | Light |
| 26 | `aurora` | Nordic Dark Emerald | `#10B981` | Dark |
| 27 | `storm` | Dark Brutalist Silver | `#94A3B8` | Dark |
| 28 | `canary` | Bold Dark Yellow | `#EAB308` | Dark |
| 29 | `plum` | Dark Luxury Purple | `#C084FC` | Dark |
| 30 | `sage-garden` | Organic Muted Light | `#4B7A5E` | Light |
| 31 | `blood-moon` | Cinematic Dark Red | `#EF4444` | Dark |
| 32 | `chrome` | Metallic Light Minimal | `#6B7280` | Light |
| 33 | `neon-pink` | Cyberpunk Dark | `#F0ABFC` | Dark |
| 34 | `cobalt-night` | Dark SaaS Deep Blue | `#3B82F6` | Dark |
| 35 | `peach-cream` | Lifestyle Warm Light | `#FB7185` | Light |
| 36 | `onyx` | Silver / Platinum Premium Dark | `#C0C0C0` | Dark |
| 37 | `verdigris` | Jewel Teal Dark | `#2DD4BF` | Dark |
| 38 | `champagne` | Warm Luxury Gold Light | `#C5A028` | Light |
| 39 | `electric-indigo` | Purple-to-Cyan Dark | `#818CF8` | Dark |
| 40 | `lagoon` | Tropical Sky Blue Light | `#0EA5E9` | Light |
| 41 | `noir` | Pure Editorial Black & White | `#FFFFFF` | Dark |
| 42 | `marigold` | Bright Bold Yellow Light | `#CA8A04` | Light |
| 43 | `rust` | Industrial Dark Warm | `#C2410C` | Dark |
| 44 | `pearl` | Editorial Minimal Warm Light | `#3C3A37` | Light |
| 45 | `venom` | Cybersecurity Dark Toxic Green | `#22C55E` | Dark |
| 46 | `blush` | Fashion Fuchsia Light | `#C026D3` | Light |
| 47 | `prussian` | Maritime Navy-Teal Dark | `#06B6D4` | Dark |
| 48 | `harvest` | Autumn Warm Light | `#B45309` | Light |
| 49 | `neon-azure` | Electric Sky Blue Dark | `#00D4FF` | Dark |
| 50 | `ivory` | Architectural Stone Warm Light | `#57534E` | Light |

## CSS Token Reference

Every theme exposes the same 12 + 8 tokens:

```css
/* Surface & structure */
--bg           /* page background */
--surface      /* elevated surface — header, sidebar, nav */
--card         /* card / panel background */
--card2        /* tinted secondary well */
--border       /* subtle 1px divider */
--border2      /* stronger border, input outlines */

/* Text hierarchy */
--text         /* primary body text */
--text2        /* secondary text */
--muted        /* placeholder, labels, captions */
--subtle       /* very faint / decorative */

/* Brand */
--accent       /* primary brand color */
--accent2      /* secondary / hover shade */
--accent-bg    /* accent tint — hover state bg, badge fill */
--grad         /* gradient — gradient text, fills, progress bars */

/* Data visualization (8 distinct chart colors) */
--viz1 → --viz8
```

Shared layout tokens (same across all themes):

```css
--font-sans    --font-serif   --font-mono
--radius-sm    --radius-md    --radius-lg    --radius-xl    --radius-full
--shadow-sm    --shadow-md    --shadow-lg    --shadow-glow
```

## Font Stack Roles

| Role | Use case | Stack |
|------|----------|-------|
| `--font-sans` | Tech, SaaS, dashboards, modern UI | `'Segoe UI', system-ui, -apple-system, sans-serif` |
| `--font-serif` | Food, heritage, luxury, editorial, lifestyle | `Georgia, 'Palatino Linotype', serif` |
| `--font-mono` | Dev tools, code, terminals, data | `'Courier New', Consolas, monospace` |

Themes with `--font-display: var(--font-serif)`: saffron, ember, forest, copper, sakura, terra, sage-garden, pearl, champagne, harvest, ivory, noir, gold-rush, rose-gold, peach-cream

Themes with `--font-display: var(--font-mono)`: neon-lime, venom

All others: `--font-sans`

## Components Documented

- Color palette (12 tokens + 8 viz colors, live-rendered per theme)
- Typography scale (12 steps, 3 font stacks with specimens)
- Buttons (6 variants × 3 sizes + pill + icon + all states)
- Form elements (input, select, textarea, toggle, checkbox)
- Cards (default, elevated, glass, accent-border)
- Stat cards with SVG sparklines
- Badges (8 types) + Alerts (4 variants)
- Navigation (tabs, breadcrumb, tag pills)
- Progress bars (3 heights, gradient fill)
- Data visualization (bar chart + area line chart)
- Data table (responsive, hover states)
- Typewriter component with blinking cursor + gradient text
- Dividers (4 styles)
- Spacing scale, border radius scale, shadow scale

## Integration — Vue 3 + Laravel + Inertia

Apply tokens in Vue SFCs:

```css
/* In <style scoped> */
.my-component {
  background: var(--card);
  color: var(--text);
  border: 1px solid var(--border2);
}

.accent-text {
  background: var(--grad);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
```

Set theme on the root layout component:

```html
<!-- PublicLayout.vue or AppLayout.vue -->
<div :data-theme="currentTheme" class="pub-root">
  <slot />
</div>
```

Switch via user preference stored in Inertia shared data or localStorage:

```js
const theme = ref(localStorage.getItem('cd-theme') ?? 'midnight-cyan')
watch(theme, v => localStorage.setItem('cd-theme', v))
```

---

© CursorDrive · All rights reserved

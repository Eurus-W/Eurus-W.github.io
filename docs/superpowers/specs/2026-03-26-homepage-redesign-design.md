# Homepage Redesign — Warm Elegant Style

## Context

The current academic homepage (Jekyll-based, AcademicPages theme) uses a cold indigo/purple color scheme with a sidebar layout. While functional, the design feels generic. This redesign transforms it into a warm, elegant style with a modern Hero + Grid layout, giving the site a distinctive personality that balances academic rigor with approachability.

## Design Decisions

- **Style direction:** Warm elegant — earthy tones, serif/sans-serif mixed typography, generous whitespace
- **Layout:** Hero header (avatar + bio side-by-side) → content grid, replacing the current sidebar layout
- **Dark mode:** Retained, redesigned with warm dark tones (brown-black instead of cold indigo)
- **Content sections:** Same as current — Bio, Research Interests, News, Selected Publications
- **Pages affected:** All pages get the new color/typography; homepage gets the layout overhaul

## Color Palette

### Light Mode

| Role | Color | Usage |
|------|-------|-------|
| Background | `#faf8f5` | Page background |
| Surface | `#ffffff` | Cards, sections |
| Border | `#e8e0d4` | Card borders, dividers |
| Title | `#2c1810` | H1, H2, author name |
| Body | `#4a3728` | Paragraph text |
| Secondary | `#8b7355` | Subtitles, metadata |
| Label | `#b8a080` | Section labels, dates |
| Accent | `#c0785c` | Links, interactive elements |
| Accent hover | `#a8624a` | Link hover states |
| Divider gradient | `transparent → #d4c5a9 → transparent` | Elegant horizontal rules |

### Dark Mode

| Role | Color | Usage |
|------|-------|-------|
| Background | `#1c1714` | Page background |
| Surface | `#2a241e` | Cards, sections |
| Border | `rgba(212, 184, 150, 0.15)` | Card borders |
| Title | `#f0e6d6` | Headings |
| Body | `#c8b8a0` | Paragraph text |
| Secondary | `#8b7d6b` | Metadata |
| Accent | `#d4b896` | Links, interactive elements |
| Masthead bg | `rgba(28, 23, 20, 0.88)` | Nav backdrop |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings (H1, H2) | Georgia, `Noto Serif SC`, serif | 400 | Replaces DM Serif Display |
| Body text | Inter, `Noto Sans SC`, sans-serif | 400 | Keep existing Inter |
| Labels/dates | JetBrains Mono | 500 | Monospace for timestamps, badges |
| Section labels | Inter | 500 | Uppercase, letter-spacing 1.5px |

**Font loading change:** Replace `DM Serif Display` with `Noto Serif SC` in Google Fonts import (Georgia is a system font, no load needed). Keep Inter and JetBrains Mono.

## Layout — Homepage

### Current structure (sidebar layout)
```
┌──────────────────────────────┐
│         Masthead/Nav         │
├────────┬─────────────────────┤
│Sidebar │  Bio                │
│(avatar,│  Research Interests │
│ links) │  News Timeline      │
│        │  Selected Papers    │
└────────┴─────────────────────┘
```

### New structure (Hero + Grid)
```
┌──────────────────────────────┐
│     Masthead/Nav (simplified)│
├──────────────────────────────┤
│  ┌─────────────────────────┐ │
│  │  [Avatar]  Name         │ │
│  │           Title/Bio     │ │  ← Hero section
│  │           Social links  │ │
│  └─────────────────────────┘ │
│                              │
│  RESEARCH INTERESTS          │
│  ┌──────┐┌──────┐┌──────┐   │  ← 3-column grid
│  │ LLM  ││ PEFT ││Compr.│   │
│  └──────┘└──────┘└──────┘   │
│                              │
│  ┌─────────────┐┌──────────┐│
│  │   NEWS      ││ SELECTED ││  ← 2-column grid
│  │   list      ││ PAPERS   ││
│  │             ││          ││
│  └─────────────┘└──────────┘│
│                              │
│         © Footer             │
└──────────────────────────────┘
```

### Implementation approach

The homepage currently uses `layout: single` with `author_profile: true`, which renders the sidebar via `_includes/sidebar.html`. To achieve the Hero + Grid layout:

1. **Create a new layout** `_layouts/home.html` (extends `default`), which:
   - Does NOT include `sidebar.html`
   - Renders a full-width `<article>` without the sidebar column
   - The hero section and grid are built in the page content itself (`_pages/about.md`)

2. **Update `_pages/about.md`**:
   - Change `layout: single` → `layout: home`
   - Set `author_profile: false`
   - Add a hero section at the top with avatar, name, bio, and social links (using HTML in markdown)
   - Restructure Research Interests / News / Publications into the grid layout

3. **Other pages** (Publications, Projects, Talks, Teaching, CV):
   - Keep `layout: single` with `author_profile: true`
   - The sidebar on these pages provides useful context
   - Just restyle with the new warm color palette

### Masthead changes

Simplify the masthead navigation:
- Replace the full site title `"Hanqing Wang / Homepage"` with a short logo mark `"HW"` (Georgia serif)
- Keep navigation links as-is
- Keep dark mode toggle button
- Change backdrop from cold `rgba(248,249,252)` to warm `rgba(250,248,245, 0.88)` with blur
- Dark mode masthead: `rgba(28, 23, 20, 0.88)`

### Hero section

- Flexbox layout: avatar (circle, ~120px) on left, text on right
- Subtle gradient background: `#faf8f5 → #f0ebe3`
- Border radius 16px, padding 2rem
- Name in Georgia serif, 1.8rem
- Title/affiliation in Inter, secondary color
- Bio paragraph below
- Social icons row (email, Google Scholar, GitHub) using Font Awesome

### Research Interest cards

- 3-column CSS Grid (responsive: 1 column on mobile)
- Each card: white background, warm border (`#e8e0d4`), 8px radius
- Icon (Font Awesome) + title (Georgia serif) + subtitle
- Hover: subtle shadow increase, no dramatic translate
- Section label: uppercase, letter-spacing, `#b8a080` color

### News + Selected Publications

- 2-column CSS Grid on desktop, stack on mobile
- Both in white card containers with warm borders
- News: simple date-value list (replace timeline dots with clean monospace dates)
- Publications: conference badge + title, keep existing badge colors but soften them slightly
- Scrollable news with custom warm-toned scrollbar

## Files to Modify

| File | Change |
|------|--------|
| `_layouts/home.html` | **New file** — full-width layout for homepage |
| `_pages/about.md` | Restructure to Hero + Grid, change layout to `home` |
| `_sass/layout/_custom.scss` | Major rewrite — new color variables, Hero styles, grid layout, warm card styles |
| `_includes/head/custom.html` | Update Google Fonts import (swap DM Serif Display → Noto Serif SC) |
| `_includes/masthead.html` | Simplify title to "HW" logo mark |
| `_sass/theme/_default.scss` | Update `:root` CSS variables to warm palette (light mode colors defined here) |
| `_sass/theme/_dark.scss` | Not actively used for toggle-based dark mode (dark mode is in `_custom.scss` via `[data-theme="dark"]`); leave as-is |
| `_sass/_themes.scss` | Update `$header-font-family` to use Georgia/serif for headings |

## Files NOT to modify

- `_config.yml` — no config changes needed
- `_layouts/single.html` — keep as-is for other pages
- `_includes/author-profile.html` — still used by non-homepage pages
- `_data/navigation.yml` — keep current nav structure
- Publication/talk/teaching collection files — content unchanged

## Animations

- Keep existing staggered fade-in on cards and publication entries
- Reduce hover transform from `translateY(-4px)` to `translateY(-2px)` for subtlety
- Transition timing: `0.25s ease` (unchanged)

## Responsive Breakpoints

- **Desktop (>900px):** Hero flexbox, 3-col research grid, 2-col news/papers grid
- **Tablet (600–900px):** Hero flexbox (smaller avatar), 2-col research grid, 1-col news/papers stack
- **Mobile (<600px):** Hero stacks vertically (avatar centered above text), 1-col everything

## Verification

1. Run `bundle exec jekyll serve` locally and check:
   - Homepage renders with Hero + Grid layout (no sidebar)
   - Other pages (Publications, Projects, CV) still show sidebar
   - Dark mode toggle works with warm dark colors
   - Responsive behavior at all breakpoints (mobile, tablet, desktop)
   - News section scrolls properly
   - Publication badges still display correctly
   - All links (paper, code, social) are functional
   - Font loading: Georgia for headings, Inter for body, JetBrains Mono for labels
2. Check in both Chrome and Safari
3. Validate no broken images or missing icons

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Hugo-based static website** for the Cod3rs Community - a developer-focused community spanning Denmark and Slovakia. The site showcases community information, events, projects, and provides links to Discord and GitHub. It uses a brutalist design aesthetic with a custom Hugo theme.

## Development Commands

### Building and Local Development

```bash
# Development server with live reload (includes component navigation)
hugo server

# Production build
hugo

# Clean build artifacts and rebuild
rm -rf public && hugo
```

### Creating New Content

```bash
# New event page (uses archetype template with front matter structure)
hugo new events/my-event-name.md

# New project
hugo new projects/my-project.md

# New blog post
hugo new blog/my-post.md
```

### Testing Changes

The site is static - no automated tests. Verify changes by:
1. Running `hugo server`
2. Opening `http://localhost:1313` in browser
3. Checking responsiveness at different screen sizes
4. Verifying all links work (internal and external)
5. Testing interactive elements (animations, navbar toggle)

## Architecture and Structure

### Technology Stack

- **Static Site Generator**: Hugo v0.41.0+
- **Frontend**: HTML5, CSS3, Bootstrap 5.3.6 (CDN), vanilla JavaScript
- **Templating**: Go templates (Hugo native)
- **Content Format**: Markdown with YAML front matter
- **Deployment**: Static files (JAMstack - no backend, no database)
- **Libraries**: AmCharts 5 (map on About page), Bootstrap (responsive grid)

### Template and Layout System

**Template Hierarchy** (in `themes/custom/layouts/`):

```
baseof.html (root template with navbar and footer)
├── _default/index.html (custom homepage)
├── _default/single.html (individual pages, blog posts, events)
├── _default/list.html (content collections like /projects/, /blog/)
├── _default/events.html (special layout for /events/ with timeline)
├── partials/navbar.html (navigation menu with active state detection)
├── partials/footer.html (footer with social links)
└── shortcodes/ (9 reusable component templates)
    ├── section, section-dark, section-light, section-accent
    ├── section-full, section-two-column, section-image
    ├── card-image, hero-image, column, rawhtml
```

**Shortcodes** are reusable content blocks defined in `layouts/shortcodes/`. They're used in Markdown files to build page layouts without writing HTML. Key shortcodes:

| Shortcode | Purpose |
|-----------|---------|
| `section` | Basic section wrapper |
| `section-dark` | Dark background section with secondary text |
| `section-light` | White background section |
| `section-accent` | Purple accent (#755AFB) background section |
| `section-full` | Full-width section |
| `section-two-column` | Responsive two-column grid |
| `card-image` | Card component with image header |
| `hero-image` | Large hero banner section |
| `section-image` | Section with image and overlay |
| `column` | Child of two-column layout |

### Content Organization

```
content/
├── about/              Single page about the community
├── blog/               Blog post listing (currently hidden in nav)
├── contact/            Contact/join page
├── events/             Event pages and event listing
├── locations/          Location information pages
├── projects/           Project showcase listing
└── components/         Component documentation (visible only in hugo server)
```

**Event Pages** use the `events` archetype template. Front matter includes:
- `title`, `date`, `endDate`, `description`, `location`, `draft`

The special `events.html` template separates events into "Upcoming" (by date) and "Past Events" (with timeline layout).

### Styling and Design

**CSS Structure** (in `themes/custom/static/css/`):

- `main.css` (426 lines) - Core: typography, layout, navbar, footer
- `sections.css` (140 lines) - Section shortcode responsive layouts
- `components.css` (268 lines) - 8 design components, color variations
- `events.css` (316 lines) - Timeline layout, event cards, animations

**Color Scheme** (brutalist, high contrast):
- **Primary**: `#212121` (dark gray/black) - 60% usage
- **Secondary**: `#FFFFFF` (white) - 30% usage
- **Accent**: `#755AFB` (purple) - 10% usage

**Typography**:
- Headers: Rubik Mono One (bold), Raleway (body)
- Code/nav: JetBrains Mono, Roboto
- Font loading: Google Fonts CDN
- Style: Uppercase, bold borders, minimal decoration

### Key Features Implementation

**Navigation** (`partials/navbar.html`):
- Dynamic menu from `config.toml` menu section
- Active state detection: compares current page with menu URL
- Responsive navbar toggle (Bootstrap component)
- Components menu only visible in `hugo server` dev mode

**Events Timeline** (`_default/events.html`):
- Splits events by `endDate` vs current date
- Upcoming: Card grid layout
- Past: Alternating left/right timeline with images
- Logic: `{{ if ge $endDate.Unix now.Unix }}`

**Interactive About Page**:
- AmCharts 5 world map (highlight Denmark and Slovakia)
- 3D orthographic projection

**Component Documentation** (`_default/single.html`):
- Sidebar auto-generated from `/components/` markdown files
- Only rendered when `hugo.IsServer` is true (dev mode only)
- Links to sections via ID anchors

### Configuration

**config.toml** key settings:
- `baseURL`: Site domain for link generation
- `theme`: Points to `themes/custom/`
- `permalinks`: Blog posts route to `/blog/:year/:month/:slug/`
- `[menu.main]`: Navigation items with ordering weights
- `[params]`: Site metadata, social links (GitHub, Discord)

## Code Patterns and Conventions

### Adding New Pages

1. Create markdown file in appropriate `content/` section
2. Use YAML front matter with `title`, `date` (if applicable), `description`
3. Build layout using shortcodes (preferred) or raw HTML with `rawhtml` shortcode
4. Add menu entry in `config.toml` `[menu.main]` section if top-level navigation needed

### Adding New Shortcodes

1. Create `.html` file in `themes/custom/layouts/shortcodes/`
2. Access parameters via `.Get "paramname"`
3. Access inner content via `.Inner`
4. Keep styling minimal - delegate to CSS for flexibility

### Linking and Routing

- Internal links: Use relative paths like `/about/` or `/blog/2025/01/post-title/`
- External links: Full URLs (GitHub, Discord hardcoded in footer)
- Active nav detection: navbar compares `.Permalink` with menu URL
- Blog permalinks: Configured in `[permalinks]` section

### Responsive Design

- Bootstrap 5.3.6 grid system via CDN
- Custom CSS uses media queries in `.css` files
- Mobile-first approach preferred
- Test at 320px, 768px, and 1024px+ breakpoints

## File Locations Reference

| Purpose | Location |
|---------|----------|
| Site configuration | `config.toml` |
| Theme metadata | `themes/custom/theme.toml` |
| Base HTML structure | `themes/custom/layouts/_default/baseof.html` |
| Navigation partial | `themes/custom/layouts/partials/navbar.html` |
| CSS styles | `themes/custom/static/css/` (4 files) |
| Shortcode templates | `themes/custom/layouts/shortcodes/` (9 files) |
| Content markdown | `content/` (7 subdirectories, 12 files) |
| Build output | `public/` (generated, ignored in git) |
| Static assets | `static/` (images, favicon, robots.txt) |

## Important Notes

- **No build pipeline**: Pure HTML/CSS/JS - no Node.js or npm needed
- **No backend**: Completely static - no API, database, or server-side processing
- **Component development**: Component shortcodes visible in Hugo server nav when `hugo.IsServer` is true
- **Date formatting**: Hugo uses RFC3339 for front matter dates (`2025-01-15T10:00:00Z` or `2025-01-15`)
- **Asset fingerprinting**: Not used - safe for CDN caching
- **Environment URLs**: `baseURL` in `config.toml` controls absolute link generation

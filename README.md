# Saikrishna Rao M — Portfolio

Personal portfolio website for a Digital Marketing Manager with 11+ years of experience in healthcare. Built as a **single self-contained HTML file** — no build tools, no dependencies, no framework required.

---

## Quick Start

1. Open `saikrishna-portfolio-v3.html` in any browser — it works immediately
2. Add your photos following the [Photo Guide](#photo-guide) below
3. Upload to any web host (see [Hosting](#hosting))

---

## File Structure

```
saikrishna-portfolio-v3.html   ← the entire site (HTML + CSS + JS)
README.md                      ← this file
your-photos/                   ← add your images here (any folder name)
  profile.jpg
  apollo-award.jpg
  konnect-award.jpg
  ...
```

---

## Page Sections

| # | Section | Photo Slots | Notes |
|---|---------|-------------|-------|
| 1 | **Hero** | 1 | LinkedIn profile photo — right column |
| 2 | **About** | 0 | Bio text + animated skill bars |
| 3 | **Experience** | 5 | One 80×80 thumbnail per role |
| 4 | **Impact** | 0 | Animated stat band (numbers only) |
| 5 | **Skills** | 0 | 6-panel grid + tool token strip |
| 6 | **Awards** | 4 | Full-width banner per award card |
| 7 | **Gallery** | 6 | Editorial magazine grid (AOP, team, events) |
| 8 | **Certifications** | 4 | 2×2 cert badge/screenshot grid |
| 9 | **Education** | 0 | 2-card grid (MBA + B.Tech) |
| 10 | **Contact** | 0 | Email, LinkedIn, location links |

**Total: 20 photo slots across the page**

---

## Photo Guide

Every photo slot has a comment in the HTML that tells you exactly what to do. The pattern is always the same:

**Find the comment:**
```html
<!-- LINKEDIN PROFILE PHOTO: replace below -->
<div class="photo-placeholder">...</div>
```

**Replace the placeholder div with your image:**
```html
<!-- LINKEDIN PROFILE PHOTO: replace below -->
<img src="your-photos/profile.jpg" alt="Saikrishna Rao M">
```

That's it. The image fills its container automatically — no extra CSS needed.

### Recommended Image Sizes

| Slot | Location | Recommended Size | Orientation |
|------|----------|-----------------|-------------|
| Profile photo | Hero (right column) | 600 × 800 px min | Portrait |
| Award banners | Awards section × 4 | 800 × 400 px min | Landscape |
| Gallery slot 1 (large) | Gallery section | 800 × 560 px+ | Portrait |
| Gallery slots 2–6 | Gallery section | 400 × 280 px min | Landscape |
| Cert badge grid | Certifications × 4 | 320 × 160 px display | Any |
| Experience thumbnails | Experience × 5 | 80 × 80 px | Square |

> All images use `object-fit: cover` so any photo ratio will work — the browser crops to fit the slot.

### What Photos to Use

| Section | Suggested content |
|---------|-----------------|
| Hero | LinkedIn profile headshot |
| Award card 1 | Apollo Stellar Achiever 2025 ceremony / trophy photo |
| Award card 2 | Konnect Insights Excellence Award 2022 ceremony photo |
| Award card 3 | Dashboard screenshot or AOP slide showing 300% growth |
| Award card 4 | Campaign report screenshot showing 50% CPL reduction |
| Gallery slot 1 | AOP annual strategy presentation or large team photo |
| Gallery slots 2–6 | Award events, office moments, campaign launches, conferences, cert achievements |
| Cert grid | Google Skillshop certificate badge screenshots (4 certs) |
| Experience thumbnails | Company logos or team photos (one per role) |

### Using Your LinkedIn Profile Photo

LinkedIn CDN URLs expire, so download the photo first, then reference it locally:

1. Go to your LinkedIn profile
2. Click your profile photo → "View profile photo"
3. Right-click → Save image as `profile.jpg`
4. Place it next to the HTML file
5. Replace the placeholder with `<img src="profile.jpg" alt="Saikrishna Rao M">`

---

## Updating Content

Everything is plain HTML — open in any text editor (VS Code recommended).

### Text Content
Search for the visible text string and edit it directly. No templating involved.

### Colors
All colors are CSS variables at the top of the `<style>` block inside the file:

```css
:root {
  --gold: #c9a84c;      /* primary accent — change this to rebrand */
  --gold2: #e8c96d;     /* hover state for gold */
  --ink: #0c0c0f;       /* main background */
  --cream: #f4efe6;     /* primary text */
  --dust: #7a7468;      /* muted/secondary text */
}
```

Changing `--gold` updates every accent, border, and highlight across the entire page.

### Contact Details
Two strings appear in multiple places. Find-and-replace both:

- `krishna2609@gmail.com` — appears in nav, hero, and contact section
- `saipuramshetty` — appears in the LinkedIn URLs

### Stats / Metrics
Located in the Hero section (`hero-stats`) and Impact band (`impact-band`). Edit the number and label text directly.

### Adding / Removing Skills or Tools
- **Skill panels** — find `class="skills-grid"` and add/remove `<div class="skill-panel">` blocks
- **Tool tokens** — find `class="tools-row"` and add/remove `<span class="tool-token">` elements

### Adding More Experience Entries
Copy an existing `<div class="exp-row">` block, paste it below the last one, and update the content.

---

## Design System

| Element | Value |
|---------|-------|
| Display font | Bebas Neue (Google Fonts) |
| Heading font | Cormorant Garamond (Google Fonts) |
| Body font | DM Mono (Google Fonts) |
| Primary accent | Gold `#c9a84c` |
| Background | Near-black `#0c0c0f` |
| Primary text | Cream `#f4efe6` |
| Cursor | Custom gold dot + lagging ring |
| Scroll animation | Intersection Observer — staggered fade-up |
| Skill bars | Animate on scroll into view |

---

## Hosting

The entire site is one `.html` file. Any static host works.

### Netlify Drop (easiest — no account needed)
1. Go to [drop.netlify.com](https://drop.netlify.com)
2. Drag your HTML file (and photo folder) onto the page
3. Get a live URL instantly

### GitHub Pages (free with custom domain)
1. Create a new GitHub repository
2. Upload `saikrishna-portfolio-v3.html` — rename it `index.html`
3. Go to Settings → Pages → deploy from main branch
4. Live at `https://yourusername.github.io/repo-name`

### Vercel (fast CDN, CLI or drag-and-drop)
1. Go to [vercel.com/new](https://vercel.com/new)
2. Import from GitHub or drag-and-drop the file
3. Deploy — live in under 60 seconds

### Custom Domain
All three hosts above support custom domains for free. Point your domain's DNS A record or CNAME to the host, then configure it in the host's dashboard.

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome / Edge | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Mobile (iOS / Android) | ✅ Responsive — hero photo column hides on small screens |

---

## Credits

- **Fonts**: Cormorant Garamond, Bebas Neue, DM Mono via [Google Fonts](https://fonts.google.com)
- **Animations**: Pure CSS + Intersection Observer API (no libraries)
- **Cursor**: Vanilla JS lagging ring effect

---

*© 2025 Saikrishna Rao M · Digital Marketing Manager · Hyderabad*

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for **QuantumQuacks**, an independent Spanish video game studio. The site is hosted on GitHub Pages (quantumquacks.es) and serves as the studio's online presence, showcasing their game "Bouncing to the Top with Quantum Quacks" and collecting newsletter subscriptions.

## Technology Stack

- **Pure HTML/CSS/JavaScript** - No build process or framework dependencies
- **External Libraries:**
  - Lenis (v1.3.3) - Smooth scrolling library
  - MailerLite - Newsletter subscription integration
- **Hosting:** GitHub Pages with custom domain (quantumquacks.es)

## Development Workflow

This is a static site with no build process. Changes can be made directly to HTML files and pushed to the repository. The site will automatically update on GitHub Pages.

To test locally, open HTML files directly in a browser or use a simple HTTP server:
```bash
python3 -m http.server 8000
```

Then navigate to `http://localhost:8000`

## File Structure & Architecture

- **index.html** - Main homepage with hero section, games showcase, about section, and contact/newsletter form
- **bouncingtothetop.html** - Dedicated landing page for the "Bouncing to the Top" game
- **icons/** - Social media icons (Instagram, TikTok, YouTube, Mail) in multiple sizes (50px, 100px, 150px, 250px, 500px)
- **logo.jpg** - Studio logo (used in hero section)
- **logo_4k_transparent.png** - High-resolution transparent logo (used for game showcase and Open Graph)
- **sitemap.xml** - SEO sitemap listing both pages
- **robots.txt** - SEO configuration allowing all crawlers
- **CNAME** - Custom domain configuration for GitHub Pages

## Styling & Design System

The site uses CSS custom properties for theming:
```css
--primary-color: #00e0b8 (teal/cyan)
--bg-color: #181c24 (dark blue-gray)
--section-bg: #23283a (lighter blue-gray)
```

### Key Design Patterns:
- **Alternating section backgrounds** - Sections alternate between `--bg-color` and `--section-bg`
- **Scroll-triggered animations** - Elements fade in and translate when scrolling into view (controlled by `.in-view` class)
- **Parallax effects** - Background circles move at different speeds (data-speed attributes)
- **Smooth scrolling** - Implemented via Lenis library with easing functions
- **Responsive navigation** - Fixed nav changes style on scroll (`.scrolled` class)

## Content & Localization

All content is in **Spanish (es)**. Key sections:
- Hero section with studio tagline
- Games section (currently showcasing one game with "Próximamente" button)
- About section with studio description
- Contact section with newsletter signup and social media links

Social media accounts:
- Instagram: @quantum_quacks
- TikTok: @quantum_quacks
- YouTube: @quantumquacks
- Email: contacto@quantumquacks.es

## SEO Configuration

The site includes comprehensive SEO setup:
- Meta description and keywords
- Open Graph tags for social sharing
- Twitter Card metadata
- Canonical URL
- Sitemap and robots.txt

The logo_4k_transparent.png is used as the Open Graph image for social media previews.

## JavaScript Architecture

Both HTML files use Lenis for smooth scrolling. The main index.html includes:
- **Intersection Observer pattern** - Sections tracked for scroll animations
- **Active navigation tracking** - Updates nav links based on scroll position
- **Parallax calculations** - Updates element transforms based on scroll position
- **Smooth scroll navigation** - Click handlers for nav links use Lenis.scrollTo()

## Third-Party Integrations

**MailerLite Newsletter:**
- Account ID: 1528903
- Embedded form: data-form="mLQrzf"
- Universal script loaded from assets.mailerlite.com

## Making Changes

When editing this site:
1. Maintain the Spanish language throughout
2. Keep the consistent color scheme (teal primary, dark backgrounds)
3. Ensure animations remain consistent across sections
4. Test smooth scrolling behavior after changes
5. Update sitemap.xml if adding new pages
6. Remember there's no build process - changes to HTML/CSS/JS are direct

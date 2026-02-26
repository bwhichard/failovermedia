# Failover Media - Website

## Project Overview
Failover Media is a B2B podcast network that bundles three enterprise technology podcasts under one sponsorship umbrella.

**Website:** https://failovermedia.com
**GitHub Repo:** https://github.com/bwhichard/failovermedia

> **Note:** This is the public website repo. Business operations, lead tracking, and sales strategy are in the private `failovermedia-internal` repo.

## The Podcast Network

### The Reasoning Show (formerly The Cloudcast)
- **Website:** https://thecloudcast.net
- **Hosts:** Aaron Delp, Brian Gracely
- **Description:** Builds on 15 years of The Cloudcast's success. Focused on AI and cloud computing.

### Software Defined Talk
- **Website:** https://www.softwaredefinedtalk.com
- **Description:** A weekly roundtable on enterprise software, cloud computing, and working in tech.

### The Cloud Pod
- **Website:** https://thecloudpod.net
- **Description:** A weekly deep-dive into the latest announcements from AWS, Azure, and GCP.

## Key Files in This Repository

| File | Purpose |
|------|---------|
| `index.html` | Main website (deployed to GitHub Pages) |
| `CNAME` | Custom domain configuration for failovermedia.com |
| `deck.pdf` | Sales deck with vanity URL |
| `deck/index.html` | Redirect page for vanity URL |
| `FailoverMediaHeader.png` | Open Graph image for social sharing |
| `favicon.png` | Browser favicon |

### Artwork Files
- `SDT Square Medium.jpg` - Software Defined Talk podcast artwork
- `The_Cloudcast_Artwork.png` - The Cloudcast artwork (from RSS feed)
- `The_Cloudpod_Artwork.png` - The Cloud Pod artwork (from RSS feed)

## Design System

### Colors (from website)
- **Primary Blue:** #2563eb (accents, CTAs, links)
- **Deep Slate:** #1e293b (headers, primary text)
- **Slate Gray:** #64748b (secondary text)
- **Light backgrounds:** #f8fafc, #f1f5f9, #f8fafc
- **Light borders:** #e2e8f0

### Typography
- **Failover Media logo:** Courier New, Bold, All Caps (monospace/technical feel)
- **Website body:** Inter font family

### Design Decisions
- Clean, white/minimalist enterprise theme
- Podcast artwork displayed with rounded corners (rounded-lg)
- The Cloud Pod artwork has a border (border-2 border-slate-300) because it's white on white

## Website Structure

The site is a single-page layout with these sections:
1. **Hero** - Value proposition and CTA
2. **Why Failover Media** - Three cards: Enterprise Decision-Makers, Technical Influencers, Budget Holders
3. **Our Podcast Network** - Three podcast cards with artwork, descriptions, and links
4. **By the Numbers** - Stats: 20M+ downloads, 60% enterprise, 141 countries, 30% C-suite
5. **Network-Wide Sponsorship Packages** - Three pricing tiers + custom option
6. **Footer** - CTA, contact info, legal entity

### Social Sharing / Meta Tags
- Open Graph (`og:*`) and Twitter Card meta tags configured in `index.html`
- `og:image` points to `FailoverMediaHeader.png` (1200x630)
- Use LinkedIn Post Inspector to force re-scrape: https://www.linkedin.com/post-inspector/
- Favicon: `favicon.png` (32x32)

## Technical Setup

### Hosting
- GitHub Pages at https://github.com/bwhichard/failovermedia
- Custom domain: failovermedia.com
- HTTPS enforced

### DNS (Namecheap)
- A Records pointing to GitHub Pages IPs: 185.199.108.153, .109, .110, .111
- CNAME for www: bwhichard.github.io

### Vanity URLs
- **Sales Deck:** failovermedia.com/deck (or failovermedia.com/deck.pdf)

## How to Update the Sales Deck

When you update the Google Slides presentation:
1. Export as PDF from Google Slides
2. Save to this folder as `Failover Media.pdf`
3. Run: `cp "Failover Media.pdf" deck.pdf && git add deck.pdf && git commit -m "Update sales deck" && git push`
4. The vanity URL (failovermedia.com/deck) will update in 1-2 minutes

# Korea Vibe Blog - Project Plan

## 0) Goal

- **English blog** about traveling Korea
- Topic priority: **Itineraries > Cafes & Food > K-Drama Trips**
- Hosting: **Cloudflare Pages** (free plan)
- Engine: **Hugo**
- Theme: **Hugo Theme Stack** (starter template)
- Domain: **https://koreavibe.blog/** (www redirects here)

---

## 1) Current Status (Completed)

- [x] GitHub repo created + Cloudflare Pages auto-deploy connected
- [x] Hugo version issue resolved: Cloudflare Pages env var `HUGO_VERSION >= 0.157.0`
- [x] Domain nameserver delegated to Cloudflare, DNS records set, site connected
- [x] `baseurl = "https://koreavibe.blog/"` updated in config
- [x] Menu structure configured (Start Here, Itineraries, Seoul Guides, Cafes & Food, K-Drama Trips, About, Contact)
- [x] Sidebar subtitle & emoji set
- [x] Dummy social links removed

---

## 2) Cloudflare Free Plan - Build Limit Tips

> Push = Deploy. Manage push frequency to stay within free tier.

- **Writing posts**: Draft in local/Notion/Google Docs, then batch push 1-2x per day
- **Pushing to GitHub**: Make multiple commits locally, but squash before push (1 push = 1 deploy)
- **Theme/config experiments**: Test on a branch, merge to main once confirmed (1 deploy)

---

## 3) Hugo Config File Locations

| File | Purpose |
|------|---------|
| `config/_default/config.toml` | baseurl, title, language, pagination |
| `config/_default/params.toml` | sidebar, OG, widgets, comments, theme options |
| `config/_default/menu.toml` | top nav menu, social links |
| `config/_default/module.toml` | Hugo module (theme) config |
| `config/_default/markup.toml` | Markdown rendering options |
| `config/_default/permalinks.toml` | URL structure |
| `config/_default/related.toml` | Related content settings |

---

## 4) Content Section Structure

```
content/
  itineraries/        # Travel itineraries (priority 1)
  seoul-guides/       # Seoul neighborhood guides
  kfood-cafes/        # Korean food & cafe spots
  kdrama-trips/       # K-Drama filming locations
  culture-etiquette/  # Korean culture tips
  page/               # Static pages (about, contact, etc.)
```

URL pattern: `/<section>/<slug>/`
Example: `/itineraries/seoul-3-day-itinerary/`

---

## 5) Required Pages (for trust, revenue, AdSense approval)

| Page | Path | Status |
|------|------|--------|
| Start Here | `/start-here/` | TODO |
| About | `/about/` | TODO |
| Contact | `/contact/` | TODO |
| Privacy Policy | `/privacy-policy/` | TODO |
| Disclaimer (Affiliate Disclosure) | `/disclaimer/` | TODO |

---

## 6) Menu Structure (Configured)

**Top Navigation:**
1. Start Here
2. Itineraries
3. Seoul Guides
4. Cafes & Food
5. K-Drama Trips
6. About
7. Contact

**Social links:** Only add when actually running (Instagram, etc.)

---

## 7) Content Templates

### A) Itinerary Post Template

```markdown
---
title: "Seoul 3-Day Itinerary: ..."
description: "..."
date: YYYY-MM-DD
categories: ["itineraries"]
tags: ["seoul", "3-day", "budget"]
image: cover.jpg
---

## Overview
- Who this is for / Duration / Budget / Highlights

## Day 1: ...
- Morning / Afternoon / Evening
- Getting around / Where to eat

## Day 2: ...

## Day 3: ...

## Practical Tips
- Transportation / Reservations / Peak hours to avoid

## Related Posts
- [Link to cafe post]
- [Link to K-Drama location post]
```

### B) Cafe/Food Post Template

```markdown
---
title: "Best Cafes in Hongdae: ..."
description: "..."
date: YYYY-MM-DD
categories: ["kfood-cafes"]
tags: ["hongdae", "cafes", "aesthetic"]
image: cover.jpg
---

## Quick Facts
- Area / Price range / Best time to visit

## How to Get There
- Subway line & exit number

## What to Order
- Top 3 recommendations with prices

## Nearby Spots
- 2-3 places within walking distance

## Photo Tips
- Best angles / lighting / Instagram spots
```

---

## 8) SEO Initial Setup Checklist

- [ ] Google Search Console - domain property connected
- [ ] Verify sitemap.xml & robots.txt are working
- [ ] Create default OG image (1200x630px) and set in params
- [ ] Write `description` meta for every post
- [ ] Set up Google Analytics (optional, can use Cloudflare Web Analytics instead)

---

## 9) Next Steps (Priority Order)

1. **Create required static pages** (About, Contact, Privacy Policy, Disclaimer, Start Here)
2. **Remove demo posts** (hello-world, image-gallery, markdown-syntax, math-typesetting, shortcodes)
3. **Create category `_index.md` files** for each section (itineraries, seoul-guides, etc.)
4. **Write first real post** - recommend starting with a Seoul 3-Day Itinerary
5. **OG image** - create and configure default social sharing image
6. **Google Search Console** - connect and submit sitemap
7. **Write 5-10 posts** before applying for AdSense

---

## 10) Monetization Roadmap

1. **Phase 1 (0-10 posts):** Focus on quality content, internal linking
2. **Phase 2 (10-20 posts):** Apply for Google AdSense, add affiliate links (Klook, Trazy, etc.)
3. **Phase 3 (20+ posts):** Optimize top performers, add email newsletter, consider sponsored content

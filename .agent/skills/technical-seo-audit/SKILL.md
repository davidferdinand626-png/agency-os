---
name: technical-seo-audit
description: Perform comprehensive technical SEO audits covering crawlability, indexability, Core Web Vitals, URL architecture, and internal linking.
allowed-tools: Read, Glob, Grep
---

# Technical SEO Audit & Infrastructure Architecture

> Guarantee flawless search engine discovery, indexation, and ranking performance through systematic technical inspection.

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Conduct an in-depth technical audit of a client website or web app.
- Diagnose sudden drops in organic search visibility or crawl budget waste.
- Review website redesigns or migrations before DNS cutover.
- Optimize site architecture, canonical tag hierarchy, and robots.txt directives.

---

## 1. The 6 Technical SEO Audit Pillars

### Pillar 1: Crawlability & Indexability
- **Robots.txt Directives:** Verify that critical CSS, JS, and high-value conversion pages are not blocked. Check for misconfigured `Disallow: /` directives.
- **XML Sitemap Health:** Check sitemap format, encoding (`UTF-8`), freshness, and inclusion in `robots.txt`. Ensure 100% of sitemap URLs return `200 OK` (zero redirects, zero 404s, zero noindex tags).
- **HTTP Status Code Hygiene:**
  - Eliminate 301 redirect chains (A -> B -> C; must resolve directly A -> C).
  - Resolve 404/410 dead ends and redirect high-equity broken links.
  - Eliminate internal 5xx server error loops.

### Pillar 2: Canonicalization & Duplicate Content
- **Self-Referential Canonicals:** Every indexable page must contain a clean, self-referential `<link rel="canonical" href="https://example.com/clean-path">`.
- **Parameter Handling:** Ensure UTM tracking parameters, search queries (`?q=...`), and pagination do not generate duplicate indexation spikes. Enforce canonicalization to the base clean URL.
- **Protocol & Subdomain Consistency:** Enforce sitewide 301 redirects to a single canonical version:
  - `http://` -> `https://`
  - `http://www.` -> `https://example.com` (or vice-versa).

### Pillar 3: Core Web Vitals & Page Performance
Audit according to current Google Core Web Vitals thresholds:
- **LCP (Largest Contentful Paint):** $\le 2.5\text{ seconds}$ (optimize hero images with WebP/AVIF, preload critical fonts, eliminate render-blocking CSS).
- **INP (Interaction to Next Paint):** $\le 200\text{ milliseconds}$ (break up long JavaScript tasks, defer non-essential third-party trackers).
- **CLS (Cumulative Layout Shift):** $\le 0.1$ (explicit `width` and `height` attributes on all images, videos, and dynamic ad containers).

### Pillar 4: Semantic URL & Architecture Hierarchy
- URL paths must be clean, lowercase, hyphen-separated, and descriptive (e.g., `/services/corporate-transportation` vs. `/p?id=9482`).
- Flat crawl depth: All high-value commercial pages must be reachable within $\le 3$ clicks from the homepage.

---

## 2. Technical SEO Audit Report Schema

Structure technical findings using this standard format:

```markdown
# Technical SEO Audit Report: [Target Domain]

## 1. Executive Summary & Health Grade
- Overall Technical SEO Score: [0-100]
- Critical Blocking Issues (P0): [Count]
- Major Warnings (P1): [Count]
- Minor Opportunities (P2): [Count]

## 2. Detailed Technical Findings & Remediation Matrix
| Category | Severity | Issue Description | Impact | Specific Remediation Code/Action |
| :--- | :---: | :--- | :--- | :--- |
| Indexability | P0 | Multiple canonical tags on homepage | Splits page equity | Remove duplicate header injection in template |
| Performance | P1 | LCP image lacks preload link | Delays paint by 1.2s | Add `<link rel="preload" as="image" href="...">` |
| Crawling | P2 | 3-hop redirect chain on /pricing | Wastes crawl budget | Update internal links to point directly to destination |
```

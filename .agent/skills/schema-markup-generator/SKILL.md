---
name: schema-markup-generator
description: Generate valid, production-grade JSON-LD structured data schema markup for Organization, LocalBusiness, FAQPage, Product, and VideoObject.
allowed-tools: Read, Glob, Grep
---

# Schema Markup Generator & Structured Data Engineering

> Unlock rich snippets, knowledge graph cards, and enhanced search engine SERP presence using validated Schema.org JSON-LD markup.

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Generate valid, error-free JSON-LD structured data for client websites and landing pages.
- Enable Google Rich Results (FAQ accordions, review stars, video previews, breadcrumbs).
- Establish authoritative entity graphs for brands and executive personas.
- Validate structured data against Google's Structured Data Testing Tool standards.

---

## 1. Supported Schema Types & Core Templates

### 1. `Organization` / `LocalBusiness` Schema
*Best for: Brand homepages, contact pages, multi-location companies.*

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Little Ride Tanzania",
  "image": "https://littleride.co.tz/images/logo.png",
  "url": "https://littleride.co.tz",
  "telephone": "+255700000000",
  "priceRange": "$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Ali Hassan Mwinyi Road",
    "addressLocality": "Dar es Salaam",
    "addressRegion": "Dar es Salaam",
    "postalCode": "14111",
    "addressCountry": "TZ"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": -6.7924,
    "longitude": 39.2083
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": [
      "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"
    ],
    "opens": "00:00",
    "closes": "23:59"
  },
  "sameAs": [
    "https://twitter.com/LittleRideTZ",
    "https://linkedin.com/company/little-ride-tanzania"
  ]
}
</script>
```

### 2. `FAQPage` Schema
*Best for: High-converting landing pages, product pages, pricing FAQs to capture expanded SERP real estate.*

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How does automated corporate invoicing work for businesses?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Little Ride provides corporate accounts with automated monthly consolidated billing, detailed trip logs, and direct integration into enterprise accounting software, eliminating manual paper expense receipts."
      }
    },
    {
      "@type": "Question",
      "name": "Are Little Ride drivers vetted for passenger safety?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Every driver undergoes rigorous police background checks, vehicle safety inspections, and in-person professional hospitality training before activation on the platform."
      }
    }
  ]
}
</script>
```

### 3. `VideoObject` Schema
*Best for: Commercials, product explainer videos, video marketing landing pages.*

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "VideoObject",
  "name": "Little Ride: Seamless Business Commutes in Dar es Salaam",
  "description": "Discover how corporate teams save hours on transportation with verified drivers and automated monthly invoicing.",
  "thumbnailUrl": "https://littleride.co.tz/thumbnails/commercial-hero.jpg",
  "uploadDate": "2026-10-18T00:00:00Z",
  "duration": "PT0M35S",
  "contentUrl": "https://littleride.co.tz/video/little-ride-commercial.mp4",
  "embedUrl": "https://littleride.co.tz/embed/commercial",
  "publisher": {
    "@type": "Organization",
    "name": "Little Ride Tanzania",
    "logo": {
      "@type": "ImageObject",
      "url": "https://littleride.co.tz/logo.png"
    }
  }
}
</script>
```

---

## 2. Validation & Quality Rules

1. **Strict JSON-LD Syntax:** Output must be strictly valid JSON (double-quoted keys, no trailing commas, no unescaped line breaks).
2. **Context Requirement:** Always include `"@context": "https://schema.org"`.
3. **No Hidden Content:** All structured data properties (prices, hours, text) must be visible on the actual rendered HTML page. Hidden spam markup is strictly prohibited.
4. **ISO 8601 Compliance:** All dates and durations must follow standard formats (e.g., `YYYY-MM-DDThh:mm:ssZ` and `PT#M#S` for durations).

# Bolt's Journal - Critical Learnings

## 2025-05-10 - Shopify CDN Preconnect & LCP Image Fetchpriority
**Learning:** In Shopify Liquid themes with static hero images, adding `fetchpriority="high"` directly to hero `<img>` elements and `<link rel="preconnect" href="https://cdn.shopify.com" crossorigin>` in `<head>` significantly improves Largest Contentful Paint (LCP) by prioritizing network fetch and eliminating DNS/TLS latency for Shopify asset CDN requests.
**Action:** Always check hero image tags for `loading="eager"` combined with `fetchpriority="high"`, and ensure Shopify CDN preconnect hints are present in `layout/theme.liquid`.

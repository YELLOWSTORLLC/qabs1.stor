# Bolt's Journal - Performance Learnings

## 2025-05-18 - Shopify CDN Preconnect & Fallback Image Loading
**Learning:** Shopify Liquid snippets rendering images without respecting the `loading` variable default to lazy-loading, which delays critical LCP (Largest Contentful Paint) elements when snippets are rendered above the fold (e.g., product detail hero image). Preconnecting to `cdn.shopify.com` saves 100-300ms in DNS/TLS handshake overhead for assets.
**Action:** Always ensure fallback/image snippets propagate the `loading` attribute (`loading="{{ loading | default: 'lazy' }}"`) and add preconnect/dns-prefetch hints for CDN domains in `layout/theme.liquid`.

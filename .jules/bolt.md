## 2026-10-03 - Hardcoded loading="lazy" in Reusable Snippets Delays LCP
**Learning:** Shared snippet components like fallback image renderers (`snippets/product-image-fallback.liquid`) can unwittingly enforce `loading="lazy"` on above-the-fold content even when parent sections pass `loading: 'eager'`.
**Action:** Always verify that reusable liquid image snippets support dynamic `loading` and `fetchpriority` parameters so LCP elements on key templates (such as `main-product-v4.liquid`) can load greedily.

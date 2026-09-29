## 2025-05-18 - Cache DOM references in client event handlers
**Learning:** Re-querying the DOM with `querySelector` inside high-frequency event handlers (like select or checkbox `change` events) creates unnecessary CPU cycles and layout recalculations. Caching element references in closure scope once during component initialization improves update performance.
**Action:** Always pre-query and cache DOM target elements outside event handlers when initializing dynamic components or widgets.

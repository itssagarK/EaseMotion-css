# Enhanced Breadcrumb Component

## What does this do?
Enhances the existing breadcrumb component with support for icons, collapsible intermediate items for deep structures, dropdown menus on intermediate nodes, and 5 distinct separator styles.

## How is it used?
Configure a standard breadcrumb container with your desired items and custom features:

```html
<!-- Breadcrumb with Icons, Separator & Dropdowns -->
<nav aria-label="Breadcrumb" class="ease-breadcrumb ease-breadcrumb-sep-chevron">
  <ol class="ease-breadcrumb-list">
    <li class="ease-breadcrumb-item">
      <a href="/" class="ease-breadcrumb-link">
        <svg class="ease-breadcrumb-icon" viewBox="0 0 24 24"><!-- Home Icon --></svg>
        Home
      </a>
    </li>
    <li class="ease-breadcrumb-separator" aria-hidden="true"></li>
    
    <!-- Item with Dropdown -->
    <li class="ease-breadcrumb-item ease-breadcrumb-dropdown">
      <a href="/products" class="ease-breadcrumb-link">Products</a>
      <ul class="ease-breadcrumb-dropdown-menu">
        <li><a href="/products/electronics" class="ease-breadcrumb-dropdown-link">Electronics</a></li>
        <li><a href="/products/apparel" class="ease-breadcrumb-dropdown-link">Apparel</a></li>
      </ul>
    </li>
    <li class="ease-breadcrumb-separator" aria-hidden="true"></li>

    <li class="ease-breadcrumb-item ease-breadcrumb-current" aria-current="page">Laptops</li>
  </ol>
</nav>

<!-- Collapsed Path -->
<nav aria-label="Breadcrumb" class="ease-breadcrumb">
  <ol class="ease-breadcrumb-list">
    <li class="ease-breadcrumb-item"><a href="/">Home</a></li>
    <li class="ease-breadcrumb-separator" aria-hidden="true"></li>
    <li class="ease-breadcrumb-collapse-item" aria-label="Show more path">...</li>
    <li class="ease-breadcrumb-separator" aria-hidden="true"></li>
    <li class="ease-breadcrumb-item ease-breadcrumb-current">Current Page</li>
  </ol>
</nav>
```

### Separator Variants
- `.ease-breadcrumb-sep-chevron` (default, `>`)
- `.ease-breadcrumb-sep-slash` (`/`)
- `.ease-breadcrumb-sep-arrow` (`→`)
- `.ease-breadcrumb-sep-dot` (`.`)
- `.ease-breadcrumb-sep-bullet` (`•`)

## Why is it useful?
Allows users to navigate complex folder hierarchies or deep URL routing easily. Icon support improves visual scanning, collapsible path items save space on mobile layouts, and dropdown menus let users jump sideways into parallel categories directly from the trail.

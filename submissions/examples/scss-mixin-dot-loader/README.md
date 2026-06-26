# SCSS Mixin for Animated Dot Loader

A reusable, loop-based Sass mixin generating fluid loading dots with sequential delays.

## What does this do?

This feature adds `@mixin dot-loader` to `scss/_mixins.scss`. It automatically generates the container flexbox styles, dot sizing, and uses a `@for` loop to assign mathematical sequence delay timings (`animation-delay`) to each dot item.

## How is it used?

### Including the Mixin in SCSS

Import the mixins module and declare the loading class:

```scss
// style.scss
@use '../../../scss/mixins';

.my-spinner {
  @include mixins.dot-loader(
    $dot-size: 12px,
    $dot-spacing: 8px,
    $dot-color: #ef4444,
    $dot-count: 3
  );
}
```

### HTML Implementation

Structure the wrapper with items matching your `$dot-count` configuration:

```html
<div class="my-spinner" aria-label="Loading workspace data">
  <div class="ease-dot-loader-item"></div>
  <div class="ease-dot-loader-item"></div>
  <div class="ease-dot-loader-item"></div>
</div>
```

## Why is it useful?

1. **DRY Timings Logic**: Avoids hardcoding complex animation structures (`:nth-child(1) { animation-delay: 0s }`, etc.) for every individual spinner.
2. **Infinite Custom Sizing**: Scales instantly to fit compact form buttons, content card panels, or full-viewport splash screens.
3. **No-Jank CSS Animation**: Runs purely on GPU-accelerated transition properties (`transform` and `opacity`), preventing render blocks.

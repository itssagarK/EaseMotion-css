# SCSS Mixin for Gradient Border Animation

A modern, high-performance Sass mixin generating rotating gradient borders around card containers using element masking and CSS animation.

## What does this do?

This feature adds `@mixin gradient-border-animation` to `scss/_mixins.scss`. It uses absolute overlays: `::before` hosts the large rotating gradient, and `::after` masks the center of the container using the background color, creating the appearance of a clean, animated border outline.

## How is it used?

### Including the Mixin in SCSS

Import the mixins module and declare the border class, specifying the border width, gradient color stops, animation speed, and matching container background:

```scss
// style.scss
@use '../../../scss/mixins';

.live-card {
  @include mixins.gradient-border-animation(
    $border-width: 3px,
    $gradient: conic-gradient(#f59e0b, #ef4444, #f59e0b),
    $animation-duration: 6s,
    $background-color: #111827
  );
  
  // Custom sizing pad
  padding: 2rem;
}
```

### HTML Implementation

Structure the component normally:

```html
<div class="live-card">
  <h2>Server Monitor</h2>
  <p>The rotating outline will render automatically.</p>
</div>
```

## Why is it useful?

1. **Pure-CSS Rotating Borders**: Creates rotating gradient outlines without complex SVG shapes or heavy JavaScript tracking libraries.
2. **Dynamic Math Masks**: Computes border-radius inner overrides automatically using `calc($border-radius - $border-width)` to keep shapes aligned.
3. **GPU-Accelerated Physics**: Animates strictly via CSS `transform: rotate()`, avoiding layout triggers and maintaining high framerates.
4. **Reduced Motion Safety**: Automatically overrides and disables rotation animations when system preferences specify prefers-reduced-motion.

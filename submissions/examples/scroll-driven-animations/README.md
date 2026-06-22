# Scroll-Driven & View-Driven Animation Utilities

Add high-performance, native CSS Scroll-Driven Animations to your layout without adding any JavaScript weight to your pages. This feature introduces a set of classes leveraging the CSS Scroll-Driven Animations API (binding animations to the page scroll or viewport scroll intersections).

## Features

- **Progressive Enhancement**: Runs natively via GPU acceleration on modern browsers.
- **Graceful Degradation**: Fallback classes (`.ease-scroll-fallback`) provide instant or smooth time-based animation entries for non-supporting browsers.
- **Predefined Range Variables**: Includes customizable CSS custom properties for start scales, blur amount, parallax translate limits, and animation ranges.
- **Fully Accessible**: Respects OS `prefers-reduced-motion` settings.

---

## Utility Classes Reference

### 1. Scroll-Driven Progress Bar
- **Class**: `.ease-scroll-progress-bar`
- **Behavior**: A fixed top indicator bar indicating how far down the document the user has scrolled.
- **Target Timeline**: `scroll(root)`

### 2. View Timeline Animations (Linked to Intersection Viewport)
| Class Name | Effect Description | Range Property |
| :--- | :--- | :--- |
| `.ease-scroll-reveal` | Fades and translates up on viewport entry. | `--ease-scroll-reveal-range` |
| `.ease-scroll-parallax` | Moves background images or layers at slower rates. | `--ease-scroll-parallax-range` |
| `.ease-scroll-zoom` | Elegant scale zoom-in relative to scroll. | `--ease-scroll-zoom-range`, `--ease-scroll-zoom-start` |
| `.ease-scroll-blur` | Smoothly unblurs element as it scrolls up. | `--ease-scroll-blur-range`, `--ease-scroll-blur-amount` |
| `.ease-view-reveal` | Fades element in relative to scroll boundaries. | `--ease-view-reveal-range` |
| `.ease-view-slide-in` | Slides element in horizontally from the side. | `--ease-view-slide-in-range`, `--ease-view-slide-in-x` |

---

## Usage Example

```html
<!-- Top Progress Bar -->
<div class="ease-scroll-progress-bar ease-scroll-fallback"></div>

<!-- Scroll Zoom-In card with Custom Start Scale -->
<div class="glass-card ease-scroll-zoom ease-scroll-fallback" style="--ease-scroll-zoom-start: 0.75;">
  <h3>Zooming Content</h3>
  <p>This content will scale up dynamically as it enters the viewport.</p>
</div>
```

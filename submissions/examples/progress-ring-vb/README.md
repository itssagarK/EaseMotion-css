# Ease Progress Ring

A circular SVG-based progress indicator with smooth CSS stroke animation. This component fills a gap in the EaseMotion CSS library by providing a circular alternative to the linear progress bars.

## How is it used?

Apply the `.ease-progress-ring` class to a wrapper containing an SVG with two circles (`.ease-ring-track` and `.ease-ring-fill`). Set the progress using the `--ease-ring-progress` CSS variable (0-100).

```html
<div
  class="ease-progress-ring ease-progress-ring-animate"
  style="--ease-ring-progress: 75"
>
  <svg viewBox="0 0 100 100">
    <circle class="ease-ring-track" cx="50" cy="50" r="40" />
    <circle class="ease-ring-fill" cx="50" cy="50" r="40" />
  </svg>
  <span class="ease-ring-label">75%</span>
</div>
```

### Variants

- `.ease-progress-ring-success`: Green ring
- `.ease-progress-ring-danger`: Red ring
- `.ease-progress-ring-warning`: Yellow ring
- `.ease-progress-ring-animate`: Animates fill from 0 to the target percentage on page load.

## Why is it useful?

Circular progress rings are widely used in dashboards, portfolios, and app UIs for skill bars, loading indicators, countdown timers, and profile completeness widgets. This implementation is lightweight, uses native CSS variables for logic, and supports EaseMotion's design tokens and motion philosophy.

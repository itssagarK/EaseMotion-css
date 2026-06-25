# ease-virtual-list-skeleton

## What does this do?
A performant list loader placeholder featuring:
- A linear-gradient shimmer background animation (`ease-shimmer`)
- Row elements with varied widths for a natural text shape look
- A staggered row entrance transition on loading initialization
- Support for smooth transitions where the skeleton fades out (`ease-fade-out`) and actual content fades in (`ease-fade-in`)

## How is it used?
Construct a list matching the shapes of your final data objects. Use `.ease-shimmer` on the lines or nodes that represent placeholders:

```html
<div class="skeleton-row">
  <!-- Avatar Shimmer -->
  <div class="skeleton-avatar ease-shimmer"></div>
  
  <!-- Content Lines with varied widths -->
  <div class="skeleton-info">
    <div class="skeleton-line title ease-shimmer" style="width: 40%;"></div>
    <div class="skeleton-line subtitle ease-shimmer" style="width: 85%;"></div>
  </div>
</div>
```

## Why is it useful?
It provides visual feedback during high-volume data load (e.g. infinite scroll, virtual lists). The varied line widths mimic the structural shape of actual text lists, offering a superior visual transition that prevents layout shifts.

## Tech Stack
- HTML
- CSS (Vanilla, hardware-accelerated shimmer)
- Minimal JS (for simulation only)

## Preview
Open `demo.html` directly in your browser and click **Simulate Load Data** to see the shimmer and load transitions.

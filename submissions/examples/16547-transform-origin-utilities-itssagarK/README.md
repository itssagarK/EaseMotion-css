# CSS Transform-Origin Utilities (Issue #16547)

This submission introduces **transform-origin** utility classes for the **EaseMotion CSS** framework. These utilities provide declarative configuration of pivot/origin points for 2D and 3D CSS transforms (rotate, scale, skew) corresponding to 9 spatial layout coordinates.

## 📋 Features & Classes

| Utility Class | CSS Rule | Description |
| :--- | :--- | :--- |
| `.ease-transform-origin-center` | `transform-origin: center !important;` | Pivots from the center. |
| `.ease-transform-origin-top` | `transform-origin: top !important;` | Pivots from the top edge. |
| `.ease-transform-origin-top-right` | `transform-origin: top right !important;` | Pivots from the top right corner. |
| `.ease-transform-origin-right` | `transform-origin: right !important;` | Pivots from the right edge. |
| `.ease-transform-origin-bottom-right` | `transform-origin: bottom right !important;` | Pivots from the bottom right corner. |
| `.ease-transform-origin-bottom` | `transform-origin: bottom !important;` | Pivots from the bottom edge. |
| `.ease-transform-origin-bottom-left` | `transform-origin: bottom left !important;` | Pivots from the bottom left corner. |
| `.ease-transform-origin-left` | `transform-origin: left !important;` | Pivots from the left edge. |
| `.ease-transform-origin-top-left` | `transform-origin: top left !important;` | Pivots from the top left corner. |

## 🛠️ Usage Example

Set the pivot point of a card hover tilt effect to the bottom edge:

```html
<div class="card ease-transform-origin-bottom">
  <h3>Interactive Panel</h3>
</div>
```

## 🎨 Interactive Demo

The included [demo.html](demo.html) showcases:
1. **Interactive Spin Canvas:** Contains a rotating R-CARD block spinning infinitely.
2. **Interactive 9-Point Grid Selector:** Switch pivot coordinates dynamically.
3. **Visual Pivot Tracking Dot:** A visual pointer dot positioned dynamically over the rotating card to illustrate the current location of the pivot coordinates in action.

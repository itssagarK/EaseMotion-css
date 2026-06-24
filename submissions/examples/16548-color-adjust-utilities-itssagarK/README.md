# CSS Color-Adjust Utilities (Issue #16548)

This submission introduces **color-adjust** utility classes for the **EaseMotion CSS** framework. These utilities provide control over background colors, graphics, and borders when exporting pages as PDFs or printing them.

## 📋 Features & Classes

| Utility Class | CSS Rule | Description |
| :--- | :--- | :--- |
| `.ease-color-adjust-economy` | `print-color-adjust: economy !important;` | Allows browsers to omit background graphics to conserve ink. |
| `.ease-color-adjust-exact` | `print-color-adjust: exact !important;` | Forces high-fidelity rendering of all colors and gradients when printing. |
| `.ease-print-color-adjust-economy` | `print-color-adjust: economy !important;` | Fallback print wrapper alias. |
| `.ease-print-color-adjust-exact` | `print-color-adjust: exact !important;` | Fallback print wrapper alias. |

## 🛠️ Usage Example

To ensure a progress chart widget maintains its background color and status values when printing, apply `.ease-color-adjust-exact`:

```html
<div class="chart-widget ease-color-adjust-exact">
  <div class="bar-fill" style="background-color: var(--ease-color-primary);"></div>
</div>
```

## 🎨 Interactive Demo

The included [demo.html](demo.html) showcases:
1. **Economy Mode Sandbox:** Displays standard rendering. In print preview, the gradient block will be optimized or stripped to save toner.
2. **Exact Mode Sandbox:** Displays identical design. In print preview, the radial gradient block remains fully rendered and colorful.
3. **Print Simulator Action Button:** Launches the browser print preview dialog directly to compare the outputs.

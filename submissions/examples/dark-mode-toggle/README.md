
# Create the README.md file
readme_content = '''# Dark Mode Toggle

A pure CSS dark mode toggle component with smooth theme transitions and sun/moon icon morph animation.

## Features

- ✅ **Pure CSS** — No JavaScript required (uses `:has()` selector)
- ✅ **Smooth transitions** — All colors animate over 0.3s
- ✅ **Icon morph** — Sun rotates and morphs into moon on toggle
- ✅ **Accessible** — Keyboard focusable, respects `prefers-reduced-motion`
- ✅ **Composable** — Works with any EaseMotion CSS classes

## Demo

Open `demo.html` in your browser and click the toggle to see the theme switch.

## How It Works

The component uses a hidden checkbox input and the CSS `:has()` selector to toggle CSS custom properties:

```css
body:has(#dark-mode-toggle:checked) {
  --dm-bg: #0f172a;
  --dm-text: #f1f5f9;
  /* ... other dark mode variables */
}
```

## Browser Support

- Chrome 105+
- Edge 105+
- Safari 15.4+
- Firefox 121+

> For older browsers, a small JS fallback can be used to toggle a `.dark` class on `<body>`.

## Integration with EaseMotion CSS

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/SAPTARSHI-coder/EaseMotion-css@main/easemotion.min.css">
<link rel="stylesheet" href="style.css">
```

## Customization

Override these CSS variables in your own stylesheet:

| Variable | Light Mode | Dark Mode |
|----------|-----------|-----------|
| `--dm-bg` | `#ffffff` | `#0f172a` |
| `--dm-surface` | `#f8fafc` | `#1e293b` |
| `--dm-text` | `#1e293b` | `#f1f5f9` |
| `--dm-toggle-active` | `#3b82f6` | `#60a5fa` |

## Files

- `demo.html` — Live demo with EaseMotion CSS integration
- `style.css` — Component styles
- `README.md` — This file

## Author

Submitted for GSSoC contribution to EaseMotion CSS.
'''

with open('/mnt/agents/output/README.md', 'w') as f:
    f.write(readme_content)

print("✅ README.md created")

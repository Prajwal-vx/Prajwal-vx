# GitHub UI/UX Redesign — Platinum × French Gray × Gunmetal

## Objective

Redesign the GitHub UI/UX into a premium, modern, futuristic developer workspace.

The design must feel:

- Unique
- Attractive
- Professional
- Minimal
- Premium
- Developer-focused
- Dark and sophisticated
- Visually different from the standard GitHub interface

Do not simply apply a dark theme. Create a cohesive new design system using the supplied Platinum / French Gray / Gunmetal palette.

---

# 1. Color Palette

The entire application should use the following color system.

| Purpose | Color | Hex |
|---|---|---|
| Dominant | Platinum | `#D3D0D5` |
| Secondary | French Gray | `#A4A2AB` |
| Accent | Gunmetal | `#292B39` |
| Page Background | Deep Gunmetal | `#20222D` |
| Elevated Surface | Gunmetal Surface | `#323442` |
| Border | Soft Gray | `#6F707A` |
| Primary Text | Soft White | `#F3F2F4` |
| Secondary Text | Cool Gray | `#C0BEC5` |
| Muted Text | Muted Gray | `#8F909A` |
| Success | Muted Green | `#A9C2B0` |
| Warning | Muted Gold | `#D0B98A` |
| Error | Muted Red | `#C49A9F` |

Create global CSS variables:

```css
:root {
  --platinum: #D3D0D5;
  --french-gray: #A4A2AB;
  --gunmetal: #292B39;

  --background: #20222D;
  --surface: #292B39;
  --surface-elevated: #323442;

  --border: rgba(211, 208, 213, 0.10);
  --border-hover: rgba(211, 208, 213, 0.22);

  --text-primary: #F3F2F4;
  --text-secondary: #C0BEC5;
  --text-muted: #8F909A;

  --success: #A9C2B0;
  --warning: #D0B98A;
  --danger: #C49A9F;
}

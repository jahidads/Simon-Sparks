ProBank — Sidebar enhancement

What I added
- A mobile-friendly, accessible sidebar with hamburger toggle, overlay, and smooth transitions.
- `sidebar.js` implements keyboard support (Esc to close, basic focus trap), and wires quick action buttons to existing modals.
- Small CSS additions in the inline `<style>` block of `index.html` to style the sidebar and overlay.

Files changed/added
- `index.html` — added hamburger button, sidebar markup, overlay, and CSS; included `sidebar.js` via a `<script>` tag.
- `sidebar.js` — new file providing toggle and accessibility behavior.
- `README.md` — this file.

How to try locally (Windows PowerShell)
1. Open PowerShell in the `d:\OneDrive\Desktop\html` folder.
2. Start a simple static server (Python required):

```powershell
python -m http.server 8000
```

3. Open http://localhost:8000 in your browser and resize the window to test mobile behavior. Click the hamburger to open the sidebar, press Esc to close, and try keyboard navigation (Tab / Shift+Tab).

Notes & customization
- Colors and sizes use CSS variables at the top of the inline `<style>` block in `index.html` — adjust `--primary`, `--secondary`, etc.
- `sidebar.js` is purposely small and dependency-free. It expects the modals and elements from the existing app (e.g., `sendMoneyModal`).
- For more advanced focus management and animations, consider adding a small library (e.g., focus-trap) or expanding the JS logic.

Accessibility
- The sidebar has `aria-hidden` toggled and `aria-controls` / `aria-expanded` on the hamburger button.
- Basic focus trapping is implemented; further testing with screen readers is recommended.

Next steps (optional)
- Animate active nav item, add icons as SVGs, and add tests that assert DOM state after toggle.
- Extract CSS to `styles.css` for maintenance.

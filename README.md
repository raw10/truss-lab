# Popsicle Bridge / Truss Lab

Interactive stick-first lab for designing and analyzing a popsicle-stick bridge in the browser.

**Live site:** [https://raw10.github.io/truss-lab/](https://raw10.github.io/truss-lab/)

Build a pin truss or a bending frame, hang a mass in kilograms, and read member forces (and moments in frame mode) with colors on the canvas and in a results table.

## Features

### Stick-first editing
- **Add stick** — place members from the supports or existing joints
- **Rotate ends** — drag stick ends; they snap to the grid or stick crossings
- **Move joint** — reposition free joints (supports stay fixed)
- **Set load** — click a joint for a downward hanging mass
- **Delete** — remove sticks or joints
- **Clear** — wipe the bridge (with confirmation); undo can restore it

### Geometry & view
- Editable **bridge length**, **span**, **grid**, and **max stick length** (inches)
- Grid snap, joint merge when ends land nearby, and automatic split/merge at stick crossings
- **Pinch-zoom** and scroll-wheel zoom; joints stay a constant screen size
- **Fit** recenters the view on the bridge

### Analysis
- **Truss mode** — pin joints, axial force only (tension / compression)
- **Frame mode** — joints resist bending; reports axial force and moment
- **Stick depth** (frame mode) for in-plane bending stiffness
- **Load in kg** converted to newtons (\(F = mg\)) for real force magnitudes
- Forces shown as **N**; moments as **N·m**
- Canvas colors: **red = tension**, **blue = compression**, tan = unloaded
- On-canvas force labels on every member; hover tooltips for detail
- Stability checks with suggestions for brace sticks when the model is a mechanism

### Results & parameters
- Member-forces table with Stick / Force (N) / Moment (N·m) columns (moment in frame mode)
- Colored LED indicators in the legend and table (also visible when printing)
- Editable **Bridge parameters** JSON panel with **Apply** and **Copy**
- Design persists in **localStorage** across visits

### History & shortcuts
- **Undo / Redo** toolbar buttons
- Keyboard: **Ctrl/Cmd+Z** undo, **Ctrl/Cmd+Y** or **Ctrl/Cmd+Shift+Z** redo

### Print
- Landscape single-page layout: compact settings table, canvas, and forces side by side
- Parameter editor hidden when printing; force LEDs keep their colors
- Grid cells stay square (isotropic scale) so the bridge is not squished

### Hosting
- Static single-page app (`index.html`) — no build step
- Deployed to **GitHub Pages** from `main` via Actions

## Quick start

Open the live site: [https://raw10.github.io/truss-lab/](https://raw10.github.io/truss-lab/)

Or run locally:

```bash
python3 -m http.server 5173
```

Then visit [http://localhost:5173](http://localhost:5173).

You can also open `index.html` directly in a browser.

## GitHub Pages

If the live URL 404s, enable Pages once (repo admin):

1. Open [Settings → Pages](https://github.com/raw10/truss-lab/settings/pages)
2. Under **Build and deployment**, set **Source** to **GitHub Actions**
3. Open [Actions → Deploy GitHub Pages](https://github.com/raw10/truss-lab/actions/workflows/pages.yml) → **Run workflow** on `main`

Or set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.

## License

[MIT](LICENSE) © Rob Watts

# Truss Lab

Interactive popsicle-stick bridge lab: place sticks, rotate their ends (snap to grid or crossings), set a load, and read axial member forces (tension / compression) as a fraction of one downward load.

## Live site

**https://raw10.github.io/truss-lab/**

If that 404s, enable Pages once (repo admin):

1. Open [Settings → Pages](https://github.com/raw10/truss-lab/settings/pages)
2. Under **Build and deployment**, set **Source** to **GitHub Actions**
3. Open [Actions → Deploy GitHub Pages](https://github.com/raw10/truss-lab/actions/workflows/pages.yml) → **Run workflow** on `main`

Or set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.

## Run locally

Open `index.html` in a browser, or:

```bash
python3 -m http.server 5173
```

Then visit http://localhost:5173

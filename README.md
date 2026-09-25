# Insert mount for waveplates and polarisers – Ø100 rotation stage

Interactive, parametric 3D model (Three.js) of a drop-in mount that holds a
quarter-wave plate or linear polariser in the central bore of a Ø100 motorised
rotation stage (42BYGH613 stepper drive). The page also generates a live
workshop section drawing, dimension table, parts list and assembly procedure.

## Project structure

```
index.html              the whole app (HTML, CSS, JS in one file)
vendor/three/           Three.js r147 (MIT licence), served locally
  three.min.js
  OrbitControls.js
  RoomEnvironment.js
  LICENSE
vercel.json             static hosting config (clean URLs, caching)
```

No build step, no npm install, no framework. It is a plain static site.

## Run locally

Open `index.html` directly in a browser, or serve the folder:

```
python3 -m http.server 8000
# then open http://localhost:8000
```

## Put it on GitHub

```
cd rotation-stage-optic-mount
git init
git add .
git commit -m "Rotation stage optic mount viewer"
git branch -M main
git remote add origin https://github.com/<your-user>/rotation-stage-optic-mount.git
git push -u origin main
```

## Deploy on Vercel

1. Sign in at vercel.com with GitHub and choose **Add New… → Project**.
2. Import the `rotation-stage-optic-mount` repository.
3. Framework Preset: **Other**. Leave Build Command and Output Directory empty
   (Root Directory: `./`).
4. Click **Deploy**. Every later `git push` redeploys automatically.

## Before machining

The stage bore diameter (≈ Ø30 read from the supplier drawing), the depth of
the four M4 threads in the table, and the height of the four factory screw
heads must be measured on the real stage. Enter the measured bore in the page;
all dimensions update.

## Licences

Three.js is © 2010–2022 three.js authors, MIT licence (see
`vendor/three/LICENSE`). Fonts are loaded from Google Fonts (Archivo, SIL OFL);
the page falls back to system fonts if they are unavailable.

# TASH — Stair-Climbing Robotic Oxygen Carrier (pitch site)

Live interactive pitch site for **TASH**, a stair-climbing robotic dog that
carries oxygen alongside therapy patients so they don't have to haul a heavy
tank up the stairs themselves.

**Live site:** https://anthony-sin.github.io/Stair-Climbing-Robotic-Dog-for-Oxygen-Therapy-Patients-Website/

It's a no-build-step [Three.js](https://threejs.org/) scroll-deck: a flat
"blueprint" render of the robot with hand-scrubbable follow/climb animation
clips, plus embedded demo footage of the real and simulated system.

## How it's deployed

This is a fully static site (plain ES modules, Three.js vendored locally under
`vendor/`, no bundler). Every push to `main` runs
[`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml),
which publishes the repository root to GitHub Pages.

## Running locally

Because the page fetches `models/*.glb` and uses ES module imports, it needs an
HTTP origin — opening `index.html` via `file://` won't work.

```sh
python -m http.server 8000
# then open http://localhost:8000/
```

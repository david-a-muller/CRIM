# CRIM: Claude's Range of Ions in Materials

Browser-based Monte Carlo simulators for ion and electron beams in solids. Each tool is a single self-contained HTML file: no installation, no server-side code, and all calculations run in the visitor's browser.

| Page | What it does |
|---|---|
| `index.html` | Landing page linking the tools |
| `crim.html` | Ion transport (He, Ne, Ar, Ga, Kr, Xe; 100 eV – 1 MeV): ranges, straggle, damage cascades, vacancies, sputtering, energy deposition, stopping powers, energy sweeps |
| `crim-sweep.html` | Line plots of Range, straggle, sputter yield, damage or stopping versus beam energy, with overlaid runs and PDF/CSV export |
| `electron.html` | Electron transport (100 eV – 1 MeV): trajectories, interaction volume, depth–dose, backscatter, lateral spread |

## Running it

Open the GitHub Pages site for this repository, or download any HTML file and open it directly in a browser.

URL parameters set the starting values, for example:

```
crim.html?ion=Xe&material=si&energy=30&tilt=52
crim-sweep.html?ion=Ga&material=gaas&plot=Rp
```

## Physics (ion tools)

Binary-collision approximation in an amorphous target: ZBL universal potential with the magic-formula scattering angle, ZBL85 electronic stopping with Bragg additivity, TRIM-style free flight, displacement/replacement rules, and planar surface binding for sputtering. Ranges typically agree with SRIM within about 10%; sputter yields are typically within a factor of two of experiment. No channeling, damage build-up or electronic straggling.

## Credits

Developed by David A. Muller and Claude. 
ZBL85 electronic-stopping coefficients are taken from [pyRUMP](https://github.com/ikost/pyRUMP) (MIT License). See `THIRD_PARTY_NOTICES.md`.

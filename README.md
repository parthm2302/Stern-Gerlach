# Stern–Gerlach Experiment Simulator

A single-page static website (HTML + CSS + JavaScript, no dependencies, no build step).

## Run locally
Open `index.html` in any browser.

## Deploy on Vercel
**Option A: GitHub (recommended)**
1. Create a GitHub repo and upload `index.html` (and this README).
2. Go to vercel.com → Add New → Project → import the repo.
3. Framework preset: **Other**. Leave build command and output directory empty. Click Deploy.

**Option B: CLI**
```
npm i -g vercel
cd stern-gerlach
vercel --prod
```

## How the simulation works
- Inputs: number of particles N, field axis (x/y/z), initial spin state, spin quantum number s.
- The angle γ between the spin direction and the field axis gives p = cos²(γ/2).
- Each particle's outcome m is drawn from a binomial distribution over 2s trials (for s = 1/2: up with probability p, down with 1 − p). Unpolarised beams give all 2s+1 outcomes equal probability.
- Observed counts are compared with the quantum prediction in the results table.

# Stern–Gerlach Experiment Simulator

An interactive website that simulates the Stern–Gerlach experiment, a landmark of quantum mechanics.

**Live site:** https://sterngerlach.vercel.app

## What it does
- Fires a chosen number of atoms (1 to 1,000,000) through a magnetic field.
- Lets you choose the field axis (x, y or z), the direction of the incoming spin, and the particle's spin (1/2, 1 or 3/2).
- Animates the atoms splitting into discrete beams and landing on a detector plate.
- Compares the quantum result with what classical physics would predict.
- Shows predicted and observed counts for each beam.
- Includes a short explanation of the physics and the history of the experiment.

## How the simulation works
1. The angle γ between the incoming spin direction and the field axis is found from the inputs.
2. The probability of the "up" outcome is p = cos²(γ/2).
3. Each atom's result is drawn at random from that probability. For spin s, the outcomes follow a binomial distribution over 2s trials. A random (unpolarised) beam gives every outcome equal probability.
4. Observed counts are compared with the predicted counts. The gap shrinks as the number of atoms grows.

## Run it on your computer
Download this repository and open `index.html` in any browser. No installation is needed.

## Built with
Plain HTML, CSS and JavaScript (canvas for the graphics). Hosted on Vercel.

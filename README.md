# monte-carlo-simulation
Physics 286 (Computational Physics) Final Project - Monte Carlo Simulation &amp; Data Visualization

# Monte Carlo Convergence in Estimating π

Final project for PHY 286 (Computational Physics) at Miami University, completed with Adam Feldman. The project uses Monte Carlo sampling to estimate the value of π and analyzes how the estimate for π converges as the sample size increases, including how much more it costs to compute each additional digit of accuracy.

## Method

Random (x, y) points are generated inside a 2x2 square, where the fraction that lands inside the inscribed unit circle estimates π/4. Running this from n = 1 up to 1,000,000 samples produces the convergence curve. The n = 100,000 case was repeated 200 times to get a stable error estimate. A digit of accuracy formula (d = −log₁₀|estimate − π|) was used to find how many samples are needed to reliably gain each additional decimal digit of π.

## Results

- At 100,000 samples (200 run median), achieved mean error ≈ 0.0044, standard deviation ≈ 0.0034
- The estimate visibly converges to π within ~10,000–100,000 samples
- Confirms the theoretical O(1/√n) convergence rate where each additional correct digit costs roughly 6–10x
  more samples than the one before it.

Full write up with references and figures can be found at `PHY286_FINAL_LukeAdam_MonteCarlo.pdf`.

## Built with

Built using Python, NumPy, Matplotlib

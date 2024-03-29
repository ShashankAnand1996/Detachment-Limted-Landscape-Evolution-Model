# Landscape Evolution Model (LEM)

- This Python code implements an algorithm to implicitly and efficiently compute the erosion term for the detachment-limited landscape evolution model (LEM).
- The numerical results using this algorithm have been tested for accuracy based on analytical predictions in the publication referred to below.
- The resulting numerical scheme allows us to achieve accurate steady-state solutions in high erosion rates leading to heavily dissected landscapes.

# Publication

The peer-reviewed research article can be found here: https://doi.org/10.1016/j.envsoft.2020.104804.

# Installation

- The code is presented as a *jupyter notebook*, which can be installed using pip as `pip install notebook` or using Conda `conda install -c conda-forge notebook`.
- Required python libraries are *numpy* and *scipy* libraries, which can be installed using pip as `pip install numpy` and `pip install scipy`, respectively. 
- The presented algorithm is compatible with the *landlab* modeling environment in Python, which can be installed as `pip install landlab
` or using Conda `conda install landlab -c conda-forge`.
- The jupyter notebook also uses *display* module from the *ipython* library, which can be installed as `pip install ipython` or using Conda `conda install -c anaconda ipython`.
- File **Zinitial_500_100.npy** in the repository is the elevation array used as the initial condition in the solver (the user can use other initial conditions as well).

# Code structure

Each number in the list below explains the operations and functions of the particular Cell of the Jupyter Notebook.
1. Import relevant packages from the above-mentioned libraries.
2. Define the Python function for computing the erosion term implicitly using the D_infinity flow direction method and define the Python function that implicitly updates the diffusion term using the LGMRES algorithm. 
3. Initializing the coefficients, domain size, and model parameters to be used in the solver.
4. Initializing the raster grid, boundary conditions, and the initial condition for the simulation run.
5. *While* loop for the simulation run until the steady-state is reached.
9. Save the elevation and drainage area arrays for plotting and further investigations.

# Results

* The "Results" folder in this GitHub directory contains all the steady-state solutions shown in the manuscript figures.
* Numpy arrays with keywords **acc** and **ele** indicate the drainage area and elevation array, respectively, at the steady state.
* Numpy arrays with keyword **diff** is the array of the list with
  * diff[0] - time-step.
  * diff[1] - maximum change in elevation at a node from the previous time step.
  * diff[2] - change in mean elevation from the previous time step.
 
 # Updates
 
The Python code has been updated to be compatible with the recent changes in the Landlab version.

# Contact Us

For more information about this research, you can reach out to me: [Shashank Kumar Anand](mailto:skanannd@tamu.edu?subject=[GitHub]%20Landscape%20Evolution%20Model%20(LEM)%20Numerical%20Solver). 

# Other Links

Well-commented Python code for solving the linear stability analysis problem regarding the first channel instability of the Landscape Evolution Model (LEM) by the same author is obtainable at [ShashankAnand1996/LEM_Stability_Analysis](https://github.com/ShashankAnand1996/LEM_Stability_Analysis). The peer-reviewed article has been published in JGR:Earth Surface and is available here: [Inception of Regular Valley Spacing in Fluvial Landscapes: A Linear Stability Analysis](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2022JF006716).

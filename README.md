## About
**Genetic Algorithm** for efficient single and multi-layer **solar cell** thickness optimization

## Contents
[Dependencies](#dependencies) • [Solar Cell](#solar-cell-device-structure) • [How to Use](#how-to-use) • [Results](#results) • [Cite](#acknowledgement)

## Dependencies
* Tested on Windows 7 and Ubuntu 18.04
* Test on Matlab 2018b and 2019a
* Toolboxes:
    * Add-Ons > Get Add-Ons
    * *de2bi* and *bi2de* functions:
        * Communication System Toolbox (Matlab 2018b)
        * Communications Toolbox (Matlab 2019a)
    * Parallel Computing Toolbox
    * Trading Toolbox
* `cprintf.m` ([download link](https://www.mathworks.com/matlabcentral/fileexchange/24093-cprintf-display-formatted-colored-text-in-the-command-window))

## Solar cell device structure
Evolutionary algorithm in ZnO and MoOx Optical Spacer
  <p align="left">
  <img src="./assets/solar_cell_device_structure.png" width="200" alt="Solar cell device structure">
  </p>

## Requirements:
1. Lumerical, FDTD solutions software + license (you can get 1 month trial version from their website if you have a organization email)
2. The solar cell FDTD file (`Evo_alg__P3HT-ICBA.fsp`)
3. In the file that starts with `jsc_FDTD_...`, under the comment `%Load simulation file`, change the file directory to the directory you have saved the solar cell FDTD file in.

## How to Use
1. Run code:
    * Single layer: `./[MoOx or ZnO folder]/[MoOx or ZnO]_Main_frontend_gui.m`
    * Multiple layer: `./[ZnO+MoOx folder]/[ZnO_and_MoOx]_Main_frontend_gui.m`
2. Choose how many runs of each selection method has to perform. Each section has a repeat counter of 1000 times. This was used for finding the average number of simulations required by the selection method. For real time usage, change the 'repeat_runs' variable value to 1 in the .m file that starts with Evo_alg_...

## Results
> Saved in Excel files, with number of sheets equivalent to the number of runs in each selection.

> Accuracy of 100%: all the 5000 runs converged to the optimal solution.

#### ZnO single layer optimization [[excel](./ZnO%20optical%20spacer%20optimization%20files/RESULTS)]
  <p align="left">
    <img src="./assets/optim_zno.png" height="200" alt="ZnO single" hspace="15cm">
    <img src="./assets/optim_zno_plot.png" height="200" alt="ZnO single plot">
  </p>

#### MoOx single layer optimization [[excel](./MoOx%20optical%20spacer%20optimization%20files/RESULTS)]
  <p align="left">
    <img src="./assets/optim_moox.png" height="200" alt="MoOx single" hspace="15cm">
    <img src="./assets/optim_moox_plot.png" height="200" alt="MoOx single plot" hspace="15cm">
  </p>

#### ZnO+MoOx multi-layer optimization [[excel](./ZnO+MoOx%20optical%20spacer%20optimization%20files/RESULTS)]
  <p align="left">
    <img src="./assets/optim_zno_moox.png" height="200" alt="ZnO+MoOx" hspace="15cm">
    <img src="./assets/optim_zno_moox_plot.png" height="200" alt="ZnO+MoOx" hspace="15cm">
  </p>

## Acknowledgement
Co-First Authors: [Premkumar Vincent](https://github.com/vinpremkumar) and [Gwenaelle Cunha Sergio](https://github.com/gcunhase) had equal contribution

Include citation once available

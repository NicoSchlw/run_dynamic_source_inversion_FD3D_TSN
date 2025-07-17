# Running a Dynamic Source Inversion

This repository contains the **FD3D_TSN** source code for performing joint coseismic and postseismic dynamic source inversion, as described in [Premus et al., 2020](https://doi.org/10.1785/0220190374). The code version included here is specifically associated with the dynamic source inversion of the 2004 Parkfield, California earthquake ([Schliwa et al., 2024](https://doi.org/10.1029/2024JB029410)).

---

## Compiling the Code

The GPU-accelerated Fortran code requires the **`nvfortran`** compiler (part of the NVIDIA HPC SDK).

You can compile the code using one of the provided scripts:

- **`compileFVW-GPU.sh`**  
  Compiles the code for execution on a single GPU.

- **`compileFVW-MPI.sh`**  
  Compiles the code for distributed execution using multiple GPUs via MPI.

---

## Preparing Input Files

Example input files for the 2004 Parkfield earthquake are available in this repository: [Dynamic Source Inversion Input Files](https://github.com/NicoSchlw/dynamic_source_inversion_input)

> **Note:** Copy all input files into the same directory as the compiled source code before running the inversion.

---

## Running the Dynamic Source Inversion

Use the provided script to launch the inversion:

- **`start_inversion.sh`**  

> The number of MPI processes specified (minus one) determines the number of parallel Markov chains used in the inversion.

---

## References

Users of the code are requested to acknowledge the following publications:

- Gallovič, F., Valentová, L., Ampuero, J.‐P., & Gabriel, A.‐A. (2019a). Bayesian dynamic finite‐fault inversion: 1. Method and synthetic test. Journal of Geophysical Research: Solid Earth, 124(7), 6949–6969. https://doi.org/10.1029/2019jb017510
  
- Gallovič, F., Valentová, L., Ampuero, J.‐P., & Gabriel, A.‐A. (2019b). Bayesian dynamic finite‐fault inversion: 2. Application to the 2016 Mw 6.2 Amatrice, Italy, earthquake. Journal of Geophysical Research: Solid Earth, 124(7), 6970–6988. https://doi.org/10.1029/2019jb017512
  
- Premus, J., Gallovič, F., Hanyk, L., & Gabriel, A. (2020). FD3D_TSN: A fast and simple code for dynamic rupture simulations with GPU acceleration. Seismological Research Letters, 91(5),2881–2889. https://doi.org/10.1785/0220190374
  
- Premus, J., Gallovič, F., & Ampuero, J.‐P. (2022). Bridging time scales of faulting: From coseismic to postseismic slip of the Mw 6.0 2014 South Napa, California earthquake. Science Advances, 8(38). https://doi.org/10.1126/sciadv.abq2536
  
-  Schliwa, N., Gabriel, A.-A., Premus, J., & Gallovič, F. (2024). The linked complexity of coseismic and postseismic faulting revealed by seismo-geodetic dynamic inversion of the 2004 Parkfield earthquake. Journal of Geophysical Research: Solid Earth, 129, e2024JB029410. https://doi.org/10.1029/2024JB029410 

# Running a dynamic source inversion

This repository contains the **FD3D_TSN** source code ([Premus et al., 2020](https://doi.org/10.1785/0220190374)) for running a joint coseismic and postseismic dynamic source inversion. 
The code version is associated with the dynamic source inversion of the 2004 Parkfield, California earthquake ([Schliwa et al., 2024](https://doi.org/10.1029/2024JB029410)).

---

## Compiling the code

The GPU-accelerated Fortran code relies on the `nvfortran` compilier.
- `compileFVW-GPU.sh`: provides the instructions to compile the code for a single GPU
- `compileFVW-MPI.sh`: provides the instructions to compile the code for multiple GPUs

## Preparing the input files

Example input files associated with the 2004 Parkfield earthquake are available in this repository: [Dynamic source inversion input](https://github.com/NicoSchlw/dynamic_source_inversion_input)

Copy all input files in the directory of the source code before starting the inversion.

## Starting the dynamic source inversion

**`start_inversion.sh`** provides the command to run the dynamic source inversion. The number of MPI processes -1 sets the number of Markov chains of the dynamic source inversion.

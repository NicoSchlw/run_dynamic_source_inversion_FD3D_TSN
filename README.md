# Running a Dynamic Source Inversion

This repository contains the **FD3D_TSN** source code for performing joint coseismic and postseismic dynamic source inversion, as described in [Premus et al., 2020](https://doi.org/10.1785/0220190374).  
The code version included here is specifically associated with the dynamic source inversion of the 2004 Parkfield, California earthquake ([Schliwa et al., 2024](https://doi.org/10.1029/2024JB029410)).

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

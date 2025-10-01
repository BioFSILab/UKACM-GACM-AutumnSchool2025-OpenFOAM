# UKACM & GACM Autumn School 2025

---

## Repository Structure

Each folder corresponds to a specific set of tutorials or documentation:

- `Installation_Guidelines/` – Installation guides for OpenFOAM v2412 on **Ubuntu** and **Windows**, including setup of the **solids4foam** solver.  
- `OpenFOAM_FluidMechanics/` – Fluid mechanics tutorials (e.g., cavity, NACA0012 pitching and plunging airfoil).  
- `OpenFOAM_SolidMechanics/` – Solid mechanics and FSI tutorials, including the **Hron–Turek benchmark case** for fluid–structure interaction.  

Within each case folder, the standard OpenFOAM directory structure is followed:

- `0/` – Initial and boundary conditions  
- `constant/` – Mesh and physical models (transport properties, turbulence, etc.)  
- `system/` – Solver settings, schemes, and controls  

---

## About solids4foam

**solids4foam** is an open-source toolbox based on the **finite volume method (FVM)**, integrated into OpenFOAM. It is designed to perform **solid mechanics** simulations as well as **fluid–solid interaction (FSI)** using the finite volume approach. This extends OpenFOAM’s capabilities beyond fluid dynamics into coupled multiphysics simulations.

---

## Getting Started

### Requirements
- [OpenFOAM v2412](https://www.openfoam.com/download/) (tested version)  
- [solids4foam](https://www.solids4foam.com/)  
- A Linux environment (WSL, Ubuntu, or native Linux recommended)  

### Running a Case
From the case directory:

```bash
# 1. Generate the mesh
blockMesh

# 2. Run the solver
<solverName>   # e.g., icoFoam, simpleFoam, pimpleFoam, solids4Foam

# 3. Post-process results
paraFoam

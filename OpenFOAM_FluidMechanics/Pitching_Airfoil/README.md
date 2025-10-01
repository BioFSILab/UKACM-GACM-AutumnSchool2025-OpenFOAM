# Pitching NACA0012 Airfoil (pimpleFoam)

## Problem Definition
This case simulates the unsteady aerodynamics of a **pitching NACA0012 airfoil**.  
- The airfoil undergoes sinusoidal pitching motion.  
- Two flow regimes are considered:
  - **Laminar flow**  
  - **Turbulent flow** using the **k-ω SST turbulence model**   
- The flow is assumed **incompressible, Newtonian**.  

---

## Solver Used
- **pimpleFoam** → Transient solver for incompressible, turbulent or laminar flows using the PIMPLE (PISO + SIMPLE) algorithm.  

---

## Case Variants
- `laminar/` → Laminar pitching simulation  
- `kOmegaSST/` → Turbulent pitching simulation with k-ω SST model  

---

## Steps to Run
From the respective case directory (`laminar/` or `kOmegaSST/`):

```bash
# 1. Generate the mesh
blockMesh

# 2. Decompose the domain for parallel execution (optional)
decomposePar -force

# 2. Run the transient solver in parallel ($np = number of processors)
mpirn -np $np pimpleFoam -parallel

# 3. Visualize results
paraFoam

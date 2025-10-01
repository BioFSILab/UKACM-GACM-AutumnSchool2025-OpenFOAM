# Lid-Driven Cavity Flow (icoFoam)

## Problem Definition
The lid-driven cavity flow is a classic CFD problem where a 2D square cavity is filled with fluid.  
- The **top wall (lid)** moves with a constant velocity in the x-direction.  
- All other walls are **stationary** with no-slip boundary conditions.  
- The case is solved as **incompressible, laminar, Newtonian flow**.  

---

## Solver Used
- **icoFoam** → Transient solver for incompressible, laminar flow of Newtonian fluids.  

---

## Steps to Run
From the case directory:

```bash
# 1. Generate the mesh
blockMesh

# 2. Run the solver
icoFoam


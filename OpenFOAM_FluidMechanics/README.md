# OpenFOAM Tutorials (v2412)

---

Within each case folder, the standard OpenFOAM directory structure is followed:

- `0/` – Initial and boundary conditions  
- `constant/` – Mesh and physical models (transport properties, turbulence, etc.)  
- `system/` – Solver settings, schemes, and controls

---

### Running a Case
From the case directory:

```bash
# 1. Generate the mesh
blockMesh

# 2. Run the solver
<solverName>   # e.g., icoFoam, simpleFoam, pimpleFoam, solids4Foam

# 3. Post-process results
paraFoam

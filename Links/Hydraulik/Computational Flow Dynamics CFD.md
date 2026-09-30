#hydraulik 
Depending on if you are working with gasses or liquids, you will have different experiences with pressure: Liquids are hardly compressible, gasses are HIGHLY compressible. This is also called numeric fluid dynamics (as opposed to experimental or theoretical).

Step by step:
Steps: 
* Setup problem and geometry, identify all dimensions and parameters 
* List all assumptions, approximations, simplifications and boundary conditions (BC) 
* Simplify partial differential equations (PDE) 
* Integrate equations 
* Apply initial conditions (IC) and BC to solve for constants of integration


Vores modeller er begrænset af kompleksitet af styrende differentialligninger
- Geometri, viskositet, fase ændringer, forbrænding
Og svære at opstille og løse styrende differentialligninger
- Empiri kan hjælpe her

CFD models include
- a description of the flow geometry,
- a set of coupled differential equations describing the physics and
- chemistry of the flow,
- boundary and initial conditions, and
- a structured mesh of points at which these equations are solved


The equations we are solving are Navier-stokes Equations (holy)
$$ \underbrace{ \frac{\partial u}{\partial t} }_{unsteady \, term} + \underbrace{ u \cdot \nabla u }_{ convective \, term } = \underbrace{ -\frac{\nabla p}{\rho} }_{ pressure \, term } + \underbrace{ \nu \nabla^2 u }_{ viscous \, term } $$
Assuming:
- Newtonian Fluid – Shear stress proportional to strain (constant viscosity)
- Incompressible flow – Constant density
- Isothermal flow – Constant temperature

And solving for
- Velocity field
- Pressure field

Step by step we:
- Build Geometry
- Create Grid
- Choose appropriate Physics
- Apply initial and boundary conditions
- Compute (choosing schemes and solving linear system of equations)
- Post-process
- Validate!
![[Pasted image 20260915134652.png]]


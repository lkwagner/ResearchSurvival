It's common for people to have trouble converging DFT calculations for correlated electron systems. 
A lot of times you have to try a few different tricks before one finally works.

## Checklist
 * Check your initial guess; does it make sense chemically?
 * Level shifting
 * Smearing
 * Converge minimal basis, then project to larger basis (easy in pyscf)
 * Vary solver (dependent on package; broyden, newton, different DIIS techniques, ...) 
 * Converge Hartree-Fock, then use as input to DFT
 * Increase number of k-points 
 * Remove approximate linear dependence if the basis overlap matrix has a large condition number 
 * Increase tolerances (TOLINTEG in CRYSTAL, direct_scf_tol in pyscf)

## Troubleshooting

| Symptom | Common causes | 
|---------|---------------|
|Initial energy large and fluctuates wildly | Initial guess is poor; try improving it or using smearing to get a better starting point | 
|Calculation almost converges but dE gets stuck at around 1e-5 | Tolerances can be too low, not enough k-points, damping is too large, approximate linear dependence, solver not performing well | 

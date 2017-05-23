It's common for students to have trouble converging DFT calculations for correlated electron systems. 
A lot of times you have to try a few different tricks for one to work. 

## Checklist
 * Check your initial guess; does it make sense chemically?
 * Level shifting
 * Smearing
 * Converge minimal basis, then project to larger basis (easy in pyscf)
 * Vary solver (dependent on package; broyden, newton, different DIIS techniques, ...) 
 * Converge Hartree-Fock, then use as input to DFT
 

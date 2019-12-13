# SW_potential_MoS2_lammps

Kaoru Hisama

LAMMPS implementation of the interatomic potential for Stillinger-Weber potential with cutoff r23.

original article for parameters : Ali Kandemir et al 2016 Nanotechnology 27 055703  / implementation: Rong Xiang et al.  arXiv:1807.06154.


LAMMPS version: lammps-16Mar18

For other versions, modification of pair_sw_TMD.cpp and pair_sw_tmd.h should be necessary.

## Usage

Build your lammps with pair_sw_TMD.cpp and pair_sw_tmd.h in your "src" directory of LAMMPS.

For execute simulations, add following expressions to your input file and MoS2.swtmd in your working directory.

```
pair_style	sw_tmd
pair_coeff	* * MoS2.swtmd Mo S C
```

Note: "C" in MoS2.swtmd also denotes Sulfur element as "S". The original article distinguishes them by their positions.
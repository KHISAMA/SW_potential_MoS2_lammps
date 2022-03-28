# SW_potential_MoS2_lammps

Kaoru Hisama

LAMMPS implementation of the interatomic potential for Stillinger-Weber potential with cutoff r23.

original article for parameters : Ali Kandemir et al. 2016 Nanotechnology 27 055703  
implementation: Rong Xiang et al.  arXiv:1807.06154. / Science 367, 537(2020).


LAMMPS version: lammps-29Sep2021 (latest) <- lammps-16Mar18 (original) 

For other versions, modification of pair_sw_TMD.cpp and pair_sw_tmd.h should be necessary.

The original version of the codes: pair_sw_TMD_16Mar18.cpp / pair_sw_tmd_16Mar18.h

## Usage

Build your lammps with pair_sw_TMD.cpp and pair_sw_tmd.h in your "src" directory of LAMMPS. (for CMake build, include them in some package directory, `src/MANYBODY` , for example.)

For execute simulations, add following expressions to your input file and MoS2.swtmd in your working directory.

```
pair_style	sw_tmd
pair_coeff	* * MoS2.swtmd Mo S C
```

Note: "C" in MoS2.swtmd also denotes Sulfur element as "S". The original article distinguishes them by their positions.
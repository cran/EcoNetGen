# EcoNetGen 0.2.4

* Removes stale references to fortran random_seed (package has used R's native 
  random number generation for fortran since v0.2.0, but code continued to 
  contain routine set set random_seed in the old fortran style. Thanks BDR
  for catching and reporting this.)

# EcoNetGen 0.2.3

* Patch a bug in fortran routine that could cause generated scalefree networks to have potentially larger average degree than targeted.
* Also address possible LTO issues in FORTRAN.

# EcoNetGen 0.2.2

* Avoid potential crashes from FORTRAN code by intercepting any
  invalid parameter combinations and returning a helpful error message.
  Please note, this changes the default parameter settings of `min_module_size`
  and `ave_degree`, which involved a potentially combination for scale-free
  and thus also some mixed-type networks.  
  
  
  
  

# EcoNetGen 0.2.1

* fix inappropriate default in `netgen_v1` routine, and add assertion to check argument lengths.

# EcoNetGen 0.2.0

* Add `netsampler()` routine

* Modify user interface for `netgen()` to provide more self-explanatory argument names. Note: the 
  old behaviour can be recovered for previous scripts you don't want to update manually by doing 
  `netgen <- EcoNetGen:::netgen_v1` after loading `EcoNetGen`.
  
* Ensure that FORTRAN correctly obeys `set.seed()` by always using the R random number generator. [#6](https://github.com/cboettig/EcoNetGen/issues/6)

# EcoNetGen 0.1.1 2018-04-10

* Initial release to CRAN

# EcoNetGen 0.1.0 2018-04-04

* Added a `NEWS.md` file to track changes to the package.




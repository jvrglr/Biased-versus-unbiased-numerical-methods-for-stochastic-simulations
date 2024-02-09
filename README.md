# Biased versus unbiased numerical methods for stochastic simulations: application to contagion processes

Python and FORTRAN codes used to generate plots in J. Aguilar, J.J. Ramasco, and R. Toral  "Biased versus unbiased numerical methods for stochastic simulations: application to contagion processes".

This collection of code is provided under an open-source license for free use and modification. If you find these codes useful in your research or project, we kindly request that you acknowledge the source by citing the following article:


Aguilar, J., Ramasco, J. J., & Toral, R. "Numerical methods for stochastic simulations: application to contagion processes. ."  2003, arXiv:2305.02902.

If you have any questions or improvements, feel free to reach out (jvrglrschz@gmail.com).

## Code list FORTRAN
FORTRAN 2008 is used in the examples dealing with meta-population systems (Section VI.B in our article). 

Compilation is achieved using the gfortran compiler:

```
gfortran  -o exe.x Random2.f90 dranxor.f90 ignbin.f  M_declarations.f90 M_functions.f90 M_subroutines_github.f90 main_compare_B_U.f90 
```

Once compiled, you can execute the program with:
```
time ./exe.x
```

1. **main_compare_B_U.f90** Reads network of contacts from an edge list file. Calls main functions and subroutines. 
2. **M_subroutines_github.f90** Contains binomial and Gillespie methods together with the program to generate dots in Fig. 6.
3. **M_declarations_github.f90** Declaration of public variables.
4. **M_functions_github.f90** Definition of public functions.
5. **dranxor.f90** Pseudo-random number generator, Toral, R., & Chakrabarti, A. (1993). Generation of Gaussian distributed random numbers by using a numerical inversion method. Computer physics communications, 74(3), 327-334. Provided by the author,  raul@ifisc.uib-csic.es.
6. **ignbin.f** Binomial generator. Dependent of dranxor.f90 for the generation of uniform samples. Extracted from: ranlib.f.tar.gz in https://www.netlib.org/random/.
7. **Random2.f90** Pseudo-random number generator. Extracted from : http://www.homepages.ucl.ac.uk/~ucakarc/work/software/randgen.f .



School of Computer Sciences, Universiti Sains Malaysia
======================================================
CCS524 Parallel Computing Architectures and Algorithms
------------------------------------------------------
Semester 1, 2015/2016
---------------------
Metaheuristic **Cuckoo Search** Algorithm on CUDA Architecture
------------------------------------------------------------
### Solving Traveling Salesman Problem:
* **Parallelization strategy:** Massively parallel by Cuckoo's random walk.
* Dataset: [TSPLIB] [1] (eil51, pr124, rat575, pr1002, fnl4461)

### Compile, run, clean and start over:

    $ make
    $ ./CUDA-CSTSP tsplib/fnl4461.tsp
    $ make clean

### Change the algorithm parameters, located in `CS.h` header file:

     #define MAX_GENERATION  10000    /* stop criterion: maximum generation of cuckoo with better fitness */
     #define N_NEST             80    /* population size: a fixed number of nests */
     #define PA               0.25    /* portion of bad solutions: cuckoo's egg probability discovered by host bird */
     #define RWALK_RSTEP         0    /* random_walk in random step */
     #define RWALK_MAX_ITER   1000    /* max iter before give up (RWALK_FITTER) */
     #define RWALK_FITTER        1    /* new random walk output need to be fitter */
     #define RWALK_NFITTER       0    /* need not fitter */
     
     #define DSIZE             768    /* dimension size */
     #define nTPB              768    /* n threads per block */



##### References
----------------
1. N. Bacanin. An object-oriented software implementation of a novel cuckoo search algorithm Faculty of Computer Science. Computing, pages 245–250.

1. R. Jovanovic, M. Tuba, and I. Brajevic. Parallelization of the cuckoo search using cuda architecture. In Proceedings of the 7th International Conference on Applied Mathematics, Simulation, Modelling, Recent Ad- vances in Mathematics, ASM13. WSEAS Press, 2013.

1. Azizah Mohamad, Azlan Mohd Zain, Nor Erne Nazira Bazin, and Amirmudin Udin. Cuckoo Search Algorithm for Optimization Problems - A Literature Review. Applied Mechanics and Materials, 421(September 2015):502–506, 2013.

1. A. Ouaarab, B. Ahiod, and X. S. Yang. Improved and discrete cuckoo search for solving the travelling salesman problem. In X. S. Yang, editor, Cuckoo Search and Firefly Algorithm, volume 516 of Studies in Com- putational Intelligence, pages 63–84. Springer International Publishing, 2014.

1. X.Ouyang,Y.Zhou,Q.Luo,andH.Chen.Anoveldiscretecuckoosearch algorithm for spherical traveling salesman problem. Applied Mathematics and Information Sciences, 7(2):777–784, 2013.

1. M. Subotic, M. Tuba, N. Bacanin, and D. Simian. Parallelized cuckoo search algorithm for unconstrained optimization. In Proceedings of the 5th WSEAS Congress on Applied Computing Conference, and Proceedings of the 1st International Conference on Biologically Inspired Computation, BICA’12, pages 151–156, Stevens Point, Wisconsin, USA, 2012. World Scientific and Engineering Academy and Society (WSEAS).

1. X. Xu, Z. Ji, F. Yuan, and X. Liu. A novel parallel approach of cuckoo search using mapreduce. In International Conference on Computer, Communications and Information Technology. Atlantis Press, January 2014.

1. X. S. Yang. Cuckoo search (cs) algorithm - file exchange - matlab central. http://www.mathworks.com/matlabcentral/fileexchange/ 29809-cuckoo-search-cs-algorithm, 2009. [Online; accessed 2015-10-5].

1. TSPLIB95 - http://www.iwr.uni-heidelberg.de/groups/comopt/software/TSPLIB95


[1]: http://www.iwr.uni-heidelberg.de/groups/comopt/software/TSPLIB95
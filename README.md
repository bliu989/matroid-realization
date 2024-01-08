# matroid-realization

This project uses code from the [Github repository](https://github.com/dcorey2814/matroidRealizationSpaces/tree/main) from Daniel Corey and Dante Luber used for the paper [Singular matroid realization spaces](https://arxiv.org/abs/2307.11915). The goal of this project is to classify the irreducibility of realization spaces, up to complex conjugation, of simple $(3,11)$-matroids with the 3 lines property. 

The Jupyter notebook `collect_polynomials.ipynb` is written in Julia and utilizes Daniel Corey's and Dante Luber's code to obtain the polynomials that can generate the ideals of the realization spaces of the matroids we are interested in. The calculated polynomials have been written to the directory `data`. The file `data/univariate_polys.txt` gives the polynomials that generate the ideals of the realization spaces of the matroids given [here](https://github.com/dcorey2814/matroidRealizationSpaces/tree/main/d3n11/data) in the file `univariate_ideal_3_11.dat` in the same order. Likewise, `data/multivariate_polys.txt` gives polynomials corresponding to the matroids given in `multivariate_principal_ideal_3_11.dat` of [this directory](https://github.com/dcorey2814/matroidRealizationSpaces/tree/main/d3n11/data). 

The files `data/univariate_polys.txt` and `data/multivariate_polys.txt` were then fed to `determine_poly_irreducibility.ipynb` and processed with SageMath. Out of the 16234 simple $(3,11)$-matroids with the 3 lines property, there are
- 4718 are not realizable over $\mathbb{C}$,
- 7745 with irreducible realization space and thus irreducible realization space up to complex conjugation,
- 870 with realization space that consists of two irreducible complex conjugate components and thus irreducible realization space up to complex conjugation, and
- 2901 with realization space that consists of at least two irreducible components up to complex conjugation and thus reducible realization space up to complex conjugation.

Out of the 2901 matroids with realization space that consists of at least two irreducible components up to complex conjugation, there are 42 where there are at least two components sharing a common point. Further analysis is needed to see if these realization spaces are connected.

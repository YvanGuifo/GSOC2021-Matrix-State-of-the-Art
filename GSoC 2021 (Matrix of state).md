# GSoC-2021 : Matrix State of the Art

I was selected for [GSoC 2021](https://summerofcode.withgoogle.com) under the organization
[Pharo Consortium](https://pharo.org) to work on the project, [Matrix State of the Art](https://summerofcode.withgoogle.com/dashboard/project/6196707039117312/details/).

# Brief description of the project

Today, many fields of computational sciences (Data Science, Data Visualization and even Machine Learning),
mathematics, engineering, geology and others make use of matrices. Usually described from tables,
it is a central tool used by many programming languages.

A tensor is a generalization of vectors and matrices and is easily understood as a multidimensional array.
In the PolyMath project (a Pharo project that implements numerous mathematical algorithms),
there is already a support for vectors (tensors with rank 1) and matrices (tensors with rank 2),
but not general multi-dimensional matrices (aka tensors).
The main objective of this project is to extend the existing PolyMath classes to support tensors and related operations.

# Implementations carried out

- Initially we carried out the implementations through the epidemiological simulation platform
 [Kendrick](https://github.com/UNU-Macau/kendrick). More specifically, we implemented operations and tests on rank 2 tensors:
   - [The link of operations implemented for rank 2 tensors](https://github.com/UNU-Macau/kendrick/blob/master/src/Kendrick/TensorRank2.class.st)
   - [The link of tests implemented for rank 2 tensors](https://github.com/UNU-Macau/kendrick/blob/master/src/Kendrick/TensorRank2Test.class.st)

- After this phase, it was necessary to generalize the operations to multi-dimensional matrices (aka tensors).
 But we especially wanted to be inspired by the development vision of [Polymath](https://github.com/PolyMathOrg/PolyMath)
 concerning the matrices. For this reason, we have redefined, refactor certain operations and generalize some of them.
   - Integration of the [`PMNDArray` class and the` PMNDArrayTest`](https://github.com/PolyMathOrg/PolyMath/pull/210)
    class in the `Math-Matrix` package of [Polymath](https://github.com/PolyMathOrg/PolyMath).
   - [Generalization of the hadamard product for matrices of dimension greater than 2](https://github.com/PolyMathOrg/PolyMath/pull/213).


# Additional work to be carried out

It would also be important to generalize operations such as outer product and the kronecker product for matrices
of dimension greater than 2



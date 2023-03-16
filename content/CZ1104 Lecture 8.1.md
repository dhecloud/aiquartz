---
---
- An [[Eigenvector]] of an $$n \times n$$ matrix $$A$$ is a non zero vector $$x$$ such that $$Ax=\lambda x$$ for some scalar $$\lambda$$. A scalar $$\lambda$$ is called an [[Eigenvalue]] of $$A$$ if there is a nontrivial solution $$x$$ of $$Ax = \lambda x$$; such an $$x$$ is called an [[Eigenvector]] corresponding to $$\lambda$$
- [[Eigenvalue]]s and [[Eigenvector]]s are only for square matrices. For rectangular matrices, [[Singular Values]] are defined
- Checking for [[Eigenvector]]s
- $$u$$ is an eigenvector if $$Au = \lambda u$$ where $$\lambda$$ is a real or complex number
- Checking for [[Eigenvalue]]s
    1. $$Ax = \lambda x$$
    2. $$Ax - \lambda x = 0$$
    3. $$(A - \lambda I)x = 0$$ has a non-trivial solution $$x$$ if and only if the [[Determinant]] of $$(A-\lambda I)$$ is 0. 
- [[Characteristic Equation]]: $$det(\lambda I - A) = 0$$
- [[Singular]] matrix
- [[Determinant]] is 0
- Dependent rows and columns
- [[Algebraic Multiplicity]] of [[Eigenvalue]]s
- The integer $$n_i$$ is the number of times an eigenvalue appears as a root of the characteristic polynomial
- [[Geometric Multiplicity]]
- Same as [[Nullity]] of $$(A - \lambda_i I)$$
- The set of solutions (eigenvalues) is called the [[Spectrum]] of matrix A
- [[Null Space (kernel)]] is the set of eigenvectors that satisfies the "[[Characteristic Equation]]: $$det(\lambda I - A) = 0$$"
- [[Nullity]] is the dimension of the [[Null Space]]
- The [[Eigen Space]] of $$A$$ is the set of [[Eigenvector]]s associated with each [[Eigenvalue]]
- [[Eigendecomposition]]]] is also known as [[Spectral Decomposition]]
- Factorize a matrix in terms of [[Eigenvalue]]s and [[Eigenvector]]s
- Only a [[Diagonalisable]] matrix can be factorized this way
- [[Algebraic Multiplicity]] equals [[Geometric Multiplicity]] 

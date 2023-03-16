---
---
- Two non zero vectors $$u$$ and $$v$$ are said to exhibit [[Orthogonality]] or to be perpendicular if $$u \cdot v =0$$
- By this definition, the zero vector in $$R^n$$ is [[Orthogonality|orthogonal]] to every vector in $$R^n$$
- $$\theta = \pi/2$$ if and only if $$u \cdot v = 0$$
- [[Point Normal Equations]]
- **line**: $$a(x - x_0) + b(y-y_0)=0$$
- if $$a$$ and $$b$$ are constants that are not both zero, then $$ax + by + c = 0$$
- **plane**: $$a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$$
- if $$a$$, $$b$$ and $$c$$ are constants that are not all zero, then $$ax + by + cz +d = 0$$
- [[Standard Basis]] for $$R^n$$
- Basically a one hot vector with only one '1' in each dimension
- [[Orthogonality|Orthogonal]] Projections
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2Fzl5OpokP0T.png?alt=media&token=573d8f01-7541-46b8-8b2c-2bdbee487358)if $$u$$ and $$a$$ are vectors in $$R^n$$, and if $$a \neq 0$$, then $$u$$ can be expressed in exactly one way in the form $$u = w_1 + w_2$$, where $$w_1$$ is a scalar multiple of $$a$$ and $$w_2$$ is [[Orthogonality|orthogonal]] to $$a$$
- $$w_1 = proj_au = \frac{u \cdot a}{\lVert a \rVert^2} a$$
- $$w_2 = u - proj_au = u- \frac{u \cdot a}{\lVert a \rVert^2} a$$
- $$\lVert proj_au \rVert = \frac{|u \cdot a|}{\lVert a \rVert} = \lVert u \rVert |\cos \theta|$$ 
- [[Pythagoras Theorem]] in $$R^n$$
- If $$u$$ and $$v$$ are [[Orthogonality|orthogonal]] vectors in $$R^n$$ with the Euclidean inner product, then $$\lVert u + v \rVert^2 = \lVert u \rVert^2 + \lVert v \rVert^2$$ 
- [[Orthogonality|Orthogonal]] Sets and [[Orthogonal Basis]]
    If $$S = {u_1, ... u_p}$$ is an [[Orthogonality|orthogonal]] set of nonzero vectors in $$R^n$$, then $$S$$ is linearly independent and hence is a basis for the subspace spanned by $$S$$
    An [[Orthogonal Basis]] for a subspace $$W$$ of $$R^n$$ is a basis for $$W$$ that is also an [[Orthogonality|orthogonal]] set
    The weights in the linear combination $$y = c_1u_1 + ... + c_pu_p$$, where $${u_1, ..., u_p}$$ is an [[Orthogonal Basis]], can be easily found by $$c_j = \frac{y \cdot u_j}{u_j \cdot u_j}$$
    An [[Orthonormal]] set is an [[Orthogonality|orthogonal]] set of unit vectors. ie an [[Orthogonality|orthogonal]] set which has a norm of 1
- [[Orthogonality|Orthogonal]] Matrix
- An $$m \times n$$ matrix $$U$$ has orthonormal columns if and only if $$U^TU = 1$$
- Implies that $$U^{-1} = U^T$$
- Properties
- **a**: $$\lVert Ux \rVert = \lVert x \rVert$$
- **b**: $$(Ux) \cdot (Uy) = x \cdot y$$
- **c**: $$(Ux) \cdot (Uy) = 0$$ if and only if $$x \cdot y = 0$$
- [[Orthogonality|Orthogonal]] Decomposition Theorem
- Any $$y$$ in $$R^n$$ can be written uniquely in the form $$y = \hat{y} + z$$  where $$\hat{y}$$ is in $$W$$ and $$z$$ is in $$W^⟂$$.
- if $$u_1, ... , u_p$$ is any [[Orthogonal Basis]] of $$W$$, then $$\hat{y} = \frac{y \cdot u_1}{u_1 \cdot u_1}u_1 + ... + \frac{y \cdot u_p}{u_p \cdot u_p}u_p $$
- [[Best Approximation Theorem]]
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FPaperReadings%2FIfI4lNFXGA.png?alt=media&token=c71f1ffa-138f-4db5-a76e-d0e0b5ecffcf)For any $$y$$ in $$R^n$$ and its [[Orthogonality|orthogonal]] projection $$\hat{y}$$, $$\hat{y}$$ is the closest point in $$W$$ to $$y$$, in the sense that $$\lVert y - \hat{y} \rVert < \lVert y - v \rVert$$ for all $$v$$
- The vector $$\hat{y}$$ is called the best approximation to y by the elements of W
- If $${u_1, ... , u_p}$$ is an orthonormal basis for a subspace $$W$$ of $$R^n$$, then
$$proj_wy = (y \cdot u_1)u_1 + (y \cdot u_2)u_2 + ... + (y \cdot u_p)u_p $$  if $$p < n $$

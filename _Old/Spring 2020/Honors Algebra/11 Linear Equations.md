# Linear Systems of Differential Equations (Chapter 3)

* $\mathbf{x}(t) \in C^1(\mathbb{R},\mathbb{R}^n)$
* $\mathbf{b}(t) \in C(\mathbb{R},\mathbb{R}^n)$
* $A(t) \in C(\mathbb{R},\text{Mat}_{n\times n}(\mathbb{R}))$
* A linear differential equation is
* $$\dot{\mathbf{x}}(t) = A(t)\mathbf{x}(t)+\mathbf{b}(t)$$
	* $\mathbf{x}(0)=\mathbf{x}_0$

### Homogeneous
* when $\mathbf{b}(t) = 0$, the equation is called homogenous 

### Constant Coefficients
* If $A(t)=A$ is constant, then it is an equation with constant coefficients

## Homogeneous Linear Systems of ODEs with Constant Coefficients
* Of the form 
* $$\frac{d}{dt}\mathbf{x}(t) = A\mathbf{x}(t)$$
	* $\mathbf{x}(0)=\mathbf{x}_0$

### Matrix Exponential
* the matrix exponential is 
* $$\frac{d}{dt}e^{tA} = Ae^{tA}$$
* To compute $e^{tA}$, find a Jordan normal form and Jordan canonical basis for $A$

### Solution
* the solution to homogenous linear ODE is
* $$\mathbf{x}(t) = e^{tA}\mathbf{x}_0$$
* or in Jordan Normal Form
* $$\mathbf{x}(t) = C^{-1}e^{tJ_A}C\mathbf{x}_0$$

### Behavior of Solution
* Behavior as $t\rightarrow +\infty$ is governed by the eigenvalues of $A$
* In more detail
* $$\mathbf{x}(t) = \sum_{i=1}^k \mathbf{x}_i(t)$$
	* where $k$ is the number of different eigenvalues $\lambda_i$
* and
* $$\mathbf{x}_i(t) =
\left\{\begin{matrix}
	\sum_{j=0}^{d_{i}-1}e^{\lambda_i t} t^i \mathbf{x}_{ij} & \text{if } \lambda_i \in \mathbb{R} \\ \\
	\sum_{j=0}^{d_{i-1}}e^{\mu t}(\cos(\nu t)\cdot\mathbf{x}_{ij} + \sin(\nu t)\cdot\mathbf{y}_{ij})t^j& \text{where } \lambda_j = \mu + i\nu \\
\end{matrix}\right.$$
	* where $d_i$ is the depth of $\lambda_i$
* Arranging the eigenvalues in descending order
* $$\mathbf{x}(t) 
= \mathbf{x}_1(t) + \cdots + \mathbf{x}_k(t) 
= e^{t\text{Re}(\lambda_1)}(P(t)+e^{lambda_2-\text{Re}(\lambda_1)})$$
* So if $\text{Re}(\lambda_1)< 0$, then every solution approaches $0$ as $t\rightarrow +\infty$
* If  $\text{Re}(\lambda_1) <= 0$ and for $\text{Re}(\lambda_1)=0$ there are no nontrivial Jordan blocks, then the solution is going to be bounded for all $t\geq 0$

#### Asymptotically Stable
* If $\lVert\mathbf{x}(t)\rVert \rightarrow 0$, the solution is called asymptotically stable

#### Stable
* If $\lVert\mathbf{x}(t)\rVert\leq 0$ for $t\geq 0$, the solution is called stable

## Theorem (Corollary 3.6)
* Every solution of an autonomous homogenous linear system of ODEs is asymptotically stable $\iff$ For every eigenvalue of $A$, its' real part is less than $0$

## Criterion
* To figure out if the solutions are asymptotically stable, need to investigate the characteristic polynomial of $A$
	* $$P_A(\lambda) = \det(\lambda\mathbb{I} - A)$$
* Construct the following new matrix
$$H=\begin{bmatrix}
p_{n-1} & 1 & 0 & 0 & 0 & \cdots & 0 \\
p_{n-3} & p_{n-2} & p_{n-1} & 1 & 0 & \cdots & 0\\
p_{n-5} & p_{n-4} & p_{n-3} & p_{n-2} & p_{n-1} & \cdots & 0\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots &\\
0 & 0 & 0 & \cdots & p_0 & p_1 & p_0 \\
0 & 0 & 0 & \cdots & 0 & 0 & p_0
\end{bmatrix}$$

## Routh Hurwitz Theorem
* $P_A(\lambda) = 0$ has all solutions with real part less than $0$ $\iff$ (positivity criterion)


## Higher Order Linear ODEs with constant coefficients
* Define 
* $$\mathbf{x} = \begin{bmatrix}y \\ y' \\ \vdots \\  y^{(n-1)}\end{bmatrix}$$
* $\frac{d}{dt}\mathbf{x}(t)$ is the companion matrix associated with the polynomial $p_A(\lambda)=a_0+a_{1}\lambda+\cdots+a_{n-1}\lambda^{n-1}+\lambda^n$
* then $e^{tA}$ will be an expression that contains for each real eigenvalue $\lambda$,
	* $$e^{\lambda_i t}, \cdots, t^{a_i - 1}e^{\lambda_i t}$$
		* where $a_i$ is the algebraic multiplicity of $\lambda_i$
* for each pair of complex conjugate eigenvaules, $\lambda_i = \mu_i + i \nu_i, \overline{\lambda_i} = \mu_i + i \nu_i$
	* $e^{\mu_i t}\cos(\nu_i t), te^{\mu_i t}\cos(\nu_i t), \cdots, t^{a_i - 1}e^{\mu_i t}\cos(\nu_i t)$
	* $e^{\mu_i t}\sin(\nu_i t), \cdots, t^{a_i - 1}e^{\mu_i t}\cos(\nu_i t)$
* Therefore the general solution to the $n$ th order equation is a linear combination of 
	* $$t^je^{\lambda_i t}, t^je^{\mu_i t}\cos(\nu_i t), t^je^{\nu_i t}\sin(\nu t)$$

## Solving Inhomogeneous Equations
* Trying to find solution to
$$\frac{d}{dt}\mathbf{x}(t) = A\mathbf{x}(t) + g(t)$$

### Duhamel's Formula
* The solution ends up as
$$\mathbf{x} = 
e^{tA}\mathbf{x}_0 + \int_0^t e^{(t-s)A}g(s)~ds$$
* Easier to solve when $\mathbf{b}(t) = p(t)e^{\beta t}$ 
	* where $p(t)$ is a vector polynomial
* (Just look in notes)

### General Solution
* A solution to $y(t)$ of the inhomogeneous equation looks like
* $$y(t) = y_{\text{hom}}(t) + \int_0^tu(t-s)g(s)~ds$$
	* where $y_{\text{hom}}$ is the general solution of the homogenous equation
	* $u$ is the special solution of the homogenous equation

### Special Case
* There's an easier way to solve when
* $$g(t) = \left\{\begin{matrix}
p \times e^{\beta} t \\
(p_1\sin(\beta t) + p_2\cos(\beta t))e^{\alpha t}
\end{matrix}\right.$$
	* where $p$ is a polynomial

#### In general
* Let $g(t)$ be the RHS of an $n$ th order linear ODE with constant coefficients
* If $$g(t) = p(t)e^{\beta t}$$
	* we look for a solution of the form 
	* $$y(t) = Q(t)e^{\beta t}$$
		* where the degree of $Q(t)$ is the sum of the degree of $P(t)$ and the multiplicity of $\beta$ as a root of the characteristic polynomial (which is zero if $\beta$ is not a root)
* Similarly if $$g(t) = e^{\alpha t}(P_1(t)\cos(\beta t) + P_2(t)\sin(\beta t))$$
	* then the solution of is of the form
	* $$y(t) = e^{\alpha t}(Q_1(t)\cos(\beta t)+Q_2(t)\sin(\beta t))$$
		* where the degree of $Q_1,Q_2$ is the sum of the maximum of the degrees of $P_1,P_2$ and the multiplicity of $\alpha\pm i \beta$ as a root of the characteristic polynomial


## General Linear Systems
* In the form $$\frac{d}{dt}\mathbf{x}(t) = A(t)\mathbf{x}(t) + \mathbf{b}(t)$$
* In a particular case, reduces to the general nth order linear equation
	* $$a_n(t)y^{(n)}+a_{n-1}(t)y^{(n-1)}+\cdots+a_0(t)y = g(t)$$

### Homogenous Case
* $$\frac{d}{dt}\mathbf{x}(t) = A(t)\mathbf{x}(t)$$
* need to study a matrix ODE
* $$\frac{d}{dt}X(t) = A(t)X(t)$$
	* $X(t_0) = X_0$
	* $X(t)$ is an $n\times n$ matrix
* Solution exists and is unique in some neighborhood of $t_0$
* If $X(t)$ is a solution and $C$ is a constant matrix, then $X(t)\cdot C$ is also a solution
* therefore if we know a solution $X(t)$ such that $X(t_0) = \mathbb{I}$, then we can find a solution with any initial data at $t_0$

### Principal Solution
* $X(t)$ called the principal solution and is denoted by $\Psi(t,t_0)$
* which is a matrix-valued function such that
* $$\frac{d}{dt}\Psi(t,t_0) = A(t)\Psi(t,t_0)$$
	* and $\Psi(t,t_0)=\mathbb{I}$

#### Superposition Principle
* $$Psi(t,t_1)\Psi(t_1,t_0) = \Psi(t,t_0)$$

#### Inverse
* $$\Psi^{-1}(t,t_0) = \Psi(t_0,t)$$

### Fundamental (System of) Solution
* more generally, if $$\frac{d}{dt}U(t) = A(t)U(t)$$
	* where $U(t_0) = C$
* then $U(t)$ is called a fundamental solution
* define $\varphi_1(t),\cdots,\varphi_n(t)$ as the columns of $U(t)$
* then $$\varphi_i(t) = U(t)e_i$$
* therefore $$\frac{d}{dt}\varphi_i(t) = A(t)\varphi_i(t)$$
* we call $\varphi_1,\cdots,\varphi_n$ a fundamental system of solutions
* therefore $$\Psi(t,t_0) = U(t)U^{-1}(t_0)$$

## Wronskian (Wronski Determinant)
* $$W(\varphi_1, \varphi_2,\cdots,\varphi_n) := \det U(t) = \det(\varphi_1(t),\cdots,\varphi_n(t))$$
* and from linearity of determinant, $\frac{d}{dt}W(t)$ is
	* $$\frac{d}{dt}W(\varphi_1, \varphi_2,\cdots,\varphi_n) = \sum_{i=1}^n \det(\varphi_1(t),\cdots,\frac{d}{dt}\varphi_i,\varphi_{i+1},\cdots,\varphi_n(t))$$
* Ends up that $W(\varphi_1, \varphi_2,\cdots,\varphi_n)$ is
	* $$W(\varphi_1(t), \varphi_2(t),\cdots,\varphi_n(t)) = W(\varphi_1(t_0), \varphi_2(t_0),\cdots,\varphi_n(t_0)) e^{\int_{t_0}^t\text{Tr}(A(s))~ds}$$
	
### Example (Vandermonde Determinant)
- $W(e^{\lambda_1t},e^{\lambda_2t},\cdots,e^{\lambda_nt})$ is the Vandermonde determinant

## Summary of General Solutions
### Homogenous Case
* must satisfy
	* $$\frac{d}{dt}\mathbf{x}(t)=A(t)\mathbf{x}(t)$$
	* $\mathbf{x}(t_0) = \mathbf{x_0}$
* so the solution is
	* $$\mathbf{x}(t)=\Psi(t,t_0)\mathbf{x_0}$$

### Inhomogenous Case
* must satisfy
	* $$\frac{d}{dt}\mathbf{x}(t)=A(t)\mathbf{x}(t)+\mathbf{b}(t)$$
	* $\mathbf{x}(t_0) = \mathbf{x_0}$
* so the solution is
	* $$\mathbf{x}(t) = \Psi(t,t_0)\mathbf{x}_0 +\int_{t_0}^t\Psi(t_0,s)\mathbf{b}(s)~ds$$


## Remark
* $\Psi(t,t_0)$ can rarely be found explicitly
* But with additional information, this task can be simplified 

### Reduction of Order
* Suppose we are given a solution $\varphi_1(t)$ of the homogenous equation
* Can then perform a change of variables for the general equation 
	* $$\frac{d}{dt}\mathbf{x}(t) = A(t)\mathbf{x}(t)$$
* by defining $\mathbf{y}(t)$ as 
	* $$\mathbf{x}(t) = [\varphi_1(t), \mathbf{e}_2,\cdots,\mathbf{e}_n]\mathbf{y}(t)$$
	* let that matrix be denoted by $C'(t)$
* then
	* $$\frac{d}{dt}\mathbf{x}=C'(t)\mathbf{y}+C(t)\frac{d}{dt}\mathbf{y}$$
* And so after some matrix subtraction and multiplication ends up that 
	* $$\frac{d}{dt}\mathbf{y} = C^{-1}(t)(A(t)C(t)-C'(t))\mathbf{y}$$
* which becomes
	* $$\frac{d}{dt}\mathbf{y} = 
	\begin{bmatrix}
	0 &  * \\
	0 &   \hat{A}
	\end{bmatrix}\mathbf{y}$$
		* where $\hat{A}$ is an $(n-1)\times(n-1)$ matrix
* Therefore ends up that
	* $$\frac{d}{dt}\mathbf{\hat{y}} = \hat{A}(t)\mathbf{\hat{y}}$$

### Application to higher order linear ODEs
* of the form $$y^{(n)}+a_{n-1}(t)y^{(n-1)}+\cdots+a_0(t)y = g(t)$$
 
## Variations of Parameters Formula
* should look this up


# Differential Equations
* (New Book: Ordinary Differential Equations and Dynamical Systems)
* Encountered in any situation where some quantity is described using instantaneous rate of change 

## Examples
### Modeling (Population growth)
* Simple Model
	* rate of change is proportional to current population $$\frac{dp(t)}{dt} = kp(t)$$
	* so $$p(t)=p_0e^{kt}$$
* Logistic Model
	* Taking into account scarcity of resources, $$\frac{dp(t)}{dt} = kp(t)-\nu p^2(t)$$
	* which is equivalent to $$\frac{dp(t)}{dt} = \nu p(t) \left(\frac{k}{\nu}-p(t)\right)$$

### Physics 
#### Newton's 2nd Law of Motion
* Since $$F = ma~~~~~F=-kx$$
* $$\ddot{x}+kx = 0$$

#### Laplace Operator
* $$\Delta f(x,y) = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2}$$
* Laplace Equations
	* $\Delta f = \lambda f$
		* for $x^2+y^2\leq R^2$
* Wave Equation (Linear)
	* $$\frac{\partial^2 u}{\partial t^2} = c^2\Delta u$$
* Nonlinear Wave Equations (Soliton Waves)
	* Korteveg-deVries Equation 
	* $$\frac{\partial u}{\partial t} + \frac{\partial^3 u}{\partial x^3}-6u\frac{\partial^2 u}{\partial x^2} = 0$$

### Geometry
* $$\frac{dy}{dt} = f(y)$$
	* Can determine a graph given a differential equation
* Differential equations help to define new classes of functions
	* exponentials, trigonometric functions can be defined as solutions to differential equations
	* Painléve Equations
		* Example 1 $$\frac{d^2y}{dt^2} = 6y^2 + t$$
		* Cannot be expressed by polynomial, exponential, trigonometric functions, etc.
		* Solutions are transcendental

## Classification of Differential Equations
### Ordinary Differential Equation (ODE)
* Equations of the form $$F(t,y,y^{1},\cdots,y^{k})=0$$
	* one independent function, a function, and its partial derivatives
### Partial Differential Equation (PDE)
* Equations of the form $$P(x,y,z,u(x,y,z))$$
	* Multiple independent variables, one function, and its partial derivatives
* Won't be covered

### Order
* The highest derivative Involved

### Linearity
* $F$ is linear if it is a multilinear function

### Systems of ODEs
* Systems of differential Equations

### Autonomous / Nonautonomous
* $F$ is autonomous if it does not explicitly depend on the independent variable $t$

## First Order ODE
* General formula is $$F(t,y,y')=0$$ where $y$ depends on $t$ and $F$ is differentiable in every variable
* To solve, find $y=y(t)$ where $y\in C^1(I)$, where $I$ is some interval, such that for all $t\in I$, $$F(t,y(t),y'(t)) = 0$$

### Initial Value Problem
* Find a solution such that at any $t=t_0$, $y(t_0)=y_0$

### Simpler version
* A simpler version of a first order ODE is $$y' = f(t,y)$$, where $f\in C(X\subset\mathbb{R}^2)$

## Classes of Explicitly Solvable 1st Order ODEs
### Equation Solvable in Quadratures
* If the equation is autonomous, $$y' = f(y)$$
* rewriting it $$\frac{dy}{dt} = f(y)$$
* so "technically", $$f^{-1}(y)dy = dt$$
* let $$\phi(y) \coloneqq \int \frac{dy}{f(y)} = t + C$$
* then $$\phi(y) = t + C$$
* So $$y(t) = \phi^{-1}(t+C)$$
* solving IVT, $$\phi(y_0) = t_0 + C \implies C = \phi(y_0)-t_0$$

### Separable Equations
* in the form $$y' = f(y)g(t)$$
* so $$\frac{dy}{f(y)} = g(t)~dt$$
* let $$F(y) = \int\frac{1}{f(y)}~dy,~~G(t) = \int g(t)~dt$$
* then $$F(y) = G(t) + C$$

### Homogeneous Equation
* In the form $$y' = f\left(\frac{y}{t}\right)$$
* Substitute $y(t) = tu(t)$, so $y' = u(t) + tu'(t)$
* so $$u'(t) = \frac{1}{t}\left(f(u) - u\right)$$

### Linear Equations
* In the form $$y'=a(t)y + b(t)$$
	* is linear in $y$
* Look for function is form $$y(t) = g(t)e^{\int_{t_0}^t a(s)~ds}$$
* ends up that $$y(t) = y_0e^{\int_{t_0}^t a(s)~ds} + \int_{t_0}^t b(s)e^{\int_{t_0}^sa(\tau)~d\tau}~ds$$

### Bernoulli Equation
* In the form $$y' = a(t)y + b(t)y^{\alpha},\alpha\neq 0,1$$
* Not linear
	* but can be reduced to known equations through substitution
* let $z=y^{1-\alpha}$
* then $$z' = (1-\alpha)y^{-\alpha}y' = \cdots = (1-\alpha)a(t)z+b(t)$$

### Exact Equation 
* In the form $$y' = \frac{g(t,y)}{h(t,y)}$$
* Exact if there exists $F(t,y) such that $$\frac{\partial F}{\partial y} = h(t,y)$$ and $$\frac{\partial F}{\partial t} = g(t,y)$$
* then $$dF = h~dy - g~dt$$

### Riccati Equation
* Of the form $$y' = a(t)y+b(t)y^2 + c$$
* Cannot always be solved
* but suppose we are given one solution, $\varphi(t)$
* define $z(t) = y(t)-\varphi(t)$
* so $$z'=(a+2\varphi b)z+bz^2$$
	* which is bernoulli 

## Existence and Uniqueness of Solutions of ODEs

### Higher Order ODE
* Can be reduced to first order systems of ODE
* let $$y^{(n)}=f(t,y,y',\cdots,y^{(n-1)})$$
* Define a vector-valued function $$\mathbf{x}=\mathbf{x}(t)=[x_1,\cdots,x_n]$$
* set $$x_i(t)=y^{(i-1)}(t)$$ then $$x_i'(t) = x_{i+1}(t)$$ 
* with $$x_n'(t) = f(t,x_1,\cdots,x_n)$$
	* called a $1$ st order system
* More generally, can consider differential equation of the first order of the form $$\mathbf{x}'=\mathbf{F}(t,\mathbf{x})$$
	* $\mathbf{x}\in C^1(\mathbb{R},\mathbb{R}^n)$
	* $\mathbf{F}=C(\mathbb{R}^{n+1},\mathbb{R}^n)$


### Picard-Lindelöf Theorem
* $U\subset\mathbb{R}^{n+1}$ open
* If $\mathbf{F}\in C(U,\mathbb{R}^n)$
* and if $\mathbf{F}$ is locally Lipschitz continuous w.r.t. the second argument 
* and uniformly w.r.t. the first argument
* then there exists a unique local solution $$\mathbf{\tilde{x}}(t)\in C^1(I,\mathbb{R}^n)$$ where $I$ contains the initial point $t_0$
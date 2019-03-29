# Chapter 7: Conservative Forces

## Conservative Force
- Value of work does not depend on path, only depends on final and initial value

$$W_{ab}=\int_a^b\vec{F}~d\vec{s}$$

### Examples
* Gravitational Force
* Force from Work
* Spring Force

## Potential Energy ($U$)

Where potential energy is defined being $0$ is arbitrary

All that matters is $\Delta U$

$$\Delta U =-W_{ab}$$

Where $W_{ab}$ is the work from conservative force from point $a$ to $b$

$$\Delta U_g=mg\Delta{h}$$

## Total Mechanical Energy
$$E_T = KE + U$$

$$\Delta(E_t) = \Delta KE + \Delta U$$
$$\Delta(E_t) = W_c - W_c$$
$$\Delta(E_t) = 0$$

## Conservation of Energy
* Total energy for an **Isolated** (no external forces acting on system) System with conservative forces is constant

## Potential Energy in Springs
$$\Delta U = \frac{1}{2}k(x_f^2-x_i^2)$$
$$U(s)=\frac{1}{2}kx^2$$

## Non-Conservative Forces
$$(E_T)_f=(E_T)_i+W_{nc}$$
$$KE_f+U_f=KE_i+U_i+W_{nc}$$

$W_{nc}$ describes flow of energy into or out of system

$$\Delta KE + \Delta U - W_{nc} = 0$$

## Potential Energy and Energy Conversion 
$$\Delta U_g = -W_g$$
### Potential Energy and Force
$$F = -\frac{\delta U}{\delta y}$$ 

$$\vec{F} = -\nabla U=\begin{pmatrix}U_x' \\ U_y' \\ U_z'\end{pmatrix}$$

### Stable Equilibrium
$$\frac{\delta^2 U}{\delta^2 y}>0$$ 
$$F\propto -x$$
### Unstable Equilibrium
$$\frac{\delta^2 U}{\delta^2 y}=0$$ 
$$F\propto x$$

# Chapter 8: Momentum, Impulse, and Collisions

## Momentum ($p$)
$$\vec{p}=mv$$

### Impulse ($\vec{I}$)
* Change in momentum
* Time derivative of impulse is force
	$$\int_{t_i}^{t_f}\vec{F}~dt=\Delta \vec{p} = \vec{I}$$
* When $F$ is constant
	$$I=Ft$$
	
## Isolated Systems
No external forces, energy is conserved, momentum is constant
$$p_{sys}=\sum p_i$$
$$\frac{dp_{sys}}{dt}=0$$

## Collisions
### Inelastic
* Momentum is conserved
	* $$m_1u_{1}+m_2u_{2}=m_1v_{1}+m_2v_{2}$$
* Kinetic Energy is not conserved
* 
* **Perfectly Inelastic**
	* Colliding bodies stick together

### Elastic
* Bounce off each other
* Momentum and Kinetic Energy are conserved
	* $$m_1u_{1}+m_2u_{2}=m_1v_{1}+m_2v_{2}$$
	* $$\frac{1}{2}m_1u_{1}^2+\frac{1}{2}m_2u_{2}^2=\frac{1}{2}m_1v_{1}^2+\frac{1}{2}m_2v_{2}^2$$

#### Shortcut (1D collisions)
$$v_{1i}+v_{1f}=v_{2i}+v_{2f}$$

#### General Form of Shortcut
$$e=\frac{v_{1f}-v_{2f}}{v_{1i}-v_{2i}}$$

$$e=\left\{\begin{matrix} 1 & \text{ if elastic} \\ 0\leq e < 1 &\text{ if inelastic} \\ 0 &\text{ if perfectly inelastic}\end{matrix}\right.$$ 

## Center of Mass ($x_{cm}$)
Consider masses $m_i$ a distance $x_i$ from the origin
	$$x_{cm}=\frac{\sum{m_ix_i}}{\sum{m_i}}$$
Let $M=\sum{m_i}$
	$$P_{sys}=MV_{cm}$$
Meaning, derivative of $Mx_{cm}$ is momentum of system, and double derivative is sum of external 

# Chapter 9: Rotational Motion
## Rotational Analogues to Linear
$x \rightarrow \theta$
$v \rightarrow \omega$
$a \rightarrow \alpha$
## Kinematic Equations
$$\omega = \omega + \alpha t$$
$$\theta = \theta_0 + \omega_0t + \frac{1}{2}\alpha t^2$$
$$\omega^2 = \omega_0^2 + 2\alpha\Delta\theta$$

## Right Hand Rule ($\omega$)
Direction of $\omega$ is direction of thumb
# Chapter 1: Units, Physical Quantities, and Vectors

--------------------------------------------

## Dimensional Analysis
* Units
	* SI Base Units
		* length (metres/$m$), mass (kilogram/$kg$), time (second/$s$)
	* Derived units
		* like Joules ($kg\,m^2\,s^{-2}$)
* Important to keep track of units while doing calculations

# Chapter 2: Motion along a Straight Line

----------------------------------

## Kinematics

### Coordinate Systems and Reference Frames
* Any origin is acceptable
* If an object is moving in a straight line it can be described as one-dimensional motion
* ![](/1dMotion.JPG)

### Definitions
#### Position
* $\pm x_i$
* 
* **Displacement**
	 $$\Delta x = x_f-x_i$$
	* vector
	* does not depend on origin
* **Three-dimensional**
	$$\vec{r} = x\hat{\imath} + y\hat{\jmath} + z\hat{k} = \begin{pmatrix} x \\  y \\  z \end{pmatrix}$$

#### Velocity
* **Average Velocity**
	 $$v_{ave} = \frac{\Delta x}{\Delta t}$$
* **Instantaneous Velocity**
	$$v_{inst} = \frac{dx}{dt}$$

#### Acceleration
* **Average Accleration**
	 $$a_{ave} = \frac{\Delta v}{\Delta t}$$
* **Instantaneous Velocity**
	$$a_{inst} = \frac{dv}{dt}=\frac{d^2x}{dt^2}$$
	
### Kinematic Equations (constant acceleration)
#### Velocity (No Displacement)
$$v(t) = v_i+at$$

####  Displacement (No Final Velocity)
$$x(t)=x_i+v_it+\frac{1}{2}at^2$$

####  No Time
$$\Delta x = \frac{v_f^2-v_i^2}{2a}$$
$$v_f^2=v_i^2+2a(x_f-x_i)$$

### 4th Kinematic Equation
* $\Delta x = v_{ave}\Delta t$
* for constant $a$, $v_{ave}=\frac{1}{2}(v_i+v_f)$
* $\Delta x=\frac{1}{2}(v_i+v_f)\Delta t$

#### If $a$ not constant
$$a\,dt=dv$$
$$\int_{t_i}^{t_f}a\,dt=v(t)-v_i$$

### Helpful Hints for Kinematics
* **<u>Time</u>** is the key to kinematics:
	- the independent variable
	- horizontal axis for motion graphs
* **For problem solving:**
	- you can always refer everything back to the time which it happens
	- Simultaneous events occur at the same time
	- multiple objects must be referenced to the same coordinate system
	- Things that collide --- same position at same time

# Chapter 3: Motion In Two or Three Dimensions 

----------------------------------------
## Vectors
* $A_x=|\vec{A}|\cos\theta$
* $A_y=|\vec{A}|\sin\theta$
* $\vec{A}=\begin{pmatrix}A_x \\ A_y\end{pmatrix}$
* $|\vec{A}|=\sqrt{A_x^2+A_y^2}$

## Position
$$\vec{r}=\begin{pmatrix}x\\y\\z\end{pmatrix}=x\hat{\imath}=y\hat{\jmath}+z\hat{k}$$

### Distance
$$|\hat{r}|=\sqrt{x^2+y^2+z^2}$$

### Displacement 
$$∆ r=r_f-r_i=\begin{pmatrix}x_f-x_i \\ y_f-y_i \\ z_f-z_i\end{pmatrix}$$

## Velocity 
$$\vec{v}_{ave}=\frac{∆\vec{r}}{\Delta t}=\frac{1}{t}\begin{pmatrix}x\\y\\z\end{pmatrix},\vec{v}||\vec{r}$$
$$\vec{v}_{inst}=\begin{pmatrix}v_x\\v_y\\v_z\end{pmatrix}=\begin{pmatrix}\frac{dx}{dt}\\\frac{dy}{dt}\\\frac{dz}{dt}\end{pmatrix}$$

## Acceleration
$$\vec{a}=\begin{pmatrix}a_x\\a_y\\a_z\end{pmatrix}=\begin{pmatrix}\frac{dv_x}{dt}\\\frac{dv_y}{dt}\\\frac{dv_z}{dt}\end{pmatrix}$$

## Kinematic Equations (3D Motion)
### Velocity (Vector)
$$\vec{v}(t) = \vec{v}_i+\vec{a}t$$

####  Displacement (Vector)
$$\vec{r}(t)=\vec{r}_i+
\vec{v}_it+\frac{1}{2}\vec{a}t^2$$

####  Scalar
$$|\vec{v}_f|^2=|\vec{v}_i|^2+2(\vec{a}\cdot \Delta\vec{r})$$

## Projectile Motion
![](/projectileMotion.png)

### Max Height
$$t_{max}=\frac{v_0\sin\theta}{g}$$
$$h_{max}=\frac{v_0^2\sin^2\theta}{2g}$$

### Time to reach ground
$$t=\sqrt{\frac{2h}{g}}$$
ff

## Uniform Circular Motion
![](/ucm.jpg)

### Constants
radius, and magnitude of velocity

### Displacement
$$x=|\vec{r}|\cos\theta,y=|\vec{r}|\sin\theta$$

### Arc Length ($s$)
$$s=r\theta$$

### Angular Frequency ($\omega$)
$$v = r\omega$$
$$\omega = \frac{d\theta}{dt}$$

### Period ($T$)
$$T=\frac{2\pi}{\omega}$$

### Frequency ($f$ in Hz)
$$f=\frac{1}{T}$$

### Centripetal Acceleration ($a_c$)
$$a_c=\frac{v^2}{r}=\frac{4\pi^2R}{T^2}$$

## Non-Uniform Circular Motion
### Angular Acceleration ($\alpha$)

#### Radial Acceleration ($a_r$)
Acceleration towards center

#### Tangential Acceleration ($a_t$)
When zero, radial acceleration is zero

#### Total Acceleration ($a_t$)
$$\vec{a}_t=\vec{a}_r+\vec{a}_t=r\alpha$$
$$\vec{a} = \sqrt{a_r^2+a_t^2}$$

## Relative Velocities
$$\vec{r}_{P/A} = \vec{r}_{P/B}+\vec{r}_{B/A}$$
$$\vec{v}_{P/A} = \vec{v}_{P/B} + \vec{v}_{B/A}$$
$$\vec{a}_{P/A} = \vec{a}_{P/B} + \vec{a}_{B/A}$$

### Inertial Reference Frames
Constant acceleration

$$v_{A/B}=-v_{B/A}$$
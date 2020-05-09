# 31: Alternating Current

## Root Mean Square Value
* Take the Root of the Mean of the Squares
* Average of $g(x)$ is 
	* $$f\int^T_0 g(x)~dx$$
	* where $f$ is frequency

### Current
* $$I_{rms}=\frac{I}{\sqrt{2}}$$
### Voltage
* $$V_{rms}=\frac{V}{\sqrt{2}}$$

## Resistance and Reactance
### Inductive Reactance (Basically Resistance)
* $$X_L=\omega L$$
* $$V_L=IX_L$$

### Capacitive Reactance
* $$X_C=\frac{1}{\omega C}$$
* $$V_C=IX_C$$

### Impedance (Still like a resistance) and Phase Angle
* $$Z=\sqrt{R^2+\left(\omega L-\frac{1}{\omega C}\right)^2}$$
* $$\tan\phi = \frac{\omega L - \frac{1}{\omega C}}{R}$$

## Power in Alternating Current
### Resistor 
* $$P_{av}=\frac{1}{2}VI=V_{rms}I_{rms}=I_{rms}^2R$$

### Power in Inductor
* Average Power is $0$
* Net energy transfer is $0$

### Power in Capacitor
* Average Power is $0$
* Net energy transfer is $0$

### Average Power in General AC Circuit
* $$P_{av}=V_{rms}I_{rms}\cos\phi$$

## Resonance in AC Circuit
### Resonant Frequency
* $$\omega_0 = \frac{1}{\sqrt{LC}}$$
* Since $$I_{max}=\frac{V_{max}}{Z}$$
	* if $\omega=\omega_0$, then $Z=R$ and $I$ is maximized

## Transformers
* Has to be AC
* Two coils together to change voltage
* $V_1,N_1$ is primary coil
* $V_2,N_2$ is secondary coil
* $$\frac{V_2}{V_1}=\frac{N_2}{N_1}$$

### Step Down
* $V_2 < V_1$ so $N_2< N_1$

### Step Up
* $V_2 > V_1$ so $N_2 > N_1$

### Power (Ideal Transformer)
* $$V_1I_1=V_2I_2$$
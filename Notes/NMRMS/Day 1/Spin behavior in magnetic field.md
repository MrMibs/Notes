![[Spin angular momentum P#Spin angular momentum P]]

This has a related magnetic moment which is a vector connecting magnetic south and north with direction from south to north.
![[Gyromagnetic ratio (γ)#Gyromagnetic ratio (γ)]]

Nuclei are small magnets, which orient randomly. External magnetic fields align them. However energy is quantized. 

![[Dipole energy in magnetic field (E)#Dipole energy in external magnetic field]]

Since [[Magnetic moment (μ)]] is given as a constant for each nucleus, [[Magnetic field strength (B)]] is variable as we like. Thereby, to make sure energy ([[Dipole energy in magnetic field (E)]]) is quantized, the angle has to be constrained.

These angles are described as so
![[Pasted image 20260524122310.png|271]]

With $\mu$ being split in a Z component $\mu_z$ and an x-y component $\mu_{xy}$. In the Z direction, $P_z$ and $\mu_z$ can be found as:
$$P_z = m \cdot \hbar \quad \text{and} \quad \vec{\mu}_z = m \cdot \gamma \cdot \hbar$$
where:
- (m) is the [[Magnetic quantum number (m)]]
- ($\hbar = \frac{h}{2\pi})$ is the reduced Planck constant
- ($\gamma$) is the [[Gyromagnetic ratio (γ)]]

If we are looking in a specific direction (z) we drop vectorial quantities:

![[Dipole energy in magnetic field (E)#Dipole energy in external magnetic field along z-axis]]

Thereby
1: $E \propto B$ and 2: $E \propto \gamma$
1 The stronger the magnetic field, the more energy involved in changing a magnetic moment
2 The stronger the magnet, the more energy you need to orient it in an unfavorable way

Convention states positive [[Magnetic quantum number (m)]] values means the magnet is oriented favorably.
![[Pasted image 20260524130410.png]]
We call these $\alpha$ and $\beta$ based on if they are parallel or antiparallel. The ratio of these can be calculated using Boltzmann distribution.
$$\frac{N_\beta}{N_\alpha}=e^{-\frac{\Delta E}{k\cdot T}}$$
where:
- $N_a$ is amount of nuclei in $\alpha$ state
- $N_\beta$ is amount of nuclei in $\beta$ state
- e is exponential e
- $\Delta E$ is [[Dipole energy in magnetic field (E)]] difference
- k is Boltzmann constant
- T is temperature
## Boltzmann distribution of spin-up and spin-down states
This gives a few possible situations:
$$1. \; \Delta E \gg k \cdot T \rightarrow \frac{N_\beta}{N_\alpha}=\text{small value} \quad \text{or} \quad 2.\; \Delta E \ll k \cdot T \rightarrow \frac{N_\beta}{N_\alpha}=\text{1}$$
As $e^0 = 1$. Situation 2 is what is seen in NMR.

##
These situations are seen in spectroscopic methods! Situation 1: UV, Situation 2: NMR. e.g. for AAU NMR on 1H atom.
![[Dipole energy in magnetic field (E)#$ Delta E$ equation]]
Even for a mol, this is less than 0.01 joule pr mol. We need to excite that system! This is done using electromagnetic radiation with the energy needed to match our system. 

$$E = h \cdot \nu$$
$$E = \gamma \cdot \hbar \cdot B$$	$$v = \gamma \cdot B \cdot \frac{1}{2 \pi}$$
$$v = 6 \cdot 10^8 \, Hz = 600\, MHz$$
Waves at this scale are radio waves, low energy waves for low energy differences :)
Building on
![[Chemical shift evolution]]

Assume we have 2 [[Scalar-coupling]] nuclei (I,S), we can use the equation from chemical shift evolution, expanding the angular frequency

We have
###### Eq 2 for x
$$I_x \xrightarrow {\tau} \underbrace{I_x \cdot cos(\pi \cdot J \cdot \tau)}_{in-phase}+\underbrace{2S_z\cdot I_y\cdot  sin(\pi \cdot J\cdot \tau)}_{anti-phase}$$
###### Eq 2 for y
$$I_y \xrightarrow {\tau} \underbrace{I_y \cdot cos(\pi \cdot J \cdot \tau)}_{in-phase}-\underbrace{2S_z\cdot I_x\cdot  sin(\pi \cdot J\cdot \tau)}_{anti-phase}$$
######
where:
- J is [[Coupling constant (J)]] \[Hz]
- I is orientation of magnetization for nuclus I
- $\tau$ is time 
- $S_z$ is magnetization depending on spin state, either -1/2 or 1/2 and eq is multiplied by 2 for normalization. (Actually it is a superposition so both are there)

Hereby we have x-magnetization amount $\pm$ (depending on S) I_y magnetization amount.

![[Pasted image 20260526133805.png]]
The second part means they are dependant on eachother, as Iy always moves opposite direction of coupled partner Sz. The first peak is the positive effect of Sz the other is the negative (of course, as coupling works by affecting spin of adjacent carbons). 

When measuring a signal, we then get a peak that is in-phase with the rest of the response from the sample and one that is anti-phase compared to the rest of the sample.

How to add precession AND coupling
![[Chemical shift evolution#Eq 1]]
and insert the coupling effect on Ix from
![[Describing scalar coupling#Eq 2 for x]]
and
![[Describing scalar coupling#Eq 2 for y]]

ADDING PRECESSION AND COUPLING HAPPENS SEQUENTIALLY IN ANY ORDER e.g. for I, S
###### Precession coupling
$$I_x \xrightarrow {\omega\tau} I_x\cdot cos(\omega\cdot\tau)+I_y\cdot sin(\omega\cdot\tau) \xrightarrow {\pi J\tau}$$
$$cos(\omega\tau)\cdot[I_x\cdot cos(\pi \cdot J_{I,S} \cdot \tau) + 2 \cdot I_y \cdot S_z \cdot sin(\pi\cdot J_{I,S}\cdot\tau)] +$$
$$sin(\omega\tau)\cdot[I_y\cdot cos(\pi \cdot J \cdot \tau) - 2 \cdot I_x \cdot S_z \cdot sin(\pi\cdot J\cdot\tau)]$$
######
To build on this with an extra coupling we need some definitions to make it easier
$$A=cos(\omega\tau)cos(\pi J_{I,S} \,\tau)$$
$$B=sin(\omega\tau)cos(\pi J_{I,S} \,\tau)$$
$$C=cos(\omega\tau)sin(\pi J_{I,S} \,\tau)$$
$$D=sin(\omega\tau)sin(\pi J_{I,S}\, \tau)$$
$$c=cos(\pi J_{S,T}\,\tau)$$
$$s=sin(\pi J_{S,T} \,\tau)$$
Note: $cos(\omega\tau)$ describes how much of the original x-component remains after chemical shift rotation and $sin(\pi J_{I,S}\, \tau)$ describes how much remains unconverted by coupling.

Adding this to our previous notation (excluding the last 2) we get
$$I_x\cdot A  +  2S_zI_y \cdot C  +  I_y \cdot B  -  2S_zI_x \cdot D $$
Now to add more coupling, single terms become (signs caused by rotation in x-y plane direction shown on first image on site)
$$I_x \rightarrow I_x\cdot c+2S_z\cdot I_y \cdot s$$
$$I_y \rightarrow I_y\cdot c-2S_z\cdot I_x \cdot s$$
Correlated terms become
$$2S_zI_y \rightarrow 2S_z(I_y\cdot c-2S_z\cdot I_x \cdot s)$$
Here we can do a neat trick, as $S_z$ only tells us the direction of the spin, squaring it removes any useful information and just makes it a scaling factor of 1/4, which cancels 4.
$$2S_zI_y \rightarrow 2S_z \cdot I_y\cdot c- 4S_z^2\cdot I_x \cdot s$$
$$\rightarrow 2S_z \cdot I_y\cdot c- I_x \cdot s$$
For 2$S_z I_x$
$$2S_zI_x \rightarrow 2S_z \cdot I_x\cdot c+ 4S_z^2\cdot I_y \cdot s$$
$$\rightarrow 2S_z \cdot I_x\cdot c + I_y \cdot s$$
Finally

###### precession coupling x2
$$(I_x\cdot c+2S_z\cdot I_y \cdot s)\cdot A  +  (2S_z \cdot I_y\cdot c- I_x \cdot s) \cdot C  +  (I_y\cdot c-2S_z\cdot I_x \cdot s) \cdot B  -  (2S_z \cdot I_x\cdot c + I_y \cdot s) \cdot D $$
where:
- $\tau$ is time
- $\omega$ is angular precession frequency of a spin due to its chemical shift
- J is [[Coupling constant (J)]]
- $A=cos(\omega\tau)cos(\pi J_{I,S} \,\tau)$
- $B=sin(\omega\tau)cos(\pi J_{I,S} \,\tau)$
- $C=cos(\omega\tau)sin(\pi J_{I,S} \,\tau)$
- $D=sin(\omega\tau)sin(\pi J_{I,S}\, \tau)$
- $c=cos(\pi J_{S,T}\,\tau)$
- $s=sin(\pi J_{S,T} \,\tau)$















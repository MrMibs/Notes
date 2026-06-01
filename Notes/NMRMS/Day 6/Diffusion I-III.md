#nmrms
# Basics and Pulse Sequences
Gradients work really well if solutions don't diffuse.
![[Pasted image 20260528181457.png]]
This can be used to measure diffusion using e.g. the [[The Spin-Echo sequence - Refocusing sequence]].


![[Pasted image 20260528182028.png|697]]
We dont like magnetization in the x-y plane during diffusion. It is the same as above, but we split the 180 degree pulse into 2.
![[Pasted image 20260528182147.png]]

To find diffusion we can use the Stejskal-Tanner equation:
###### Stejskal-Tanner equation
$$I=I_0\cdot exp(\frac{-2\tau}{T_2}-\frac{T}{T_1}-(\gamma \, \delta \, G)^2 \cdot D \cdot (\Delta-\frac{\delta}{3}))$$
where:
- $I_0$ is
- $\tau$ is time
- $T$ is time between central 90$\degree$ pulses
- $T_1$ is [[T1-relaxation]] time
- $T_2$ is [[T2-relaxation]] time
- $\gamma$ is [[Gyromagnetic ratio (γ)]]
- $\delta$ is length of gradient pulse
- $G$ is strength of gradient pulse
- $D$ is the diffusion coefficient
- $\Delta$ is the diffusion delay
######

Gradient pulses introduce eddy-currents as they are switched on and off very abruptly which generates magnetic fields in your sample.
![[Pasted image 20260528182528.png]]
Eddy-currents can be further prevented by splitting your gradient into half.
![[Pasted image 20260528182650.png]]
This works really well
![[Pasted image 20260528182748.png]]
Convection i.e. heat differences also exists and changes diffusion. These occur as samples are heated from below. To prevent it we use this sequence:
![[Pasted image 20260528182929.png]]
As we split the sequence into 2 and combine the middle part.

# How to determine diffusion constants
Say we now have this fancy equation
![[Diffusion I-III#Stejskal-Tanner equation]]
Say we have [[The Spin-Echo sequence - Refocusing sequence]] experiment. First thought is to vary $\Delta$ and $\tau$.
![[Pasted image 20260528184005.png]]
As we know $\gamma$, $\delta$ and G, we only need $T_2$ but that is annoying. We have a better way! Same experiment, but instead of varying diffusion delay, we vary gradient strength G.
![[Pasted image 20260528191128.png]]
Easily derived. Again, we know $\gamma$, $\delta$ and G as well as $\Delta$ now that we dont vary it. That means our regression results in our D value! :)

Green is faster diffusion, red is slower diffusion.

It looks like this.
![[Pasted image 20260528191215.png]]

Also the bigger the molecule the slower it is (at least here).

# DOSY and some applications
You can do an inverse laplace transform which will result in something that looks like a 2d spectrum but isn't (its a DOSY)
![[Pasted image 20260528191348.png]]Suddenly your NMR sample is ordered by diffusion constants. This is really cool!
![[Pasted image 20260528191542.png]]
Say you have your cyclodextrin, they increase viscosity which is inversely proportional to diffusion, so we correct for that. Even then, we can see the diffusion of our guest molecule is lower as we bind it to the non-moving big molecule.
![[Pasted image 20260528191832.png]]
Further, studying a big molecule like this protein, we can see some things move even though they are a part of the protein. This is due to exchange, as some atoms are able to get of the protein temporarily and then back in the protein. This allows us to calculate fraction of time in water and in protein to get exchange rate and secondary structure stability.
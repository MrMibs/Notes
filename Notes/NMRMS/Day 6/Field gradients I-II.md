#nmrms
This is based on no [[Diffusion I-III]]

A magnetic field gradient is a linearly inhomogeneous magnetic field. This is useful as you can edit what you observe. A magnetic field gradient is described as:
$$B(z)=B_0+G\cdot z$$
where:
- z is position
- g is gradient strength \[T/m] (sometimes in \[gauss/cm], high resolution get up to 60 gauss/cm)
![[Pasted image 20260527163903.png]]

In an NMR tube, after a 90 degree pulse, you have a ton of vectors precessing at different frequencies and you induce a phase difference. It is found as $$\Phi(x)=\underbrace{G(z) \cdot \tau}_{chosable} \cdot \underbrace{\omega}_{given \, pr \, nucleus}$$
where:
- $\Phi(x)$ is phase difference
- $G(z)$ is field strength depending on sample position
- $\tau$ is time
- $\omega$ is precession frequency or [[Larmor frequency (ν)]] for each nucleus
So double time with half field strength is the same as at a given field strength and time.
![[Pasted image 20260527164250.png]]
Phase difference also depends on nucleus as seen in the equation above, with $\omega$ varying for each nucleus, meaning you can create a phase difference between H and C. As long as all magnetization vectors are aligned you get a signal. This is called **dephasing**.
![[Pasted image 20260527165016.png]]
To undo the gradient, you can just undo the gradient by using same time but opposite sign (mirror the red line). Gradients are shown like:
![[Pasted image 20260527165239.png]]

You always need gradients to equal 0
$$\sum_iG_i\tau_i\gamma_ip_i=0$$
where
- $G(z)$ is field strength depending on sample position
- $\tau$ is time
- $\gamma$ is [[Gyromagnetic ratio (γ)]]
- p is coherence order
Coherence order is illustrated below:
![[Pasted image 20260527165815.png]]
Here coherence order would go from 1 to -1 when you invert the signal. Thereby you get a signal from this pulse sequence. This is really useful for e.g. [[WATERGATE sequence]]
![[Pasted image 20260527170044.png]]
Water signal is normally 100000x the signal of the sample you are interested in, however atoms with the same chemical shift as water also disappear.

Another application is coherence pathway selection. E.g. in this 2QF-COSY and NOESY spectrum we need to be able to distinguish these peaks and only show one.
![[Pasted image 20260527171012.png]]
Just put a phase difference between peak 2 and 3 to filter away COSY, and put it in the middle at 1/2 the time of the inverse at the last part to filter away NOESY. HOWEVER in COSY we have +2 and -2, so we lose half the signal but it is very clean.
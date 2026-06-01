#nmrms
CW NMR was the first NMR ever done, working by creating a magnetic field and sweeping with different frequency radio waves or oppositely sweeping with difference magnetic field strengths.

Instead we use FT-NMR because it is better. It works by:
1. Exite the sample using radio waves
2. Record output
3. FT to get frequency

Sample goes into strong magnet ($B_0$). Sample can have +1/2 or -1/2. HOWEVER only Z-value is fixed on angle, but x and y is free. This results in a cone of angles from origin to this circle. There is however a slight excess of vectors in the Z+ direction. All this is illustrated on the figure below.
![[Pasted image 20260524135621.png]]
Here $M_0$ is the sum magnetization vector called [[Equilibrium magnetization (M0)]] or Mz. When applying RF waves, we flip a spin 180 degrees. This model does not explain the reason we only take from one side of the cone, but it shows where the M0 vector goes.

If you have a [[Magnetic moment (μ)]] and a [[Magnetic field strength (B)]], then the magnetic field will exert a rotating force (torque) on the magnetic moment. This torque is calculated as
$$\vec{c}=\vec{\mu}\times \vec{B}$$
Say our magnetic moment is our M0, no force will be observed. When we apply radio wave, it will have an electric component, which will rotate M0 around B1 (the radio wave).
![[Pasted image 20260524140318.png]]

Same logic means that if you do a 90 degree pulse and stop it, the B0 would rotate in the x-y direction due to the torque excreted by B0 (this is called precession). This rotation has a frequency and can be measured using an antenna + Fourier Transformation. This is called the precession/ [[Larmor frequency (ν)]].

This does not go on forever as the spin is not in equilibrium. They will decay back to equilibrium, this is called relaxation. The specific one that goes back to Z-axis is called [[T1-relaxation]] and intensity decreases exponentially over time.

![[Pasted image 20260524141658.png]]

This is not the only one, there is also [[T2-relaxation]]. This does not reestablish equilibrium, but instead decreases x-y axis magnetization towards 0 as it is not being sustained by the RF wave. Also exponential.

![[Pasted image 20260524141920.png]]
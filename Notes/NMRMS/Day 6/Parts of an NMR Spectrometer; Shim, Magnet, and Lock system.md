#nmrms
Magnet is very important, it enhances the population difference between the $\alpha$ and $\beta$ state, which is our goal as instead of looking at transitions we look at spins which are VERY sensitive. As we know from the
![[Spin behavior in magnetic field#Boltzmann distribution of spin-up and spin-down states]]
and the
![[Dipole energy in magnetic field (E)#$ Delta E$ equation]]
Our population difference is small and we want to make it as large as possible, which we do by increasing magnet strength.
![[Pasted image 20260527153445.png]]
Thereby we want a strong magnet. The probe sends and measures signals. The console has the necessary electronics to make the transmitter send pulses and to receive pulses from the receiver. A spectrometer also has a Shim&Lock controller and other components.

Magnets range from benchtop NMRs with 1.4T to super NMRs with 28.2T. We have a 14.1T magnet which gives hydrogen a 600MHz frequency. It works by having many kilometers of superconducting wire. Our spectrometer has a current of 134A. To uphold this, a lot of power and cooling is needed. To circumvent this superconducting wire without and resistance is used, but only work at around 4K (liquid helium). To avoid boiloff we incase this in liquid nitrogen (77K) which is cheaper. Two tubes are in there for refilling and so pressure doesnt build up.
![[Pasted image 20260527154046.png]]
It is VERY important to keep field homogeneity. A sample is typically has a diameter of 5mm, 3mm or 1.7mm, but the sample is 2cm tall and even very small differences in field strength across the sample as the [[Larmor frequency (ν)]] depend on the field strength.
![[Pasted image 20260527154219.png]]
The field needs to be VERY stable over time and small things like cars driving by or so is measurable in NMR. To exemplify why homogeneity is so important, 1\% deviation is 6MHz difference for 1H, which is a change of 10000ppm for hydrogen. 0.0001\% is 1ppm difference. Example of terrible field homogeneity with long tails:
![[Pasted image 20260527154817.png]]
Comparison:
![[Pasted image 20260527154904.png]]
Magnets cannot have that high a homogeneity and the sample will affect the magnetic field. However if you cant make the magnet homogeneous enough, you can add variable extra coils to correspond to the difference. Then you make a linearly inhomogeneous field, by adding z-shim coils to your system as shown. These exist mostly in the z-direction (as the sample is tallest in that direction) but also in the x-y directions.
![[Pasted image 20260527155211.png]]
You then do a polynomial fit of your shim coils to the inhomogeneity and cancel out the noise.

Field stability is also important, as liquid He is boiling off, which is affected by weather, and so on, affect field stability. To fix this we use a deuterium lock, which monitors field strength and attempts to counteract changes in field strength. It works by measuring magnetic fields using NMR on a known component of our sample (deuterium from deuterated solvents), hence deuterium lock. If it is drifting, we correct for it using a Z0 coil that increases or decreases magnetic field strength slightly to compensate for small errors from field drift. As a user of NMR you type in your solvent and the computer finds out itself.

Related:
- [[The Probe - the Antenna of an NMR Spectrometer]]
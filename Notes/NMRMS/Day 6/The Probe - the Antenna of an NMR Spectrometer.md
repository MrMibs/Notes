The antenna sending and measuring pulses is called the probe.
![[Pasted image 20260527161045.png]]
I consists of 2 primary things, electronics at the bottom and a stick appropriate so the antenna (top of stick) gets to where the magnetic field is strongest. The antenna is shown all the way on the right and is a helmholtz-coil (that is where your sample goes). There are many different probes, they handle different amounts of frequencies and have different features. Most antenna have 2H for deuterium lock and 1H because it is the most common NMR but from there it varies with more types of nuclei (e.g. double/triple/quadruple resonance probes). Broad-band tunable probes let you use them for a lot of things, but they are less sensitive.

You typically have an inner coil and an outer coil. The inner coil is most sensitive and depending on if it is for 1H or something else they have different names (this matters a lot, $\pm 30\%$ signal to noise ratio)

![[Pasted image 20260527161535.png]]
Example with our own T = triple resonance (H C N), I = inverse (1H specialized), 5mm is sample diameter and [[Field gradients I-II]] we get to later, but are sometimes wanted in specific tests.
![[Pasted image 20260527161641.png]]

---
## Temp control
It also has temperature control which works by heating nitrogen and pumping it through the probe as a heater to the sample. Temperature differences from air to sample and internally in sample is done through software unless you need >0.1K precision.
![[Pasted image 20260527161851.png]]
For water an even temperature is extra important as its chemical shift is dependent on it, but for most organic solvents temperature precision is not that important.

---

We also have a gradient coil which makes the magnetic field inhomogeneous, but for some applications you sometimes want a very specific gradient in your magnetic field. When you do solid state NMR you also want a spinning device so samples are spun at an angle to the magnetic field very quickly, this is called MAS (Magic Angle Spinning 1000s of rounds per seconds 54 deg to the magnetic field).

--- 

The probe contains a probe with an inductivity and capaciance. The frequency of an antenna is given as: $\omega = \frac{1}{L \cdot C}$. We need to make this match the [[Larmor frequency (ν)]] for optimal results. Thereby, as inductivity is constant, you need to adjust capacitance (**tuning** of the antenna). This needs to be done every time using a good old knob and inductivity varies based on sample. There is a resistance/impedance on the system and the amplifier has an impedance of 50$\ohm$ and the antenna needs the same impedance. This is why there are 2 capacitors and this is called **matching**. This specialization of tuning and matching is called wobbling or severe hardware damage will occur.
![[Pasted image 20260527163334.png]]
If you are doing several experiments to get an average you don't have to redo this unless you take the sample out.
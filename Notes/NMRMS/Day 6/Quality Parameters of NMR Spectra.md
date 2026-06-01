#nmrms
Spectral quality is defined by different parameters as a spectrum is good when you get information you need. However, we try to define parameters, there are 2:
1. Sensitivity (Signal-to-noise ratio)
2. Resolution (can i tell my samples apart?)

Electronics create noise (N). Our signal (S) needs to be stronger then this. To increase S/N we:
- Repeat the measurement (S $\propto$ NS & N $\propto$ $\sqrt{NS}$, so signal grows faster. S/N $\propto$ $\sqrt{NS}$) Useful for short scans
- Increase concentration S/N $\propto$ $C$. VERY IMPORTANT FOR LONG SCANS
- Higher field strength S/N $\propto$ $B^{3/2}$
- Exponential multiplication of FID (resolution dies, noise reduced)
- cryo-probe (cooled probe) reduces noise. Very expensive. Improves by factor 2.5-4 or 4-8 depending on N or He. We have an N one.
- Spectroscopic tricks like the [[The INEPT sequence]]

Resolution can be improved by
- Higher [[Magnetic field strength (B)]]
- Gaussian multiplications can help slightly sometimes maybe
- Improve field homogeneity (limited)
- $\cancel {Number of scans}$
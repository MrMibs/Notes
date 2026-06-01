[[Larmor frequency (ν)]] is affected by field strength. We dont like this. For this reason we use [[Chemical shift (PPM)]] which standardizes across magnets.
$$\delta=\frac{\nu_{sample}-\nu_{standard}}{\nu_{standard}}\cdot10^6[PPM]$$
This does 2 things, 1. i scales the difference in shift down to a scale of 0-something instead of using real frequency and 2. it standardizes magnetic field strength to the magnet by dividing by it, leaving the relative change in [[Magnetic moment (μ)]] and thereby [[Gyromagnetic ratio (γ)]]. To do this we need a 0ppm compound for the standard and this is chosen as the highest shielded value so all PPM values are positive. Here, TMS $(SiC_4H_{12})$ is chosen. It is inert (does not sabotage sample), volatile (removable) and soluble in most things except water (where it gets a 4 long carbon chain with SO3- Na+ on the end).

e.g.
$$\frac{60.3468056-60.03424471}{60.03424471}\cdot1000000=7.26[PPM]$$
Shifts seen:
1H 0-10 ppm
13C 0-230 ppm

In old papers ppm is defined as:
$$\tau = 10-\delta$$
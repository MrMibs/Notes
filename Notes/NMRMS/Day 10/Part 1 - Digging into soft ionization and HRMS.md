#nmrms
HRMS comes from [[Part 4 - Resolution]], which means you narrow peak width and high isotopic resolution at higher charge states. Close m/z space is resolvable. Mass accuracy is more accurate. Not always necessary, but in general really useful. TL;DR data depth is increased at the cost of something. Example of necessity:
![[Pasted image 20260602133915.png]]
HRMS allows us to understand the specific charge states:
![[Pasted image 20260602134052.png]]

This allows us to deconvolute charge states to measure mass.
![[Pasted image 20260602134111.png]]
Again but with more focus on isotopic distribution:
![[Pasted image 20260602134254.png]]
Charge state for the lower peak (n1) is calculated as:
$$n_1 = \frac{m/z_2 - m_H}{m/z_1 - m/z_2}$$
where
- $m/z_2$ for the higher peak
- $m_H$ is the difference in mass
- $m/z_1$ for the lower peak

![[Pasted image 20260602134758.png]]
For more peaks this works even better! We also have a lot of salts using soft ionization such as Na K and rarely Cs Ag.
![[Pasted image 20260602134919.png]]
Here we use unit mass resolution. It is really convenient sometimes and confusing at other times. HRMS gives us even more decimals and even more certainty.
![[Pasted image 20260602135019.png]]


This can be used to characterize unknown compounds, identifying predefined molecules in a sample and to identify components within a complex. Here, controlled fragmentation is key. HRMS is typically used for these as they allow for it:
![[Pasted image 20260602135220.png]]
EI is good for fragmentation, however this does not work for larger as we would get infinite fragments. When we ionize biomolecules via ESI or [[Matrix-Assisted Laser De-sorption or Ionization (MALDI)]] (post source decay in TOF) we get very limited fragmentation. Higher mass gives more post source decay especially in reflector mode where the ions fly for longer. This can make us lose information.
![[Pasted image 20260602135620.png]]
[[ElectroSpray Ionization (ESI)]] has a potential due to needing to control ions which allows for in source fragmentation. This leads to neutral losses! This can be useful as we can match these fragments to controlled fragmentation so we know what we have.







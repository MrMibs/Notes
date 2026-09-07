#RPM 
$$\frac{dN}{dt}=F_0-F+G$$
Hvor:
- N = antal mol af reaktant eller produkt i reaktoren (mol)
- t = tid (s (eller anden enhed))
- F0, F er mol-flow hhv. ind og ud af reaktoren (mol/t)
- G = totale produktions-hastighed (generation), (mol/t)

Her ser vi ændring af N ift. tid er afhængig af F0 (input) minus F (output) + G (ændring af ting i reaktoren)

Generaton kan omskrives
$$G=r \cdot V$$
Hvor:
- r = proceshastighed (mol/(s $\cdot$ L))
- V = volumen af reaktions-mediet i reaktoren (L)

$$\frac{dN}{dt}=F_0-F+r \cdot V$$

#### Eksempel ved batch reaktor (intet input eller output) fjernes F0 og F
$$\frac{dN}{dt}=r \cdot V$$
Dermed kan reaktionshastighed findes (da V kan deles over og ændring i stof-pr-volumen er koncentration kan dette udskiftes):
$$\frac{dN/V}{dt}=\frac{dC}{dt}=r$$

**Vi må gerne invertere fortegn så vi kan skrive "vi forbruger 10" i stedet for "vi producere -10"**
Her bruger vi termerne: Produktionshastigheder og Forbrugshastigheder.





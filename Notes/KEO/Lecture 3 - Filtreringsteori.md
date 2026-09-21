#KEO 
Vi kan lave sådan et setup:
![[Pasted image 20260921135237.png]]
Her kan vi være interesserede i hastigheden vores væske kan skældes fra vores faste stof igennem et filter. Hastigheden væsken kommer igennem filteret er beskrevet af dV dt altså ændring af filtratvolumen pr tid gange med arealet det kommer ud igennem for at finde "højden" af det væske der kommer igennem. (Se ligning 1)

Darcys lov lyder:
$$
\frac{\text{d}V}{\text{d}T}=A\cdot \frac{1}{\eta\cdot R}\cdot \nabla P
$$
Hvor:
- $\eta$ = viskositet
- R er modstand
$$
\nabla P=\frac{P_{ext}}{L}
$$
Og sammen med den specifikke modstand for membranen ([[Kage]]modstand)

$$
R=\alpha(1-\varepsilon)\rho_{s}
$$
Giver det os:
$$
u=\frac{1}{\eta \alpha(1-\varepsilon)\rho_{s}}\cdot \frac{P_{ext}}{L}
$$
Hvor:
- $\alpha$ er den specifikke kagemodstand (m/kg)
- $\varepsilon$ er porøsiteten $\frac{\text{volumen vand}}{\text{total volumen}}$ af kagen (mellem 0 og 1, mellem total kompakt og ren vand)
- $\rho_{s}$ er densitet af kagen (kg/L)
- Resten er nævnt tidligere eller tegnet

Som mere kommer igennem bliver kagen tykkere og der kommer mindre igennem. Den spefikke kagemodstand kan overslagesregnes via. kozeny-carman:
$$
\alpha=k\cdot \frac{(1-\varepsilon)\cdot S^{2}_{O}}{\rho_{s} \varepsilon^{3}}
$$
Hvor $S_{O}$ er:
$$
S_{O}=\frac{\text{surface area}}{\text{particle volume}}=\frac{6}{d_{p}}
$$
Hvilket giver mening grundet fi
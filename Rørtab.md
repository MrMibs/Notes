#hydraulik 
[[Friktionstal, f]] kan findes for [[Laminær strømning]] relativt simpelt. Dette gøres ved:
$$
f=\frac{4}{Re}
$$
for et cirkulært rør. I dette tilfælde kan Re beregnes som:
$$
\mathrm{Re}=200000\cdot V\cdot D
$$
Hvor 200000 er en konstant baseret på $\nu$ og dermed rørformen, V er hastighed, D er diameter. [[Reynolds tal, Re]].

Dette er ikke nær så nemt for [[Turbulent strømning]]. Nikuradse limede nogen sandkorn på et rør. De havde diameter k. Røret havde kente værdier af R og $\nu$. V og tryniveautab måles på samme tid.
![[Pasted image 20260911104303.png]]
Dette gav flg:
![[Pasted image 20260911104237.png]]

Her kan vi se at friktionstallet er uafhængigt af Re ved område 1, 2 og 3 men ikke mellem 2 og 3. Dermed, for et glasvægget rør har vi:
$$
\sqrt{ \frac{2}{f} }=2.6+2.45\ln(\mathrm{Re}\sqrt{ f })
$$
og for rug væg
$$
\sqrt{ \frac{2}{f} }=6.4-2.45\ln\left( \frac{k}{R} \right)
$$
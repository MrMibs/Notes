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
og for ru væg
$$
\sqrt{ \frac{2}{f} }=6.4-2.45\ln\left( \frac{k}{R} \right)
$$
Hvor R er [[Karakteristisk længde, Lc]] (altså hydraulisk radius for dette). Fordi jeg ikke gider overveje om mit rør er ru eller glat kan vi samle ligningerne:
$$
\sqrt{ \frac{2}{f} }=6.4-2.45\ln\left( \frac{k}{R}+\frac{4.7}{\mathrm{Re}\sqrt{ f }} \right)
$$Eksempel på side 95 til hvordan denne bruges og hvordan $\sqrt{ f }$ på begge sider håndteres. Det vi gør er at gætte på f, så får vi et resultat der giver os et andet f der er tættere på.
![[Pasted image 20260911105212.png]]
Til et grovt overslag kan vi bruge:
![[Pasted image 20260911105245.png]]
Hvis man ikke kan lide iterative formler kan man bruge:
$$f=\frac{0.341}{\left[ \ln\left( \frac{k}{14.8\cdot R}+\frac{1.65}{Re^{0.9}} \right) \right]^2} \quad \text{for} \, 4\cdot 10^{-5}< \frac{k}{R}<0.08$$
Hvis man ikke kender rughed ret godt kan man bruge ![[Manning formlen]]
#hydraulik 

----
TIL FREMTIDIG MIG, DEN "RIGTIGE" LIGNING ER:
$$
(z+\frac{p}{\gamma})_{A}+\frac{\alpha_{A}V_{A}^{2}}{2g}=(z+\frac{p}{\gamma})_{B}+\frac{\alpha_{B}V_{B}^{2}}{2g}+\Delta H_{AB}
$$
OG STÅR INDE PÅ [[Energiligning for strømrør mellem 2 snit med hydrostatisk trykfordeling]]

---

Vi har et strømrør med en fast bund og fri overflade:
![[Pasted image 20260909092538.png]]
Vi ender med at kunne sige energien i $E_{a}-E_{tab}=E_{b}$. Tilbage til udledningen

---

Vi har flg. forudsætninger:
1. Energisætningen lyder $A_{ydre}=\Delta E_{kin}+\Delta E_{varme}$ altså ydre arbejde bliver enten kinetisk energi eller varme
2. Stationær strømning, dvs. strømlinjer ligger fast
3. Usammentrykkelig væske
4. Laminær strømning eller middelstrømning i turbulent strømning benyttes

Vi observere væsken bevæger sig $\Delta A$ afstand på $\Delta t$ tid (stiplet linje) hvor der er friktion mod bunden og skaber en kurve, men vi antager der ikke er mod luften (det er der men ikke meget). Dermed har vi
$$
\tau =0, \, v \neq 0 \, \text{for luft} \quad \text{og} \quad \tau \neq 0, \, v = 0 \, \text{for bund}
$$
Vi har 3 ydre kræfter: tryk, forskydning og tyngde. De beskrives enkeltvis som:
$$
A_{p}=\int_{A}\,p_{A}\,\text{dA} \; v_{A}\Delta t-\int_{B}\,p_{B}\,\text{dB} \;v_{B}\Delta t
$$
Dette er tryk, hvis vi deler det op kan vi se den klassiske $\int_{A}p_{A}\text{dA}$ altså tryk på en flade. Dette bliver ganget med en afstand $\frac{m}{s}\cdot s=m$. Forskellen på A og B er dermed arbejdet udført.

Næst har vi forskydning, dog er denne kraft vinkelret på strømningen så i strømningsretningen kan vi se bort fra denne.

Sidst har vi tyngdekraften:
$$
A_{G}=\sum-mg(z(\Delta t)-z(0))=\sum mg \, z(0)-\sum mg \, z(\Delta t)
$$
Hvis vi forstiller os det hele består af små elementer der hver har massen m, så ved vi kraften er $\sum m\cdot g$. Derudover har tyngdekraften også et $z(\Delta t)-z(0)$ element, hvilket bare beskriver ændringen i højden. Af definitionsmæssige årsager betyder det at vi siger z er opad og tyngdekraften er nedad (dermed -mg).

Dernæst indser vi at det der er forskudt i A og B er det samme, hvilket betyder der ikke er en ændring imellem dem (da væskeforskydelsen fra A -> A' er det samme som fra B -> B' og dette sker bare igennem A' -> B, ligesom strøm). Dette betyder vi kan omskrive $A_{g}$:

$$
\sum mg \, z_{A}-\sum mg \, z_{B}
$$

$$
=\int_{A}(pv_{A}\Delta t\text{dA})gz_{A}-\int_{B}(pv_{B}\Delta t\text{dB})gz_{B}
$$
Altså igen $\frac{m}{s}\cdot s=m$ så afstand gange med en kraft på en overflade $\frac{N}{m^{2}}\cdot m^{2}=N$. Dermed får vi enheden $N\cdot m = J$. Dette kan endnu omskrives da vi har fælles udtryk.
$$
=\Delta t\left[ \int_{A}\gamma z_{A}v_{A}\text{dA}-\int_{B}\gamma z_{B}v_{B}\text{dB}\right]
$$
Hvor:
- [[Specifik tyngde, γ]]
- z er højde fra referenceplan
- v er hastighed

Ekin definition er $\frac{1}{2}\cdot m\cdot v^{2}$. Igen kun område 1 og 3 er vigtige, dette omskrives med energiligning.
$$
\Delta E_{kin}=E_{kin,III}-E_{kin,I}
$$
$$
=\int_{B}\frac{1}{2}(pv_{B}\Delta t\text{dB})v_{B}^{2}-\int_{A}\frac{1}{2}(pv_{A}\Delta t\text{dA})v_{A}^{2}
$$
Nu er vi et godt sted! Vi kender Ekin og Aydre. Sammensat får vi dermed:
$$
\Delta E_{varme}=\Delta t \left[ \int_{A}\left( \gamma z_{A}+p_{A}+\frac{1}{2}pv_{A}^{2} \right)v_{A} \;\text{dA} - \int_{B}\left( \gamma z_{B}+p_{B}+\frac{1}{2}pv_{B}^{2} \right)v_{B} \;\text{dB} \right]
$$
Fordi det er et træls udtryk vil vi gerne have et andet i stedet, $W_{vame}$, altså mekanisk energi der omdannes til varme pr tid: $\frac{J}{s}=W$. Dette betyder vi kan omskrive vores udtryk:
$$
\Delta E_{varme}=W_{varme}\cdot \Delta t
$$
Og dermed
$$
W_{varme}=\int_{A}\left( \gamma z_{A}+p_{A}+\frac{1}{2}pv_{A}^{2} \right)v_{A} \;\text{dA} - \int_{B}\left( \gamma z_{B}+p_{B}+\frac{1}{2}pv_{B}^{2} \right)v_{B} \;\text{dB}
$$
Del med gamma
$$
\frac{W_{varme}}{\gamma} = \int_{A} (z_{A} + \frac{p_{A}}{\gamma})v_{A} dA + \int_{A} \frac{v_{A}^{3}}{2g} dA- \int_{B} (z_{B} + \frac{p_{B}}{\gamma})v_{B} dB - \int_{B} \frac{v_{B}^{3}}{2g} dB
$$
Her kan [[Tryk niveau, h]] genkendes fra ledet efter integral 1 og 3. Derudover hader vi integral 2 og 4 så vi vil afskaffe dem. Det gør vi ved brug af ![[Hastighedsfordelingskoefficient - α]]
Benyttes dette fås det endelige udtryk:
$$
\frac{W_{varme}}{\gamma} = \int_{A} (z_{A} + \frac{p_{A}}{\gamma})v_{A} dA + \frac{\alpha_{A}V_{A}^{3}A}{2g}- \int_{B} (z_{B} + \frac{p_{B}}{\gamma})v_{B} dB - \frac{\alpha_{B}V_{B}^{3}B}{2g}
$$
Det er dog ikke mega simpelt, men vi har specialtilfælde versioner der er mere overskuelige.

![[Energiligning for strømrør mellem 2 snit med hydrostatisk trykfordeling]]
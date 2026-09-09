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
- [[Specifik vægt, γ]]

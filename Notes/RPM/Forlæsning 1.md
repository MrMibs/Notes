#RPM
Overblik:
Modeller har 2 komponenter (mindst):
**Balanceligning** bestemmer IO af det du holder styr på (ind, ud, dannelse, forbrug)
**Hastighedsudtryk** (dannelses/forbrugshastighed) hvilket sættes ind i dannelse og forbrug.

Lad os sige vi tilsætter O2 gas til en beholder og dræner noget væske, så skal vi bruge noget kemi til at beskrive hvordan gassen bliver overført til vandet. Også bare tilføjelsen af materiale i sig selv. Dette hedder **transportligninger**.
![[Pasted image 20261028102010.png]]



Balanceligning:
$$
\frac{\text{d}N}{\text{d}t}=F_{0}-F+G
$$
Hvor G er generation og resten ses ovenstående. For en ideel reaktor kan vi skrive G som:
$$
G=r\cdot V
$$
Hvor r er volumetrisk reaktionshastighed (mol pr m$^3$ t) og V er volumen. r kan eksempelvis være et hastighedsudtryk for en 0,1 eller 2 orden reaktion. Hvis den er ikke ideel har vi i stedet:
$$
G = \int^V_{0} r \; \text{d}V
$$
Hvor vi selvfølgelig tager de små volumenbidrag og lægger hver deres reaktionshastighed sammen. Vi har nok måder at regne hastighed ud i specifikke slices af en reaktor eller noget så det er bare hvadend dele vi kan beregne. Dette benyttes som:
$$
3 \frac{\text{mol}}{m^{3}\cdot \text{s}} \cdot 1 m^{3}+2\frac{\text{mol}}{m^{3}\cdot \text{s}}\cdot 1m^{3}=5 \frac{\text{mol}}{\text{s}}
$$

---

Faget handler om at lave et experiment? Hvpordan får man det man har til at gøre det man vil have det til at gøre. f.eks. Støkiometri, kinetik osv.

Ligger sig meget op ad enhedsoperationer.

![[Reaktor]]

![[Reaktion]]

![[Modeller]]

[[Designligning]]

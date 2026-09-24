#KEO 
Til fremtidige mig: Læs op på Zeta potentiale og kappa. Også skriv alle formelerne ned pænt et sted.

Et kolloid er en partikel mellem 5 nm - 1 µm. For disse partikler har overfladeegenskaberne stor betydningen i en række sammenhænge f.eks. i vandige opløsninger. En af de vigtig overfladeegenskaber er partiklernes ladning. I kurset gives en gennemgang af den basale kolloid kemi, herunder især partikelladning og hvordan partiklers ladning indvirker på kolloid systemers stabilitet.

Vi kigger på overflade og interaktioner. ![[Stern lag]]
Efter det har vi
![[Diffusive lag]]

![[Elektrisk dobbeltlag]]

Fordeling ift. afstand fra negativt ladet kolloid
![[Pasted image 20260923103156.png]]

Hvor ladninger er balanceret når vi kommer længere væk. Integralet mellem de to linjer for + og - ioner giver ladningen af kolloidet, og ligeledes omvendt.

[[Modion]]
[[Medion]]

![[Potentiale]]

![[Kolloid potentiale]]

De bevæger sig væk fra hinanden
[[Elektrostatisk kraft]]
Og mod hinanden
[[Van der waal krafter]]

Som udgangspunkt vil vi gerne have 
$$
vdw > elektrostatisk
$$
da vi gerne vil have vores stoffer klumper sammen.
![[Pasted image 20260923114818.png]]

Vi vil gerne have dem ned i sammenhængsminimum.

Hvis vi ændre ph så zeta-potentiale bliver mindre eller tilsætter salt bliver de frastødende kræfter mindre. Dette er nødvendigt da vi skal mindske barrieren og vi kan ikke bare tilføje energi da T indgår i ligningerne og bare modvirker det (vist nok øger frastødning).

Opsummering
![[Pasted image 20260923115017.png]]

---
Video 2

## DLVO teori er centralt for kolloid kemi.
Kolloider er oftest negativt ladede. Dette minder om det fra før tror jeg, her har vi
IHP (Inner Helmholtz Plane) hvilket er ioner ionbundet til kolloidet. Vi har også OHP lige udenfor, der er positive ioner med vand omkring som også kan have vdw krafter tiltrækkende dem til kolloidet. Disse tilsammen er stern laget.
![[Pasted image 20260923122957.png]]

Det diffusive lag er defineret som det lag hvor potentialet falder med 64% ift. OHP / stern. Det falder selvfølgelig fortsat.
![[Pasted image 20260923123433.png]]

For mono valent salt
$$\psi = \psi_0 \cdot e^{-\kappa x}$$
I vand
$$λ_D = \frac{3.04 \text{ Å}}{\sqrt{c_0 \frac{L}{\text{mol}}}}$$

к: [[Debye-Hückel parameter, κ]] (m¯¹) - Afhænger af c｡ (salt koncentration) 
λ$_D$: Debye length (m)  (1/kappa)
ɛ$_0$: Permittivitet i vacuum (8,85·1012 C2/Nm²) 
ε: Dielectric constant (Vand: 78) 
e = 1,602 176 565(35) · 10-19 С

![[Pasted image 20260923124246.png]]
Hvor:
- $n_{0}$ er koncentration i bulk
- z er ladning
- e er [[elementarladning, e]]
- $\psi$ er fra tidligere lige ovenover (for monovalent salt)
- k er [[Boltzmann konstant, kb]]
- T er temperatur

Yderligere kan vi regne på energi ift. afstand (ift. uendelig, skal nok regnes for før og efter afstand) vi antager disse partikler er samme størrelse og 
$$V_{R} = 2\pi ea\zeta^{2} \exp(-\kappa d)$$
Hvor:
- e er [[elementarladning, e]]
- a er radius
- $\zeta$ er zetapotentiale
- $\kappa$ er [[Debye-Hückel parameter, κ]]
- d er afstand mellem kolloid

![[Pasted image 20260923124624.png]]

Som vi ved:
![[Pasted image 20260923124756.png]]

Og i kolloid kemi bruger vi hamaker konstanter, disse er konstante for e.g. vand, materialer osv. 
![[Pasted image 20260923125052.png]]
I praksis bruger man en effektiv hamaker konstant, hvor 1 er partikel 1, 2 er partikel 2 og 3 er mediet de er i.
$$A_{132} = (\sqrt{A_1} - \sqrt{A_3})(\sqrt{A_2} - \sqrt{A_3})$$
Dette indsættes i lignigen fra vdw krafter:
![[Van der waal krafter]]


Sammenlagt for vdw og elektrostatisk:
$$
V_{r}=2\pi ea\zeta^{2}\exp(-\kappa d)-\frac{Aa}{12d}
$$
Hvor:
- $V_r$ = Repulsionspotentialet
- $\pi$ = Pi (≈ 3,14159)
- $e$ = Elementarladning
- $a$ = Partikelradius
- $\zeta$ = Zeta-potentiale
- $\kappa$ = Debye-Hückel-parameter (invers Debye-længde)
- $d$ = Afstand mellem partiklernes overflader
- $A$ = Hamaker-konstanten

KbT kan plottes ift. Vt for at sammenligne kinetisk energi og afstand.

![[Pasted image 20260923130118.png]]

Toppunkt:
![[Pasted image 20260923130138.png]]


Kritisk [[Debye-Hückel parameter, κ]] for aggregering findes som
$$ \kappa_{crit} = 23 \pi \varepsilon_r \varepsilon_0 e^{-1} \frac{\zeta^2}{A} = 2,3 \cdot 10^{-8} \frac{\zeta^2}{A} $$ 
Her kender vi zeta potentiale og hammaker konstant. Omskrivning 2 er for vand.
$$ \kappa = \left( \left( \frac{10^3 \cdot e^2 \cdot N_A}{kT} \right) \cdot \left( \frac{1}{\varepsilon \cdot \varepsilon_0} \right) \cdot (2 \cdot I) \right)^{1/2} $$

Kritisk ionstyrke:
Iccc = $\frac{1}{2}(24\pi exp[-1])^2 \frac{\epsilon_r^3 \epsilon_0^3 kT \zeta^4}{e^2 N_A A^2}$  (mol/m3)
Iccc vand 25C = $3.36 \cdot 10^{-35} \frac{\zeta^4}{A^2}$ (mol/L)

Afhængig af valens:
![[Pasted image 20260923130638.png]]

---
### Video 3:

Hvis vi arbejder med metaller så kan vi blive meget skuffede:
![[Pasted image 20260923130830.png]]
Da det ikke bliver så ladet som vi ønsker, da i stedet for at give 3 negativt ladede ioner får ikke det.

![[Pasted image 20260923130951.png]]



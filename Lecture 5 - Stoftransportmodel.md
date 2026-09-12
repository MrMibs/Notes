#hydraulik 
En stoftransportmodel består af:
![[Pasted image 20260912092055.png]]


Der er mange ting der kan få noget til at bevæge sig:
Advektion (Stof flyttet fremad), Diffusion (koncentrationsforskelle) og Dispersion (Stofsky spredt ud) er de primære. 

Yderligere har vi Sorption, Nedbrydning, Hydrolyse, fordampning biotransformation. Til det meste bruger vi ![[1D advektion-diffusion-ligningen]].
Vi bruger finite volume metoden:
- Diskretisering af domæne i kontrolvolumer
- Opstilling af massebalancer
- Diskretisering af differentialled i den styrende transportligning
- Indsæt randbetingelser og begyndelsesbetingelser (initial betingelse)
- Løs de diskrete ligninger

## Firkantificer vandet
![[Pasted image 20260912095620.png]]
Massebalancen er selvfølgelig $\sum\text{Ind}-\sum$
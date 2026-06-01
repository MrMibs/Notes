#nmrms
To really understand how we encode 2 spectra into 1 we need to look at [[HSQC sequence]] and thereby its pulse sequence. it has an inept and a reverse inept

![[Pasted image 20260527140328.png]]

a: $H_z$
b: $2C_yH_z$
What happens during $t_1$? Carbon magnetization undergoes [[Chemical shift evolution]] and couples to hydrogen (this is undone by the $\tau \, 180 \, \tau$ sequence, also called [[The Spin-Echo sequence - Refocusing sequence]]). Using the rules for chemical shift evolution: 
![[Chemical shift evolution#Eq 1]]
sticking to c,s notation
![[c,s Notation#c,s Notation]]

in this case $\omega_C$ and $\tau_1$

c: $2C_yH_z\cdot C - 2C_xH_z \cdot S$
d: $H_y \cdot C$

When we record a 2D spectrum, we record many (100-1000) 1d spectra with different values of $t_1$. Time during FID is called $t_2$. Depending on our $\tau$, our $H_y \cdot C$ will look different, as C is dependent on $\tau$ and a constant for C. Illustration.
![[Pasted image 20260527150511.png]]
Real life measurements
![[Pasted image 20260527143100.png]]

Hereby, we can plot $t_1$ as an axis and encoded in it is the omega value. This gives us our 2 axis, the FT'd $t_2$ and the $1^H$ $t_2$ spectra vs. $t_1$ plot.
![[Pasted image 20260527143354.png]]

In real life:
![[Pasted image 20260527143645.png]]
Where the frequency difference is clear, as they carry their hydrogen atoms specific carbon's information. After FT on $t_1$.
![[Pasted image 20260527143749.png]]
TL;DR we have equation $H_y \cdot C$. intensity of H depends on C. We measure H at varying values of t1, on which C depends. We then FT H so we have intensity at different frequencies with changing t1:
![[Pasted image 20260527143645.png]]
The colors represent intensity. Following this, we can FT the t1 axis to get its frequency too.
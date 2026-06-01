We transfer magnetization from one nucleus to another! We excite H first then transfer it to carbon!

![[Pasted image 20260527125534.png]]

To analyse this pulse sequence, we do exactly like in [[The Spin-Echo sequence - Refocusing sequence]]. We set up timestamps we calculate from. To make this followable, we set them up as

pre90x, post90x, pre180x, postH180x, post180x, pre90xy, post90y and post90xy, for a, b... illustrated above.


a: $H_z$, ($C_z$) <-- not useful, we ignore it.
b: $-H_y$
Thereby, as we have [[The Spin-Echo sequence - Refocusing sequence]] on our H, we can ignore chemical shift evolution and only look at scalar coupling.
![[Describing scalar coupling#Eq 2 for y]]
As it is for hydrogen, we write H for hydrogen instead of I for spin or M for net magnetization. Further, S becomes C as it is carbon we couple to.

c: $$\underbrace{-H_y \cdot cos(\pi \cdot J \cdot \tau)}_{in-phase}+\underbrace{2C_z\cdot H_x\cdot  sin(\pi \cdot J\cdot \tau)}_{anti-phase}$$
Now we apply the 180deg pulse. In first part, there is one term: Hy. There are 2 terms in part 2: Hx and Cz, we apply to each of them. Hy gets flipped across x. C does not care about a (H) pulse and x-magnetization does not either, meaning the second part stays
d: $${H_y \cdot cos(\pi \cdot J \cdot \tau)}   +   {2 \underbrace{C_z}_{wrong \,frequency}\cdot \underbrace{H_x}_{wrong \, axis}\cdot  sin(\pi \cdot J\cdot \tau)}$$
Now we apply 180x pulse on carbon and it gets flipped
e: $${H_y \cdot cos(\pi \cdot J \cdot \tau)}   -   {2 C_z\cdot H_x\cdot  sin(\pi \cdot J\cdot \tau)}$$
Now we have a delay, so we apply time dependent coupling again. Hy becomes -Hx and 2CsHx becomes Hy.
f:
$${cos(\pi \, J \, \tau)\cdot [H_y\cdot cos(\pi \, J \, \tau)-2H_xC_z\cdot sin(\pi \, J \, \tau)]}   -   

sin(\pi \, J\, \tau)\cdot[2 C_zH_x\cdot cos(\pi \, J \, \tau)+H_y\cdot sin(\pi \, J \, \tau)]$$

time to simplify (see [[The Spin-Echo sequence - Refocusing sequence]])
$$H_y\cdot[cos(\pi \, J \, \tau)^2-sin(\pi \, J \, \tau)^2]$$
$$2H_xC_z\cdot[-2cos(\pi \, J \, \tau) \cdot sin(\pi \, J \, \tau)]$$
Trigonometry says $cos(\pi \, J \, \tau)^2-sin(\pi \, J \, \tau)^2=cos(2 \pi \, J \, \tau)$ and $-\cdot cos(2 \pi \, J \, \tau) \cdot sin(\pi \, J \, \tau) = sin(2 \pi \, J \, \tau)$

$$H_y \cdot cos(2 \pi \, J \, \tau) - 2H_xC_z\cdot sin(2 \pi \, J \, \tau)$$
As the [[Coupling constant (J)]] is constant, we can set $\tau = \frac{1}{4\cdot J}$ (i think its J=$J_{CH}$). Thereby

$$H_y \cdot cos(\pi/2) - 2H_xC_z\cdot sin(\pi/2)$$
We know cos(pi/2)=0 and sin(pi/2)=1. Thereby
$$-2H_xC_z\cdot sin(\pi/2)$$

now time for g! 90y degree pulse on H. Hx becomes Hz.
$$-2H_zC_y\cdot sin(\pi/2)$$

90 degree on phase x of carbon
$-2H_zC_y$

We transfer magnetization from one nucleus to another! We excite H first then transfer it to carbon! Lets consider a sample with C-H. The population difference between $\alpha$ and $\beta$ state depends on energy difference also called [[Gyromagnetic ratio (γ)]]. If we excite C directly, only 1/4 of them will be excited as this energy difference is small so there are fewer to excite. If we instead excite H we get 4x as many excited! 4x signal amplification for carbon! H -> N gets 10x! However we lose things not directly bound to hydrogen.

small problem, spectrum will look like this:
![[Pasted image 20260527114204.png]]

HOWEVER WE CAN FIX THAT! With refocused INEPT. We just let it run for a bit, then flip it! This is like the car analogy in [[The Spin-Echo sequence - Refocusing sequence]], we move forward, then back. However, this time we changed the sign! It works like this, and i will start using [[c,s Notation]]
![[c,s Notation#c,s Notation]]

![[Pasted image 20260527115020.png]]

end of inept, before180, after180, FID
a: $2C_yH_z$
b: $2C_yH_z\cdot c - C_x \cdot s$
180 on all
c: $2C_yH_z\cdot c + C_x \cdot s$
d: $c \cdot [2C_yH_z\cdot c - C_x \cdot s] + s \cdot [C_x \cdot c + C_y \cdot s ]$

simplify
$2C_yH_z\cdot[c^2]$
$C_x\cdot[-c\cdot s + c \cdot s]$
$C_y \cdot [s]$

As we set  $\tau = \frac{1}{2\cdot J}$, c becomes 0 and s becomes 1.

![[Pasted image 20260527130507.png]]
We can stack INEPTS!
![[Pasted image 20260527130646.png]]

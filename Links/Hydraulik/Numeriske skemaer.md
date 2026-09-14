#hydraulik 
![[Pasted image 20260914093728.png]]
Vi diskretere tid og position (duh). Mange metoder til at bruge disse skemaer, men som regel er det simulering så vidt jeg forstår. Her er der 3 typer beregninger: FTCS FTBS og CTCS hvoraf CTCS klart er bedre.

Ligninger FTCS:
$C_i^{n+1} = C_i^n + \left(-u \cdot \frac{C_{i+1}^n - C_{i-1}^n}{2\Delta x} + D \cdot \frac{C_{i+1}^n - 2C_i^n + C_{i-1}^n}{\Delta x^2}\right) \cdot \Delta t$

hvor:
- u er hastighed
- D er diffusionskoefficient
- $\Delta X$ er afstand mellem punkter
- i er pos index
- n er tidsindex

![[Pasted image 20260914113157.png]]
Eller på denne form hvor a og b antages at være 1 for at få den ovenstående

C kan tolkes fra ovenstående figur (de hedder de j) ellers kan de ses her:
![[Pasted image 20260914112958.png]]
Hvor de røde er de tal den interagere med (+ u dt dx a og b)

FTBS
$C_i^{n+1} = C_i^n + \left(-u \cdot \frac{C_{i+1}^n - C_{i-1}^n}{\Delta x} + D \cdot \frac{C_{i+1}^n - 2C_i^n + C_{i-1}^n}{\Delta x^2}\right) \cdot \Delta t$

![[Pasted image 20260914111146.png]]

CTCS
$$ \frac{\partial u}{\partial t} = k * \frac{\partial^2 u}{\partial x^2} $$ $$ \frac{u_j^{n+1} - u_j^n}{k} = \frac{1}{2} \left( \frac{u_{j+1}^{n+1} - 2u_j^{n+1} + u_{j-1}^{n+1}}{h^2} + \frac{u_{j+1}^n - 2u_j^n + u_{j-1}^n}{h^2} \right) $$ $$ (1 + 2r)u_j^{n+1} - ru_{j-1}^{n+1} - ru_{j+1}^{n+1} = u_j^n $$
Testes med flg:
$Cr_d = \frac{D\Delta t}{\Delta x^2}$
$Cr_c = \frac{u\Delta t}{\Delta x}$
$Pe = \frac{u\Delta x}{D}$
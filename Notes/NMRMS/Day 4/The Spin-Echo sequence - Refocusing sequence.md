#nmrms
What it does: THIS IS EXCITING! THIS MEANS AT STEP B AND E WE HAVE THE SAME NUMBER!!! Thereby, we can store magnetization in the x-y plane and eliminating chemical shift evolution between the two points. This is useful for facilitating coupling and such.

![[Pasted image 20260527105611.png]]

To track what we get from a sequence, we define points before and after each pulse as well as before the FID. So pre90 = a, post90 = b, pre180 = c, post180 = d, and preFID = e.

a: $I_z$
b: $I_{-y}$
Assuming no coupling nor relaxation (only chemical shift evolution)
![[Chemical shift evolution#Eq 1]]

c: $-I_y\cdot cos(\omega\cdot\tau_1)+I_x \cdot sin(\omega\tau_1)$

next we apply 180 degree pulse from y, y is unaffected, x gets flipped:
d: $-I_y\cdot cos(\omega\cdot\tau_1)-I_x \cdot sin(\omega\tau_1)$

½Lastly, we wait again so we apply chemical shift evolution again. The evolution from part 1 can be factored out as it is a constant.
$cos(\omega\cdot\tau_1) \cdot [-I_y \cdot cos(\omega\tau_2) \cdot I_x \cdot sin(\omega\tau_2)]+sin(\omega\tau_1)\cdot[-I_x \cdot cos(\omega\tau_2) \cdot -I_y \cdot sin(\omega\tau_2)]$

Say we decide $\tau_1=\tau_2$, now we can collect some terms. What is applied onto $I_x$ and $I_y$?
$$I_x \cdot [cos(\omega\tau) \cdot sin(\omega\tau) - cos(\omega\tau) \cdot sin(\omega\tau)]=0$$
$$I_y \cdot [-cos(\omega\tau)^2-sin(\omega\tau)^2]$$
we know $cos(x)^2+sin(x)^2=1$
$$I_y \cdot 1$$
e: $-I_y$

THIS IS EXCITING! THIS MEANS AT STEP B AND E WE HAVE THE SAME NUMBER!!! Thereby, we can store magnetization in the x-y plane and eliminating chemical shift evolution between the two points. This is useful for facilitating coupling and such.

Analogy:
![[Pasted image 20260527105029.png]]
Two cars driving out and back, speed doesnt matter as long as it is constant.

 $\tau \, 180 \, \tau$ sequence that makes sure coupling doesn't happen during a time.
 
![[Pasted image 20260527105029.png]]
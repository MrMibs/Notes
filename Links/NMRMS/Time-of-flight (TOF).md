In TOF we have ion generation region "sample holder" here MALDI. Then we accelerate ions using a magnetic field and the voltage accelerates ions based on their charge and the higher the mass the slower they fly:
![[Pasted image 20260528160426.png]]

$$\frac{m_i}{z}=\frac{2 \, e \, U \, t^2}{s^2}$$
where
- e is electron charge \[C]
- U is accelerating voltage \[V]
- s is distance in a field-free flight tube \[m]
- t is time of flight \[s]
- $m_i$ is mass of analyte \[Kg]
Since e, U, and s are constant, we can find m/z as a function of t.

Just doing this is called linear mode. Acceleration might start at slightly different times
![[Pasted image 20260528160958.png]]
This will be a huge problem for our resolution. Therefore we use reflector mode. 
![[Pasted image 20260528161116.png]]
This works because the higher the initial velocity, the deeper into the reflector the analytes penetrate, which means their earlier arrival is counteracted 1-1 by the deeper penetration, allowing for identical flight times for identical m/z ratios.
![[Pasted image 20260528161314.png]]
This is great for resolution! We however lose signal and get higher signal/noise due to post source decay. This is because not all molecules stay stable after excitation. This means some molecules will decay before they are reflected, leading to increased noise and lower signal. However, still good, what is left is not decayed.

You can keep doing this!
![[Pasted image 20260528161654.png]]
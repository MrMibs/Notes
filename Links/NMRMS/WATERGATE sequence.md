#nmrms
Not really a pulse sequence on its own. Using gradients from [[Field gradients I-II]] we know for any observable signal
$$\sum_iG_i\tau_i\gamma_ip_i=0$$
So this sequence
![[Pasted image 20260527170126.png]]
Creates a phase difference, then inverts it for everything that is not water. Here, however, we don't invert water which lets us remove it from the sample, as its net magnetization is not 0 because coherence order doesn't change.

Water signal is normally 100000x the signal of the sample you are interested in, which makes it really useful, however atoms with the same chemical shift as water also disappear.
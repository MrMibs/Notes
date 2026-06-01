#nmrms
In 1d we have waiting time, excitation, acquisition of data. In 2D we need to acquire data twice! In 2d we do

1. Preparation: Any pulse sequence really
2. Evolution: We record the first spectrum
3. Mixing: We need to transfer magnetization to make sure we have our correlation
4. Acquisition: The FID
![[Pasted image 20260527134056.png]]
Example of [[EXCY sequence]]:

![[Pasted image 20260527134418.png]]
Here we do a 90 degree pulse evolution and time itself is our mixing. This mixing allows for exchange, meaning we would get a spectrum like this shown where 50% remain in their initial positions and 50% are exchanged. In the real signal we would have the mix of these and we would see the cross peaks.
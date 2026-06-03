#nmrms

How do we go from MS1 to MS2?
![[Pasted image 20260603101358.png]]
In reality it is not that pretty
![[Pasted image 20260603101504.png]]
To select MS1 fragments we do either untargeted analysis / discovery mode. This allows us to identify all proteins in sample. We go fish! Here we create large datasets and need a lot of computing power to interpret this. 
![[Pasted image 20260603101737.png]]

If we got through all these peaks sequentially, start with the ones marked on the left then mark new ones on the right, we can go through a lot of them.
![[Pasted image 20260603101819.png]]
This takes time. But modern spectrometers can do this in the millisecond range. To get high equality data however we need to trap ions which means we have to wait, but if we wait too long we ruin the sample. (this is called the exclusion time). To overcome the problem of relying on initial data and having to go through each and this taking time we can do Data-independent acquisition, DIA.
![[Pasted image 20260603102105.png]]
Here you do a wider bandpass.
![[Pasted image 20260603102128.png]]
Allowing us to separate bandwidths of m/z values which means we don't rely on selection. This also takes a lot shorter as we don't have to do MS2 on each peak but instead do it on wider sections. This seems complex. Comparison:
![[Pasted image 20260603102330.png]]
DIA MS has a lot of methods
![[Pasted image 20260603102345.png]]
They differ based on selection window definition.

---

![[Pasted image 20260603102658.png]]
You can combine DDA and DIA using a long gradient in chromatography (LC) which gives ad DDA analysis matched to a database search, which tells us what we are interested in. We can then do DIA.

If you have bad MS2 spectra you will have less coverage of B and Y ions which only allows us to get fragments of the wanted information. 
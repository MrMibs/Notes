#nmrms

MS IS NOT QUANTITATIVE! Ions do not ionize the same way and they have different flyability. Also in-source fragmentation and post source decay. Amounts are NOT related to the peak intensity:
![[Pasted image 20260603105944.png]]

Response is orders of magnitude different
![[Pasted image 20260603110058.png]]

Can we correct for intensity to find concentration? Using a ML model we at AAU try to predict intensities based on structure. Some important factors:
![[Pasted image 20260603110226.png]]

Also peptide features have an effect. If we take local environment into account we get different results, but not that different. 
![[Pasted image 20260603110402.png]]
Here charge and hydrophobicity is important for both but charge is more important on the second one. We can also guess how well they fly:
![[Pasted image 20260603110436.png]]
The yellower the more correct our predictions.

---

Workflow summary:
Chromatography -> MS1 for specific peak -> fragment -> MS2 for specific peaks in MS1. Based on MS2 we predict peptide candidates and then filter each peptide to a specific signal. We can then identify proteins based on which peptides we di
![[Pasted image 20260603110757.png]]


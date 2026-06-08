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

![[Workflow summary]]

If we can quantify peptides we can quantify proteins! We want to do it untargeted too!
![[Pasted image 20260603111142.png]]
We typically do this using labeling.

Spiked: We introduce a known concentration of an enriched version of a peptide allowing us to quantify the amount based on the signal from the known peptide concentration. Here we assume they are intensity-wise identical pr concentration.

We can also tag the proteins using stable isotope labeling with amino acids in cell culture (SILAC). Here we supply our samples with either heavy or light arginine (13C). We mix them 1:1 and we do the MS/MS analysis in one go, which gives us 2 different responses and we can compare the relative amount of each.
![[Pasted image 20260603111431.png]]

We can also tag later using isobaric tags, TMT and iTRAQ. This works by having the samples we want to compare. We put them onto the peptides The mass of the peptide needs to be the same so we can select them in MS1 as we wanted to. Then when we fragment in MS2 we can identify these reporter balance and reactive groups.
![[Pasted image 20260603111552.png]]
This is e.g. done using TMT
![[Pasted image 20260603111719.png]]

iTRAQ is the same
![[Pasted image 20260603111814.png]]
You need to mix 1:1 to get accurate samples
![[Pasted image 20260603111852.png]]

We can also do label-free. This requires some assumptions. A common way is using maxLFQ algorithm which assumes most proteins and peptides are the same except what we change during treatment. We can then use intensity of precursor ions allowing us to do a sophisticated normalization.
![[Pasted image 20260603112011.png]]

Alternatively we can to topN. This means we take the top N most intense precursor ions and take the average. We then divide it by the sum of top3 for all proteins.
![[Pasted image 20260603112052.png]]

iBAQ does the same
![[Pasted image 20260603112225.png]]
But iBAQ is seen proteins and sum iBAQ is the expected. You then normalize to expected values.

---

MALDI-TOF imaging.
You cut small tissue samples onto the matrix
![[Pasted image 20260603112510.png]]
Then you track specific areas (dotted with red), your cut samples. Then you get a 2d image. More slices gives you a 3d image. When you make this image you track intensity of something, so you need to know what you image to know how you look for patterns in it.

Microbiological profiling is also possible. This is done using pattern ID and database searching. If we have microbes we shoot they will have different things in their surface. This is kind of like a barcode and very characteristic. We can then profile microorganisms.
![[Pasted image 20260603112817.png]]



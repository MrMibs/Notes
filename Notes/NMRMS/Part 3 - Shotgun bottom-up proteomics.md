#nmrms
Proteomics is the investigations of proteins present in e.g. an organ in a specific time but also useful for finding enzymes for certain tasks and cell response to medical treatment. Large scale industrial processes with enzymes

Why is this useful? Cant you sequence genome? When we move from the genome to the transcriptome we can find more interesting thing from the initial products. There are also post-translation modification which means we can generate >1.000.000 proteins. Therefore proteomics allows us to investigate information about the current state of an organism instead of the potential state.
![[Pasted image 20260603093610.png]]
Modes in proteomic analysis

Top-down - MS1 then MS2, we fragment the protein and compare to full protein
Bottom-up - We cut up the protein (digest) and seperate them with LC allowing us to generate MS1 and MS2 spectra. We need LC or we will drown in MS2
Shotgun (bottom-up) - Digestion -> LC (we need to separate them as there is A LOT)


![[Pasted image 20260603093915.png]]



Workflow in BUP (bottom up proteomics)
![[Pasted image 20260603094158.png]]
1. Digest / treat proteins to get peptides
2. chromatography and separate by time
3. Pick out a time and do MS on it
4. Pick fragments we want with LIT, fragment it and do MS2
5. Database searching (software does this), genome gives a lot of information the database needs

Protein mixtures are difficult due to size since they are big, but if we cut them into peptides and they are now easier to study. We want them to be 6-30 amino acids. They need to be below 30 because that is the entire point, but they need to be above 6 amino acids. This is because sequences of less than 6 amino acids don't really tell us anything as that could be millions of proteins.

To cleave proteins we either
1. reduce and alkylate them (by binding to the 3')
2. Chemically cleave them using CNBr which cleaves C-terminal of Met (amino acid). Too large for bottom-up, but this is followed up by ->
3. Enzymatic cleavage using trypsin, which cleaves after only Argenine R and Lysine K which gives predictable fragments. Also good for nicely-sized peptides. Also creates R or K (positively charged) at the C terminus and N terminus is always positive which gives us 2 positive charges on each fragment.

Peptides are fragmented into 3 sets of ions depending on the nature of the disrupted bond. a b c or x y z.
![[Pasted image 20260603100152.png]]

Fragmentation is done using either collision, electron or photon. Depending on what we use we get different fragments
![[Pasted image 20260603100312.png]]
Collision is most commonly used. For collision we get these fragments:
![[Pasted image 20260603100334.png]]
Based on which we break we can get different fragments
![[Pasted image 20260603100408.png]]
Because of the terminal the species will look slightly different. Depending on if we look at B or Y we calculate using these equations:
![[Pasted image 20260603100623.png]]
For amino acids we know:
![[Pasted image 20260603100808.png]]

--- 

Workflow
1. Create spectrum
![[Pasted image 20260603100838.png]]
Ask quadrupole to isolate it (done on qTOF)
![[Pasted image 20260603100901.png]]
We then fragment it
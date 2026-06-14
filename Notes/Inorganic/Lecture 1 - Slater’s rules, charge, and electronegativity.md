#inorganic
[[Electron configuration table]]
3 bond types exist:
![[Pasted image 20260609102740.png]]
Ionic bonds, where atoms donate electrons to each other
Covalent bonds where they share electrons
Metallic bonds where electrons are kind of everywhere

To predict which bond type you have, you typically use 2 values:
(a) First ionization energy
(b) Electron affinity

First ionization energy is given as  $A(g) \rightarrow A^+(g)+e^- \quad \Delta H>0$ and for different atoms this is:
![[Pasted image 20260609103014.png]]

Factors affecting this is
1. Attraction, positive attracts negative, core attracts electrons
2. Shielding, electrons push each other away

In e.g. Helium we have 2 electrons close to the core and they are on opposite sides so they push each other away. In Li however we have a third electron that is shielded by inside electrons and the core hasn't gotten significantly stronger which explains the trend seen.

Slater proposed a way to calculate the effective nuclear charge, taking shielding and attraction into account to create a model of the attraction seen.
$$Z_{eff}=Z-\sigma$$
where:
- $Z_{eff}$ is the effective nuclear charge
- $Z$ is the atomic number (amount of protons = attraction)
- $\sigma$ is the Slater's shield constant
e.g.
He: $Z_{eff}=2-0.30=1.70$
Li: $Z_{eff}=3-(0.85\cdot 2)=1.30$

Spin has a lot of orientations and nuances, how do we take orbitals into account?

**Very formally**
1. All electrons in orbitals of greater principal quantum number contribute 0.
2. Each electron in the same principal quantum number contributes 0.35, except for the (1s) group, where the other electron contributes only 0.30.
3. If the reference is a ns or np electron, we count 0.85 for each electron with principal quantum number (n–1), and 1.00 for each electron with principal quantum number (n–2) or less.
4. If the reference is a nd or nf electron, we count 1.00 and for electrons with principal quantum number n and a smaller azimuthal quantum number l, and for from each electron with principal quantum number (n–1) or less.
![[Pasted image 20260609104048.png]]

In practice:
Step 1: Write the electron configuration, separating the different sub-
shells: e.g. (1s) (2s, 2p) (3s, 3p) (3d) (4s, 4p) (4d) (4f) (5s, 5p) . . .
Step 2: Identify the electron of interest, and ignore all electrons in higher groups, because, these do not shield electrons in lower groups
Step 3: Use the Slater's Rules. Be aware that rules for s or p electron are different from those for a d or f electron.
![[Pasted image 20260609104048.png]]

Example: Calculating effective nuclear charge on the outer shell electrons of Sodium 1s$^2$ 2s$^2$ 2p$^6$ 3s$^1$
Here we look at 3s$^1$, which means we have 0 electrons in the same shell, 8 in the shell below and 2 in the shell below that.
$0\cdot 0.35+8\cdot0.85+2\cdot1=8.80$

Which means we can calculate effective nuclear charge as $Z_{eff}=Z-\sigma=11-8.80=2.20$. It is, however, not always clear what is higher and lower in energy. Therefore, we need to look at quantum numbers. Here we have: 

| Quantum number                                  | Allowed values  | Meaning                                                                                  |
| ----------------------------------------------- | --------------- | ---------------------------------------------------------------------------------------- |
| Principal quantum number (n)                    | 1, 2, 3, 4, ... | Defines the energy level (shell) and average distance from the nucleus.                  |
| Azimuthal / Angular momentum quantum number (l) | 0 → n−1         | Defines the subshell and orbital shape. l = 0 (s), 1 (p), 2 (d), 3 (f).                  |
| [[Magnetic quantum number (m)]]                 | −l → +l         | Defines the orientation of an orbital in space.                                          |
| Spin quantum number (mₛ)                        | +½, −½          | Defines the electron spin orientation ("spin up" or "spin down"). (2 electrons pr shape) |
note quantum number also called $m_I$ and we know this from NMR. Then the values of the slater shield constants are given as:

| Electron of interest | Electrons in same group (n=n) | n=n and angular quantum number < l | Electrons in group(s) with principal quantum number n−1 | Electrons in all group(s) with principal quantum number < n−1 |
| -------------------- | ----------------------------- | ---------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------- |
| [1s]                 | 0.30                          | 0                                  | 0                                                       | 0                                                             |
| [ns, np]             | 0.35                          | 0.85                               | 0.85                                                    | 1.00                                                          |
| [nd] or [nf]         | 0.35                          | 1.00                               | 1.00                                                    | 1.00                                                          |

Where the third column means "Electrons in the **same shell** but in orbitals with **lower angular momentum** than the electron you're calculating $Z_{eff}$ for." So nd and nf counts everything below it as 1. e.g.
$$Nd = [Xe] \, 4f^4 \, 6s^2$$
Say we look at 4f we get 3 in the same shell, 54 below from Xe and the 6s$^2$ electrons are also counted as they are written to the left of 4f$^4$:
1s² 2s² 2p⁶ 3s² 3p⁶ 4s² 3d¹⁰ 4p⁶ 5s² 4d¹⁰ 5p⁶ 6s² 4f⁴

Thereby we get:
$$54 \cdot 1 + 2 \cdot 1 + 3 \cdot 0.35= 57.05$$
Further, ionic radii can be estimated from this value, thereby:
![[Pasted image 20260609113305.png]]

This leads to the concept of Electronegativity, which is "the power of an atom in a molecule to attract electrons for itself". It is calculated as the geometric average of the dissociation energy between a bond with 2 of the same atoms:
$$D(A-B) = \sqrt{D(A-A) \times D(B-B)}$$
where
- D(A-B) is the dissociation energy of the A-B bond
- D(A-A) is the dissociation energy of the A-A bond
- D(B-B) is the dissociation energy of the B-B bond

e.g.
D (Cl2) = 242 KJ mol$^{-1}$
D (H2) = 432 KJ mol$^{-1}$
$$\sqrt{242 \cdot 432}=323 \, kJ/mol$$
This is an estimate and far off due to not considering the polar contribution, which in this case is **105kJ/mol!!!!!!**.

For the sake of having it we also have Allred-Rochow electronegativity scale 
$$\chi^{AR} = 3590 \frac{Z_{eff}}{r_{cov}^2} + 0.744$$ (radius expressed in pm = 0.01Å)

![[Pasted image 20260609114141.png]]

And Bond continuum / bond triangle
![[Pasted image 20260609114154.png]]
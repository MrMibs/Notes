Ja — det her er faktisk en **meget god opgave til at forstå præcis det, vi lige har snakket om**. Lad os tage den trin for trin og især koble den til kontrolvolumen.

## Først: hvad sker der fysisk?

Vi har:

```text
Reaktor 1                         Reaktor 2
C = 50 mg/L                       C = 0 mg/L
   │                                  │
   ▼                                  ▼
   ┌─────────────── 20 cm ───────────────┐
   │                                     │
   │      diffusion → → →               │
   └─────────────────────────────────────┘
                 A = 1 cm²
```

Der er **ingen advektion**:

u=0u=0

Så vores ligning er bare:

∂C∂t=D∂2C∂x2\boxed{ \frac{\partial C}{\partial t} = D\frac{\partial^2C}{\partial x^2} }

---

# 1. Massebalance for ét kontrolvolumen

Forestil dig én af vores små celler:

```text
             kontrolvolumen i
       ┌─────────────────────┐
       │                     │
───────┤         Cᵢ          ├───────
       │                     │
       └─────────────────────┘
       i-½                   i+½
```

Vi laver:

ophobning=ind−ud\text{ophobning} = \text{ind} - \text{ud}

Der er kun diffusion.

Fra Ficks lov:

J=−D∂C∂xJ=-D\frac{\partial C}{\partial x}

Så massebalancen bliver:

AΔxdCidt=AJi−12−AJi+12A\Delta x\frac{dC_i}{dt} = A J_{i-\frac12} - A J_{i+\frac12}

A går faktisk ud på begge sider:

ΔxdCidt=Ji−12−Ji+12\boxed{ \Delta x\frac{dC_i}{dt} = J_{i-\frac12}-J_{i+\frac12} }

Det er den **fysiske massebalance**, som I derefter skal lave numerisk.

---

# 2. Hvordan udvikler koncentrationsprofilen sig?

I starten:

```text
C
↑
50│●
  │ \
  │  \
  │   \
  │    \
  │     ●
 0└────────────→ x
  reaktor 1    reaktor 2
```

Altså:

C(0,t)=50C(0,t)=50

og:

C(0.20,t)=0C(0.20,t)=0

Efter noget tid begynder farvestoffet at sprede sig:

```text
50│●───
  │   ╲
  │    ╲
  │     ╲
  │      ╲___
 0│          ●
  └────────────→ x
```

Efter endnu længere tid bliver profilen mere og mere jævn.

Til sidst er den:

```text
C
↑
25│────────────────
  │
  │
  └────────────────→ x
```

Altså **25 mg/L overalt**.

Hvorfor 25?

Fordi de to reaktorer ender i ligevægt med samme koncentration:

Ceq=50+02=25 mg/LC_{eq}=\frac{50+0}{2}=25\text{ mg/L}

_forudsat at reaktorerne har samme volumen._

---

# 3. Initial- og randbetingelser

### Initialbetingelse

Ved $t=0$ er røret fyldt med rent vand, så:

C(x,0)=0\boxed{C(x,0)=0}

for $0<x<0.20$ m.

### Randbetingelser

Reaktorernes koncentrationer holdes konstant:

C(0,t)=50 mg/L\boxed{C(0,t)=50\text{ mg/L}} C(0.20,t)=0 mg/L\boxed{C(0.20,t)=0\text{ mg/L}}

Det er meget vigtigt:

**Randbetingelserne ændrer sig ikke med tiden**, fordi opgaven siger, at reaktorerne hele tiden udskifter vand.

---

# 4. Fem kontrolvolumener

Nu kommer den del, forelæseren sandsynligvis prøver at lære jer.

Røret er:

L=0.20 mL=0.20\text{ m}

Vi deler det i 5:

Δx=0.205=0.04 m\Delta x=\frac{0.20}{5}=0.04\text{ m}

Så:

```text
50 mg/L                                  0 mg/L
   │                                        │
   ▼                                        ▼
   ┃  CV1  ┃  CV2  ┃  CV3  ┃  CV4  ┃  CV5  ┃
   ┃        ┃        ┃        ┃        ┃        ┃
   ┃   C₁   ┃   C₂   ┃   C₃   ┃   C₄   ┃   C₅   ┃
   ┃        ┃        ┃        ┃        ┃        ┃
   ─────────────────────────────────────────────→ x
       0.04     0.04     0.04     0.04     0.04 m
```

For celle 3:

ΔxdC3dt=J2.5−J3.5\Delta x\frac{dC_3}{dt} = J_{2.5}-J_{3.5}

Hvis vi approksimerer gradienterne:

J2.5=−DC3−C2ΔxJ_{2.5} = -D\frac{C_3-C_2}{\Delta x}

og:

J3.5=−DC4−C3ΔxJ_{3.5} = -D\frac{C_4-C_3}{\Delta x}

så får vi:

ΔxdC3dt=DC2−C3Δx−DC3−C4Δx\Delta x\frac{dC_3}{dt} = D\frac{C_2-C_3}{\Delta x} - D\frac{C_3-C_4}{\Delta x}

og dermed:

dC3dt=DC2−2C3+C4Δx2\boxed{ \frac{dC_3}{dt} = D\frac{C_2-2C_3+C_4}{\Delta x^2} }

**Kan du se forbindelsen til det, vi snakkede om før?**

Det er præcis:

∂2C∂x2≈Ci+1−2Ci+Ci−1Δx2\frac{\partial^2C}{\partial x^2} \approx \frac{C_{i+1}-2C_i+C_{i-1}}{\Delta x^2}

Control Volume-metoden har altså givet os den samme slags udtryk ved at lave en **massebalance omkring hver celle**.

---

## 5. Hvor lang tid tager det?

Her skal man være lidt forsigtig med formuleringen **"koncentrationsprofilet ikke ændrer sig længere"**.

Matematisk når diffusionen til ligevægt **asymptotisk** — den bliver aldrig helt præcis konstant efter en endelig tid.

Så i en numerisk model skal I vælge en tolerance, fx:

> "Vi definerer ligevægt som det tidspunkt, hvor ændringen er mindre end 0,01 mg/L."

Med:

D=3×10−3 m2/sD=3\times10^{-3}\text{ m}^2/\text{s}

og:

L=0.20 mL=0.20\text{ m}

er den karakteristiske diffusionstid omtrent:

t∼L2Dt\sim\frac{L^2}{D} t∼0.2023×10−3t\sim\frac{0.20^2}{3\times10^{-3}} t≈13.3 st\approx13.3\text{ s}

Så **størrelsesordenen er sekunder**, ikke minutter eller timer.

Den præcise tid til jeres valgte tolerance skal findes fra den numeriske model.

---

# 6. Hvad hvis $D=3\times10^{-10}$?

Her bliver det rigtig tydeligt, hvad diffusionskoefficienten betyder.

Vi har:

t∼L2Dt\sim\frac{L^2}{D}

Så hvis $D$ bliver:

3×10−33×10−10=107\frac{3\times10^{-3}}{3\times10^{-10}} = 10^7

gange mindre, bliver diffusionstiden:

107 gange længere\boxed{10^7\text{ gange længere}}

Den karakteristiske tid bliver derfor:

13.3 s×107≈1.33×108 s13.3\text{ s}\times10^7 \approx1.33\times10^8\text{ s}

eller cirka:

4.2 a˚r\boxed{4.2\text{ år}}

Det er en **meget vigtig fysisk pointe**:

> Diffusion over en afstand $L$ tager omtrent en tid proportional med $\frac{L^2}{D}$.

Så selv en lille ændring i $D$ kan have enorm betydning for, hvor hurtigt systemet når ligevægt.

### Og det vigtigste fra hele opgaven

Opgaven tager jer igennem præcis denne kæde:

Fysisk system→massebalance→kontrolvolumener→numeriske ligninger→Excel/MATLAB\boxed{ \text{Fysisk system} \rightarrow \text{massebalance} \rightarrow \text{kontrolvolumener} \rightarrow \text{numeriske ligninger} \rightarrow \text{Excel/MATLAB} }

Det er **Control Volume-metoden i praksis**.
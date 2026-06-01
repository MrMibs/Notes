#datascience
2 types of signals exist, digital and analog signals. Package size can be e.g. 8 bit $$00010010$$This 8 bit package size would result in a 10 bit signal as we need a startbit (0) and an end bit (1) (i think they call this 8 bit in the exam)
$$0 \, 00010010 \, 1$$
The first one is used as it differes from the idle signal which makes it possible to discern between noise and signal. The stop one idk. Idle signal:
$$1111111111$$
Data transfer is denoted as bit pr. sec. Example:
![[Pasted image 20260529110457.png]]

Computers use exclusively digital signals. Analog signals are continuous and lose precision when converted to digital signals. Bits can be converted to resolution as:
$$Resolution = \frac{Range \, of \, data}{2^{bitcount}}$$
![[Pasted image 20260529111705.png]]

Thereby resolution can be increased by lowering the range of data or increasing the amount of bits. (or calibrating the component or measuring within the calibration range)
Say you calibrated your signal to be 1V=0C 5V=100C
$$T=25 C/V \cdot U-25C$$
For a 12 bit signal, this calibration would lead to a resolution of
$$Resolution(V)=\frac{5V}{2^{12}}\cdot \frac{25 \degree C}{V}=0.03\degree C$$
where we split the voltage into each voltage sized bin and convert this voltage bin to a signal size. 

---

# Example with A -> V conversion 

An Arduino can read signals in the 0-5V range. Thereby lets say we have a pressure sensor with an exit current of 4-20mA (0,004-0,02A). This needs to be converted to the 0-5V range using ohms law.
$$U = R \cdot I$$
where
- U is voltage \[V]
- I is amperage \[A]
- R is resistance \[$\omega$]

Thereby we solve for R
$$R = \frac{U}{I} = 5V/0.02A = 250 \Omega$$
Which sets 1V to 4mA and 5V to 20mA. For this, the resolution would be:
$$Resolution(V)=\frac{5V}{2^{10}}\cdot \frac{1.2 bar}{V}=0.005859375 bar$$
As 5V/2^10 is the amount of discrete packages and we measure 6 (0-5) bar using 5 volts (1-5).

---

If the resistance was e.g. 10 ohm
$$10\Omega \cdot 0.004A-0.02A = 0.04-0.2V$$
Thereby:
$$\frac{5 \, bar}{0.16 \, V}=31.25 \, bar/V$$
And
$$Resolution(V)=\frac{5V}{2^{10}}\cdot \frac{31.25 bar}{V}=0.153 bar$$
Where the calibration curve is
$$31.25 \, bar/V \cdot (U-0.04V) \, bar$$
and we subtract 0.04 as that is the voltage at 0 bar.



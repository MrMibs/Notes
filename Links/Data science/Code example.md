#datascience
![[Pasted image 20260529132219.png]]
![[Pasted image 20260529132155.png]]

What each line does
1+3-5 initiates variables with their [[Data types]]. 
2 sets flow sensor pin to 2.

10 starts setup
12 sets pin 2 to input
13 sets voltage level to high
14 begins serial monitor
15-16 allows interrupts
17 sets currentTime to milliseconds after arduino started running
18 sets "cloopTime" to be equal to "currentTime"

20 starts loop
22 sets current time to be time after Arduino started running
23-24 says if time between last override of cloopTime is >=1000 we start the loop.
26 updates cloopTime
28 converts pulse frequency to flowrate in L/h
29 resets counter for flow frequency
30-31 prints to serial monitor
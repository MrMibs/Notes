An exponential filter looks like this:
$$Y_F=\alpha Y_m+(1-\alpha)Y_{F-1}$$
where
- $Y_F$ is current weighted average
- $Y_m$ is latest measurement
- $Y_{F-1}$ is the last weighted average
- $\alpha$ is calibration value ranging from 1 (only last measurement) to 0 (ignore last measurement). A normal value would be like 0.6-0.8 as that would weigh the new measurement 60-80% and the old average 20-40%.

**Compared to a moving average** (across last 5 measurements) as it has a lower delay because you weigh new data higher than old data. $\alpha$ decides the weighting of new points in comparison to old points. As written above, if $\alpha=1$, we only care about last measurement.

---

In general, these filters let us increase measurement precision and lower spread at the cost of delaying new information.
![[Pasted image 20260529130308.png]]
Moving average takes the average of n measurements, if we increase the amount of data points we average over we increase precision and delay changes.
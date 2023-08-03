# RC Circuit Design and Simulation - README

Author: **Afzal Malik**
S.No.: **9**

## Objective
To design and simulate an RC circuit for the given cutoff frequency.

**Cutoff Frequency** (Fc) = (S.no. * 10) + 100 Hz  
So, Fc = 190 Hz

## Design
As we know, for an RC circuit:  
Fc = 1 / (2 * π * RC)

Assuming the value of the capacitor to be 1uF, then from the above formula:  
Value of Resistor (R) = 837.66 ohms  
Hence, RC time constant is 0.837 milisecond  

## Schematic in LT SPICE
Input given is the square pulse using the following command:  
`PULSE(0 5 0 1u 1u 6m 12m)`    
Suitable time period should be chosen for the Pulse Signal by observing the RC time constant.

![Schematic](https://github.com/afzalamu/LTSpice-Lab/assets/124300839/43510fdd-4c56-4780-ba39-6618ac976204)

## Simulation Results
This circuit will act as a Low Pass Filter with a cutoff frequency of 190Hz. We verify it using the simulation by performing AC analysis and plotting the Transfer Function with the following command:  
`.ac dec 10 1 250`

The simulation results were in accordance with the given specification, as Fc obtained from the Transfer Function graph is also 190Hz.

![Cutoff Frequency](https://github.com/afzalamu/LTSpice-Lab/assets/124300839/3fc975ed-ecbb-4182-989a-d2d7c96b2cb7)  

Now, as we know the capacitor gets fully charged in 5 * Time constant, and we will verify it using transient analysis and calculate the charging time of the capacitor from the resulting waveforms.  
Transient analysis is performed using:  
`.tran 15m`  
Suitable time period should be chosen in the above command by observing the time period of the given input pulse signal.  
![charge time](https://github.com/afzalamu/LTSpice-Lab/assets/124300839/1f561bb0-1e85-4d1e-b9b5-766f8ed587dd)  
From the resulting waveform, we can observe that the time taken to get the capacitor charged to its 99 percent value is near to 5 * RC time constant value, and hence the results are verified.

---
Feel free to reach out to the author for any questions or clarifications.  
Let's keep exploring and learning together! 😊

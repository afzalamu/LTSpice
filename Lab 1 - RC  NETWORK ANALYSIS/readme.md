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

## Schematic in LT SPICE
Input given is the square pulse using the following command:  
`PULSE(0 5 0 1u 1u 6m 12m)`  

This circuit will act as a Low Pass Filter with a cutoff frequency of 190Hz. We verify it using the simulation by performing AC analysis and plotting the Transfer Function with the following command:  
`.ac dec 10 1 250`

![Schematic](https://github.com/afzalamu/LTSpice-Lab/assets/124300839/43510fdd-4c56-4780-ba39-6618ac976204)

## Simulation Results
The simulation results were in accordance with the given specification, as Fc obtained from the Transfer Function graph is also 190Hz.

![Cutoff Frequency](https://github.com/afzalamu/LTSpice-Lab/assets/124300839/3fc975ed-ecbb-4182-989a-d2d7c96b2cb7)

---
Feel free to reach out to the author for any questions or clarifications.  
Let's keep exploring and learning together! 😊

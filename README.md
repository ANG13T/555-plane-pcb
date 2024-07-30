# 555 Airplane PCB with Astable Dual LED Flashing ✈️
A simple airplane PCB to teach the principles of the 555 timer IC and astable mode using blinking LEDs.

<img src="https://github.com/ANG13T/555-plane/blob/main/assets/preview.PNG" alt="Preview" width="800" />

## Schematic
<img src="https://github.com/ANG13T/555-plane/blob/main/assets/schematic.PNG" alt="Schematic" width="800" />

## PCB Design
<img src="https://github.com/ANG13T/555-plane/blob/main/assets/pcb.PNG" alt="PCB" width="500" />

## Bill of Materials
| Component                   | Link                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| 1x 3mm Red LED             | [Amazon Link](https://www.amazon.com/Diode-Lights-120Pcs-Emitting-Assorted/dp/B0BY28JTFC/ref=sr_1_4?sr=8-4) |
| 1x 3mm Green LED           | [Amazon Link](https://www.amazon.com/Diode-Lights-120Pcs-Emitting-Assorted/dp/B0BY2CZN7M/ref=sr_1_2?sr=8-2) |
| 1x 3mm White LED           | [Amazon Link](https://www.amazon.com/Diode-Lights-120Pcs-Emitting-Assorted/dp/B0BY2DDW65/ref=sr_1_5?sr=8-5) |
| NE555 IC                    | [Amazon Link](https://www.amazon.com/MCIGICM-ne555-Timer-Pulse-Generator/dp/B077BRB6W6/ref=sr_1_2?sr=8-2) |
| 10uF Electrolytic Capacitor| [Amazon Link](https://www.amazon.com/Capacitors-5x11mm-Aluminum-Electrolytic-Capacitor/dp/B0C4DHZV7J/ref=sr_1_5?sr=8-5) |
| 3V Coin Cell Battery        | [Amazon Link](https://www.amazon.com/LiCB-CR2032-Lithium-Battery-10-Pack/dp/B071D4DKTZ/ref=sr_1_8?sr=8-8) |
| 3V Coin Cell Battery Holder | [Amazon Link](https://www.amazon.com/bnafes-Surface-CR2032-Button-Battery/dp/B09KG8S6Z9/ref=sr_1_3?sr=8-3) |
| 100k ohm Axial Resistor    | [Amazon Link](https://www.amazon.com/EDGELEC-Resistor-Tolerance-Multiple-Resistance/dp/B07QK9793W/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| 2k ohm Axial Resistor      | [Amazon Link](https://amazon.com/EDGELEC-Resistor-Tolerance-Multiple-Resistance/dp/B07QJB31M4/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| SPDT Slide Switch          | [Amazon Link](https://www.amazon.com/HiLetgo-SS-12D00-Toggle-Switch-Vertical/dp/B07RTJDW27/ref=sr_1_2?sr=8-2) |
| 10k Potentiometer          | [Amazon Link](https://www.amazon.com/Potentiometer-Breadboard-Resistors-Assortment-Compatible/dp/B09G9TBY38/ref=sr_1_9?sr=8-9) |

## Design Analysis: Pulse Time and Duty Cycle Determination

The duty cycle of a circuit is ratio of the time the signal is active (high) to the total period of the signal. 
We want the duty cycle of this circuit to be close to 50% in order to get a congruent off/on blinking pattern form the airplane LEDs.

*R1:R2 ratio predominately is what sets the duty cycle for the circuit*

#### Output High Time Interval of Pulse

$$
t_h = ln(2) * (R_1 + R_2) * C
$$

#### Output Low Time Interval of Pulse

$$
t_l = ln(2) * R_2 * C
$$

Given the above equations describing the HIGH and LOW times of the pulse sequence, I was able to determine the resistor values for the PCB to be following:

```
R1 =

R2 = 
```

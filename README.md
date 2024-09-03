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
| 1.2k ohm Axial Resistor    | [Amazon Link](https://www.amazon.com/Resistor-Tolerance-Resistors-Limiting-Certificated/dp/B08QRLJJMC/ref=sr_1_2?crid=1XO8TBOSAJE5G&dib=eyJ2IjoiMSJ9.J3auG2H4WZTOObK24EMEwMHixvXQSgTAiXmCLPUavk8lEBMYc0UgROmcN-fGNpdqcrTDksYpao5EO3ZdPUwKgKXEfbjg4xZHU3bvYozqyGLjhxVkTzp7j7RoQ0sKGPukwDZppi5YI-SRhVc-4V5K9H3FRc-dGQocXg5JyDqY8zOzu9vHjxXS9hii6lWyJLlg60AJXZD8loqtqa-kVq2q2vHkEpv_SoRb3CLDACrcsNE.qBvZuAiz1Tx_7UBDNaSkkvGUZpht9CtA_XDBnFLCsCs&dib_tag=se&keywords=1.2k+ohm+Axial+Resistor&qid=1725355536&sprefix=1.2k+ohm+axial+resistor%2Caps%2C199&sr=8-2) |
| 90 ohm Axial Resistor      | [Amazon Link](https://www.amazon.com/Resistor-Tolerance-Resistors-Limiting-Certificated/dp/B08QRCQY4J/ref=sr_1_1?crid=2P65OJP9ZBERH&dib=eyJ2IjoiMSJ9.x79ivvPhUMsOgn0mwYi9Hb9uRK6pI78LsWD1ODuvME31esHscaQ3XmQ6eRmgyCy8LNcIgHTpyCCOhpXpfFwZ4K6o7sdwaiVad6_RpKEA4FGb4V3TpdmGCvB_mnqf3u24kWs74CwBAMsMFL_6uiWd0rEt5OHJ3l9ea84o8HbqdsTJDhKgy9QlfBLbPQ22ZGJuqqiGYy0TaaCtAksy3y2Xbt0wpDdHxEzHFQIcbKdhO80.uUqVKTISPma7kuN_FFYvuO3TUlLL1qIimxFYdXzapwc&dib_tag=se&keywords=90+ohm+Axial+Resistor%3A&qid=1725355502&sprefix=resistor+kit%2Caps%2C448&sr=8-1) |
| SPDT Slide Switch          | [Amazon Link](https://www.amazon.com/HiLetgo-SS-12D00-Toggle-Switch-Vertical/dp/B07RTJDW27/ref=sr_1_2?sr=8-2) |
| 100k Potentiometer          | [Amazon Link](https://www.amazon.com/Sscon-Breadboard-Potentiometer-Arduino-3386MP-104/dp/B07QZ67C2K/ref=sr_1_9?crid=2Q0OB7FIJKUU1&dib=eyJ2IjoiMSJ9.ALke2vkdw7lw76jKYVkSClADKMUWpDwLt9F9fBt9kANdQOxKkSMRoLvK76evAaEMBJGv3oWoc8ovCdX2RCvYZAAW5Tj4AbflrHdmW93cn4yD62liEbXnU9AmyE0mp6pLo1DvB4yUYAyy4ATBrHct-sTnE3Z8m04pFxvhDt6R8w5xZ76kbbcxzj4s_I2-FKSanbE5Ls2nP-mXaQ69XZrV-E2VMvNiinxDPVepDnqBE_I.dU7tQpuBAAKw9xvEH3SvLnyW_zsAgCWHLjo5D9JwQsY&dib_tag=se&keywords=trim%2B100k%2BPotentiometer&qid=1725355575&sprefix=trim100k%2Bpotentiometer%2Caps%2C143&sr=8-9&th=1) |

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

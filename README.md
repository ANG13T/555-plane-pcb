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
| 1.2k ohm Axial Resistor    | [Amazon Link](https://www.amazon.com/Resistor-Tolerance-Resistors-Limiting-Certificated/dp/B08QRLJJMC/ref=sr_1_1?dib=eyJ2IjoiMSJ9.bFnVsUm-rVIZ6nX8IE_TEPs7SgKgCY3qj1LEilxAHpuvGoYnb3mmiQbKKKpo_tM6u-t2sj83XdvzmXBt9RKYuscte5cM64rO5gwJF7Q2mJHEqQ6HsQSrPICmN9_nm_wJEFFB8QsNW6jEbVCV2X12iC20LLi6wLUwBakHlDmNA9R1VerKR5a2s5Ljt-hzVRfmMenS-k2R81ucrrkHRmhCZkBb2QShM-brWdWwz93MzvQ.LCsJyJAFStVPh2yPoYC7kh_r7XQRArlWfB6xSpTg1yc&dib_tag=se&keywords=1.2k+ohm+Axial+Resistor&qid=1726619978&sr=8-1) |
| 90 ohm Axial Resistor      | [Amazon Link](https://www.amazon.com/Resistor-Tolerance-Resistors-Limiting-Certificated/dp/B08QRCQY4J/ref=sr_1_1?crid=F2035RURHFBE&dib=eyJ2IjoiMSJ9.x79ivvPhUMsOgn0mwYi9HUloh9rnRkPpkXcuSqcw5OXEl9Cs1SuK7oR7BfTgjhcwOo_rqmqnKAM40pgPe2HuJyJLvH-tKOiYtoQv4_Z_gx0eyhZ2A_wuGBNZC3UL7YncR_JdDpczxGDcS4udbnNEJzen4JAIEpgiWtH1PSp4bgNQaFhoFz2KVE_hxS4hzb3GkhP3tD9eyJu9U71x6Od3G-ec5ASPbc3hb2fvMvKYevM.9YJKewUHyJnDPIFXBN1C6Bp7SCnlo2DcytGkNcYiPLE&dib_tag=se&keywords=90+ohm+Axial+Resistor&qid=1726619999&sprefix=1.2k+ohm+axial+resistor%2Caps%2C245&sr=8-1) |
| SPDT Slide Switch          | [Amazon Link](https://www.amazon.com/HiLetgo-SS-12D00-Toggle-Switch-Vertical/dp/B07RTJDW27/ref=sr_1_2?sr=8-2) |
| 100k Potentiometer          | [Amazon Link](https://www.amazon.com/Sscon-Breadboard-Potentiometer-Arduino-3386MP-104/dp/B07QZ67C2K/ref=sr_1_7?crid=1ZQ1S7PVZS21Z&dib=eyJ2IjoiMSJ9.ALke2vkdw7lw76jKYVkSCsz7yyM2giK0dFq_aH_VpgXj6_QP1JfsWtv0vz2UfV4qxAuq7Htfpj3h7HFThshZVkfJSjn-1LK_C05GDaOsFXdy7CHmUE8g6ZAux-A8Mg8fl7HIi1_cJc2JLeZ1H9VO_XPKU_RMg4UzblocHcNDzP0vG59jG24hv_xCvfZdxmIBon_iU5moHPPxIBydwMKM1kP2T3MDoluO-GZkw-gWJkg.H77FQo1L84C_nGlk5uuYeE7-Us3chvHOX5xWOAhK78I&dib_tag=se&keywords=100k+trim+Potentiometer&qid=1726620068&sprefix=100k+trim+potentiometer%2Caps%2C157&sr=8-7) |

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


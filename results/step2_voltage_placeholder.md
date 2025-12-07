Placeholder for Step 2 voltage plot (reverse polarity test).
Replace this file with step2_voltage.png after simulation.
![WhatsApp Image 2025-12-07 at 00 46 27_162d436b](https://github.com/user-attachments/assets/cd3641e9-b96b-4968-93c6-6df471f20875)

This test simulates a situation where a car battery is accidentally connected backwards.

In automotive systems, reverse polarity is a common mistake during:
Battery replacement
Jump-starting
Maintenance wiring
To protect the electronics, a series protection diode (D1) is added in the circuit.

Reverse Polarity Test – Output Voltage Response
The reverse polarity test evaluates the circuit’s behavior when the battery is connected backward. A series protection diode (D1) is used to block reverse current.The output voltage waveform remains stable at approximately 11.21 V, representing the expected diode forward voltage drop during normal conduction. When reverse voltage is applied, the diode becomes reverse-biased and prevents current flow, ensuring that the load is not exposed to negative or damaging voltages.The micro-level oscillations seen in the plot are simulation artifacts and not physical effects. Overall, the graph confirms that the reverse-polarity protection circuit is functioning correctly.

revrse polarity testing with negative potential as input 
![WhatsApp Image 2025-12-07 at 00 51 59_3a2c2055](https://github.com/user-attachments/assets/a86edc73-d61a-465d-a002-a090e2ff4098)

This test simulates the situation where the car battery is connected backwards, meaning the ECU receives –12 V instead of +12 V. If not protected, this condition can instantly destroy automotive electronics.
Reverse Polarity Test – Negative Input Voltage Response
In this test, the power supply is reversed by applying –12 V instead of +12 V. The reverse-polarity protection diode (D1) becomes reverse-biased and blocks all current flow into the circuit. As a result, the load voltage remains near 0 V, with the simulation displaying approximately –1.20 nV due to numerical rounding.This confirms that the protection diode prevents the negative input voltage from reaching the ECU load, ensuring that no reverse current flows and that sensitive components remain fully protected. The graph clearly validates the effectiveness of the reverse-polarity protection design.

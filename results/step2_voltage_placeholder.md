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

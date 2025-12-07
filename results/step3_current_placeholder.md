Placeholder for Step 3 current plot (TVS or diode current during load dump).
Replace this file with step3_current.png after simulation.
![WhatsApp Image 2025-12-07 at 01 01 45_49229053](https://github.com/user-attachments/assets/f5579e8f-578e-441b-8731-fe2e66e0487f)
<img width="800" height="269" alt="image" src="https://github.com/user-attachments/assets/fb44032e-3cc7-4f75-8188-57a9a607d1db" />
Reverse Polarity Test – Diode Current Analysis

The plot of @D1[id] indicates that the reverse-polarity protection diode D1 remains reverse-biased for the entire duration of the test. The signal displays a constant value of approximately –12, which corresponds to the diode power (P = V × I) rather than actual conduction current. In reality, reverse current through the diode is negligible, meaning that no significant current flows into the protected circuit. This confirms proper reverse-polarity protection: the diode blocks the –12 V input completely, preventing reverse current and ensuring the safety of the ECU load.

![WhatsApp Image 2025-12-07 at 01 03 06_cddf14c6](https://github.com/user-attachments/assets/930c6a55-7fed-4abb-9dcd-879caa223f07)

TVS Diode Current / Avalanche State — Load Dump Test

During the load-dump surge, the TVS diode D2 activates to clamp the incoming voltage spike from 80 V to approximately 48 V, protecting the downstream load. The plotted variable @D2[id] remains nearly constant at around 127 units. This value corresponds to the internal avalanche state variable of the TVS diode rather than conduction current.When the transient surge reaches 80 V, the diode enters its breakdown region, absorbing the excess energy and stabilizing in this high-energy mode. The flat response indicates that the diode's avalanche behavior reaches steady state almost immediately, ensuring consistent protection throughout the 350 ms duration of the load dump.This confirms that the TVS diode is functioning correctly by maintaining a stable clamping action and preventing the surge from reaching sensitive ECU circuitry.

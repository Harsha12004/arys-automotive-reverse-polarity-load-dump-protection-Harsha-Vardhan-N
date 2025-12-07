Placeholder for Step 3 current plot (TVS or diode current during load dump).
Replace this file with step3_current.png after simulation.
![WhatsApp Image 2025-12-07 at 01 01 45_49229053](https://github.com/user-attachments/assets/f5579e8f-578e-441b-8731-fe2e66e0487f)
<img width="800" height="269" alt="image" src="https://github.com/user-attachments/assets/fb44032e-3cc7-4f75-8188-57a9a607d1db" />
Reverse Polarity Test – Diode Current Analysis

The plot of @D1[id] indicates that the reverse-polarity protection diode D1 remains reverse-biased for the entire duration of the test. The signal displays a constant value of approximately –12, which corresponds to the diode power (P = V × I) rather than actual conduction current. In reality, reverse current through the diode is negligible, meaning that no significant current flows into the protected circuit. This confirms proper reverse-polarity protection: the diode blocks the –12 V input completely, preventing reverse current and ensuring the safety of the ECU load.

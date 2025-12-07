<img width="735" height="415" alt="image" src="https://github.com/user-attachments/assets/f95dd73d-2e6e-4004-9203-3f3af89ff968" />
Legend:
- VIN: input battery / test source
- TVS1: unidirectional TVS from VIN to GND (standoff ~13.3V)
- C1: bulk input capacitor (100uF, low-ESR)
- R3 + L1: optional surge resistor/inductor (damping for load dump)
- D1: fast diode from VIN to M1.D (optional for extra reverse blocking during extreme transients)
- M1: N-channel MOSFET (drain tied to VIN, source drives VOUT). Gate driven via Rg from VIN. A gate-source Zener (Z1) clamps Vgs to safe value (~12–15V).
- CLOAD: ECU input decoupling (10uF + 0.1uF ceramic)
- Add series fuse or current sense resistor in series with M1 source to record current.

Note: Place TVS1 & bulk cap physically close to VIN pin; place TVS2 (if used) across VOUT to GND.
fig.1 MOSFET-Based Reverse Polarity Protection With Gate Zener Clamp
<img width="557" height="499" alt="image" src="https://github.com/user-attachments/assets/c9ce6ea4-1721-430c-b3e7-eb18dc03c6b0" />
fig.2a and 2b Automotive Input Filter + MOSFET Protection
<img width="1210" height="642" alt="image" src="https://github.com/user-attachments/assets/a0094949-02dd-4c06-bbab-cacf9636d846" />
<img width="370" height="130" alt="image" src="https://github.com/user-attachments/assets/92b5145f-666c-4f39-913e-0f04892e0d6a" />
fig.3 the circuit diagram for ECU protection
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/27c2bf4f-a273-4c8e-9ee2-3bb724cf273f" />


Placeholder for Step 3 voltage plot (load dump test).
Replace this file with step3_voltage.png after simulation.

![WhatsApp Image 2025-12-07 at 00 38 19_2f80fc07](https://github.com/user-attachments/assets/5059d335-a764-40e5-b4b7-efe614ee1c3a)

1. Surge rises instantly from 12 V → 80 V at t = 2 ms
The input voltage (V(in)) jumps sharply to 80 V, simulating a real automotive load-dump event caused by alternator/regulator disconnection.This is normal behavior for a load-dump waveform.

2. Protected output clamps at ~27 V

Even though the input goes to 80 V, the protected output (V(mid)) rises only to around 27 V and remains stable throughout the surge.
This clamping occurs because:
The TVS diode enters avalanche breakdown at ~48 V
The series diode and load resistor divide the voltage
The TVS absorbs the surge energy and prevents damage downstream
This is exactly what a load-dump protection circuit must achieve.

3. At t ≈ 353 ms the surge ends (80 V → 12 V)

When the load-dump transient ends:
V(in) drops back to 12 V immediately
V(mid) settles smoothly back to normal load voltage (~11–12 V range depending on diode drop)
The circuit transitions cleanly with no ringing or overshoot, indicating good stability.

Load Dump Voltage Response – V(in) and V(mid)
The load dump simulation shows the expected surge from 12 V to 80 V at 2 ms. While the input voltage increases to 80 V, the protected output node (V(mid)) rises only to approximately 27 V due to the action of the TVS diode and the series protection diode.The TVS diode clamps the surge and absorbs excess energy, preventing high voltage from reaching the ECU load. Throughout the entire 350 ms surge duration, V(mid) remains stable and within a safe range.When the surge ends, the voltage at V(in) returns to 12 V, and V(mid) settles back to normal operating levels without overshoot. This confirms that the designed circuit successfully mitigates load-dump conditions, ensuring reliable protection for automotive electronics.

Arys Garage – Electronics / EEE Assignment
# arys-automotive-reverse-polarity-load-dump-protection-Harsha-Vardhan-N
Section A of the Assignment: Automotive Reverse-Polarity &amp; Load-Dump Protection Circuit(Q2)

Author: Harsha Vardhan N
Email: harshavardhann12004@gmail.com
Tools Used: Ngspice & ChatGPT for debugging and  simulation assistnace 

## 🔍 1. Project Overview

This project implements a **12-volt automotive input protection circuit** designed to protect an Electronic Control Unit (ECU) from:

- Reverse battery connection  
- Load-dump surge transients (12 → 80 V → 12 V)  
- General overvoltage conditions  

The circuit uses automotive-rated components:

- **D1 – Reverse polarity protection diode**  
- **D2 – TVS diode (48 V clamp)**  
- **Rload – ECU load resistor**

Three test cases were simulated using **Ngspice** as required by the Arys assignment guidelines.

---

## 🔧 2. Circuit Protection Strategy

### 🔹 Reverse Polarity Protection (D1)
A series diode that blocks current when the battery is connected backward.  
Prevents ECU damage during –12 V scenarios.

### 🔹 Load Dump Protection (D2: TVS Diode)
A 48 V automotive-grade TVS diode clamps high-voltage spikes during alternator load-dump events.

### 🔹 ECU Load
A 100 Ω resistor models the input impedance of an automotive ECU.

---

## 📊 3. Test Cases Simulated

### ✅ Test 1 – Normal Battery (12 V DC)
**Expected:** Clean ECU voltage, no clamping.  
**Observed:** v(mid) ≈ 11–12 V, no diode conduction.

Files:
```
circuits/q2_test1_normal.cir
results/test1_voltage.png
```

---

### ✅ Test 2 – Reverse Battery (–12 V)
**Expected:** D1 blocks, v(mid) ≈ 0V, TVS inactive.  
**Observed:** v(mid) ≈ 0 V, current blocked.

Files:
```
circuits/q2_test2_reverse.cir
results/test2_voltage.png
```

---

### ✅ Test 3 – Load Dump Surge (12 V → 80 V → 12 V)
**Expected:** TVS clamps voltage, ECU protected around 25–30 V.  
**Observed:** v(mid) clamped ~27 V; TVS current increases during surge.

Files:
```
circuits/q2_test3_loaddump.cir
results/test3_voltage.png
results/test3_currents.png
```

---

## 📁 4. Repository Structure

```
arys-q2-automotive-protection-<yourname>
│
├── circuits/
│   ├── q2_test1_normal.cir
│   ├── q2_test2_reverse.cir
│   └── q2_test3_loaddump.cir
│
├── results/
│   ├── test1_voltage.png
│   ├── test2_voltage.png
│   ├── test3_voltage.png
│   └── test3_currents.png
│
├── diagrams/
│   └── circuit_diagram.png
│
└── report/
    └── Q2_Final_Report.pdf
```

---

## ▶️ 5. Running the Simulations (Ngspice)

### Run Test 1:
```
ngspice circuits/q2_test1_normal.cir
```

### Run Test 2:
```
ngspice circuits/q2_test2_reverse.cir
```

### Run Test 3:
```
ngspice circuits/q2_test3_loaddump.cir
```

### Inside Ngspice – Plot commands:
```
plot v(in) v(mid)
plot @d1[id]
plot @d2[id]
```

---

## 🤖 6. AI Usage Notes (Required by Arys Garage)

ChatGPT was used for:

- Checking Ngspice syntax  
- Debugging netlist errors  
- Explaining diode and TVS operation  
- Writing documentation  
- Structuring test outputs  

Engineering decisions and validation were done manually.

---

## 🏁 7. Conclusion

The designed circuit **successfully protects the ECU** against all required automotive scenarios:

- ✔ Reverse battery → ECU isolated  
- ✔ Load-dump surge → Voltage clamped safely  
- ✔ Normal operation → Stable and safe ECU voltage  

This makes the design suitable for automotive ECUs, battery systems, vehicle controllers, and similar 12 V electronics.

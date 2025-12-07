         ┌──────────────────────────┐
         │        Car Battery       │
         │    (Normal / Reverse /   │
         │     Load Dump Surge)     │
         └─────────────┬────────────┘
                       │ 12V / -12V / 80V
                       ▼
        ┌──────────────────────────────┐
        │ Reverse Polarity Protection  │
        │  (Diode / MOSFET-Based)      │
        └─────────────┬────────────────┘
                       │ Protected Input
                       ▼
        ┌──────────────────────────────┐
        │  Load Dump Protection (TVS)  │
        │  Clamps 60–100V Surges       │
        └─────────────┬────────────────┘
                       │ Stable 12V Line
                       ▼
        ┌──────────────────────────────┐
        │      Filtering Network       │
        │   (C1, C2, C3 — EMI/Noise)   │
        └─────────────┬────────────────┘
                       │ Clean DC Supply
                       ▼
        ┌──────────────────────────────┐
        │        ECU / Load Circuit    │
        │   Sensitive Electronics       │
        └──────────────────────────────┘

The block diagram represents a complete protection path used in automotive ECUs to ensure safe and reliable operation under real vehicle electrical conditions. Each stage in the diagram performs a specific defensive function against faults such as reverse polarity, load-dump surges, and electrical noise. The following explains the purpose of every block from left to right.

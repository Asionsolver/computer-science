# Chapter 4 — Anatomy of a Flashlight

## 1. Chapter Overview

Chapter 4-এ আমরা Binary Code-এর ধারণা থেকে বাস্তব Electrical Circuit-এর দিকে যাই।

```text
Chapter 1
Code
  ↓
Chapter 2
Combinations → 2ⁿ
  ↓
Chapter 3
Binary Codes
  ↓
Chapter 4
Electricity → Circuit → Switch
  ↓
Digital Logic
```

---

# 2. Basic Flashlight

একটি সাধারণ Flashlight-এর প্রধান অংশ:

```text
┌─────────────────────────────────────────────┐
│                 FLASHLIGHT                  │
│                                             │
│   ┌────────┐  ┌────────┐       ┌───────┐  │
│   │Battery │  │Battery │──────▶│ Bulb  │  │
│   │ 1.5 V  │  │ 1.5 V  │       │       │  │
│   └────────┘  └────────┘       └───────┘  │
│        │                              │     │
│        └────────── Switch ───────────┘     │
│                                             │
└─────────────────────────────────────────────┘
```

মূল উপাদান:

```text
Battery
   ↓
Wires / Metal Contacts
   ↓
Switch
   ↓
Lightbulb
   ↓
Complete Circuit
```

---

# 3. Complete Circuit

Electricity প্রবাহিত হওয়ার জন্য একটি complete path প্রয়োজন।

```text
          ┌───────────────┐
          │               │
      (+) Battery       Lightbulb
          │               │
          │               │
          └─── Switch ────┘
               CLOSED

          ↑
      Complete Path

      Current flows
          ↓
      💡 Light ON
```

অর্থাৎ:

```text
Complete Circuit
      ↓
Current can flow
      ↓
Lightbulb lights
```

---

# 4. Open Circuit

Switch open থাকলে circuit-এর path ভেঙে যায়।

```text
          ┌───────────────┐
          │               │
      (+) Battery       Lightbulb
          │               │
          │               │
          └─── Switch ──  ─┘
                    ↑
                  OPEN

              Path broken
                   ↓
             No current
                   ↓
               💡 OFF
```

---

# 5. Closed vs Open Switch

```text
OPEN SWITCH

───────/  ───────

Circuit broken
Current = No
Light = OFF
```

```text
CLOSED SWITCH

───────●───────

Circuit complete
Current = Yes
Light = ON
```

মনে রাখার মতো:

```text
Open   → Circuit broken → Current নেই → OFF
Closed → Circuit complete → Current আছে → ON
```

---

# 6. Battery

একটি Battery-এর দুটি terminal থাকে:

```text
       Battery
    ┌───────────┐
    │           │
 (-)│           │(+) 
    └───────────┘
```

Book অনুযায়ী সাধারণ flashlight battery প্রায়:

```text
1.5 volts
```

---

# 7. Two Batteries in Series

দুটি 1.5 V battery একই direction-এ series-এ যুক্ত হলে:

```text
   +     -     +     -
   │     │     │     │
  ┌───────┐   ┌───────┐
  │ 1.5 V │───│ 1.5 V │
  └───────┘   └───────┘
```

Total voltage:

```text
1.5 V + 1.5 V
     =
3.0 V
```

সুতরাং:

```text
Series Connection
       ↓
Voltage adds
       ↓
3.0 V
```

---

# 8. Batteries in Parallel

দুটি battery parallel-এ যুক্ত করলে:

```text
        ┌── Battery ──┐
        │    1.5 V    │
   ─────┤              ├─────
        │    1.5 V    │
        └── Battery ──┘
```

Book-এর উদাহরণ অনুযায়ী:

```text
Parallel
   ↓
Total voltage = 1.5 V
```

অর্থাৎ series এবং parallel-এর ফল এক নয়।

---

# 9. Battery → Chemical Energy → Electrical Energy

Battery নিজে শুধু "বিদ্যুৎ তৈরি করে"—এভাবে ভাবলে পুরো ধারণাটি অসম্পূর্ণ।

Book অনুযায়ী battery-এর ভিতরে chemical reaction হয়।

```text
Chemical Energy
       ↓
Chemical Reaction
       ↓
Electron imbalance
       ↓
Electrical Energy
       ↓
Circuit-এ Electron movement
```

---

# 10. Electron Flow

একটি complete circuit-এ electrons circuit-এর মধ্য দিয়ে চলাচল করে।

```text
       Electron Flow
             ↓

    ┌───────────────────┐
    │                   │
    │      Lightbulb     │
    │         💡         │
    │                   │
    └─────── Switch ────┘
             │
          Battery
```

Conceptual chain:

```text
Battery
  ↓
Electron movement
  ↓
Current
  ↓
Lightbulb
  ↓
Light + Heat
```

---

# 11. Conductor vs Insulator

### Conductor

যে material দিয়ে electricity তুলনামূলক সহজে প্রবাহিত হয়।

```text
Copper
   ↓
Low Resistance
   ↓
Good Conductor
```

### Insulator

যে material electricity-এর প্রবাহকে অনেক বেশি বাধা দেয়।

```text
Plastic
   ↓
High Resistance
   ↓
Insulator
```

Simple model:

```text
Conductor
──────────────
Electron flow →→→→→


Insulator
──────────────
Electron flow ✕
```

---

# 12. Voltage

Voltage হলো electrical potential।

সহজ analogy:

```text
উঁচুতে রাখা Brick
       ↓
Potential Energy
       ↓
পড়ে গিয়ে কাজ করতে পারে
```

Electricity-তে:

```text
Voltage
   ↓
Potential for doing work
```

---

# 13. Current

Current হলো circuit-এর মধ্য দিয়ে electron movement-এর সঙ্গে সম্পর্কিত।

Water analogy:

```text
Water System

Pressure → Water Flow
   ↓           ↓
Voltage     Current
```

অর্থাৎ:

```text
Voltage ≈ Water Pressure
Current ≈ Water Flow
```

---

# 14. Resistance

Resistance হলো electron flow-কে বাধা দেওয়ার প্রবণতা।

Water analogy:

```text
Narrow Pipe
     ↓
More Resistance
     ↓
Less Water Flow
```

Electrical circuit:

```text
More Resistance
       ↓
Less Current
```

---

# 15. Ohm's Law

Book-এ ব্যবহৃত formula:

```text
I = E / R
```

যেখানে:

```text
I = Current
E = Voltage
R = Resistance
```

আরও পরিচিতভাবে:

```text
V = I × R
```

---

# 16. Flashlight Calculation

Book-এর উদাহরণ:

```text
Voltage = 3 V
Resistance = 4 Ω
```

তাহলে:

```text
I = E / R

I = 3 / 4

I = 0.75 A
```

অর্থাৎ:

```text
Current = 0.75 ampere
       = 750 mA
```

---

# 17. Lightbulb

Lightbulb-এর ভিতরে থাকে একটি thin wire:

```text
Thin Wire
   ↓
Filament
   ↓
Usually Tungsten
```

Diagram:

```text
          Glass Bulb
       ┌──────────────┐
       │              │
       │     /\       │
       │    /  \      │
       │   /    \     │
       │  /      \    │
       │              │
       └──────┬───────┘
              │
           Base
```

---

# 18. Why Does the Bulb Glow?

```text
Current
   ↓
Filament
   ↓
Resistance
   ↓
Heat
   ↓
Tungsten becomes extremely hot
   ↓
Light
```

Vacuum থাকার কারণে tungsten সরাসরি open air-এর মতো সহজে burn করে না; এটি glow করে।

---

# 19. Filament Resistance

Filament-এর resistance temperature-এর সঙ্গে পরিবর্তিত হয়।

```text
Cold Filament
      ↓
Lower Resistance
      ↓
Heating
      ↓
Higher Temperature
      ↓
Higher Resistance
```

তাই বাস্তবে cold অবস্থায় bulb-এর resistance মাপলে বইয়ের ব্যবহৃত 4 Ω-এর চেয়ে কম পাওয়া যেতে পারে।

---

# 20. Power

Electrical power-এর জন্য:

```text
P = E × I
```

Flashlight example:

```text
E = 3 V
I = 0.75 A

P = 3 × 0.75

P = 2.25 W
```

অর্থাৎ bulb-এর power প্রায়:

```text
2.25 watts
```

---

# 21. Complete Electrical Model

সবকিছু একসঙ্গে:

```text
        ┌─────────────────────────────┐
        │                             │
        │       Lightbulb             │
        │        R ≈ 4 Ω              │
        │          💡                 │
        │                             │
        └───────────┬─────────────────┘
                    │
                Switch
              ┌─────/ ─────┐
              │             │
              │             │
          ┌───┴─────────────┴───┐
          │      Batteries       │
          │    1.5 V + 1.5 V     │
          │       = 3.0 V        │
          └──────────────────────┘
```

Closed switch:

```text
Circuit Complete
      ↓
Current flows
      ↓
Filament heats
      ↓
Light ON
```

Open switch:

```text
Circuit Broken
      ↓
No Current
      ↓
Filament doesn't heat
      ↓
Light OFF
```

---

# 22. Binary Connection

Chapter 1–3:

```text
Morse
  ↓
Dot / Dash
  ↓
Binary states
```

```text
Braille
  ↓
Raised / Flat
  ↓
Binary states
```

Chapter 4:

```text
Flashlight
  ↓
ON / OFF
  ↓
Two electrical states
```

Combined:

```text
          TWO STATES
              │
      ┌───────┼────────┐
      ↓       ↓        ↓
   Morse    Braille  Flashlight
 Dot/Dash  Raised/Flat  ON/OFF
      │       │        │
      └───────┼────────┘
              ↓
        Binary Thinking
```

---

# 23. Chapter 4 Core Diagram

```text
                 ELECTRICITY
                     │
                     ↓
                 Battery
                     │
              Chemical Energy
                     │
                     ↓
              Electron Movement
                     │
                     ↓
                  Current
                     │
          ┌──────────┴──────────┐
          ↓                     ↓
      Resistance             Switch
          │                     │
          ↓                Open / Closed
      Lightbulb                 │
          │                     ↓
          ↓                  ON / OFF
      Heat + Light
          │
          └──────────┬──────────┘
                     ↓
               TWO STATES
                     ↓
                 Binary
                     ↓
              Digital Logic
```

---

# 24. Chapter 4 → Future Chapters

```text
Flashlight
    ↓
Switch
    ↓
ON / OFF
    ↓
Binary State
    ↓
Relay
    ↓
Multiple Relays
    ↓
Logic Gates
    ↓
Digital Circuits
    ↓
Computer
```

Chapter 4-এর সবচেয়ে গুরুত্বপূর্ণ bridge:

```text
Physical Electricity
        ↓
Two Distinguishable States
        ↓
Binary Logic
        ↓
Computer Hardware
```
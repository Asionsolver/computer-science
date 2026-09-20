# Chapter 5 — Seeing Around Corners

> Visual diagrams for understanding the chapter.

---

## 1. Chapter Overview

```text
Chapter 1
Best Friends
    │
    ↓
Morse Code
    │
    ↓
Chapter 2
Codes and Combinations
    │
    ↓
Binary / 2ⁿ
    │
    ↓
Chapter 3
Braille and Binary Codes
    │
    ↓
Binary Representation
    │
    ↓
Chapter 4
Anatomy of a Flashlight
    │
    ↓
Electrical Circuit
    │
    ↓
Chapter 5
Seeing Around Corners
    │
    ↓
Electrical Communication
    │
    ↓
Telegraph
```

---

# 2. The Original Problem — Line of Sight

```text
Friend A                         Friend B

   🔦 ───────────────────────────→ 👁️

        Direct Line of Sight
```

Flashlight communication requires the receiver to be within the path of the light.

---

# 3. Corner Problem

```text
Friend A
   🔦
    │
    │
    └───────────────┐
                    │
                    │
                    └────────────── Friend B

             ❌ Light cannot turn the corner
```

---

# 4. Wire-Based Solution

```text
Friend A                              Friend B

 Battery
    │
    │
 [Switch] ──────────────────────── [Lightbulb]
    │                                  💡
    └──────────────────────────────────┘
```

### Signal flow

```text
Switch
   ↓
Electrical Circuit
   ↓
Wire
   ↓
Current
   ↓
Lightbulb
   ↓
Light
```

---

# 5. Morse Code Through Electricity

```text
Morse:

A = .-

      ↓

Dot  → Short ON
Dash → Long ON

      ↓

Electrical Signal

████        █████████
Short       Long
```

Receiver:

```text
Short + Long
     ↓
    .-
     ↓
     A
```

---

# 6. One-Way Communication

```text
House A                                      House B

 Battery
    │
 Switch
    │
    ├───────────────────────────────┐
    │                               │
    │                               ↓
    │                            Lightbulb
    │                               💡
    │                               │
    └───────────────────────────────┘
```

---

# 7. Bidirectional Telegraph

```text
               Direction 1
       ─────────────────────────→

    A                                 B
  Switch                            Bulb


               Direction 2
       ←─────────────────────────

    A                                 B
  Bulb                             Switch
```

দুইটি independent circuit ব্যবহার করে দুই দিকেই message পাঠানো যায়।

---

# 8. Four-Wire Bidirectional System

```text
House A                              House B

 Switch ─────────────────────────── Bulb
    │                                  │
    │                                  │
 Bulb  ─────────────────────────── Switch
```

```text
A → B
B → A
```

---

# 9. Common Connection

দুটি circuit-এর negative terminals একসঙ্গে যুক্ত করা যায়।

```text
       Circuit A              Circuit B

 Switch ──────────────── Bulb
    │                       │
 Battery ────────┬──────── Battery
                 │
               COMMON
```

Common ব্যবহার করলে:

```text
4 wires
   ↓
3 wires
```

অর্থাৎ wiring requirement 25% কমে।

---

# 10. Earth as a Common/Conductor

High-voltage system-এ Earth-কে circuit-এর একটি অংশ হিসেবে ব্যবহার করা যায়।

```text
House A                              House B

 Battery                             Lightbulb
    │                                   │
 Switch ───────────── Wire ─────────────┘
    │
    │
 Ground                                Ground
    └────────────── Earth ──────────────┘
```

Concept:

```text
Wire + Earth
     ↓
Complete Circuit
```

---

# 11. Ground and Earth

```text
Physical Earth
      │
      ↓
Electrical Connection
      │
      ↓
Ground
```

Chapter 5-এ এখানে `ground` বলতে physical connection with Earth বোঝানো হচ্ছে।

---

# 12. Earth as Electron Reservoir

Petzold-এর useful mental model:

```text
              EARTH
        ┌────────────────┐
        │                │
        │  Huge Electron │
        │   Reservoir    │
        │                │
        └────────────────┘
```

Analogy:

```text
Ocean
  ↓
Water Reservoir

Earth
  ↓
Electron Reservoir
```

---

# 13. Voltage and Ground

```text
Voltage
   ↓
Potential for doing Work
   ↓
Like a Brick at Height
   ↓
Potential Energy
```

অন্যদিকে:

```text
Ground
   ↓
Zero Potential
   ↓
Like a Brick on the Ground
```

---

# 14. Circuit May Look Open but Still Be Complete

```text
       V
       │
    Switch
       │
       └────────── Bulb
                     │
                   Ground
                     │
                   Earth
```

Diagram-এ circle দেখা যাচ্ছে না।

কিন্তু electrical path সম্পূর্ণ হতে পারে।

---

# 15. Wire Resistance

```text
Short Wire
Battery ───────────── Bulb
          ↓
       Low R
          ↓
      More Current
          ↓
      Bright Bulb
```

```text
Long Wire
Battery ───────────────────────────── Bulb
                  ↓
               High R
                  ↓
             Less Current
                  ↓
              Dim Bulb
```

---

# 16. Ohm's Law

```text
       V
I = ─────
       R
```

Where:

```text
I = Current
V = Voltage
R = Resistance
```

Therefore:

```text
R ↑
↓
I ↓
```

---

# 17. Wire Thickness and AWG

```text
AWG Number
    │
    ├── Smaller AWG
    │       ↓
    │    Thicker Wire
    │       ↓
    │   Lower Resistance
    │
    └── Larger AWG
            ↓
         Thinner Wire
            ↓
        Higher Resistance
```

---

# 18. One-Mile Wire Example

```text
3 V Battery
     │
     ↓
Long Wire
     │
     ↓
R > 100 Ω
     │
     ↓
I < 0.03 A
     │
     ↓
4 Ω Bulb
     │
     ↓
Probably doesn't light
```

---

# 19. Relay Solution for Long Distance

```text
New York
   │
   │ Telegraph Signal
   ↓
Relay Station
   │
   │ Re-generated Signal
   ↓
Relay Station
   │
   │ Re-generated Signal
   ↓
California
```

Conceptually:

```text
Weak Signal
    ↓
Receive
    ↓
Relay
    ↓
Strong Signal
    ↓
Send Again
```

---

# 20. Telegraph Sounder

```text
Telegraph Key
      │
      ↓
Electrical Signal
      │
      ↓
Electromagnet
      │
      ↓
Metal Bar
      │
      ↓
Click / Clack
      │
      ↓
Morse
```

Timing:

```text
Fast click-clack
      ↓
     Dot

Slow click...clack
      ↓
     Dash
```

---

# 21. Complete Chapter 5 Pipeline

```text
Human Message
      ↓
Morse Code
      ↓
Switch
      ↓
Electrical Signal
      ↓
Wire
      ↓
Distance / Corner
      ↓
Receiver
      ↓
Lightbulb / Sounder
      ↓
Morse Code
      ↓
Human Message
```

---

# 22. Chapter 1 → Chapter 5

```text
Communication
      ↓
Code
      ↓
Morse
      ↓
Binary-like states
      ↓
Electrical States
      ↓
Wire
      ↓
Telegraph
```

---

# 23. Big Picture

```text
             INFORMATION
                   │
                   ↓
                  CODE
                   │
                   ↓
              MORSE CODE
                   │
                   ↓
             BINARY STATES
                   │
                   ↓
             ELECTRICITY
                   │
                   ↓
                  WIRE
                   │
                   ↓
             LONG DISTANCE
                   │
                   ↓
               TELEGRAPH
                   │
                   ↓
                 RELAY
                   │
                   ↓
             LOGIC / SWITCHING
                   │
                   ↓
               COMPUTER
```

---

# 24. Core Mental Model

```text
Code
 ↓
Representation
 ↓
Physical Signal
 ↓
Transmission
 ↓
Reception
 ↓
Decoding
 ↓
Information
```

**Chapter 5-এর মূল শিক্ষা:**

> Code একই থাকতে পারে, কিন্তু সেই Code বহন করার physical medium পরিবর্তন করা যায়।
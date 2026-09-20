# Chapter 5 — Seeing Around Corners

## 1. Chapter Overview

Chapter 5-এর মূল উদ্দেশ্য হলো আগের অধ্যায়ের **Flashlight + Binary-like Electrical States** ধারণাকে ব্যবহার করে দেখানো যে Electrical Signal কীভাবে **line of sight-এর বাইরে এবং অনেক দূর পর্যন্ত Communication** করতে পারে।

Chapter 1-এ Flashlight দিয়ে Morse Code পাঠানো হয়েছিল। কিন্তু Flashlight-এর একটি বড় সীমাবদ্ধতা ছিল—Sender এবং Receiver-কে আলোর পথে থাকতে হতো।

Chapter 5 সেই সীমাবদ্ধতা দূর করে:

```text
Flashlight
    ↓
Wire
    ↓
Electrical Signal
    ↓
Long-distance Communication
    ↓
Telegraph
```

বইয়ে এই পরিবর্তনটিকে Communication-এর ইতিহাসে একটি গুরুত্বপূর্ণ পদক্ষেপ হিসেবে দেখানো হয়েছে। 

---

# 2. Original Problem: Flashlight-এর সীমাবদ্ধতা

দুই বন্ধু রাতে Flashlight দিয়ে Morse Code ব্যবহার করে Communication করছিল।

কিন্তু নতুন বন্ধুর bedroom window এমনভাবে ছিল যে দুই জানালা একে অপরের দিকে মুখ করছিল না।

তাই:

```text
Flashlight
    ↓
Light
    ↓
Line of Sight
```

প্রয়োজন হচ্ছিল।

Corner থাকলে:

```text
🔦 ───────┐
          │
          └──────── 👤

❌ Light সরাসরি পৌঁছাতে পারে না
```

এখান থেকেই Chapter-এর নাম **Seeing Around Corners**।

---

# 3. Flashlight থেকে Electrical Communication

সমাধান:

Flashlight-এর পরিবর্তে battery, switch, wire এবং lightbulb ব্যবহার করা।

```text
Battery
   ↓
Switch
   ↓
Wire
   ↓
Lightbulb
```

Sender-এর switch বন্ধ করলে Receiver-এর bulb জ্বলে।

অর্থাৎ:

```text
Switch ON
    ↓
Current flows
    ↓
Wire
    ↓
Bulb ON
```

বইয়ের Chapter 5-এ এই experiment-এর মাধ্যমেই long-distance flashlight তৈরি করা হয়।

---

# 4. Morse Code পরিবর্তন হয়নি

এখানে খুব গুরুত্বপূর্ণ বিষয় হলো:

**Morse Code পরিবর্তন হয়নি।**

শুধু Code-এর physical carrier পরিবর্তিত হয়েছে।

আগে:

```text
Morse
  ↓
Flashlight
  ↓
Light
```

এখন:

```text
Morse
  ↓
Switch
  ↓
Electrical Signal
  ↓
Wire
  ↓
Lightbulb
```

অর্থাৎ:

> একই Code বিভিন্ন physical medium ব্যবহার করে পাঠানো যেতে পারে।

---

# 5. Morse Code এবং Electrical Signal

ধরা যাক:

```text
A = .-
```

তাহলে:

```text
Dot = Short signal
Dash = Long signal
```

Electrical circuit-এ:

```text
Short ON
    ↓
Dot

Long ON
    ↓
Dash
```

Receiver:

```text
Short + Long
     ↓
    .-
     ↓
     A
```

এখানে information সরাসরি `"A"` হিসেবে wire দিয়ে ভ্রমণ করছে না। বরং একটি physical signal pattern পাঠানো হচ্ছে, Receiver সেই pattern decode করে `"A"` বুঝছে।

---

# 6. Bidirectional Telegraph

একদিকে Communication সফল হওয়ার পর বন্ধুর কাছ থেকেও message পাঠানোর প্রয়োজন হলো।

তাই আরেকটি একই ধরনের circuit তৈরি করা যায়।

```text
A → B

A: Switch
B: Lightbulb
```

এবং:

```text
B → A

B: Switch
A: Lightbulb
```

ফলে:

```text
A ↔ B
```

এটিই একটি **bidirectional telegraph system**।

বইয়ে বলা হয়েছে, দুটি identical কিন্তু independent circuit ব্যবহার করে দুই দিকেই Communication করা সম্ভব।

---

# 7. Four-Wire System

প্রথমে দুইটি independent circuit ব্যবহার করলে মোট চারটি wire প্রয়োজন হতে পারে।

```text
A                               B

Switch ─────────────────────── Bulb
Bulb   ─────────────────────── Switch
```

এতে:

```text
A → B
B → A
```

দুই দিকেই Communication সম্ভব।

---

# 8. Common Connection

Petzold দেখান যে wiring কমানোর জন্য দুই circuit-এর negative terminals একসঙ্গে যুক্ত করা যায়।

এই shared connection-কে বলা হয়:

**Common**

```text
Circuit A ───────┐
                 │
               COMMON
                 │
Circuit B ───────┘
```

এভাবে:

```text
4 wires
   ↓
3 wires
```

অর্থাৎ wiring requirement 25% কমানো যায়।

---

# 9. Earth ব্যবহার করে Wiring আরও কমানো

Common থাকার পরে প্রশ্ন আসে:

> এই common wire-টিও কি অন্য কোনো কিছুর মাধ্যমে replace করা যায়?

বই এখানে **Earth** ব্যবহার করার ধারণা দেয়।

Earth বিশাল একটি physical object এবং electrical conductor হিসেবে ব্যবহার করা যেতে পারে।

Conceptually:

```text
House A
   │
 Wire
   │
   ├──────────────── House B
   │
 Earth
   │
 Earth
```

তবে এখানে একটি গুরুত্বপূর্ণ সীমাবদ্ধতা আছে।

Earth perfect conductor নয়।

এর Resistance আছে।

বিশেষ করে low-voltage flashlight batteries-এর জন্য Earth-এর Resistance অনেক বেশি হতে পারে।

---

# 10. Ground বনাম Common

এই Chapter-এ terminology খুব গুরুত্বপূর্ণ।

### Common

Circuit-এর একটি shared electrical connection।

```text
Circuit A ──┐
            ├── Common
Circuit B ──┘
```

### Ground

এই Chapter-এর context-এ **physical Earth-এর সঙ্গে electrical connection**।

```text
Circuit
   │
   ↓
Ground
   │
   ↓
Physical Earth
```

পরে বইয়ের অন্য জায়গায় `ground` শব্দটি common connection বোঝাতেও ব্যবহার করা হবে, কিন্তু Chapter 5-এ Petzold এই distinction-টি পরিষ্কার করেন।

---

# 11. Earth as a Huge Electrical Reservoir

Earth-কে শুধু “একটা বিশাল wire” হিসেবে চিন্তা করা পুরোপুরি useful mental model নয়।

Petzold-এর analogy:

```text
Ocean : Water
Earth : Electrons
```

অর্থাৎ:

```text
Ocean
  ↓
Huge reservoir of water

Earth
  ↓
Huge reservoir/source/sink of electrons
```

Earth একই সঙ্গে electrons-এর source এবং repository হিসেবে বিবেচনা করা যায়।

---

# 12. Ground এবং Zero Potential

Chapter-এ Ground-কে **point of zero potential** হিসেবে ব্যাখ্যা করা হয়েছে।

সহজ analogy:

```text
Brick high above ground
        ↓
Potential energy

Brick on ground
        ↓
Zero potential
```

Electrical context:

```text
Voltage
   ↓
Potential for doing work

Ground
   ↓
Zero potential
```

এটি Voltage বোঝার জন্য একটি mental model হিসেবে ব্যবহার করা যায়।

---

# 13. V এবং Ground Representation

পরবর্তী diagram-গুলোতে Petzold battery-এর পরিবর্তে `V` ব্যবহার করেন।

Conceptually:

```text
V
│
Switch
│
Bulb
│
Ground
```

এখানে `V` voltage source বোঝায়।

বইয়ে একটি useful analogy দেওয়া হয়েছে:

```text
V      → Electron vacuum
Ground → Ocean of electrons
```

অর্থাৎ voltage source circuit-এ কাজ করার জন্য potential তৈরি করে।

---

# 14. Circuit দেখতে Circle-এর মতো না হলেও Circuit হতে পারে

Chapter 4-এ circuit-কে আমরা closed loop হিসেবে দেখেছি।

কিন্তু Ground ব্যবহার করলে diagram দেখতে এমন হতে পারে:

```text
V
│
Switch
│
Bulb
│
Ground
```

এখানে circle নেই।

কিন্তু circuit electrically complete হতে পারে।

কারণ Ground এবং V-এর মধ্যে একটি complete electrical path তৈরি হচ্ছে।

Petzold দেখান যে Ground-কে battery-এর negative terminal-এর সঙ্গে equivalentভাবে connect করলে আগের circular circuit-এ ফিরে যাওয়া যায়।

---

# 15. Long Wire-এর প্রধান সমস্যা — Resistance

এখন আমরা long-distance Communication করতে পারছি।

কিন্তু নতুন সমস্যা:

> Wire যত লম্বা হবে, Resistance তত বাড়বে।

Ohm's Law:

\[
I = \frac{V}{R}
\]

অর্থাৎ Voltage একই থাকলে:

```text
R ↑
 ↓
I ↓
```

এবং:

```text
Current ↓
   ↓
Bulb dimmer
```

বইয়ে এই সমস্যাটিই long-distance telegraph-এর বড় practical limitation হিসেবে দেখানো হয়েছে।

---

# 16. Wire Thickness এবং AWG

Wire-এর thickness **American Wire Gauge (AWG)** দিয়ে প্রকাশ করা হয়।

গুরুত্বপূর্ণ নিয়ম:

```text
AWG number কম
      ↓
Wire মোটা
      ↓
Resistance কম
```

অন্যদিকে:

```text
AWG number বেশি
      ↓
Wire পাতলা
      ↓
Resistance বেশি
```

অর্থাৎ:

```text
10 AWG
████████████
   ↓
Thicker
   ↓
Lower Resistance


20 AWG
████
  ↓
Thinner
  ↓
Higher Resistance
```

---

# 17. বইয়ের Wire Example

বইয়ে 20-gauge speaker wire-এর একটি example দেওয়া হয়েছে।

20-gauge wire-এর resistance প্রায়:

```text
10 Ω / 1000 feet
```

এবং 100-foot round trip-এ প্রায়:

```text
1 Ω
```

কিন্তু distance এক mile হলে resistance 100 Ω-এর বেশি হতে পারে।

তখন:

\[
I = \frac{3V}{R}
\]

যদি:

```text
R > 100 Ω
```

তাহলে:

```text
I < 0.03 A
```

যা 4 Ω-এর flashlight bulb জ্বালানোর জন্য যথেষ্ট নাও হতে পারে।

---

# 18. Long-distance Communication-এর দুইটি Solution

Wire Resistance-এর সমস্যা সমাধানের জন্য Chapter-এ কয়েকটি ধারণা আসে।

### Solution 1 — Thicker Wire

```text
Thicker Wire
     ↓
Lower Resistance
     ↓
More Current
```

কিন্তু:

```text
Thicker Wire
     ↓
More Material
     ↓
More Cost
```

### Solution 2 — Higher Voltage

Higher voltage ব্যবহার করলে একই resistance-এর মধ্যেও বেশি current পাওয়া যায়।

```text
V ↑
↓
I ↑
```

এবং higher-resistance bulb ব্যবহার করা যায়।

বইয়ে 120-volt, 100-watt household bulb-এর উদাহরণ ব্যবহার করে দেখানো হয় যে wire resistance তখন circuit-এর মোট resistance-এর তুলনায় কম গুরুত্বপূর্ণ হয়ে যায়।

---

# 19. Relay কেন দরকার?

Long-distance wire অনির্দিষ্টভাবে বাড়ানো যায় না।

তাই একটি গুরুত্বপূর্ণ solution:

**Relay System**

ধরা যাক:

```text
New York
    │
    │
    ↓
Relay Station
    │
    ↓
Relay Station
    │
    ↓
California
```

প্রতি কিছু distance পর:

```text
Receive Signal
      ↓
Relay
      ↓
Send Strong Signal
```

বইয়ে কয়েকশ মাইল পরপর relay station ব্যবহার করার ধারণা দেওয়া হয়েছে।

---

# 20. Telegraph Sounder

Long-distance telegraph-এ Lightbulb-এর পরিবর্তে **electromagnet-based sounder** ব্যবহার করা যায়।

Basic structure:

```text
Telegraph Key
      ↓
Electrical Signal
      ↓
Electromagnet
      ↓
Metal Lever
      ↓
Sound
```

Key press করলে electromagnet metal bar টেনে নেয়।

ফলে:

```text
Click
```

Key release করলে:

```text
Clack
```

তাই:

```text
Fast click-clack
       ↓
      Dot


Slow click...clack
       ↓
      Dash
```

বইয়ে telegraph sounder-এর মাধ্যমে Morse Code শোনার এই পদ্ধতিটি ব্যাখ্যা করা হয়েছে।

---

# 21. Telegraph কেন এত গুরুত্বপূর্ণ?

Telegraph-এর বিশেষ গুরুত্ব হলো:

আগে মানুষ:

```text
Eye
 ↓
Light
 ↓
Limited Distance
```

অথবা:

```text
Ear
 ↓
Sound
 ↓
Limited Distance
```

এর মধ্যে সীমাবদ্ধ ছিল।

Telegraph:

```text
Electrical Signal
       ↓
Wire
       ↓
Long Distance
```

ব্যবহার করে Communication-কে অনেক দূরে নিয়ে যায়।

বইয়ে এটিকে modern Communication-এর শুরুতে গুরুত্বপূর্ণ একটি পদক্ষেপ হিসেবে উল্লেখ করা হয়েছে।

---

# 22. Telegraph এবং Binary

এখানে Chapter 1–5-এর সবচেয়ে সুন্দর connection পাওয়া যায়।

Telegraph Morse Code ব্যবহার করে:

```text
Dot
Dash
```

অর্থাৎ দুটি basic signal state।

এটি Binary-এর ধারণার সঙ্গে সরাসরি সম্পর্কিত।

```text
Two States
    ↓
Binary
    ↓
Morse
    ↓
Electrical Signal
    ↓
Telegraph
```

বই বিশেষভাবে উল্লেখ করে যে telegraph-এর Binary Code ব্যবহার Communication-এর ইতিহাসে গুরুত্বপূর্ণ ছিল।

---

# 23. Chapter 1–5 Connection

```text
Chapter 1
Code
 ↓
Morse
 ↓
Communication
```

```text
Chapter 2
Two Choices
 ↓
Combinations
 ↓
2ⁿ
 ↓
Binary
```

```text
Chapter 3
Braille
 ↓
Raised / Flat
 ↓
Binary Representation
```

```text
Chapter 4
Switch
 ↓
Open / Closed
 ↓
Electrical State
```

```text
Chapter 5
Electrical State
 ↓
Wire
 ↓
Long Distance
 ↓
Telegraph
```

---

# 24. সবচেয়ে গুরুত্বপূর্ণ Conceptual Connection

এই Chapter-এর মূল chain:

```text
Human Information
       ↓
       Code
       ↓
   Morse Code
       ↓
 Two Signal States
       ↓
Electrical States
       ↓
       Wire
       ↓
Long-distance Transmission
       ↓
     Receiver
       ↓
      Decode
       ↓
Human Information
```

এখানে আমরা প্রথমবার খুব পরিষ্কারভাবে দেখতে পাচ্ছি:

> **Information এবং Information বহনকারী physical signal এক জিনিস নয়।**

---

# 25. Chapter 5 থেকে Computer-এর দিকে Bridge

Chapter 5-এর শেষে আমরা সরাসরি Computer-এ পৌঁছাই না।

কিন্তু একটি গুরুত্বপূর্ণ bridge তৈরি হয়:

```text
Switch
  ↓
Electrical State
  ↓
Binary Signal
  ↓
Communication
  ↓
Telegraph
  ↓
Electromagnet
  ↓
Relay
  ↓
Automatic Switch
  ↓
Logic
  ↓
Logic Gates
  ↓
Computer
```

পরবর্তী chapters-এ Relay এবং Switching আরও গুরুত্বপূর্ণ হয়ে উঠবে।

---

# 26. Final Mental Model

Chapter 5 মনে রাখার সবচেয়ে ভালো উপায়:

```text
FLASHLIGHT
    │
    │ Line of sight
    ↓
Limited Communication
    │
    │ Replace light with electricity
    ↓
WIRE
    │
    ↓
Electrical Signal
    │
    ↓
Around Corners
    │
    ↓
Long Distance
    │
    ↓
TELEGRAPH
    │
    ↓
RELAY
    │
    ↓
COMPUTING
```

---

# 27. One-Sentence Summary

> **Seeing Around Corners দেখায় কীভাবে Morse Code-কে Electrical Signal হিসেবে Wire-এর মাধ্যমে পাঠিয়ে line-of-sight-এর সীমাবদ্ধতা অতিক্রম করে long-distance Communication এবং Telegraph-এর দিকে যাওয়া যায়।**
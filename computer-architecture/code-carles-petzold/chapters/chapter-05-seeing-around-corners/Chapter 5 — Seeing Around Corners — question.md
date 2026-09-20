# Chapter 5 — Seeing Around Corners

> প্রতিটি প্রশ্নের সঙ্গে উত্তর দেওয়া হয়েছে।

---

# Basic Questions

## Q1. Chapter 5-এর নাম কী?

**Answer:**  
Chapter 5-এর নাম **Seeing Around Corners**।

---

## Q2. Chapter 5-এর শুরুতে মূল সমস্যা কী ছিল?

**Answer:**  
দুই বন্ধুর bedroom window একে অপরের দিকে মুখ না করায় Flashlight দিয়ে সরাসরি Morse Code Communication করা সম্ভব হচ্ছিল না।

---

## Q3. Flashlight Communication-এর প্রধান limitation কী?

**Answer:**  
Flashlight-এর আলো সরাসরি line of sight-এর মধ্যে যেতে হয়। Corner বা বাধা থাকলে Communication করা যায় না।

---

## Q4. এই সমস্যার প্রথম solution কী ছিল?

**Answer:**  
Flashlight-এর পরিবর্তে Battery, Switch, Wire এবং Lightbulb ব্যবহার করে Electrical Circuit তৈরি করা।

---

## Q5. Switch বন্ধ করলে কী হয়?

**Answer:**  
Switch closed হলে circuit complete হয় এবং Current প্রবাহিত হয়। ফলে Receiver-এর Lightbulb জ্বলে।

---

## Q6. Chapter 5-এ Morse Code কি পরিবর্তন করা হয়েছিল?

**Answer:**  
না। Morse Code একই থাকে। শুধু Morse signal পাঠানোর physical medium Flashlight-এর Light থেকে Electrical Signal এবং Wire-এ পরিবর্তিত হয়।

---

## Q7. Bidirectional Communication কী?

**Answer:**  
যে Communication system-এ দুই দিকেই message পাঠানো যায় তাকে Bidirectional Communication বলে।

```text
A → B
A ← B
```

---

## Q8. Telegraph কী?

**Answer:**  
Wire এবং Electrical Signal ব্যবহার করে দূরবর্তী স্থানে message পাঠানোর Communication system হলো Telegraph।

---

## Q9. Telegraph Key কী?

**Answer:**  
Telegraph operator যে switch ব্যবহার করে Electrical Signal তৈরি করেন সেটিই Telegraph Key।

---

## Q10. Telegraph Sounder কী?

**Answer:**  
Telegraph Signal গ্রহণ করে Electromagnet-এর সাহায্যে mechanical movement এবং click/clack sound তৈরি করা device।

---

# Conceptual Questions

## Q11. Chapter-এর নাম “Seeing Around Corners” কেন?

**Answer:**  
কারণ Wire ব্যবহার করে Electrical Signal পাঠানোর ফলে সরাসরি line of sight ছাড়াই Communication করা সম্ভব হয়। অর্থাৎ physicalভাবে corner-এর ওপারে থাকা Receiver-এর কাছে signal পৌঁছানো যায়।

---

## Q12. Flashlight থেকে Wire-based Communication-এ সবচেয়ে গুরুত্বপূর্ণ পরিবর্তন কী?

**Answer:**  
Signal-এর Code পরিবর্তন হয়নি; signal বহন করার **physical medium** পরিবর্তিত হয়েছে।

```text
Morse
 ↓
Light

থেকে

Morse
 ↓
Electrical Signal
 ↓
Wire
```

---

## Q13. Morse Code এবং Binary-এর মধ্যে কী connection আছে?

**Answer:**  
Morse Code-এ দুটি basic signal type—Dot এবং Dash—ব্যবহার করা হয়। দুটি possible state-এর এই ধারণা Binary-এর সঙ্গে সম্পর্কিত।

---

## Q14. Electrical Signal কীভাবে Morse-এর Dot এবং Dash প্রকাশ করতে পারে?

**Answer:**  
Short electrical signal-কে Dot এবং Long electrical signal-কে Dash হিসেবে ব্যবহার করা যায়।

```text
Short → .
Long  → -
```

---

## Q15. Information এবং Signal কি একই জিনিস?

**Answer:**  
না।

Information হলো যে meaning বা message পাঠানো হচ্ছে, আর Signal হলো সেই information বহন করার physical representation।

উদাহরণ:

```text
Information: A

Code: .-

Physical Signal:
Short + Long
```

---

## Q16. Four-wire bidirectional system কী?

**Answer:**  
দুইটি independent Communication circuit ব্যবহার করে দুই দিকের Communication করতে মোট চারটি wire ব্যবহার করা configuration।

```text
A Switch ─────→ B Bulb
A Bulb   ←───── B Switch
```

---

## Q17. Common কী?

**Answer:**  
দুইটি electrical circuit-এর একটি shared connection-কে Common বলা হয়।

এটি ব্যবহার করে চারটি wire-এর প্রয়োজন কমিয়ে তিনটি wire করা যায়।

---

## Q18. Common ব্যবহার করলে কত শতাংশ wire requirement কমে?

**Answer:**  
Four wires থেকে three wires হওয়ায়:

\[
\frac{4-3}{4}\times100=25\%
\]

অর্থাৎ **25%** wire requirement কমে।

---

## Q19. Earth-কে circuit-এর অংশ হিসেবে কীভাবে ব্যবহার করা যায়?

**Answer:**  
যথেষ্ট উপযুক্ত electrical connection তৈরি করলে Earth circuit-এর একটি conductive path হিসেবে কাজ করতে পারে। এতে আলাদা wire-এর প্রয়োজন কমানো সম্ভব হয়।

---

## Q20. Earth কি perfect conductor?

**Answer:**  
না। Earth-এরও Resistance আছে। বিশেষ করে low-voltage flashlight battery-এর ক্ষেত্রে Earth-এর Resistance গুরুত্বপূর্ণ limitation হতে পারে।

---

# Voltage, Current এবং Resistance

## Q21. Wire যত লম্বা হয় Resistance-এর কী হয়?

**Answer:**  
সাধারণভাবে wire যত লম্বা হয়, তার total Resistance তত বাড়ে।

```text
Length ↑
   ↓
Resistance ↑
```

---

## Q22. Resistance বাড়লে Current-এর কী হয়, যদি Voltage একই থাকে?

**Answer:**

Ohm's Law:

\[
I=\frac{V}{R}
\]

তাই Voltage একই থাকলে:

```text
Resistance ↑
     ↓
Current ↓
```

---

## Q23. Long wire-এর কারণে Lightbulb dim হয় কেন?

**Answer:**  
Long wire-এর Resistance বেশি হয়। ফলে একই Voltage-এ Current কমে যায়। Current কমলে Lightbulb-এ কম electrical power পৌঁছায় এবং bulb dim হয়ে যায়।

---

## Q24. AWG কী?

**Answer:**  
AWG-এর পূর্ণরূপ **American Wire Gauge**। এটি Wire-এর thickness প্রকাশ করার একটি standard।

---

## Q25. AWG number কম হলে Wire কেমন হয়?

**Answer:**  
AWG number কম হলে Wire তুলনামূলকভাবে মোটা হয় এবং সাধারণত তার Resistance কম হয়।

---

## Q26. 20-gauge এবং 10-gauge-এর মধ্যে কোনটি মোটা?

**Answer:**  
**10-gauge** wire মোটা।

কারণ AWG scale-এ number যত ছোট, wire তত মোটা।

---

## Q27. Thicker wire ব্যবহার করলে কী সুবিধা?

**Answer:**  
Thicker wire-এর Resistance কম হওয়ায় long-distance circuit-এ Current loss কম হতে পারে।

---

## Q28. Thicker wire ব্যবহার করার অসুবিধা কী?

**Answer:**  
Thicker wire সাধারণত বেশি material ব্যবহার করে এবং বেশি ব্যয়বহুল হতে পারে।

---

## Q29. Long-distance Communication-এর জন্য Voltage বাড়ানো কেন সাহায্য করতে পারে?

**Answer:**  
Ohm's Law অনুযায়ী:

\[
I=\frac{V}{R}
\]

Resistance একই থাকলে Voltage বাড়ালে Current বাড়ে।

---

# Ground এবং Earth

## Q30. Chapter 5-এ Ground বলতে কী বোঝানো হয়েছে?

**Answer:**  
এই Chapter-এর context-এ Ground বলতে Physical Earth-এর সঙ্গে Electrical Connection বোঝানো হয়েছে।

---

## Q31. Ground-কে Zero Potential বলা হয় কেন?

**Answer:**  
Chapter-এর model-এ Ground-কে reference point হিসেবে ধরে zero electrical potential হিসেবে বিবেচনা করা হয়।

---

## Q32. Earth-কে Electron Reservoir হিসেবে ভাবার অর্থ কী?

**Answer:**  
Earth-কে বিশাল source এবং repository of electrons হিসেবে কল্পনা করা যায়। Petzold এটিকে Ocean-এর সঙ্গে তুলনা করেছেন।

```text
Ocean → Water reservoir
Earth → Electron reservoir
```

---

## Q33. Earth-এর সঙ্গে একটি ছোট wire লাগালেই কি ভালো conductor পাওয়া যাবে?

**Answer:**  
সবসময় নয়। Effective Earth connection-এর জন্য যথেষ্ট contact area দরকার। বইয়ে বড় conductive contact, যেমন দীর্ঘ Copper pole-এর উদাহরণ দেওয়া হয়েছে।

---

## Q34. Ground এবং Common কি সবসময় একই জিনিস?

**Answer:**  
না। Chapter 5-এর context-এ:

- **Common** = circuit-এর shared electrical connection
- **Ground** = physical Earth-এর সঙ্গে electrical connection

এই distinction মনে রাখা গুরুত্বপূর্ণ।

---

# Telegraph Questions

## Q35. Telegraph Sounder কীভাবে Dot এবং Dash তৈরি করে?

**Answer:**  
Telegraph Key-এর electrical signal Electromagnet-কে control করে। Electromagnet metal bar টেনে **click** তৈরি করে এবং release হলে **clack** তৈরি হয়।

```text
Fast click-clack → Dot
Slow click...clack → Dash
```

---

## Q36. Telegraph-এ Electromagnet-এর ভূমিকা কী?

**Answer:**  
Electrical Signal-কে Mechanical Movement এবং Sound-এ রূপান্তর করতে Electromagnet ব্যবহৃত হয়।

---

## Q37. Telegraph কেন modern Communication-এর জন্য গুরুত্বপূর্ণ?

**Answer:**  
Telegraph প্রথমবার Communication-কে মানুষের সরাসরি চোখে দেখা বা কানে শোনার সীমা ছাড়িয়ে Electrical Signal এবং Wire-এর মাধ্যমে অনেক দূর পর্যন্ত নিয়ে যায়।

---

# Long-Distance Communication

## Q38. Wire অনির্দিষ্টভাবে লম্বা করা যায় না কেন?

**Answer:**  
Wire যত লম্বা হয় তার Resistance তত বাড়ে। ফলে Current কমে যায় এবং Receiver-এর device পর্যাপ্ত signal পেতে পারে না।

---

## Q39. Long-distance Telegraph-এর জন্য Relay কেন প্রয়োজন?

**Answer:**  
দীর্ঘ Wire-এ signal দুর্বল হয়ে যেতে পারে। Relay Station signal গ্রহণ করে আবার পাঠাতে পারে, ফলে Communication অনেক বেশি দূর পর্যন্ত চালানো সম্ভব হয়।

---

## Q40. Relay Station কীভাবে কাজ করে?

**Answer:**

```text
Incoming Signal
      ↓
Receive
      ↓
Relay
      ↓
New/Strong Signal
      ↓
Next Station
```

অর্থাৎ একটি Relay Station signal গ্রহণ করে পরবর্তী অংশে আবার পাঠায়।

---

# Deep Thinking Questions

## Q41. Chapter 4 এবং Chapter 5-এর মধ্যে মূল connection কী?

**Answer:**  
Chapter 4-এ আমরা Electrical Circuit এবং Switch-এর ON/OFF state শিখেছি।

Chapter 5-এ সেই Electrical State ব্যবহার করে Communication করা হয়েছে।

```text
Chapter 4
Switch → Electrical State

Chapter 5
Electrical State → Communication
```

---

## Q42. Chapter 3-এর Braille এবং Chapter 5-এর Telegraph-এর মধ্যে কী conceptual connection আছে?

**Answer:**  
দুটিই limited physical states ব্যবহার করে information represent করে।

Braille:

```text
Raised / Flat
```

Telegraph:

```text
Dot / Dash
```

Electrical system:

```text
ON / OFF
```

অর্থাৎ:

```text
Two States
    ↓
Code
    ↓
Information
```

---

## Q43. একই Morse Code কীভাবে ভিন্ন physical medium ব্যবহার করতে পারে?

**Answer:**

```text
Morse Code
   │
   ├── Flashlight → Light
   │
   ├── Electrical Circuit → Bulb
   │
   └── Telegraph → Electromagnet → Sound
```

Code একই থাকে, কিন্তু physical representation পরিবর্তিত হয়।

---

## Q44. Long-distance Communication-এ Resistance কেন গুরুত্বপূর্ণ?

**Answer:**  
কারণ wire-এর Resistance signal-এর Current কমিয়ে দেয়।

\[
I=\frac{V}{R}
\]

তাই:

```text
Wire Length ↑
    ↓
Resistance ↑
    ↓
Current ↓
    ↓
Signal weaker
```

---

## Q45. Chapter 5 কীভাবে Computer Architecture-এর দিকে নিয়ে যায়?

**Answer:**

```text
Switch
 ↓
Electrical State
 ↓
Binary Signal
 ↓
Telegraph
 ↓
Electromagnet
 ↓
Relay
 ↓
Automatic Switching
 ↓
Logic
 ↓
Logic Gates
 ↓
Computer
```

অর্থাৎ Chapter 5 physical Electrical Communication থেকে Switching এবং পরবর্তীতে Logic-এর দিকে bridge তৈরি করে।

---

# Practical Thinking Questions

## Q46. ধরো একটি 3V battery এবং একটি 4Ω bulb আছে। Wire-এর Resistance বাড়লে Current-এর কী হবে?

**Answer:**

মূল circuit-এ:

\[
I=\frac{3}{4}=0.75A
\]

কিন্তু wire-এর Resistance যুক্ত হলে মোট Resistance বাড়বে:

\[
I=\frac{3}{R_{total}}
\]

তাই Current 0.75A-এর চেয়ে কম হবে।

---

## Q47. কেন long-distance system-এ 4Ω flashlight bulb-এর পরিবর্তে higher-resistance bulb ব্যবহার করা সুবিধাজনক হতে পারে?

**Answer:**  
Higher-resistance bulb ব্যবহার করলে wire-এর Resistance মোট circuit Resistance-এর তুলনায় কম গুরুত্বপূর্ণ হয়ে ওঠে। বইয়ে 120V, 100W household bulb-এর example দিয়ে এই ধারণা দেখানো হয়েছে।

---

## Q48. যদি একজন Sender এবং Receiver-এর মধ্যে সরাসরি line of sight না থাকে, Chapter 5-এর কোন ধারণা ব্যবহার করবে?

**Answer:**  
Wire-based Electrical Communication ব্যবহার করা যায়।

```text
Switch
 ↓
Electrical Signal
 ↓
Wire
 ↓
Receiver
```

এতে line of sight প্রয়োজন হয় না।

---

## Q49. Telegraph-এ Relay ব্যবহার করলে কী সুবিধা?

**Answer:**  
Long-distance transmission-এ signal দুর্বল হওয়ার সমস্যা কমাতে মাঝখানে Relay Station বসানো যায়। Relay Station signal গ্রহণ করে আবার পরবর্তী অংশে পাঠায়।

---

# Final Challenge

## Q50. Chapter 1 থেকে Chapter 5 পর্যন্ত পুরো conceptual journey ব্যাখ্যা করো।

**Answer:**

```text
Chapter 1
Communication Problem
       ↓
Code
       ↓
Morse Code

Chapter 2
Dot / Dash
       ↓
Two Possibilities
       ↓
Combinations
       ↓
Binary

Chapter 3
Braille
       ↓
Raised / Flat
       ↓
Binary Representation

Chapter 4
Electrical Circuit
       ↓
Switch
       ↓
Open / Closed
       ↓
ON / OFF

Chapter 5
Electrical State
       ↓
Wire
       ↓
Long Distance
       ↓
Telegraph
       ↓
Relay
```

অর্থাৎ Petzold ধীরে ধীরে আমাদের শেখাচ্ছেন:

> **Information → Code → Binary → Physical State → Electricity → Communication → Telegraph**

---

# Final Revision Questions

## Q51. Chapter 5-এর সবচেয়ে গুরুত্বপূর্ণ নতুন ধারণা কী?

**Answer:**  
Electrical Signal এবং Wire ব্যবহার করে line of sight-এর বাইরে Communication করা।

---

## Q52. Chapter 5-এর সবচেয়ে গুরুত্বপূর্ণ Engineering problem কী?

**Answer:**  
Long wire-এর Resistance।

---

## Q53. Resistance বাড়লে Current কীভাবে পরিবর্তিত হয়?

**Answer:**

\[
I=\frac{V}{R}
\]

Voltage একই থাকলে Resistance বাড়লে Current কমে।

---

## Q54. Common কেন ব্যবহার করা হয়েছিল?

**Answer:**  
দুইটি circuit-এর shared connection তৈরি করে wiring requirement কমানোর জন্য।

---

## Q55. Ground এবং Earth-এর relationship কী?

**Answer:**  
Chapter 5-এর context-এ Ground হলো Physical Earth-এর সঙ্গে Electrical Connection।

---

## Q56. Telegraph কীভাবে Flashlight-এর চেয়ে বেশি কার্যকর?

**Answer:**  
Flashlight line of sight-এর ওপর নির্ভরশীল। Telegraph Electrical Signal এবং Wire ব্যবহার করে line of sight-এর বাইরে এবং অনেক বেশি দূরত্বে Communication করতে পারে।

---

## Q57. Relay কেন প্রয়োজনীয় হয়ে ওঠে?

**Answer:**  
Long wire-এর Resistance-এর কারণে signal দুর্বল হতে পারে। Relay Station signal গ্রহণ করে আবার পাঠিয়ে Communication distance বাড়াতে সাহায্য করে।

---

## Q58. Chapter 5-এর একটি বাক্যে সারাংশ কী?

**Answer:**  
**Morse Code-কে Electrical Signal হিসেবে Wire-এর মাধ্যমে পাঠিয়ে line-of-sight-এর সীমাবদ্ধতা অতিক্রম করে Long-distance Communication এবং Telegraph-এর দিকে এগিয়ে যাওয়াই Chapter 5-এর মূল শিক্ষা।**

---

# One-Minute Revision

```text
Seeing Around Corners
        ↓
Flashlight limitation
        ↓
Wire-based electrical circuit
        ↓
Morse over electricity
        ↓
Bidirectional Telegraph
        ↓
Common
        ↓
Earth / Ground
        ↓
Voltage
        ↓
Wire Resistance
        ↓
Ohm's Law
        ↓
AWG / Wire Thickness
        ↓
Long-distance limitation
        ↓
Relay
        ↓
Telegraph
        ↓
Future → Switching → Logic → Computer
```
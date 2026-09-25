# Chapter 6 — Telegraphs and Relays

## 1. Chapter-এর মূল উদ্দেশ্য

এই Chapter-এ Charles Petzold দেখাচ্ছেন কীভাবে **Electrical Signal** ব্যবহার করে অনেক দূরে তথ্য পাঠানো যায় এবং কীভাবে **Relay** ব্যবহার করে সেই signal-কে আবার পরবর্তী circuit-এ পাঠানো যায়।

সবচেয়ে গুরুত্বপূর্ণ বিষয় হলো:

> **একটি Relay হলো এমন একটি Switch যেটিকে মানুষের হাত নয়, Electrical Current control করে।**

এই ধারণাটিই পরবর্তীতে **Logic Gates** এবং শেষ পর্যন্ত Computer-এর Digital Logic বোঝার ভিত্তি তৈরি করবে।

---

# 2. Telegraph কী?

**Telegraph** হলো এমন একটি communication system যেখানে Electrical Signal ব্যবহার করে দূরবর্তী স্থানে information পাঠানো হয়।

শব্দটির অর্থ roughly:

```text
Tele = Far
Graph = Writing
```

অর্থাৎ:

> **Telegraph = Far Writing**

Chapter-এ দেখানো হয়েছে যে মূল ধারণাটি খুব simple:

```text
এক প্রান্তে কিছু করো
        ↓
Wire-এর মাধ্যমে Signal পাঠাও
        ↓
অন্য প্রান্তে কিছু ঘটবে
```

এটি Chapter 5-এর long-distance flashlight-এর ধারণারই একটি উন্নত রূপ।

---

# 3. Telegraph কেন গুরুত্বপূর্ণ?

1800-এর দশকের শুরুতে দুটি সমস্যা ছিল:

### সমস্যা ১ — দ্রুত যোগাযোগ

মানুষের কণ্ঠস্বর বা চোখের দৃষ্টির সীমা ছিল।

### সমস্যা ২ — দূরত্ব

চিঠি পাঠাতে:

```text
Horse
Train
Ship
```

ইত্যাদির প্রয়োজন হতো।

ফলে:

```text
Fast communication
       +
Long distance
       =
একসঙ্গে পাওয়া কঠিন
```

Telegraph এই সমস্যার একটি গুরুত্বপূর্ণ সমাধান দেয়।

বইয়ের ভাষ্য অনুযায়ী, Telegraph এমন একটি সময়ের সূচনা করে যখন মানুষ চোখে দেখা বা কানে শোনার সীমার বাইরেও দ্রুত communication করতে পারল।

---

# 4. Samuel Morse এবং Telegraph

Samuel Finley Breese Morse Telegraph এবং তার সঙ্গে ব্যবহৃত code-এর জন্য বিশেষভাবে পরিচিত।

বইয়ে উল্লেখ করা হয়েছে:

- Morse 1832 সালে Telegraph নিয়ে experiment শুরু করেন।
- 1836 সালে তিনি patent office-কে তার successful telegraph সম্পর্কে জানান।
- 1843 সালে Congress public demonstration-এর জন্য funding দেয়।
- **May 24, 1844**-এ Washington, D.C. এবং Baltimore, Maryland-এর মধ্যে Telegraph demonstration সফল হয়।

প্রেরিত message ছিল:

> “What hath God wrought!”



---

# 5. Morse কেন Lightbulb ব্যবহার করেননি?

এখানে historical context গুরুত্বপূর্ণ।

আমরা Chapter 5-এ flashlight ব্যবহার করে electrical communication-এর ধারণা দেখেছি।

কিন্তু Morse-এর সময় practical lightbulb ছিল না।

বইয়ে বলা হয়েছে, practical lightbulb 1879 সালের আগে আবিষ্কৃত হয়নি।

তাই Morse অন্য একটি physical phenomenon ব্যবহার করেন:

> **Electromagnetism**



---

# 6. Electromagnet কী?

একটি iron bar-এর চারপাশে wire coil পেঁচিয়ে তাতে current প্রবাহিত করলে iron bar magnetic হয়ে যায়।

```text
Current
   │
   ▼
Wire Coil
(((((((((
   │
   ▼
Iron Bar
   │
   ▼
Magnet
```

Current বন্ধ করলে magnetic effect চলে যায়।

```text
Current ON
    ↓
Iron Bar becomes magnetic

Current OFF
    ↓
Magnetic effect disappears
```

এই simple mechanism-ই Telegraph-এর foundation।



---

# 7. Telegraph Key

Telegraph Key দেখতে sophisticated হলেও এর মূল কাজ হলো:

> **একটি দ্রুত এবং আরামদায়ক Switch হিসেবে কাজ করা।**

Operator key press করে signal তৈরি করত।

```text
Key Pressed
     ↓
Circuit Closed
     ↓
Current flows
```

Key ছেড়ে দিলে:

```text
Key Released
     ↓
Circuit Open
     ↓
Current stops
```

---

# 8. Short Press এবং Long Press

Telegraph Key-এর press duration Morse Code-এর অংশ।

```text
Short Press
     ↓
Dot (.)

Long Press
     ↓
Dash (-)
```

অর্থাৎ information শুধু ON/OFF-এর মধ্যে নয়; **কতক্ষণ ON রাখা হচ্ছে** সেটিও গুরুত্বপূর্ণ।

এটি Chapter 1-এর Morse Code ধারণার সঙ্গে সরাসরি connected।



---

# 9. প্রথম Telegraph Receiver

Telegraph-এর receiver-এ একটি electromagnet ছিল।

Electromagnet একটি metal lever বা mechanism control করত।

প্রথম দিকের design-এ electromagnet একটি pen control করত।

```text
Electrical Signal
       ↓
Electromagnet
       ↓
Pen Movement
       ↓
Paper
       ↓
Dots / Dashes
```

অর্থাৎ receiver signal-কে physical marks-এ পরিণত করত।



---

# 10. Telegraph Sounder

পরবর্তীতে operator-রা বুঝতে পারল যে paper-এ dots/dashes লিখে না রেখে sound শুনেও Morse Code decode করা যায়।

তখন traditional **Telegraph Sounder** গুরুত্বপূর্ণ হয়ে ওঠে।

```text
Electromagnet
      ↓
Metal Bar
      ↓
Click / Clack
```

Key press করলে:

```text
Electromagnet ON
       ↓
Metal bar pulled
       ↓
CLICK
```

Key release করলে:

```text
Electromagnet OFF
       ↓
Metal bar returns
       ↓
CLACK
```



---

# 11. Click-Clack কীভাবে Morse Code হয়?

### Dot

দ্রুত:

```text
Click-Clack
```

### Dash

ধীরে:

```text
Click ... Clack
```

অর্থাৎ operator sound-এর timing শুনে Morse Code বুঝতে পারে।

```text
Short duration → Dot
Long duration  → Dash
```

এখানে Chapter 1-এর Morse Code আবার physical world-এর সঙ্গে যুক্ত হচ্ছে।

---

# 12. Telegraph Circuit

একটি basic one-way Telegraph system:

```text
Battery
   ↓
Telegraph Key
   ↓
Long Wire
   ↓
Electromagnet
   ↓
Sounder
```

অর্থাৎ:

```text
Human Action
     ↓
Switch
     ↓
Electrical Signal
     ↓
Wire
     ↓
Electromagnet
     ↓
Mechanical Movement
     ↓
Sound
     ↓
Morse Code
```

---

# 13. Earth as Part of the Circuit

Chapter 5-এর ধারণা ব্যবহার করে দুই station-এর মধ্যে দুইটি wire-এর পরিবর্তে একটি wire ব্যবহার করা যায়, যদি Earth circuit-এর অন্য অংশ হিসেবে ব্যবহৃত হয়।

```text
Station A
   │
   │ Wire
   ▼
Station B
   │
   │
 Earth / Ground
   │
   └───────────────► Return Path
```

এতে wire-এর সংখ্যা কমানো যায়।

---

# 14. Telegraph-এর বড় সমস্যা — Wire Resistance

Long-distance communication-এর সবচেয়ে গুরুত্বপূর্ণ সমস্যাগুলোর একটি ছিল **Wire Resistance**।

Wire যত লম্বা:

```text
Length ↑
   ↓
Resistance ↑
   ↓
Current ↓
   ↓
Signal weaker
```

এ কারণে Telegraph wire অসীম দূরত্ব পর্যন্ত চালানো সম্ভব ছিল না।

বইয়ে বলা হয়েছে, কিছু Telegraph line 300 volts পর্যন্ত ব্যবহার করেও প্রায় 300-mile length-এর মতো কাজ করতে পারত, কিন্তু wire অনির্দিষ্টভাবে বাড়ানো সম্ভব ছিল না।

---

# 15. Relay Station-এর প্রাথমিক ধারণা

Long-distance problem-এর একটি solution ছিল **Relay System**।

প্রথমে মানুষ নিজেই relay হিসেবে কাজ করতে পারত।

উদাহরণ:

```text
New York
   ↓
Operator
   ↓
Operator
   ↓
Operator
   ↓
Operator
   ↓
California
```

প্রতিটি operator:

```text
Message Receive
       ↓
Message Understand
       ↓
Message Resend
```

বইয়ে প্রতি কয়েকশো miles পরপর এমন operator relay station-এর ধারণা দেওয়া হয়েছে।

---

# 16. Human Relay-এর সমস্যা

মানুষ দিয়ে relay করলে:

- মানুষকে সবসময় station-এ থাকতে হবে।
- Message শুনতে হবে।
- বুঝতে হবে।
- আবার key দিয়ে পাঠাতে হবে।

এটি automated নয়।

তখন একটি গুরুত্বপূর্ণ প্রশ্ন আসে:

> **মানুষের কাজটি যদি একটি machine নিজে করতে পারে?**

এখান থেকেই Relay-এর আসল গুরুত্ব শুরু।

---

# 17. Relay কী?

**Relay = Electrically Controlled Switch**

অর্থাৎ:

```text
Normal Switch
     ↓
Human controls switch
```

কিন্তু:

```text
Relay
     ↓
Electrical Current controls switch
```

এটি Chapter-এর সবচেয়ে গুরুত্বপূর্ণ definition।

---

# 18. Relay কীভাবে কাজ করে?

ধরি input side-এ current এসেছে।

```text
Incoming Current
       ↓
Electromagnet
       ↓
Magnetic Attraction
       ↓
Metal Strip moves
       ↓
Switch contact changes
       ↓
Outgoing Circuit
```

অর্থাৎ incoming electrical signal সরাসরি outgoing wire-কে চালায় না; এটি electromagnet-কে control করে, electromagnet mechanical switch-কে control করে, আর সেই switch একটি নতুন powered circuit control করে।



---

# 19. Relay-এর তিনটি গুরুত্বপূর্ণ অংশ

একটি simple relay-এ মূলত তিনটি ধারণা মনে রাখো:

### 1. Input

যে current relay-কে control করে।

### 2. Electromagnet

Input current পেলে magnetic effect তৈরি করে।

### 3. Output Switch

Electromagnet-এর mechanical movement দ্বারা control হয়।

```text
INPUT
  ↓
Electromagnet
  ↓
Mechanical Movement
  ↓
OUTPUT SWITCH
  ↓
OUTPUT
```

---

# 20. Relay কি Signal Amplifier?

বইয়ের ভাষায় incoming weak current ব্যবহার করে stronger outgoing current তৈরি করার অর্থে relay-কে “amplified” signal হিসেবে ব্যাখ্যা করা হয়েছে। কিন্তু conceptually আরও নির্ভুলভাবে ভাবলে:

> Relay incoming signal-এর energy দিয়ে একটি নতুন circuit-এর switch control করে।

অর্থাৎ:

```text
Weak Incoming Current
        ↓
Controls
        ↓
Electromagnet
        ↓
Controls
        ↓
New Powered Circuit
        ↓
Outgoing Current
```

এখানে output-এর power আসে **নতুন battery/power source** থেকে।

---

# 21. Relay Chain

একটি relay-এর output অন্য relay-এর input হতে পারে।

```text
Input
  ↓
Relay 1
  ↓
Relay 2
  ↓
Relay 3
  ↓
Relay 4
  ↓
Output
```

এটি অত্যন্ত গুরুত্বপূর্ণ কারণ একটি relay একা শুধু switch হলেও অনেক relay একসঙ্গে ব্যবহার করলে complex switching system তৈরি করা যায়।

---

# 22. Relay থেকে Logic Gate

Chapter-এর বড় conceptual jump:

```text
Switch
   ↓
Relay
   ↓
Multiple Relays
   ↓
Controlled Switching
   ↓
Logic Gates
   ↓
Computation
```

বই সরাসরি বলে:

> Connecting relays is the key to building logic gates.



অর্থাৎ আমরা এখন Computer-এর দিকে এগোচ্ছি।

---

# 23. Double-Throw Relay

Relay-এর metal piece একটি contact থেকে অন্য contact-এ যেতে পারে।

```text
             Contact A
                ●
                │
                │
          Metal Strip
                │
                ●
             Contact B
```

এক অবস্থায়:

```text
A = ON
B = OFF
```

অন্য অবস্থায়:

```text
A = OFF
B = ON
```

এ ধরনের relay-কে **Double-Throw Relay** বলা হয়।

---

# 24. Chapter 1 থেকে Chapter 6 পর্যন্ত Conceptual Journey

এখন পুরো journey দেখলে বইটির design অনেক পরিষ্কার হয়:

```text
Chapter 1
Code
  ↓
Morse Code
  ↓
Chapter 2
Combinations
  ↓
Two Possible States
  ↓
Binary Concept
  ↓
Chapter 3
Braille / Binary
  ↓
0 / 1
  ↓
Chapter 4
Physical Switch
  ↓
Open / Closed
  ↓
Chapter 5
Electrical Communication
  ↓
Wire
  ↓
Chapter 6
Telegraph
  ↓
Electromagnet
  ↓
Relay
  ↓
Controlled Switching
  ↓
Logic Gates
  ↓
Computer
```

---

# 25. সবচেয়ে গুরুত্বপূর্ণ Mental Model

এই Chapter-টি মনে রাখার জন্য এই chain-টি মুখস্থ না করে বুঝে রাখো:

```text
Human
  ↓
Key
  ↓
Electrical Signal
  ↓
Wire
  ↓
Electromagnet
  ↓
Mechanical Movement
  ↓
Switch
  ↓
Relay
  ↓
More Switching
  ↓
Logic
  ↓
Computation
```

---

# 26. Chapter-এর মূল শিক্ষা

এই Chapter-এ আসলে শুধু Telegraph শেখানো হচ্ছে না।

Petzold ধীরে ধীরে আমাদের দেখাচ্ছেন:

> **একটি simple electrical phenomenon কীভাবে communication system তৈরি করতে পারে, আর সেই একই switching principle কীভাবে পরে computational system তৈরির ভিত্তি হতে পারে।**

Telegraph:

```text
Communication
```

Relay:

```text
Automatic Switching
```

Logic Gate:

```text
Logical Decision
```

Computer:

```text
Large-scale Automated Computation
```

এই progression-টাই Chapter-এর সবচেয়ে গুরুত্বপূর্ণ ধারণা।
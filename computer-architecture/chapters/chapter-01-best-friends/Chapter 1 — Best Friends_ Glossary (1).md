# Chapter 1 — Best Friends

## Glossary

এই ফাইলে Chapter 1 — **Best Friends**-এ ব্যবহৃত গুরুত্বপূর্ণ terms, concepts এবং তাদের সহজ ব্যাখ্যা রাখা হয়েছে।

---

## 1. Code

**Definition:**  
কোনো তথ্যকে নির্দিষ্ট কিছু symbol, signal বা rule ব্যবহার করে প্রকাশ করার পদ্ধতিকে **Code** বলা হয়।

**সহজভাবে:**  
একটি information কীভাবে অন্য একটি form-এ represent করা হবে, তার নিয়মই Code।

**Example:**  
Morse Code-এ একটি letter-কে Dot এবং Dash-এর combination দিয়ে প্রকাশ করা হয়।

**Key Idea:**
```text
Information
    ↓
Representation Rule
    ↓
Code
```

---

## 2. Communication

**Definition:**  
একজনের কাছ থেকে অন্যজনের কাছে information পৌঁছে দেওয়ার প্রক্রিয়াকে **Communication** বলা হয়।

**Chapter Example:**  
দুই বন্ধু flashlight ব্যবহার করে একে অপরের সঙ্গে communicate করছে।

**Basic Flow:**
```text
Sender
   ↓
Information
   ↓
Code
   ↓
Signal
   ↓
Receiver
   ↓
Decode
   ↓
Information
```

---

## 3. Signal

**Definition:**  
Information বহন করার জন্য ব্যবহৃত কোনো physical বা observable পরিবর্তনকে **Signal** বলা যায়।

**Chapter Example:**  
Flashlight-এর আলো জ্বলা ও নিভে যাওয়া একটি signal হিসেবে ব্যবহৃত হচ্ছে।

**Important:**

Flashlight-এর আলো নিজে কোনো letter নয়।  
আলোর **duration এবং timing**-কে একটি Code অনুযায়ী interpret করা হয়।

---

## 4. Flashlight

Chapter-এ flashlight একটি communication device হিসেবে ব্যবহৃত হয়েছে।

দুই বন্ধু flashlight-এর আলো:

- জ্বালায়
- নিভায়
- short এবং long duration তৈরি করে
- pause ব্যবহার করে

এবং এগুলোর মাধ্যমে information communicate করে।

**Mental Model:**
```text
Flashlight
    ↓
Light ON / OFF
    ↓
Different Timing
    ↓
Different Signals
    ↓
Code
```

---

## 5. Morse Code

**Definition:**  
Morse Code হলো এমন একটি Code যেখানে **Dot** এবং **Dash**-এর বিভিন্ন combination ব্যবহার করে letters, numbers এবং অন্যান্য symbols প্রকাশ করা হয়।

**Basic Structure:**

```text
Dot  → .
Dash → -
```

**Example:**

```text
A → .-
B → -...
S → ...
O → ---
```

---

## 6. Dot

**Definition:**  
Morse Code-এ একটি **short signal**-কে Dot হিসেবে represent করা হয়।

```text
Dot → .
```

**Important:**  
Dot নিজে flashlight-এর কোনো আলাদা physical object নয়। এটি একটি **short blink-এর representation**।

---

## 7. Dash

**Definition:**  
Morse Code-এ একটি **long signal**-কে Dash হিসেবে represent করা হয়।

```text
Dash → -
```

**Important:**  
Dash হলো একটি long blink-এর representation।

---

## 8. Short Blink

Flashlight অল্প সময়ের জন্য জ্বালানো হলে সেটিকে Morse Code-এর ক্ষেত্রে **short blink** হিসেবে ব্যবহার করা যায়।

```text
Short Blink
     ↓
   Dot (.)
```

---

## 9. Long Blink

Flashlight তুলনামূলক বেশি সময় জ্বালানো হলে সেটিকে **long blink** হিসেবে ব্যবহার করা যায়।

```text
Long Blink
     ↓
   Dash (-)
```

---

## 10. Pause

**Definition:**  
একটি signal শেষ হওয়ার পর পরবর্তী signal বা character আসার আগে যে সময়ের বিরতি থাকে তাকে **Pause** বলা হয়।

Chapter-এ pause গুরুত্বপূর্ণ, কারণ শুধু light ON হওয়া নয়, **কখন ON/OFF হচ্ছে এবং কতক্ষণ অপেক্ষা করা হচ্ছে** সেটিও Code-এর অংশ।

**Concept:**

```text
Blink → Pause → Blink → Pause
```

অর্থাৎ timing এবং spacing-ও information বহন করতে পারে।

---

## 11. Timing

**Definition:**  
Signal কতক্ষণ স্থায়ী হচ্ছে এবং signal-এর মধ্যে কত সময়ের gap থাকছে—এই temporal arrangement-কে **Timing** হিসেবে বোঝা যায়।

Chapter-এর গুরুত্বপূর্ণ ধারণা:

> Signal-এর শুধু state নয়, signal-এর duration এবং timing-ও meaningful হতে পারে।

---

## 12. Representation

**Definition:**  
কোনো information-কে অন্য কোনো form বা symbol দিয়ে প্রকাশ করাকে **Representation** বলা হয়।

**Example:**

```text
Short Blink → Dot
Long Blink  → Dash
```

এখানে Dot এবং Dash হলো actual light নয়; এগুলো light-এর behavior-এর representation।

---

## 13. Symbol

**Definition:**  
কোনো information বা concept বোঝানোর জন্য ব্যবহৃত একটি চিহ্ন বা representation-কে **Symbol** বলা হয়।

**Chapter Example:**

```text
. → Dot
- → Dash
```

Dot এবং Dash এখানে symbols হিসেবে কাজ করছে।

---

## 14. Encoding

**Definition:**  
Information-কে একটি নির্দিষ্ট Code অনুযায়ী অন্য একটি representation-এ রূপান্তর করার প্রক্রিয়াকে **Encoding** বলা হয়।

**Example:**

```text
Letter A
   ↓
Morse Code
   ↓
.-
   ↓
Flashlight Signal
```

---

## 15. Decoding

**Definition:**  
Code করা signal বা representation থেকে original information বুঝে নেওয়ার প্রক্রিয়াকে **Decoding** বলা হয়।

**Example:**

```text
Flashlight Signal
       ↓
     .-
       ↓
Morse Code
       ↓
      A
```

---

## 16. Sender

**Definition:**  
যে ব্যক্তি বা system information পাঠায় তাকে **Sender** বলা হয়।

**Chapter Example:**  
এক বন্ধু flashlight ব্যবহার করে অন্য বন্ধুর কাছে message পাঠাচ্ছে।

---

## 17. Receiver

**Definition:**  
যে ব্যক্তি বা system signal গ্রহণ করে তাকে **Receiver** বলা হয়।

**Chapter Example:**  
অন্য বন্ধু flashlight-এর signal দেখে message বুঝছে।

---

## 18. Information

**Definition:**  
যে meaningful content একজন Sender থেকে Receiver-এর কাছে communicate করা হয় তাকে **Information** বলা যায়।

**Chapter Examples:**

- Letters
- Words
- Numbers
- Punctuation
- Messages

---

## 19. Binary

**Definition:**  
যে representation system-এ মাত্র **দুইটি possible state বা value** ব্যবহার করা হয়, তাকে Binary system বলা হয়।

Chapter 1-এ Morse Code-এর Dot এবং Dash-এর ধারণা পরবর্তীতে এই Binary ধারণার দিকে নিয়ে যায়।

```text
Two Possibilities

   0 / 1
   or
   Dot / Dash
```

**Important:**  
Chapter 1 সরাসরি computer-এর Binary implementation শেখায় না; বরং **দুইটি simple possibility combine করে কীভাবে অনেক information represent করা যায়**, সেই ধারণার ভিত্তি তৈরি করে।

---

## 20. Combination

**Definition:**  
একাধিক simple symbols বা signals নির্দিষ্টভাবে সাজিয়ে নতুন information তৈরি করাকে **Combination** হিসেবে বোঝা যায়।

**Example:**

```text
.
..
...
.-
-.
--
```

দুই ধরনের signal থাকলেও তাদের বিভিন্ন combination ব্যবহার করে অনেক আলাদা Code তৈরি করা যায়।

---

## 21. Possibility

একটি position-এ যদি দুটি possible signal থাকে, তাহলে প্রতিটি নতুন position মোট possible combination-এর সংখ্যা বাড়ায়।

```text
1 position → 2 possibilities
2 positions → 4 possibilities
3 positions → 8 possibilities
4 positions → 16 possibilities
```

Formula:

```text
Number of possible codes = 2ⁿ
```

এখানে `n` হলো number of positions।

---

## 22. Powers of Two

Chapter-এর একটি গুরুত্বপূর্ণ mathematical idea হলো **Powers of Two**।

```text
2¹ = 2
2² = 4
2³ = 8
2⁴ = 16
2⁵ = 32
2⁶ = 64
```

প্রতিটি নতুন position যোগ হলে সম্ভাব্য combination-এর সংখ্যা দ্বিগুণ হয়।

---

## 23. Common Letters

Morse Code-এ বেশি ব্যবহৃত letters-কে তুলনামূলকভাবে ছোট Code দেওয়া হয়েছে।

**Concept:**

```text
Frequently Used Letter
        ↓
 Shorter Code

Less Frequently Used Letter
        ↓
 Longer Code
```

এর ফলে সাধারণ message তুলনামূলকভাবে efficient ভাবে transmit করা যায়।

---

## 24. Efficient Code

**Definition:**  
যে Code information-কে তুলনামূলক কম signal বা কম সময় ব্যবহার করে represent করতে পারে, তাকে এখানে efficient Code হিসেবে বোঝা যায়।

Morse Code-এ common letters-এর জন্য ছোট sequence ব্যবহারের মাধ্যমে এই efficiency দেখা যায়।

---

## 25. Punctuation

শুধু letters নয়, Code ব্যবহার করে **Punctuation**-ও represent করা যায়।

অর্থাৎ communication system-এ শুধু alphabet নয়, message-এর অন্যান্য গুরুত্বপূর্ণ symbols-ও represent করা সম্ভব।

---

## 26. SOS

**SOS** হলো Morse Code-এর একটি পরিচিত distress signal।

```text
S → ...
O → ---
S → ...

SOS → ... --- ...
```

এটি দেখায় যে Dot এবং Dash-এর combination ব্যবহার করে একটি সম্পূর্ণ meaningful signal তৈরি করা যায়।

---

## 27. Code as a System

Code শুধু কিছু random symbols-এর collection নয়।

একটি Code-এর মধ্যে থাকে:

```text
Symbols
   +
Rules
   +
Meaning
   ↓
Code System
```

অর্থাৎ কোন signal কোন information represent করবে, তার নির্দিষ্ট rule থাকতে হয়।

---

## 28. Human Language

মানুষের language-ও information represent এবং communicate করার একটি system হিসেবে Chapter-এর Code ধারণার সঙ্গে সম্পর্কিত।

উদাহরণ:

```text
Thought / Meaning
       ↓
Language
       ↓
Words / Sounds
       ↓
Communication
```

---

## 29. Braille

**Braille** হলো touch-based writing system যেখানে raised dots-এর বিভিন্ন pattern ব্যবহার করে letters এবং অন্যান্য information represent করা হয়।

Chapter-এর Code ধারণার সঙ্গে এর সম্পর্ক:

```text
Information
    ↓
Dot Pattern
    ↓
Meaning
```

---

## 30. Sign Language

**Sign Language**-এ হাতের movement, position এবং অন্যান্য visual signs ব্যবহার করে information communicate করা হয়।

এটিও দেখায় যে information communicate করার জন্য spoken language একমাত্র মাধ্যম নয়।

---

## 31. Shorthand

**Shorthand** বা stenography হলো দ্রুত লেখার জন্য ব্যবহৃত একটি writing system যেখানে শব্দ বা sound-কে সংক্ষিপ্ত symbols বা forms দিয়ে represent করা হয়।

এখানেও মূল ধারণা:

```text
Large / Complex Information
          ↓
Compact Representation
```

---

# Core Concept Map

```text
Communication
      ↓
Information
      ↓
Need a Representation
      ↓
Code
      ↓
Signal
      ↓
Flashlight
      ↓
Short / Long Blink
      ↓
Dot / Dash
      ↓
Morse Code
      ↓
Combination
      ↓
Many Possible Messages
      ↓
Binary Concept
      ↓
Computer
```

---

# Most Important Terms

Chapter 1 শেষ করার পর অন্তত এই termsগুলো অবশ্যই মনে রাখা উচিত:

| Term | এক লাইনে অর্থ |
|---|---|
| Code | Information represent করার নির্দিষ্ট system |
| Communication | Information এক জায়গা থেকে অন্য জায়গায় পৌঁছানো |
| Signal | Information বহনকারী observable পরিবর্তন |
| Representation | Information-কে অন্য form-এ প্রকাশ করা |
| Morse Code | Dot ও Dash ব্যবহার করা Code |
| Dot | Short signal-এর representation |
| Dash | Long signal-এর representation |
| Pause | Signal-এর মধ্যে বিরতি |
| Timing | Signal-এর duration ও gap-এর arrangement |
| Encoding | Information → Code/Signal |
| Decoding | Code/Signal → Information |
| Sender | Information পাঠায় |
| Receiver | Information গ্রহণ করে |
| Binary | দুইটি possible state/value-এর representation |
| Combination | Simple symbols মিলিয়ে complex information তৈরি |
| Powers of Two | দুইটি possibility থেকে combination বৃদ্ধির mathematical pattern |

---

# Chapter 1-এর মূল Mental Model

সবচেয়ে গুরুত্বপূর্ণ ধারণাটি এভাবে মনে রাখো:

```text
একটি Information
       ↓
সরাসরি পাঠানো কঠিন
       ↓
একটি Representation দরকার
       ↓
Representation-এর Rules দরকার
       ↓
Code তৈরি হয়
       ↓
Simple Signals ব্যবহার করা হয়
       ↓
Signals-এর Combination তৈরি হয়
       ↓
অনেক Complex Information represent করা যায়
```

### One-Line Revision

> **Simple signals + rules + combinations = complex information representation.**

এই ধারণাটিই পরবর্তী chapters-এ Computer-এর Binary, Bits, Logic এবং Hardware বোঝার ভিত্তি তৈরি করবে।
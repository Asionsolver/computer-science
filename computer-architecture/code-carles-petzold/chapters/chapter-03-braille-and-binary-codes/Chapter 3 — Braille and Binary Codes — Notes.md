# Chapter 3 — Braille and Binary Codes

## 1. Chapter-এর মূল উদ্দেশ্য

এই Chapter-এর উদ্দেশ্য Braille মুখস্থ করা নয়। Petzold Braille-কে একটি example হিসেবে dissect করেছেন, যাতে **Code কীভাবে কাজ করে এবং Binary-এর সঙ্গে Code-এর সম্পর্ক কী**—সেটা বোঝা যায়।

Chapter-এর মূল প্রশ্ন:

> কীভাবে কয়েকটি simple binary state ব্যবহার করে অনেক ধরনের information represent করা যায়?

---

# 2. Braille কী?

Braille হলো raised-dot ভিত্তিক একটি code system, যা বিশেষভাবে দৃষ্টিপ্রতিবন্ধী মানুষের জন্য written language স্পর্শের মাধ্যমে পড়তে সাহায্য করে।

একটি Braille character একটি **2 × 3 cell**-এর মধ্যে তৈরি হয়।

```text
● ●
● ●
● ●
```

প্রতিটি অবস্থান:

```text
Raised
অথবা
Flat
```

অর্থাৎ প্রতিটি position-এর দুটি possible state আছে।

PDF-এ dots-গুলোকে 1 থেকে 6 পর্যন্ত number করা হয়েছে।

---

# 3. Braille কেন Binary?

Binary-এর মূল বৈশিষ্ট্য হলো—প্রতিটি element-এর দুটি possible state।

Braille-এর একটি dot:

```text
Raised → 1
Flat   → 0
```

তাই একটি Braille cell-কে আমরা binary structure হিসেবে দেখতে পারি।

```text
Dot 1 → 0 / 1
Dot 2 → 0 / 1
Dot 3 → 0 / 1
Dot 4 → 0 / 1
Dot 5 → 0 / 1
Dot 6 → 0 / 1
```

এখানে গুরুত্বপূর্ণ হলো:

> Braille নিজে computer binary system হিসেবে তৈরি হয়নি; কিন্তু এর প্রতিটি dot-এর দুটি state থাকার কারণে এটিকে Binary-এর সাহায্যে বিশ্লেষণ করা যায়।

---

# 4. 6 Dots থেকে 64 Codes

প্রতিটি dot-এর 2টি possibility:

```text
Dot → 2 possibilities
```

৬টি independent dot থাকলে:

```text
2 × 2 × 2 × 2 × 2 × 2

= 2⁶

= 64
```

অর্থাৎ ৬টি binary element থেকে সর্বোচ্চ:

```text
64 unique combinations
```

তৈরি করা সম্ভব।

এটি Chapter 2-এ শেখা combinatorics-এর সরাসরি প্রয়োগ।

---

# 5. Code Space

এখানে একটি গুরুত্বপূর্ণ ধারণা হলো **Code Space**।

৬টি binary position:

```text
000000
000001
000010
000011
...
111111
```

মোট:

```text
64 combinations
```

এগুলো হলো available code space।

এরপর designer-কে ঠিক করতে হয়:

> কোন combination-এর কী meaning হবে?

অর্থাৎ:

```text
Binary Pattern
      ↓
Assign Meaning
      ↓
Code
```

---

# 6. Braille Alphabet

Braille-এর lowercase alphabet-এর মধ্যে pattern দেখা যায়।

প্রথম row:

```text
a–j
```

এগুলো top four positions—dots 1, 2, 4, 5—ব্যবহার করে।

দ্বিতীয় row-তে সেই pattern-এর সঙ্গে dot 3 যুক্ত হয়।

তৃতীয় row-তে dot 3 এবং dot 6-এর ব্যবহার দেখা যায়।

অর্থাৎ code system-এ সব character আলাদা করে randomভাবে বানানো হয়নি; pattern এবং reuse ব্যবহার করা হয়েছে।

---

# 7. Space-ও একটি Code

Computer text representation-এর জন্য শুধু letters যথেষ্ট নয়।

আমাদের দরকার:

```text
A–Z
a–z
0–9
Punctuation
Space
```

Braille-এ word-এর মধ্যে separation-এর জন্য raised-dot ছাড়া একটি cell space হিসেবে ব্যবহৃত হয়।

এখান থেকে Computer-এর text representation সম্পর্কে গুরুত্বপূর্ণ ধারণা পাওয়া যায়:

> Space-ও একটি meaningful character/code হতে পারে।

---

# 8. 64 Codes কিন্তু শুধু 64 Letters নয়

৬টি dot থেকে 64টি combination পাওয়া গেলেও সবগুলো শুধু alphabet-এর জন্য ব্যবহার করা হয়নি।

Code space-এর মধ্যে বিভিন্ন ধরনের কাজ রাখা যায়:

```text
Letters
Numbers
Punctuation
Space
Contractions
Indicators
Shift Codes
```

এখানে একটি গুরুত্বপূর্ণ engineering idea আছে:

> Limited code space-কে কীভাবে efficiently ব্যবহার করা যায়?

---

# 9. Context এবং Shift Code

Braille-এর সবচেয়ে গুরুত্বপূর্ণ ধারণাগুলোর একটি হলো **context-dependent interpretation**।

কিছু code সরাসরি একটি character represent করে।

কিছু code আবার পরবর্তী code-গুলোর interpretation পরিবর্তন করে।

এগুলোকে Chapter-এ **precedence / shift codes** হিসেবে আলোচনা করা হয়েছে।

মূল pattern:

```text
Indicator
    ↓
Context changes
    ↓
Following codes
    ↓
New interpretation
```

---

# 10. Number Indicator

Braille-এর number representation-এর ক্ষেত্রে একটি special code ব্যবহার করা হয়।

ধারণাটি:

```text
Number Indicator
       ↓
পরবর্তী codes
       ↓
Numbers হিসেবে interpret
```

তারপর একটি letter indicator number mode থেকে আবার letter mode-এ ফিরিয়ে নেয়।

```text
Letter Mode
    ↓
Number Indicator
    ↓
Number Mode
    ↓
Digits
    ↓
Letter Indicator
    ↓
Letter Mode
```

অর্থাৎ indicator code নিজে সবসময় মূল data নয়; এটি পরের data কীভাবে interpret হবে তা নির্ধারণ করতে পারে।

---

# 11. Capital Indicator

Capital letter represent করার জন্যও একটি special indicator ব্যবহৃত হয়।

Conceptually:

```text
Capital Indicator
      +
Letter Code
      ↓
Uppercase Letter
```

অর্থাৎ একটি capital letter-এর জন্য মূল letter code-এর সঙ্গে অতিরিক্ত indicator প্রয়োজন হয়।

PDF অনুযায়ী, তাই capital letter একটি code-এর বদলে দুইটি code ব্যবহার করতে পারে।

---

# 12. কেন Context গুরুত্বপূর্ণ?

ধরো code space সীমিত।

আমাদের হাতে:

```text
64 possible patterns
```

কিন্তু আমাদের দরকার:

```text
Letters
+
Numbers
+
Punctuation
+
Other functions
```

তাহলে একই code space-কে আরও কার্যকরভাবে ব্যবহার করার একটি উপায় হলো **context**।

```text
Limited Codes
     ↓
Indicator
     ↓
Change Context
     ↓
Reuse Meaning
```

এই কারণে context-based code design গুরুত্বপূর্ণ।

---

# 13. Morse vs Braille

এখন Chapter-এর সবচেয়ে গুরুত্বপূর্ণ comparison।

### Morse

Morse হলো **Variable-Length Code**।

উদাহরণ:

```text
E → .
A → .-
S → ...
O → ---
```

কোনো character ১টি signal দিয়ে হতে পারে, আবার অন্য character-এর জন্য বেশি signal প্রয়োজন হতে পারে।

Morse frequently used letters-এর জন্য shorter code ব্যবহার করে। এটি telegraphy-এর জন্য কার্যকর, কিন্তু computer-এর ক্ষেত্রে character boundary এবং variable length handling বেশি awkward হতে পারে। Morse uppercase এবং lowercase-ও আলাদা করে না।

---

### Braille

Braille হলো **Fixed-Width Code**।

প্রতিটি character-এর জন্য ৬টি dot position আছে।

```text
Character
    ↓
6 positions
    ↓
6 bits
```

এই fixed structure computer-এর জন্য বেশি convenient।

```text
Character 1 → 6 bits
Character 2 → 6 bits
Character 3 → 6 bits
```

প্রতিটি character কোথা থেকে শুরু/শেষ হয়েছে তা নির্ধারণ করা সহজ।

---

# 14. Fixed-Length বনাম Variable-Length

```text
Variable-Length

[A]
[BB]
[CCC]
[DDDD]
[EEEEE]

প্রতিটির size আলাদা
```

অন্যদিকে:

```text
Fixed-Length

[AAAAAA]
[BBBBBB]
[CCCCCC]
[DDDDDD]

সবগুলোর size একই
```

Computer-এর জন্য fixed-width representation-এর একটি সুবিধা হলো predictable boundary।

এটি Chapter-এর Morse বনাম Braille comparison-এর মূল ধারণা।

---

# 15. Text কী?

Computer-এর দৃষ্টিতে text-কে printed page-এর মতো ভাবা উচিত নয়।

একটি printed page:

```text
┌─────────────────────────┐
│ I have 27 sisters.      │
│                         │
│ ...                     │
└─────────────────────────┘
```

কিন্তু Computer-এর জন্য conceptually:

```text
I
space
h
a
v
e
space
2
7
space
s
i
s
t
e
r
s
.
```

অর্থাৎ text হলো একটি **one-dimensional stream of characters**।

---

# 16. Character Code

Computer-কে text store/process করার জন্য প্রতিটি character-এর জন্য একটি code দরকার।

```text
Character
    ↓
Character Code
    ↓
Bits
```

যেমন:

```text
'A' → character code
'B' → character code
'7' → character code
'.' → character code
' ' → character code
```

সব character-এর code মিলে একটি **coded character set** তৈরি হয়।

---

# 17. Text String

ধরো:

```text
I have 27 sisters.
```

এখানে প্রতিটি character-এর একটি code আছে।

```text
I
space
h
a
v
e
space
2
7
space
s
...
```

এই consecutive character codes-এর sequence-কে **text string** বলা হয়।

---

# 18. Text-এর "2" এবং Number 2 একই নয়

এটি খুব গুরুত্বপূর্ণ।

ধরো:

```text
I have 27 sisters.
```

এখানে `2` এবং `7` হলো **text characters**।

তাই:

```text
'2'
'7'
```

এর character code থাকতে পারে।

অন্যদিকে:

```text
2
7
```

যখন numerical value হিসেবে ব্যবহৃত হয়, তখন binary representation অন্য concept।

অর্থাৎ:

```text
"2" as text
      ≠
2 as numerical value
```

PDF-এ বলা হয়েছে যে text-এর মধ্যে `2` এবং `7`-এর character codes তাদের numerical values-এর binary representation-এর সঙ্গে একই হওয়া বাধ্যতামূলক নয়।

---

# 19. Baudot Code

Chapter পরে একটি economical text code হিসেবে Baudot/ITA-2 নিয়ে আলোচনা করে।

এটি:

```text
5-bit Code
```

তাই possible combinations:

```text
2⁵ = 32
```

অর্থাৎ মোট 32টি possible code।

এগুলোর মধ্যে letters ছাড়াও space, carriage return, line feed এবং shift-related codes রয়েছে।

---

# 20. Teletypewriter

Baudot-এর ব্যবহার বোঝাতে Chapter-এ teletypewriter-এর কথা এসেছে।

Conceptually:

```text
Keyboard
   │
   ▼
Switches
   │
   ▼
Binary Code
   │
   ▼
One Bit at a Time
   │
   ▼
Output Cable
   │
   ▼
Receiving Machine
   │
   ▼
Printing Mechanism
```

অর্থাৎ physical keyboard switch → binary code → transmission → electromagnet → printed character—এই chain দেখা যায়।

---

# 21. Shift Code-এর সুবিধা ও সমস্যা

Shift code-এর সুবিধা:

```text
কম code
   ↓
একই code space পুনরায় ব্যবহার
   ↓
Economical
```

কিন্তু সমস্যা:

```text
Current Context / State
        ↓
পরবর্তী codes-এর meaning নির্ভরশীল
```

যদি system ভুল context-এ থাকে, তাহলে পরবর্তী character ভুলভাবে interpret হতে পারে।

Chapter-এ Baudot-এর Figure Shift এবং Letter Shift-এর মাধ্যমে এই ধরনের state problem দেখানো হয়েছে।

---

# 22. Chapter-এর বড় ধারণা: Representation

এই Chapter-এর আসল শিক্ষা শুধু Braille নয়।

মূল বিষয় হলো:

```text
Real Information
      ↓
Representation
      ↓
Code
      ↓
Binary States
      ↓
Combinations
      ↓
Computer Data
```

একটি computer সরাসরি:

```text
A
B
C
```

বোঝে না।

বরং এগুলোকে একটি agreed representation-এর মাধ্যমে code করতে হয়।

---

# 23. Binary থেকে Computer Text

পুরো concept:

```text
Physical State
     ↓
0 / 1
     ↓
Binary
     ↓
Multiple Bits
     ↓
Combinations
     ↓
Code
     ↓
Character
     ↓
Text
```

এটাই Chapter 3-এর সবচেয়ে গুরুত্বপূর্ণ bridge:

> **Binary শুধু সংখ্যা represent করার জন্য নয়; Binary states ব্যবহার করে character এবং text-ও represent করা যায়।**

---

# 24. Chapter 3-এর Core Mental Model

```text
Braille
   ↓
6 Binary Elements
   ↓
2⁶ = 64 Possible Codes
   ↓
Assign Meanings
   ↓
Letters / Numbers / Punctuation
   ↓
Context + Shift Codes
   ↓
Character Codes
   ↓
Text String
   ↓
Binary Representation
   ↓
Computer
```

---

# 25. One-Minute Revision

- Braille-এর একটি cell-এ ৬টি dot position থাকে।
- প্রতিটি dot Raised বা Flat হতে পারে।
- তাই প্রতিটি dot একটি Binary element হিসেবে দেখা যায়।
- ৬টি Binary element → `2⁶ = 64` possible combinations।
- সব code শুধু letter-এর জন্য নয়।
- Numbers, punctuation, spaces এবং control/shift functions-এর জন্যও code space ব্যবহৃত হয়।
- কিছু code context পরিবর্তন করে।
- Number Indicator → পরবর্তী code-গুলো number হিসেবে interpret হতে পারে।
- Letter Indicator → আবার letter context-এ ফিরতে পারে।
- Capital Indicator → পরবর্তী letter uppercase নির্দেশ করে।
- Morse হলো Variable-Length Code।
- Braille হলো Fixed-Width Code।
- Computer-এর জন্য fixed-width representation অনেক ক্ষেত্রে convenient।
- Text হলো character-এর একটি one-dimensional stream।
- প্রতিটি character-এর জন্য Character Code দরকার।
- Character code এবং numerical value এক জিনিস নয়।
- Consecutive character codes-এর sequence-কে Text String বলা হয়।
- Baudot/ITA-2 হলো 5-bit code → `2⁵ = 32` possible codes।
- Shift-based system economical হলেও state/context-এর কারণে complexity তৈরি করতে পারে।

### Chapter 3-এর এক বাক্যের সারাংশ

> **Braille দেখায় কীভাবে কয়েকটি binary state-এর combination ব্যবহার করে একটি limited code space তৈরি করে letters, numbers এবং অন্যান্য information represent করা যায়—এবং সেখান থেকেই computer text-এর Character Code ধারণার দিকে যাওয়া যায়।**
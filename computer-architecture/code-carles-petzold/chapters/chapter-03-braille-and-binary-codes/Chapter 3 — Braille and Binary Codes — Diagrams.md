# Chapter 3 — Braille and Binary Codes

## 1. Chapter Overview

```text
                    CODE
                      │
          ┌───────────┴───────────┐
          │                       │
       Morse                    Braille
          │                       │
   Dot / Dash                Raised / Flat
          │                       │
 Variable-Length             Fixed 6-position
          │                       │
          │                  6 Binary Elements
          │                       │
          │                    2⁶ = 64
          │                       │
          └───────────┬───────────┘
                      │
                    Binary
                      │
                      ▼
              Computer Text Code
                      │
          ┌───────────┼───────────┐
          │           │           │
       Letters     Numbers    Punctuation
          │           │           │
          └───────────┼───────────┘
                      │
                Character Codes
                      │
                      ▼
                  Text String
```

---

# 2. Braille Cell

Braille-এর একটি cell-এ ৬টি position থাকে।

```text
      Braille Cell

       1 ●    4 ●
       2 ●    5 ●
       3 ●    6 ●
```

প্রতিটি dot-এর দুটি possible state:

```text
Raised → 1
Flat   → 0
```

তাই:

```text
       6 dots
          │
          ▼
   প্রতিটি dot-এর 2 states
          │
          ▼
       2 × 2 × 2 × 2 × 2 × 2
          │
          ▼
           2⁶
          │
          ▼
          64
```

অর্থাৎ ৬টি binary element থেকে সর্বোচ্চ **64টি unique code** তৈরি করা যায়।

---

# 3. One Braille Character → Six Bits

Conceptually:

```text
Braille:

   ●    ○
   ●    ●
   ○    ○

Raised = 1
Flat   = 0

      ↓

   1    0
   1    1
   0    0

      ↓

   101100
```

অর্থাৎ Braille-এর প্রতিটি character-কে ৬টি binary position হিসেবে দেখা যায়।

```text
Braille Character
       │
       ▼
  6 dot positions
       │
       ▼
Each = 0 or 1
       │
       ▼
    6 Bits
```

---

# 4. Binary Combination

প্রতিটি position-এ দুটি সম্ভাবনা:

```text
Position 1 → 0 / 1
Position 2 → 0 / 1
Position 3 → 0 / 1
Position 4 → 0 / 1
Position 5 → 0 / 1
Position 6 → 0 / 1
```

তাই:

```text
2 choices
   ×
2 choices
   ×
2 choices
   ×
2 choices
   ×
2 choices
   ×
2 choices

= 2⁶
= 64
```

---

# 5. Braille-এর Basic Alphabet Pattern

Braille-এর lowercase alphabet-এ একটি pattern দেখা যায়।

```text
First Row
a → j

uses:
1, 2, 4, 5
```

Conceptually:

```text
a–j
 │
 ├── dots 1,2,4,5
 │
 ▼
First Row
```

তারপর:

```text
Second Row
a–j pattern + dot 3
```

তারপর:

```text
Third Row
previous pattern + dots 3 and 6
```

অর্থাৎ Braille-এ code design-এ pattern এবং reuse গুরুত্বপূর্ণ।

---

# 6. 64 Possible Codes

```text
6 Binary Dots
      │
      ▼
     2⁶
      │
      ▼
  64 possible
    codes
```

কিন্তু:

```text
64 Possible Codes
        │
        ▼
সবগুলো শুধু letters-এর জন্য নয়
        │
        ├── Letters
        ├── Numbers
        ├── Punctuation
        ├── Space
        ├── Contractions
        └── Shift / Indicator Codes
```

Chapter-এর গুরুত্বপূর্ণ observation হলো—Braille-এর available code space-এর অনেক code context অনুযায়ী বিভিন্ন কাজ করতে পারে।

---

# 7. Context / Shift Code

সব code সরাসরি data represent করে না।

কিছু code পরের code-গুলোকে কীভাবে interpret করতে হবে তা পরিবর্তন করে।

```text
        Indicator
            │
            ▼
     Context পরিবর্তন
            │
            ▼
    পরের code-এর meaning
       পরিবর্তিত হয়
```

### Number Mode

```text
Number Indicator
       │
       ▼
Number Context
       │
       ├── code → digit
       ├── code → digit
       └── code → digit
       │
       ▼
Letter Indicator
       │
       ▼
Letter Context
```

### Capital Letter

```text
Capital Indicator
       │
       ▼
Next character
       │
       ▼
Uppercase
```

PDF অনুযায়ী capital letter-এর জন্য special escape/indicator code ব্যবহৃত হয় এবং number representation-এর জন্য shift code ব্যবহৃত হয়।

---

# 8. Important Context Model

```text
Same Code Space
      │
      ▼
 ┌───────────────┐
 │ Context       │
 └───────┬───────┘
         │
   ┌─────┴─────┐
   │           │
Letters      Numbers
   │           │
code X       code X
   │           │
   ▼           ▼
Letter       Number
```

**মূল ধারণা:**

```text
Indicator
   ↓
Context
   ↓
Interpretation
```

---

# 9. Morse vs Braille

```text
             Morse              Braille
               │                   │
               │                   │
         Dot / Dash           Raised / Flat
               │                   │
               ▼                   ▼
       Variable-Length        Fixed 6-position
               │                   │
               ▼                   ▼
     Character length varies   6 bits/character
               │                   │
               ▼                   ▼
       Telegraphy useful       Computer-এর জন্য
                               বেশি convenient
```

Morse frequently-used letters-এর জন্য ছোট code এবং less-common letters-এর জন্য বড় code ব্যবহার করে। Braille fixed-width হওয়ায় computer-এর জন্য representation তুলনামূলকভাবে সহজ।

---

# 10. Text as a One-Dimensional Stream

Computer text-কে printed page-এর মতো দুই-dimensional layout হিসেবে না দেখে একটি stream হিসেবে ভাবা যায়।

```text
"I have 27 sisters."

      ↓

I
↓
space
↓
h
↓
a
↓
v
↓
e
↓
space
↓
2
↓
7
↓
space
↓
s
↓
...
```

অর্থাৎ:

```text
Text
 │
 ▼
Sequence of Characters
 │
 ▼
Character Codes
 │
 ▼
Bit Stream
```

এই consecutive character codes-এর sequence-কে **text string** বলা হয়।

---

# 11. Character Code ≠ Numerical Value

খুব গুরুত্বপূর্ণ:

```text
Text-এর "2"
```

এবং

```text
Number 2
```

একই জিনিস নয়।

Text-এর মধ্যে:

```text
"27"
```

হলে:

```text
'2' → Character
'7' → Character
```

এগুলোকে character code দিয়ে represent করা যায়।

অন্যদিকে:

```text
2 → Numerical Value
```

এটি binary number হিসেবে অন্যভাবে represent হতে পারে।

Diagram:

```text
        "2"
         │
         ├──────────────┐
         │              │
    Text Character   Numerical Value
         │              │
         ▼              ▼
   Character Code    Binary Number
```

PDF স্পষ্টভাবে এই distinction তুলে ধরে।

---

# 12. Coded Character Set

Computer-এ text represent করতে দরকার:

```text
Letters
   +
Numbers
   +
Punctuation
   +
Space
   +
Control Characters
```

তারপর:

```text
All Characters
      │
      ▼
Coded Character Set
      │
      ▼
Each Character
      │
      ▼
Character Code
```

---

# 13. Baudot / ITA-2

Baudot একটি 5-bit code।

```text
5 Bits
  │
  ▼
2⁵
  │
  ▼
32 possible codes
```

```text
Baudot
   │
   ├── Letters
   ├── Space
   ├── Carriage Return
   ├── Line Feed
   ├── Figure Shift
   └── Letter Shift
```

Teletypewriter-এ keyboard-এর switches binary code generate করে এবং bits একটির পর একটি transmit করা হয়।

---

# 14. Shift Code Problem

Baudot-এর মতো shift-code system-এ state গুরুত্বপূর্ণ।

```text
Letter Mode
    │
    ▼
Figure Shift
    │
    ▼
Number/Figure Mode
    │
    ▼
Characters interpreted
as figures
    │
    ▼
Letter Shift
    │
    ▼
Letter Mode
```

যদি shift state সঠিকভাবে reset না হয়:

```text
Expected:
I SPENT $25 TODAY.

Possible problem:
পরের অংশ ভুল context-এ interpret হতে পারে
```

অর্থাৎ shift code economical হলেও state-management complexity তৈরি করতে পারে।

---

# 15. Chapter 3 Complete Flow

```text
Braille
  │
  ▼
6 Dots
  │
  ▼
Each Dot = Raised / Flat
  │
  ▼
Binary
  │
  ▼
2⁶ = 64 Codes
  │
  ▼
Letters + Numbers + Punctuation
  │
  ▼
Context / Shift Codes
  │
  ▼
Character Codes
  │
  ▼
Text String
  │
  ▼
Binary Data
  │
  ▼
Computer Text Representation
```

---

# 16. Chapter 3 Mental Model

```text
Limited Physical States
          ↓
      Binary States
          ↓
   Many Combinations
          ↓
      Code Space
          ↓
      Assign Meaning
          ↓
   Character Codes
          ↓
     Text String
          ↓
 Computer Representation
```

### One-line revision

```text
6 binary dots → 2⁶ = 64 codes → meaning assigned through context → character codes → text as a stream of bits
```
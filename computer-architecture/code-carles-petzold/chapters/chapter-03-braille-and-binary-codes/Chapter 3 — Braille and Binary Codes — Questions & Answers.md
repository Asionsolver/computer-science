# Chapter 3 — Braille and Binary Codes

> **নোট:** প্রতিটি প্রশ্নের সঙ্গে উত্তর দেওয়া হয়েছে। প্রশ্নগুলো Basic → Conceptual → Deep Thinking → Computer Science Connection → Revision এই progression-এ সাজানো।

---

# Part 1 — Basic Understanding

## Q1. Chapter 3-এর মূল উদ্দেশ্য কী?

**Answer:**

Chapter-এর উদ্দেশ্য Braille মুখস্থ করানো নয়। Braille-কে dissect করে দেখানো যে একটি Code কীভাবে কাজ করে এবং Binary-এর সঙ্গে Code-এর কী সম্পর্ক রয়েছে।

---

## Q2. Braille কী?

**Answer:**

Braille হলো raised-dot ভিত্তিক একটি code system, যার মাধ্যমে দৃষ্টিপ্রতিবন্ধী মানুষ স্পর্শের মাধ্যমে written language পড়তে পারে।

---

## Q3. একটি Braille cell-এ কতটি dot position থাকে?

**Answer:**

একটি Braille cell-এ ৬টি dot position থাকে।

```text
1 4
2 5
3 6
```

---

## Q4. Braille-এর প্রতিটি dot-এর কী কী state থাকতে পারে?

**Answer:**

প্রতিটি dot দুটি state-এর একটিতে থাকতে পারে:

```text
Raised
Flat
```

এই দুটি state-এর কারণে dot-কে Binary element হিসেবে দেখা যায়।

---

## Q5. Braille-কে Binary হিসেবে দেখা যায় কেন?

**Answer:**

কারণ প্রতিটি Braille dot-এর দুটি possible state:

```text
Raised → 1
Flat   → 0
```

Binary-এর মূল বৈশিষ্ট্যও দুটি possible state। তাই Braille-এর dots-কে Binary elements হিসেবে বিশ্লেষণ করা যায়।

---

# Part 2 — Combinatorics and Binary

## Q6. ৬টি Braille dot থেকে কতটি possible combination তৈরি হতে পারে?

**Answer:**

প্রতিটি dot-এর ২টি state এবং মোট ৬টি dot।

```text
2⁶ = 64
```

অতএব ৬টি dot থেকে সর্বোচ্চ **64টি unique combination** তৈরি করা সম্ভব।

---

## Q7. `2⁶ = 64` কেন?

**Answer:**

প্রতিটি dot-এর ২টি possibility আছে।

```text
2 × 2 × 2 × 2 × 2 × 2
= 2⁶
= 64
```

---

## Q8. Braille-এর 64টি combination কি 64টি letter-এর জন্য ব্যবহৃত হয়?

**Answer:**

না।

এই 64টি possible code বিভিন্ন কাজের জন্য ব্যবহার করা যায়, যেমন:

- Letters
- Numbers
- Punctuation
- Space
- Contractions
- Indicator/Shift functions

---

## Q9. Code Space বলতে কী বোঝায়?

**Answer:**

একটি code system-এর মধ্যে যতগুলো possible code combination তৈরি করা যায়, সেই complete set-কে Code Space হিসেবে ভাবা যায়।

Braille-এর ক্ষেত্রে:

```text
6 binary positions
→ 2⁶
→ 64 possible codes
```

---

# Part 3 — Braille Structure

## Q10. Braille-এর lowercase alphabet-এ কী ধরনের pattern দেখা যায়?

**Answer:**

প্রথম row-এর a–j letters dots 1, 2, 4, 5 ব্যবহার করে। দ্বিতীয় row-তে dot 3 যুক্ত হয় এবং তৃতীয় row-তে dot 3 ও 6-এর ব্যবহার দেখা যায়।

অর্থাৎ code design-এ pattern এবং reuse করা হয়েছে।

---

## Q11. Braille-এ space কীভাবে represent করা হয়?

**Answer:**

Raised dot ছাড়া একটি cell word-এর মধ্যবর্তী space represent করতে ব্যবহৃত হয়।

---

## Q12. Braille-এর প্রতিটি character-কে কীভাবে binary representation হিসেবে দেখা যায়?

**Answer:**

প্রতিটি character-এর ৬টি dot position আছে এবং প্রতিটি position:

```text
Raised → 1
Flat   → 0
```

তাই একটি character-কে ৬টি binary state দিয়ে represent করা যায়।

---

# Part 4 — Context and Shift Codes

## Q13. Indicator Code কী?

**Answer:**

Indicator Code এমন একটি code যা নিজে সরাসরি মূল information represent না করে পরবর্তী code-গুলো কীভাবে interpret করতে হবে তা নির্দেশ করতে পারে।

---

## Q14. Context বলতে কী বোঝায়?

**Answer:**

Context হলো বর্তমান interpretation state।

একটি code কোন অর্থে interpret হবে তা কখনও কখনও তার আগে থাকা indicator বা shift-এর ওপর নির্ভর করতে পারে।

---

## Q15. Shift Code কী?

**Answer:**

Shift Code হলো এমন code যা পরবর্তী code-গুলোর interpretation পরিবর্তন করে।

```text
Shift Code
    ↓
Context Change
    ↓
Following Codes
    ↓
New Interpretation
```

---

## Q16. Number Indicator কী করে?

**Answer:**

Number Indicator-এর পরে আসা code-গুলোকে number হিসেবে interpret করার context তৈরি করে।

Conceptually:

```text
Number Indicator
      ↓
Number Mode
      ↓
Digits
```

---

## Q17. Letter Indicator কী করে?

**Answer:**

Number mode থেকে আবার letter interpretation-এ ফিরে আসার জন্য Letter Indicator ব্যবহৃত হয়।

```text
Number Mode
    ↓
Letter Indicator
    ↓
Letter Mode
```

---

## Q18. Capital Indicator কী?

**Answer:**

Capital Indicator পরবর্তী letter-টি uppercase হিসেবে interpret করার নির্দেশ দেয়।

```text
Capital Indicator
      ↓
Next Letter
      ↓
Uppercase
```

---

## Q19. কেন একটি capital letter-এর জন্য দুইটি code প্রয়োজন হতে পারে?

**Answer:**

একটি code capital letter-এর জন্য indicator হিসেবে কাজ করে এবং পরের code মূল letter represent করে।

অর্থাৎ:

```text
Capital Indicator
+
Letter Code
```

এই দুইটি মিলে একটি uppercase character তৈরি করে।

---

## Q20. Context কীভাবে limited code space-কে আরও কার্যকর করে?

**Answer:**

একটি limited set of codes-কে context পরিবর্তনের মাধ্যমে বিভিন্ন কাজে ব্যবহার করা যায়।

```text
Limited Code Space
       ↓
Indicator
       ↓
Context Change
       ↓
Different Interpretation
```

ফলে একই code space থেকে আরও functionality পাওয়া যায়।

---

# Part 5 — Morse vs Braille

## Q21. Morse Code কী ধরনের code?

**Answer:**

Morse একটি **Variable-Length Code**।

কারণ বিভিন্ন character-এর code-এর length ভিন্ন।

```text
E → .
A → .-
S → ...
O → ---
```

---

## Q22. Morse Code-কে Variable-Length বলা হয় কেন?

**Answer:**

কারণ প্রতিটি character একই সংখ্যক Dot/Dash ব্যবহার করে না।

কিছু character ছোট:

```text
E → .
```

আবার কিছু character বড়:

```text
O → ---
```

---

## Q23. Morse telegraphy-এর জন্য কার্যকর কেন?

**Answer:**

Morse frequently used letters-এর জন্য ছোট code এবং কম ব্যবহৃত letters-এর জন্য তুলনামূলকভাবে বড় code ব্যবহার করে।

ফলে সাধারণ English text transmit করার সময় মোট signal/time কমানো যায়।

---

## Q24. Morse Computer-এর জন্য awkward হতে পারে কেন?

**Answer:**

Morse variable-length হওয়ায় প্রতিটি character কোথায় শেষ হচ্ছে তা determine করার জন্য timing/pause বা অন্য boundary information দরকার হয়।

Computer-এর জন্য fixed-width representation-এর predictable structure বেশি convenient হতে পারে।

---

## Q25. Braille কেন Fixed-Width Code?

**Answer:**

কারণ প্রতিটি Braille character-এর জন্য একই ৬টি dot position থাকে।

Conceptually:

```text
Character 1 → 6 positions
Character 2 → 6 positions
Character 3 → 6 positions
```

---

## Q26. Fixed-Width Code Computer-এর জন্য কেন convenient?

**Answer:**

প্রতিটি character-এর size একই হলে character boundary predictable হয়।

```text
[6 bits][6 bits][6 bits][6 bits]
```

তাই কোন অংশ কোন character-এর তা নির্ধারণ করা সহজ।

---

## Q27. Morse এবং Braille-এর প্রধান structural difference কী?

**Answer:**

```text
Morse
→ Variable-Length

Braille
→ Fixed-Width
→ 6 positions
→ 6 bits conceptually
```

---

# Part 6 — Text and Character Codes

## Q28. Computer-এর কাছে Text কীভাবে ভাবা উচিত?

**Answer:**

Printed page-এর মতো দুই-dimensional layout হিসেবে নয়; বরং letters, numbers, punctuation এবং spaces-এর একটি one-dimensional stream হিসেবে ভাবা যায়।

---

## Q29. Character Code কী?

**Answer:**

একটি নির্দিষ্ট character-কে represent করার জন্য ব্যবহৃত code হলো Character Code।

```text
Character
   ↓
Character Code
   ↓
Binary Representation
```

---

## Q30. Coded Character Set কী?

**Answer:**

একটি system যেখানে text-এর বিভিন্ন character-এর জন্য নির্দিষ্ট code assignment থাকে।

এর মধ্যে letters, numbers এবং punctuation-এর মতো character অন্তর্ভুক্ত থাকে।

---

## Q31. Text String কী?

**Answer:**

একটি text-এর consecutive character codes-এর sequence-কে Text String বলা হয়।

যেমন:

```text
I have 27 sisters.
```

এর প্রতিটি character-এর একটি code থাকবে এবং সেই codes ধারাবাহিকভাবে থাকবে।

---

## Q32. Space-এরও Character Code প্রয়োজন কেন?

**Answer:**

কারণ word separation-ও text-এর information-এর অংশ।

```text
hello world
```

এখানে `hello` এবং `world`-এর মাঝের space না রাখলে text-এর meaning/structure পরিবর্তিত হতে পারে।

---

# Part 7 — Character vs Number

## Q33. Text-এর `"2"` এবং numerical `2` কি একই?

**Answer:**

না।

Text-এর `"2"` একটি character।

অন্যদিকে numerical `2` একটি numerical value।

```text
"2" → Character
2   → Numerical Value
```

---

## Q34. Text-এর `"27"` কেন সরাসরি binary number `11011` ধরে নেওয়া যাবে না?

**Answer:**

কারণ `"27"` text-এর মধ্যে দুটি character:

```text
'2'
'7'
```

এগুলো character code দিয়ে represent হতে পারে।

অন্যদিকে numerical value `27`-এর binary representation আলাদা বিষয়।

---

## Q35. Character Code এবং Numerical Value-এর মধ্যে পার্থক্য কী?

**Answer:**

Character Code কোনো character-এর identity represent করে।

Numerical Value একটি সংখ্যার mathematical value represent করে।

```text
Character:
'7'
   ↓
Character Code

Number:
7
   ↓
Numerical Representation
```

---

# Part 8 — Baudot and Teletypewriter

## Q36. Baudot Code কত-bit?

**Answer:**

Baudot একটি **5-bit code**।

---

## Q37. 5-bit Baudot Code-এ কতটি possible code আছে?

**Answer:**

```text
2⁵ = 32
```

অতএব 32টি possible code।

---

## Q38. Baudot-এর code space কীভাবে ব্যবহার করা হয়েছিল?

**Answer:**

Letters ছাড়াও space, carriage return, line feed এবং shift-related functions-এর জন্য code ব্যবহার করা হয়েছিল।

---

## Q39. Teletypewriter কীভাবে Binary Code ব্যবহার করত?

**Answer:**

Keyboard-এর switches binary code generate করত এবং সেই code output cable-এর মাধ্যমে এক bit করে পাঠানো হতো।

Receiving side-এ code electromagnets-এর মাধ্যমে printing mechanism trigger করতে পারত।

---

## Q40. Shift Code কেন economical?

**Answer:**

একটি limited code space-এর মধ্যে একই code patterns-কে context পরিবর্তনের মাধ্যমে বিভিন্ন meaning-এ ব্যবহার করা যায়।

```text
Limited Codes
    ↓
Shift
    ↓
New Context
    ↓
Same Space → More Functions
```

---

## Q41. Shift Code-এর সমস্যা কী?

**Answer:**

System-এর current state/context গুরুত্বপূর্ণ হয়ে যায়।

যদি system ভুল shift state-এ থাকে, তাহলে পরবর্তী codes ভুলভাবে interpret হতে পারে।

---

# Part 9 — Deep Thinking

## Q42. Braille থেকে Computer সম্পর্কে কী শেখা যায়?

**Answer:**

Braille দেখায় যে information-এর meaning physical form-এর সঙ্গে সরাসরি বাঁধা নয়।

কয়েকটি binary state:

```text
0 / 1
```

এর combination ব্যবহার করে:

```text
64 possible patterns
```

তৈরি করা যায়।

তারপর প্রতিটি pattern-কে একটি meaning assign করা যায়।

এটাই computer-এর code এবং representation বোঝার গুরুত্বপূর্ণ foundation।

---

## Q43. Binary কেন এত powerful?

**Answer:**

একটি মাত্র binary element-এর মাত্র ২টি state থাকলেও অনেকগুলো binary element একসঙ্গে নিলে combinations দ্রুত বৃদ্ধি পায়।

```text
1 bit  → 2 combinations
2 bits → 4
3 bits → 8
4 bits → 16
5 bits → 32
6 bits → 64
8 bits → 256
```

Formula:

```text
2ⁿ
```

---

## Q44. Code design-এ “meaning assignment” কেন গুরুত্বপূর্ণ?

**Answer:**

Binary pattern নিজে স্বাভাবিকভাবে `A`, `B`, `7` বা `.` অর্থ বহন করে না।

একটি system-কে agreement/definition-এর মাধ্যমে ঠিক করতে হয়:

```text
Pattern
   ↓
Meaning
```

এই mapping-ই code system তৈরি করে।

---

## Q45. একই code space-এ বেশি information কীভাবে রাখা যায়?

**Answer:**

Context এবং shift/indicator ব্যবহার করে।

```text
Code
+
Context
=
Interpretation
```

একটি indicator context পরিবর্তন করলে পরবর্তী code-এর meaning-ও পরিবর্তিত হতে পারে।

---

## Q46. Fixed-Width এবং Variable-Length-এর মধ্যে মূল trade-off কী?

**Answer:**

Variable-Length code frequently used symbols-কে ছোট code দিয়ে efficiency বাড়াতে পারে।

Fixed-Width code প্রতিটি character-এর size একই রাখে, ফলে parsing এবং boundary determination সহজ হয়।

অর্থাৎ:

```text
Variable-Length
→ transmission efficiency-এর সুবিধা থাকতে পারে

Fixed-Width
→ predictable structure
→ processing সহজ
```

---

# Part 10 — Computer Science Connection

## Q47. Character Encoding কেন প্রয়োজন?

**Answer:**

Computer সরাসরি human-readable character store না করে binary data store করে।

তাই:

```text
Human Character
      ↓
Encoding
      ↓
Binary Code
      ↓
Storage / Processing / Transmission
```

এই mapping-এর প্রয়োজন হয়।

---

## Q48. Text-এর জন্য শুধু letters-এর code থাকলেই হবে?

**Answer:**

না।

Text-এর জন্য প্রয়োজন হতে পারে:

```text
Uppercase letters
Lowercase letters
Digits
Punctuation
Space
Control characters
```

তাই একটি practical character encoding system-কে বিভিন্ন ধরনের character represent করতে হয়।

---

## Q49. Braille-এর Fixed-Width nature কেন গুরুত্বপূর্ণ?

**Answer:**

কারণ প্রতিটি character একই সংখ্যক position ব্যবহার করে।

এটি Computer-এর জন্য character boundary এবং data processing-এর ধারণা সহজ করে।

---

## Q50. Chapter 3-এর সবচেয়ে গুরুত্বপূর্ণ conceptual transition কী?

**Answer:**

সবচেয়ে গুরুত্বপূর্ণ transition হলো:

```text
Braille
  ↓
Binary States
  ↓
Combinations
  ↓
Codes
  ↓
Character Codes
  ↓
Text String
  ↓
Computer Representation
```

---

# Part 11 — Final Challenge Questions

## Q51. যদি একটি code system-এ 7টি binary position থাকে, কতটি possible code তৈরি হতে পারে?

**Answer:**

```text
2⁷ = 128
```

অতএব 128টি possible combination।

---

## Q52. 8-bit code-এ কতটি possible combination থাকে?

**Answer:**

```text
2⁸ = 256
```

অতএব 256টি possible combination।

---

## Q53. যদি প্রতিটি character 6 bits ব্যবহার করে, তাহলে 10টি character-এর জন্য কত bits লাগবে?

**Answer:**

```text
6 × 10 = 60 bits
```

---

## Q54. একটি 6-bit code space-এর সব 64টি pattern যদি ব্যবহার করতে হয়, তাহলে কি সবগুলোই letters হতে হবে?

**Answer:**

না।

কিছু letters, কিছু numbers, কিছু punctuation, কিছু spaces এবং কিছু control/shift function-এর জন্য ব্যবহার করা যেতে পারে।

---

## Q55. একটি Character Code-এর অর্থ কি সবসময় তার binary numerical value-এর সমান?

**Answer:**

না।

Character Code-এর binary pattern একটি character-এর identity represent করতে পারে। সেই pattern-এর numerical value এবং character-এর semantic/numerical meaning একই হওয়া বাধ্যতামূলক নয়।

---

# Part 12 — Final Revision

## Q56. Braille-এর একটি cell-এ কয়টি binary element আছে?

**Answer:**

৬টি।

---

## Q57. ৬টি binary element থেকে কতটি combination?

**Answer:**

```text
2⁶ = 64
```

---

## Q58. Morse কী ধরনের code?

**Answer:**

Variable-Length Code।

---

## Q59. Braille কী ধরনের code?

**Answer:**

Fixed-Width Code।

---

## Q60. Number Indicator-এর উদ্দেশ্য কী?

**Answer:**

পরবর্তী code-গুলোকে number হিসেবে interpret করার context তৈরি করা।

---

## Q61. Capital Indicator-এর উদ্দেশ্য কী?

**Answer:**

পরবর্তী character-টি uppercase হিসেবে interpret করার নির্দেশ দেওয়া।

---

## Q62. Character Code কী?

**Answer:**

একটি character-কে represent করার জন্য নির্ধারিত code।

---

## Q63. Text String কী?

**Answer:**

Consecutive character codes-এর একটি sequence।

---

## Q64. Baudot কত-bit code?

**Answer:**

5-bit।

---

## Q65. 5-bit code-এ কতটি possible code?

**Answer:**

```text
2⁵ = 32
```

---

# One-Minute Master Revision

```text
Braille
  ↓
6 Dots
  ↓
Raised / Flat
  ↓
Binary
  ↓
2⁶ = 64
  ↓
Code Space
  ↓
Letters / Numbers / Punctuation
  ↓
Indicator / Shift Codes
  ↓
Character Codes
  ↓
Text String
  ↓
Computer Text Representation
```

### সবচেয়ে গুরুত্বপূর্ণ 10টি কথা

1. Braille একটি code system।
2. Braille cell-এ ৬টি dot position থাকে।
3. প্রতিটি dot Raised বা Flat হতে পারে।
4. তাই ৬টি dot-কে Binary elements হিসেবে দেখা যায়।
5. `2⁶ = 64` possible combinations।
6. Limited code space-এ বিভিন্ন ধরনের information represent করা যায়।
7. Indicator/Shift code context পরিবর্তন করতে পারে।
8. Morse Variable-Length; Braille Fixed-Width।
9. Text হলো character-এর একটি stream, এবং প্রতিটি character-এর জন্য Character Code প্রয়োজন।
10. Binary → Code → Character → Text—এই representation chain-ই Chapter 3-এর মূল শিক্ষা।
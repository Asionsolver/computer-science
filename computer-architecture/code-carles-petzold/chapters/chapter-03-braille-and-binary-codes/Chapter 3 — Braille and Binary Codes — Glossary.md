# Chapter 3 — Braille and Binary Codes

## A

### ASCII
**American Standard Code for Information Interchange**। Computer text-এর জন্য ব্যবহৃত একটি character encoding standard। Chapter-এর পরবর্তী অংশে 7-bit ASCII নিয়ে আলোচনা করা হয়।

### Alphanumeric
Letters এবং numbers-এর সমন্বিত ধারণা।

---

## B

### Baudot Code
একটি 5-bit telegraph code, যা পরে ITA-2-এর সঙ্গে সম্পর্কিত standard হিসেবে ব্যবহৃত হয়।

```text
5 bits
  ↓
2⁵ = 32 possible codes
```

### Binary
যে representation system-এ দুটি possible state/value থাকে।

```text
0 / 1
```

### Binary Element
এমন একটি element যার দুটি possible state থাকে।

Braille-এর ক্ষেত্রে:

```text
Raised / Flat
```

---

## C

### Character
Text-এর একটি individual unit।

উদাহরণ:

```text
A
7
?
space
```

প্রতিটিই একটি character হতে পারে।

### Character Code
একটি character-কে represent করার জন্য নির্ধারিত code।

```text
Character
    ↓
Character Code
    ↓
Bits
```

### Coded Character Set
Letters, numbers, punctuation এবং অন্যান্য text symbols-এর জন্য character এবং code-এর একটি defined mapping।

### Code
Information represent বা transfer করার একটি system।

### Code Space
একটি code system-এ possible code combinations-এর মোট set।

৬টি binary position হলে:

```text
2⁶ = 64
```

---

## F

### Fixed-Width Code
যেখানে প্রতিটি character একই সংখ্যক bits/positions ব্যবহার করে।

Braille:

```text
1 character → 6 bits
```

### Figure Shift
Baudot/ITA-2-এর একটি shift mechanism, যা subsequent codes-কে figure/number context-এ interpret করতে সাহায্য করে।

---

## I

### Indicator Code
এমন code যা নিজে সরাসরি মূল data represent না করে পরবর্তী code কীভাবে interpret হবে তা নির্দেশ করতে পারে।

### Interpretation
একটি code-এর অর্থ নির্ধারণ বা বোঝার প্রক্রিয়া।

---

## L

### Letter Indicator
Number context থেকে letter context-এ ফিরে আসার জন্য ব্যবহৃত indicator concept।

### Letter Shift
Baudot-এর context পরিবর্তনকারী shift code, যা figure/number interpretation থেকে letter interpretation-এ ফিরতে ব্যবহৃত হয়।

---

## M

### Morse Code
Dot এবং Dash-এর combination ব্যবহার করে information represent করার code system।

এটি:

```text
Binary Code
+
Variable-Length Code
```

---

## P

### Punctuation
Text-এর punctuation marks যেমন:

```text
.
,
?
!
```

এগুলোরও character code প্রয়োজন।

---

## R

### Raised Dot
Braille-এর একটি সক্রিয় dot।

Binary interpretation-এ:

```text
Raised → 1
```

### Representation
কোনো information-কে অন্য একটি form বা code-এর মাধ্যমে প্রকাশ করার পদ্ধতি।

---

## S

### Shift Code
এমন code যা পরবর্তী code-গুলোর interpretation পরিবর্তন করে।

```text
Shift Code
    ↓
Context Change
    ↓
Following Codes
    ↓
New Meaning
```

### Space Code
দুটি word-এর মধ্যে ব্যবধান represent করার code।

---

## T

### Text String
Consecutive character codes-এর একটি sequence।

উদাহরণ:

```text
I have 27 sisters.
```

Conceptually:

```text
Character
→ Character Code
→ Character Code
→ Character Code
→ ...
```

এই sequence হলো text string।

### Teletypewriter
এক ধরনের communication/printing machine যেখানে keyboard input binary code হিসেবে transmit করা যায় এবং receiving mechanism সেই code থেকে character print করতে পারে।

---

## V

### Variable-Length Code
যেখানে প্রতিটি character-এর code-এর length একই নয়।

Morse:

```text
E → .
A → .-
S → ...
```

---

## গুরুত্বপূর্ণ Conceptual Terms

### Context
বর্তমান interpretation state, যার ওপর পরবর্তী code-এর meaning নির্ভর করতে পারে।

### Fixed Width বনাম Variable Width

```text
Variable Width
→ code length পরিবর্তিত হয়

Fixed Width
→ code length একই থাকে
```

### Code Reuse
একই code space-এর pattern ভিন্ন context-এ ভিন্ন কাজে ব্যবহার করা।

### Binary Combination
Binary states-এর বিভিন্ন combination।

```text
n binary positions
→ 2ⁿ combinations
```

### Escape Code
একটি special code যা পরবর্তী character-এর interpretation সম্পর্কে অতিরিক্ত নির্দেশনা দেয়।

---

# Most Important Terms to Remember

```text
Braille
Binary
Binary Element
Code Space
Character
Character Code
Coded Character Set
Fixed-Width Code
Variable-Length Code
Indicator Code
Shift Code
Context
Text String
Baudot Code
ASCII
Teletypewriter
```
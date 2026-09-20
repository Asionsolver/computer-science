# Chapter 2 — Codes and Combinations

## Glossary

### 1. Code

**অর্থ:**  
নির্দিষ্ট rules ব্যবহার করে information represent করার system।

**Chapter Context:**  
Morse Code Dot এবং Dash ব্যবহার করে letters ও অন্যান্য characters represent করে।

---

### 2. Combination

**অর্থ:**  
দুই বা তার বেশি elements নির্দিষ্টভাবে একত্রিত করে তৈরি pattern বা arrangement।

**Example:**

```text
.
-
```

থেকে:

```text
..
.-
-.
--
```

তৈরি করা যায়।

---

### 3. Binary

**অর্থ:**  
মাত্র দুইটি possible state বা value নিয়ে গঠিত system।

**Chapter Example:**

```text
Dot / Dash
```

Morse Code একটি Binary Code।

---

### 4. Binary Code

**অর্থ:**  
যে Code system-এ দুই ধরনের basic component বা state থাকে।

**Morse:**

```text
Dot + Dash
```

---

### 5. Dot

Morse Code-এর একটি basic component।

```text
.
```

---

### 6. Dash

Morse Code-এর অন্য basic component।

```text
-
```

---

### 7. Position

একটি Code sequence-এর একটি নির্দিষ্ট স্থান।

যদি:

```text
.-.
```

হয়, তাহলে এখানে 3টি position আছে।

---

### 8. Sequence

কোনো elements-এর নির্দিষ্ট order-এ সাজানো arrangement।

**Example:**

```text
.-.
```

এটি একটি Dot/Dash sequence।

---

### 9. Decoding

একটি Code বা coded sequence থেকে original character বা information বের করার প্রক্রিয়া।

```text
.-.
 ↓
R
```

---

### 10. Encoding

Information বা character-কে একটি Code-এ রূপান্তর করার প্রক্রিয়া।

```text
R
↓
.-.
```

---

### 11. Morse Code

Dot এবং Dash-এর combination ব্যবহার করে information represent করার Code system।

---

### 12. Code Length

একটি Code-এ মোট কতটি Dot/Dash position আছে।

উদাহরণ:

```text
.-
```

এর length:

```text
2
```

---

### 13. Powers of Two

`2`-কে বারবার নিজে দিয়ে গুণ করলে যে সংখ্যাগুলো পাওয়া যায়।

```text
2¹ = 2
2² = 4
2³ = 8
2⁴ = 16
2⁵ = 32
2⁶ = 64
```

---

### 14. Exponent

কোনো number-কে কতবার নিজের সঙ্গে multiply করতে হবে তা প্রকাশ করার mathematical notation।

```text
2⁴
```

এখানে `4` হলো exponent।

---

### 15. Combinatorics

কতভাবে বিভিন্ন elements combine করা যায় তা বিশ্লেষণ করার Mathematics-এর branch।

---

### 16. Combinatorial Analysis

Combinations-এর সংখ্যা এবং structure বিশ্লেষণের mathematical approach।

---

### 17. Unique Code

যে Code শুধুমাত্র একটি নির্দিষ্ট meaning বা character represent করে।

```text
A → .-
B → -...
```

এখানে Codes আলাদা।

---

### 18. Undefined Code

Possible Code combination থাকলেও যার কোনো defined meaning নেই।

---

### 19. Tree

Branch-এর মতো structure যেখানে বিভিন্ন choices ধারাবাহিকভাবে দেখানো হয়।

Morse Code decode করার জন্য Tree ব্যবহার করা যায়।

---

### 20. Branch

Tree-এর একটি পথ বা direction।

Morse Tree-তে প্রতিটি step-এ:

```text
Dot
```

অথবা:

```text
Dash
```

নির্বাচন করা হয়।

---

### 21. Decoding Tree

Morse Code sequence থেকে character খুঁজে বের করার জন্য ব্যবহৃত tree-like structure।

---

### 22. State

কোনো system-এর একটি possible condition বা অবস্থাকে State বলা যায়।

Binary system-এ:

```text
2 possible states
```

থাকে।

---

### 23. Possible State

একটি position বা element কী কী value নিতে পারে তার প্রতিটি সম্ভাবনা।

Morse-এর ক্ষেত্রে:

```text
Dot
Dash
```

---

### 24. Information Representation

Information-কে কোনো নির্দিষ্ট symbol বা Code-এর মাধ্যমে প্রকাশ করার পদ্ধতি।

---

### 25. Code Organization

Codes-কে এমনভাবে সাজানো যাতে তাদের খুঁজে বের করা এবং decode করা সহজ হয়।

Chapter-এ Morse Code-কে length অনুযায়ী group করার মাধ্যমে এটি দেখানো হয়েছে।

---

## Important Formula

```text
Number of Codes = 2ⁿ
```

যেখানে:

```text
n = Number of positions
```

---

## Quick Reference

| Term | Meaning |
|---|---|
| Code | Information represent করার system |
| Combination | Elements-এর arrangement |
| Binary | দুইটি possible state |
| Dot | Morse-এর একটি component |
| Dash | Morse-এর একটি component |
| Sequence | নির্দিষ্ট order-এর pattern |
| Position | Sequence-এর একটি স্থান |
| Encoding | Information → Code |
| Decoding | Code → Information |
| Powers of Two | 2¹, 2², 2³... |
| Combinatorics | Combination বিশ্লেষণের Mathematics |
| Unique Code | একটি নির্দিষ্ট meaning-এর Code |
| Undefined Code | Meaning assign করা হয়নি এমন Code |
| Tree | Branch-based structure |
| State | একটি possible condition |

---

# Core Terms to Memorize

```text
Code
Combination
Binary
Dot
Dash
Position
Sequence
Encoding
Decoding
Powers of Two
Combinatorics
Unique Code
Undefined Code
Tree
State
```
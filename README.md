# Computer Architecture

My personal study notes while learning Computer Architecture as a Software Engineer.

## 📚 Book

**Code: The Hidden Language of Computer Hardware and Software**

Author: Charles Petzold

এই repository-তে থাকা PDF-এর ২৫টি chapter অনুসরণ করে পড়ার পরিকল্পনা সাজানো হয়েছে।

- [বইয়ের PDF](computer-architecture/code-charles-petzold.pdf)
- [Chapter-by-chapter study plan](computer-architecture/timeline.md) — প্রতিটি chapter-এর বিষয়বস্তু, অনুশীলন, লক্ষ্য ও আনুমানিক সময়।

এই বইটার সবচেয়ে বড় সুবিধা হলো—এটা ধরে নেয় না যে তুমি আগে থেকেই Computer Architecture জানো।

এখান থেকে তুমি বুঝবে:

- Binary
- Bits / Bytes
- Boolean logic
- Logic Gates
- Transistors-এর basic idea
- Circuits
- Memory
- CPU
- Machine instructions
- Assembly-এর basic
- Computer কীভাবে instruction execute করে
- Character encoding (ASCII ও Unicode)
- Bus, Input/Output ও Operating System
- Fixed-point ও floating-point number
- Programming languages ও graphical interface

সবচেয়ে গুরুত্বপূর্ণ হলো, লেখক খুব ধীরে ধীরে concept build করেন।

উদাহরণস্বরূপ:

```text
Codes ও Communication
    ↓
Electricity ও Switches
    ↓
Number Systems ও Bits
    ↓
Boolean Logic ও Logic Gates
    ↓
Binary Arithmetic
    ↓
Flip-Flops ও Memory
    ↓
Automation ও CPU
    ↓
Microprocessors, Encoding ও I/O
    ↓
Operating System
    ↓
Number Representation, Languages ও GUI
```

অর্থাৎ তুমি শুধু **"CPU কী?"** পড়বে না।

তুমি বুঝতে শুরু করবে:

> এতগুলো ছোট ছোট electronic component কীভাবে একসাথে একটা computer তৈরি করে?

### কেন তোমার জন্য ভালো?

তুমি Software Engineer হিসেবে architecture শিখতে চাচ্ছ। তাই শুরুতেই transistor-level mathematics বা complicated architecture-এ যাওয়ার দরকার নেই।

**Code তোমাকে intuition তৈরি করে দেবে।**

---

## 🎯 Goal

Understand how software ultimately interacts with computer hardware.

---

## 📑 Chapters

সংযুক্ত বইয়ের chapter-এর নাম ও ক্রম:

| Chapter | Title                          |
| ------- | ------------------------------ |
| 1       | Best Friends                   |
| 2       | Codes and Combinations         |
| 3       | Braille and Binary Codes       |
| 4       | Anatomy of a Flashlight        |
| 5       | Seeing Around Corners          |
| 6       | Telegraphs and Relays          |
| 7       | Our Ten Digits                 |
| 8       | Alternatives to Ten            |
| 9       | Bit by Bit by Bit              |
| 10      | Logic and Switches             |
| 11      | Gates (Not Bill)               |
| 12      | A Binary Adding Machine        |
| 13      | But What About Subtraction?    |
| 14      | Feedback and Flip-Flops        |
| 15      | Bytes and Hex                  |
| 16      | An Assemblage of Memory        |
| 17      | Automation                     |
| 18      | From Abaci to Chips            |
| 19      | Two Classic Microprocessors    |
| 20      | ASCII and a Cast of Characters |
| 21      | Get on the Bus                 |
| 22      | The Operating System           |
| 23      | Fixed Point, Floating Point    |
| 24      | Languages High and Low         |
| 25      | The Graphical Revolution       |

পড়ার সময় প্রতিটি chapter-এর অনুশীলনের জন্য [study plan](computer-architecture/timeline.md) অনুসরণ করো।

---

## 📖 Progress

**Completed: 5 / 25 chapters (20%)**

Chapter 1–5 পড়া শেষ। পরবর্তী chapter: **6 — Telegraphs and Relays**।

| Chapter | Title                          | Status |
| ------- | ------------------------------ | ------ |
| 1       | Best Friends                   | ✅     |
| 2       | Codes and Combinations         | ✅     |
| 3       | Braille and Binary Codes       | ✅     |
| 4       | Anatomy of a Flashlight        | ✅     |
| 5       | Seeing Around Corners          | ✅     |
| 6       | Telegraphs and Relays          | 🔄     |
| 7       | Our Ten Digits                 | ⬜     |
| 8       | Alternatives to Ten            | ⬜     |
| 9       | Bit by Bit by Bit              | ⬜     |
| 10      | Logic and Switches             | ⬜     |
| 11      | Gates (Not Bill)               | ⬜     |
| 12      | A Binary Adding Machine        | ⬜     |
| 13      | But What About Subtraction?    | ⬜     |
| 14      | Feedback and Flip-Flops        | ⬜     |
| 15      | Bytes and Hex                  | ⬜     |
| 16      | An Assemblage of Memory        | ⬜     |
| 17      | Automation                     | ⬜     |
| 18      | From Abaci to Chips            | ⬜     |
| 19      | Two Classic Microprocessors    | ⬜     |
| 20      | ASCII and a Cast of Characters | ⬜     |
| 21      | Get on the Bus                 | ⬜     |
| 22      | The Operating System           | ⬜     |
| 23      | Fixed Point, Floating Point    | ⬜     |
| 24      | Languages High and Low         | ⬜     |
| 25      | The Graphical Revolution       | ⬜     |

Legend:

- ⬜ Not started
- 🔄 Learning
- ✅ Completed
- 🔁 Needs revision

---

## 🧠 Learning Philosophy

I am not trying to memorize Computer Architecture concepts.

My goal is to understand:

```text
What?
Why?
How?
Where is it used?
How does it connect to software?
```

---

## 📂 Structure

```text
computer-science/
├── README.md
└── computer-architecture/
    ├── code-charles-petzold.pdf
    ├── timeline.md
    ├── connections_chat.md
    ├── connections_goo.md
    └── code-carles-petzold/
```

- [timeline.md](computer-architecture/timeline.md): ২৫টি chapter-এর বিস্তারিত study plan।
- [connections_chat.md](computer-architecture/connections_chat.md) ও [connections_goo.md](computer-architecture/connections_goo.md): ধারণাগুলোর সংযোগ নিয়ে রাখা নোট।

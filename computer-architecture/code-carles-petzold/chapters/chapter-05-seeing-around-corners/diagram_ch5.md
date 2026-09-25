# অধ্যায় ৫: Seeing Around Corners — ছবি দেখে circuit বোঝো

**তোমার ঘরে switch চাপলে বন্ধুর ঘরের bulb জ্বলে। ফিরতি বার্তার জন্য একই ব্যবস্থা উল্টো দিকে বসাতে হয়।**

ছবিগুলো **Markdown Preview**-তে দেখো, অথবা `diagrams/`-এর SVG সরাসরি খোলো। Mermaid প্রয়োজন নেই।

### ছবি পড়ার নিয়ম

- **A = তোমার ঘর; B = বন্ধুর ঘর।** Key A চালায় Bulb B; Key B চালায় Bulb A।
- **নীল = A থেকে পাঠানো circuit; কমলা = B থেকে পাঠানো circuit; সবুজ = shared return / earth।**
- বৃত্তের মধ্যে ক্রস = bulb; হলুদ bulb = ON, ধূসর bulb = OFF।
- Switch-এর দুই বিন্দু জোড়া = closed; মাঝে ফাঁক = open। **Closed হলে current চলতে পারে।**
- Arrow বাইরের circuit-এ conventional current-এর দিক দেখায়: battery `+` থেকে `−`। বইয়ে electron-এর চলার দিক দেখালে সেটি উল্টো হবে।

## ডায়াগ্রাম ১: একমুখী থেকে দ্বিমুখী যোগাযোগ

### ক. একমুখী: একটি loop, দুটি লম্বা তার

![একমুখী circuit-এর ON ও OFF অবস্থা](diagrams/01a-one-way.svg)

**ওপরে:** Battery A (+) → Key A → যাওয়ার তার → Bulb B → ফেরার তার → Battery A (−)।

**নিচে:** Key A খোলা। পথ ভাঙা বলে Bulb B জ্বলে না।

দুটি তারে একটি সম্পূর্ণ loop তৈরি হয়; একটি wire দিয়ে শুধু দূরের bulb-এ পৌঁছালেই যথেষ্ট নয়।

### খ. দ্বিমুখী: দুটি আলাদা loop, চারটি লম্বা তার

![দুটি independent circuit দিয়ে দুই দিকে যোগাযোগ](diagrams/01b-two-way.svg)

**নীল loop:** তুমি key চাপো → বন্ধুর bulb জ্বলে। **কমলা loop:** বন্ধু key চাপে → তোমার bulb জ্বলে।

প্রতিটি loop-এর নিজস্ব battery, key, bulb এবং দুটি লম্বা wire আছে। তাই **২ + ২ = ৪টি wire**। ছবিতে দুটো key-ই বন্ধ, তাই দুটো bulb-ই জ্বলছে। ওপর-নিচে আঁকা হয়েছে আলাদা loop বোঝাতে; ঘর দুটি একই A ও B।

## ডায়াগ্রাম ২: Common wire — চারটির জায়গায় তিনটি তার

![দুটি circuit-এর shared common wire](diagrams/02-common-wire.svg)

**মূল পরিবর্তন: দুটি return wire-এর বদলে একটি সবুজ common wire।** সবুজ বিন্দুতে electrical সংযোগ আছে। দুই battery-এর negative terminal এই common-এ যুক্ত।

ছবিতে শুধু Key A বন্ধ। নীল পথ ধরে Bulb B-তে যাও, তারপর সবুজ common ধরে বাঁয়ে ফিরে Battery A (−)-এ পৌঁছাও। Key B খোলা বলে নিচের branch-এ current নেই; Bulb A নিভে থাকে।

| Key A | Key B | কোন bulb জ্বলে? |
| --- | --- | --- |
| খোলা | খোলা | কোনোটিই নয় |
| বন্ধ | খোলা | বন্ধুর Bulb B |
| খোলা | বন্ধ | তোমার Bulb A |
| বন্ধ | বন্ধ | দুটোই |

**দুটি key একসঙ্গে বন্ধ হলে:** বইয়ের সমান battery ও bulb-এর balanced উদাহরণে common wire-এর net current শূন্য হয়। তখন বাইরের বড় loop দিয়েই current চলতে পারে। কিন্তু একটি key খোলা থাকলে অন্য loop সম্পূর্ণ করার জন্য common দরকার। বাস্তবে দুই দিক অসমান হলে common-এ net current থাকতে পারে।

## ডায়াগ্রাম ৩: Earth return — ফেরার তারের কাজ করে মাটি

### ক. একমুখী: দুটি লম্বা তারের বদলে একটি

![একমুখী earth-return circuit](diagrams/03a-earth-one-way.svg)

Battery (+) → key → লম্বা তার → bulb → earth → Battery (−)। সবুজ অংশ circuit-এর return path; সেখানে current অদৃশ্য হয়ে যায় না। ছবির earth-এর arrow পথের ধারণা বোঝায়—মাটির ভেতরে একটি সরু নির্দিষ্ট wire নেই।

### খ. দ্বিমুখী: তিনটি লম্বা তারের বদলে দুটি

![দ্বিমুখী earth-return circuit](diagrams/03b-earth-two-way.svg)

এটি diagram ২-এর মতোই: **সবুজ common wire-এর জায়গায় earth**। দুই দিকে signal পাঠানোর নীল ও কমলা wire থাকে। তাই দ্বিমুখী যোগাযোগে দুই ঘরের মাঝে **২টি লম্বা wire** লাগে।

Earth-এর resistance আছে। বইয়ের সাধারণ 1.5 V cell ও flashlight bulb-এর ক্ষেত্রে মাটিকে wire-এর সরাসরি কার্যকর বিকল্প ধরে নেওয়া যায় না। এখানে circuit-এর ধারণা দেখানো হয়েছে।

**বইয়ে `V` ও ground দেখলে:** `V`-এর জায়গায় battery (+) কল্পনা করো, আর তার negative terminal earth-এ যুক্ত ভাবো। Battery ছবিতে বাদ গেলেও circuit থেকে বাদ যায়নি।

## ডায়াগ্রাম ৪: তার লম্বা হলে current কমে কেন?

![একই battery-তে ছোট ও লম্বা তারের current তুলনা](diagrams/04-resistance.svg)

**একই ধরনের তার লম্বা করো → wire resistance বাড়ে → মোট resistance বাড়ে → current কমে → bulb ম্লান হয়।**

ছবির হিসাব বইয়ের সরল model অনুসারে: battery **3 V**, bulb **4 Ω**, 20 AWG wire প্রায় **10 Ω / 1000 ft**।

| দুই ঘরের দূরত্ব | যাওয়া + ফেরার wire | Wire resistance | মোট resistance | Current: I = V / R |
| --- | --- | --- | --- | --- |
| 50 ft | 100 ft | প্রায় 1 Ω | প্রায় 5 Ω | 0.60 A |
| 1 mile = 5280 ft | 10,560 ft | প্রায় 105.6 Ω | প্রায় 109.6 Ω | প্রায় 0.027 A |

ছবির bar current-এর তুলনা দেখায়, bulb-এর brightness-এর সরাসরি মাপ নয়। বাস্তবে filament-এর resistance তাপমাত্রার সঙ্গে বদলায়, তাই এই হিসাব আনুমানিক।

একটি series loop-এর তার বেয়ে যেতে যেতে current খরচ হয়ে কমে না। **দীর্ঘ wire-সহ নতুন loop-এর মোট resistance বেশি বলে পুরো loop-এর current কম।**

## ডায়াগ্রাম ৫: একনজরে তারের সংখ্যা

![একমুখী ও দ্বিমুখী ব্যবস্থায় দীর্ঘ তারের সংখ্যা](diagrams/05-wire-count.svg)

| যোগাযোগ | ব্যবস্থা | দুই ঘরের মাঝের লম্বা তার |
| --- | --- | --- |
| একমুখী | আলাদা return wire | ২টি |
| একমুখী | Earth return | ১টি |
| দ্বিমুখী | দুটি independent loop | ৪টি |
| দ্বিমুখী | Shared common wire | ৩টি |
| দ্বিমুখী | Earth return | ২টি |

**একই দ্বিমুখী কাজ তুলনা করলে:** ৪ → ৩-এ দীর্ঘ wire-এর মোট দৈর্ঘ্য ২৫% কম; ৪ → ২-এ ৫০% কম, যদি প্রতিটি wire একই দূরত্ব অতিক্রম করে। এগুলো পুরো ব্যবস্থার মোট খরচ কমার নির্দিষ্ট হার নয়। একমুখী ব্যবস্থার ১টি wire-কে দ্বিমুখীর ৪টির সঙ্গে তুলনা করলে যোগাযোগের ক্ষমতাও বদলে যায়।

## নিজের বোঝা যাচাই করো

1. তোমার Key A চাপলে কোন bulb জ্বলে? — **বন্ধুর Bulb B।**
2. Return path কেন দরকার? — **Battery-সহ সম্পূর্ণ current loop তৈরি করতে।**
3. Common wire কী বাঁচায়? — **দুটি return-এর জায়গায় একটি shared connection দেয়।**
4. Earth ব্যবহার করলে loop কি থাকে? — **হ্যাঁ, earth return path-এর অংশ হয়।**

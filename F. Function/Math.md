# 🚀 **JavaScript Math: Full Guide with Examples**  

JavaScript-এর **Math Object** ব্যবহার করে **সংখ্যার গণনা, রাউন্ডিং, র্যান্ডম সংখ্যা তৈরি, এবং ম্যাথমেটিক্যাল অপারেশন** করা যায়। এটি একটি **built-in object**, তাই আমরা এটি **direct ব্যবহার** করতে পারি।  

---

## **📌 ১. Math Properties (গণিত বিষয়ক কনস্ট্যান্টস)**  
JavaScript-এ কিছু **Math Properties** আছে, যা বিভিন্ন কনস্ট্যান্ট মান ধারণ করে:  

| Property         | Value                  | Description                          |
|-----------------|------------------------|--------------------------------------|
| `Math.PI`       | `3.141592653589793`     | π (Pi)                              |
| `Math.E`        | `2.718281828459045`     | Euler’s number                      |
| `Math.SQRT2`    | `1.4142135623730951`    | √2 (Square root of 2)               |
| `Math.SQRT1_2`  | `0.7071067811865476`    | √(1/2)                              |
| `Math.LN2`      | `0.6931471805599453`    | Natural log of 2                    |
| `Math.LN10`     | `2.302585092994046`     | Natural log of 10                   |

🔹 **Example:**
```js
console.log(Math.PI); // 3.141592653589793
console.log(Math.E);  // 2.718281828459045
```

---

## **📌 ২. Number Rounding Methods (সংখ্যা রাউন্ড করা)**  
| Method         | Description                            | Example (`x = 4.7`) |
|--------------|--------------------------------|----------------|
| `Math.round(x)` | কাছের পূর্ণসংখ্যায় রাউন্ড করে | `5` |
| `Math.floor(x)` | নিচের দিকে রাউন্ড করে | `4` |
| `Math.ceil(x)` | উপরের দিকে রাউন্ড করে | `5` |
| `Math.trunc(x)` | দশমিক বাদ দিয়ে শুধু পূর্ণসংখ্যা নেয় | `4` |

🔹 **Example:**
```js
console.log(Math.round(4.7));  // 5
console.log(Math.floor(4.7));  // 4
console.log(Math.ceil(4.1));   // 5
console.log(Math.trunc(4.9));  // 4
```

---

## **📌 ৩. Power, Square Root & Logarithm**  
| Method              | Description                        | Example |
|--------------------|--------------------------------|---------|
| `Math.pow(x, y)`   | `x` এর `y` ঘাত (power) নির্ণয় করে | `Math.pow(2, 3) → 8` |
| `Math.sqrt(x)`     | `x`-এর বর্গমূল (square root) বের করে | `Math.sqrt(25) → 5` |
| `Math.cbrt(x)`     | `x`-এর ঘনমূল (cube root) বের করে | `Math.cbrt(27) → 3` |
| `Math.log(x)`      | `x`-এর প্রাকৃতিক লগারিদম (ln x) | `Math.log(10) → 2.30` |
| `Math.log10(x)`    | `x`-এর base 10 লগারিদম | `Math.log10(100) → 2` |

🔹 **Example:**
```js
console.log(Math.pow(2, 3));  // 8
console.log(Math.sqrt(25));   // 5
console.log(Math.cbrt(27));   // 3
console.log(Math.log10(100)); // 2
```

---

## **📌 ৪. Min, Max & Random Numbers**  
| Method          | Description                          | Example |
|----------------|----------------------------------|---------|
| `Math.min(a, b, c, ...)` | ছোটতম সংখ্যা বের করে | `Math.min(5, 3, 9) → 3` |
| `Math.max(a, b, c, ...)` | বড়তম সংখ্যা বের করে | `Math.max(5, 3, 9) → 9` |
| `Math.random()` | ০ থেকে ১-এর মধ্যে র্যান্ডম সংখ্যা তৈরি করে | `Math.random() → 0.458` |

🔹 **Example:**
```js
console.log(Math.min(5, 3, 9));  // 3
console.log(Math.max(5, 3, 9));  // 9
console.log(Math.random());      // 0.125374 (random)
```

🔹 **Random সংখ্যা 1 থেকে 100 এর মধ্যে আনতে:**
```js
console.log(Math.floor(Math.random() * 100) + 1);
```

---

## **📌 ৫. Trigonometric Methods (ত্রিকোণমিতি ফাংশন)**  
| Method         | Description                        | Example |
|--------------|--------------------------------|---------|
| `Math.sin(x)` | `x` রেডিয়ান এর sine মান নির্ণয় করে | `Math.sin(0) → 0` |
| `Math.cos(x)` | `x` রেডিয়ান এর cosine মান নির্ণয় করে | `Math.cos(0) → 1` |
| `Math.tan(x)` | `x` রেডিয়ান এর tangent মান নির্ণয় করে | `Math.tan(0) → 0` |
| `Math.asin(x)` | `x`-এর sine এর বিপরীত মান দেয় (radians) | `Math.asin(1) → 1.57` |

🔹 **Example:**
```js
console.log(Math.sin(0));  // 0
console.log(Math.cos(0));  // 1
console.log(Math.tan(0));  // 0
console.log(Math.asin(1)); // 1.5707963267948966 (π/2 radians)
```

---

## **📌 ৬. Absolute & Sign Methods**  
| Method         | Description                            | Example |
|--------------|--------------------------------|---------|
| `Math.abs(x)` | `x`-এর Absolute (ধনাত্মক) মান দেয় | `Math.abs(-10) → 10` |
| `Math.sign(x)` | সংখ্যা ধনাত্মক (+1), ঋণাত্মক (-1) বা 0 তা বলে | `Math.sign(-5) → -1` |

🔹 **Example:**
```js
console.log(Math.abs(-10));  // 10
console.log(Math.sign(-5));  // -1
console.log(Math.sign(5));   // 1
console.log(Math.sign(0));   // 0
```

---

## **📌 ৭. Exponential & Logarithmic Methods**  
| Method         | Description                            | Example |
|--------------|--------------------------------|---------|
| `Math.exp(x)` | `e^x` (Euler’s Number এর power x) | `Math.exp(2) → 7.389` |
| `Math.log(x)` | `x` এর প্রাকৃতিক লগারিদম (ln x) | `Math.log(10) → 2.30` |
| `Math.log2(x)` | `x`-এর base 2 লগারিদম | `Math.log2(8) → 3` |

🔹 **Example:**
```js
console.log(Math.exp(2));   // 7.389
console.log(Math.log(10));  // 2.302
console.log(Math.log2(8));  // 3
```

---

## **🔥 উপসংহার**  
✅ JavaScript-এর `Math` object ব্যবহার করে বিভিন্ন **গাণিতিক অপারেশন** করা যায়।  
✅ **`Math.random()`** ব্যবহার করে **random সংখ্যা তৈরি** করা সম্ভব।  
✅ **`Math.round()`, `Math.floor()`, `Math.ceil()`** সংখ্যা রাউন্ডিং করতে ব্যবহৃত হয়।  
✅ **Exponential, Logarithmic, Trigonometric** ফাংশনগুলো গণিত-সংক্রান্ত কাজে ব্যবহৃত হয়।  

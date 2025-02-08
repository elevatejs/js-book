### **📌 জাভাস্ক্রিপ্টে কন্ডিশন (Condition) সম্পর্কে সম্পূর্ণ গাইড**  

কন্ডিশন বা শর্ত হলো এমন কিছু সিকোয়েন্স যা নির্দিষ্ট শর্তের ভিত্তিতে কোড চালাতে সাহায্য করে। জাভাস্ক্রিপ্টে কন্ডিশনাল স্টেটমেন্টের মাধ্যমে শর্ত পূরণ হলে কিছু কাজ করা যায়। এটি প্রোগ্রামিংয়ের অন্যতম গুরুত্বপূর্ণ অংশ, যেটি কোডের কার্যক্রমের ধারা নিয়ন্ত্রণ করে।  

---

## **🔹 কন্ডিশনাল স্টেটমেন্টের প্রকারভেদ**  
✅ **if statement**  
✅ **if-else statement**  
✅ **else-if statement**  
✅ **switch statement**  

---

## **🔹 ১. if statement**  
`if` স্টেটমেন্ট শর্তের ভিত্তিতে কোডের কোনো অংশ চালায়। যদি শর্ত `true` হয়, তাহলে কোডটি execute হবে।  

**Syntax:**
```javascript
if (condition) {
  // Code to be executed if the condition is true
}
```

**উদাহরণ:**
```javascript
let age = 20;
if (age >= 18) {
    console.log("You are an adult.");
}
```
**Output:**
```
You are an adult.
```

এখানে, যদি `age` ১৮ বা তার বেশি হয়, তাহলে `"You are an adult."` মেসেজটি কনসোল-এ দেখাবে।  

---

## **🔹 ২. if-else statement**  
`if-else` স্টেটমেন্টে, শর্ত যদি `true` হয়, তাহলে প্রথম ব্লক execute হবে। কিন্তু শর্ত `false` হলে `else` ব্লক execute হবে।  

**Syntax:**
```javascript
if (condition) {
  // Code to be executed if the condition is true
} else {
  // Code to be executed if the condition is false
}
```

**উদাহরণ:**
```javascript
let age = 15;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```
**Output:**
```
You are a minor.
```

এখানে, যদি `age` ১৮ বা তার বেশি না হয়, তাহলে `"You are a minor."` মেসেজটি কনসোল-এ দেখাবে।  

---

## **🔹 ৩. else-if statement**  
`else-if` স্টেটমেন্ট ব্যবহার করে একাধিক শর্ত চেক করা যায়। এটি `if` এবং `else` এর মধ্যে অবস্থান নেয়, এবং একাধিক শর্তে কার্যকর হতে পারে।  

**Syntax:**
```javascript
if (condition1) {
  // Code to be executed if condition1 is true
} else if (condition2) {
  // Code to be executed if condition2 is true
} else {
  // Code to be executed if neither condition is true
}
```

**উদাহরণ:**
```javascript
let age = 20;
if (age >= 60) {
    console.log("You are a senior citizen.");
} else if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```
**Output:**
```
You are an adult.
```

এখানে প্রথমে `age >= 60` শর্তটি পরীক্ষা করা হয়, যদি না হয় তবে `age >= 18` পরীক্ষা হবে এবং তার পরে `else` অংশ execute হবে।  

---

## **🔹 ৪. switch statement**  
`switch` স্টেটমেন্টটি একাধিক শর্ত চেক করার জন্য ব্যবহৃত হয়। এটি অনেক `if-else` স্টেটমেন্টের চেয়ে সহজ এবং স্পষ্ট।  

**Syntax:**
```javascript
switch (expression) {
  case value1:
    // Code to be executed if the expression equals value1
    break;
  case value2:
    // Code to be executed if the expression equals value2
    break;
  default:
    // Code to be executed if the expression doesn't match any case
}
```

**উদাহরণ:**
```javascript
let day = 3;
switch (day) {
  case 1:
    console.log("Sunday");
    break;
  case 2:
    console.log("Monday");
    break;
  case 3:
    console.log("Tuesday");
    break;
  case 4:
    console.log("Wednesday");
    break;
  default:
    console.log("Invalid day");
}
```
**Output:**
```
Tuesday
```

এখানে, `day` এর মান ৩ হওয়ায় `"Tuesday"` মেসেজটি কনসোল-এ দেখাবে।  

---

## **🔹 ৫. তোলনামূলক অপারেটর (Comparison Operators)**  
কন্ডিশনাল স্টেটমেন্টে শর্ত নির্ধারণ করতে **তুলনামূলক অপারেটর** ব্যবহৃত হয়। যেমন `==`, `===`, `!=`, `>`, `<`, ইত্যাদি।

**উদাহরণ:**
```javascript
let x = 10;
let y = 20;
if (x < y) {
    console.log("x is smaller than y");
}
```
**Output:**
```
x is smaller than y
```

---

## **🔹 ৬. লজিক্যাল অপারেটর (Logical Operators)**  
কন্ডিশনে একাধিক শর্ত যুক্ত করার জন্য **লজিক্যাল অপারেটর** যেমন `&&` (AND), `||` (OR), `!` (NOT) ব্যবহৃত হয়।

**উদাহরণ:**
```javascript
let age = 20;
let hasPermission = true;
if (age >= 18 && hasPermission) {
    console.log("Access granted.");
} else {
    console.log("Access denied.");
}
```
**Output:**
```
Access granted.
```

এখানে, `age` ১৮ বা তার বেশি এবং `hasPermission` সত্য হলে অ্যাক্সেস গ্রান্ট করা হবে।  

---

## **🔹 ৭. নেস্টেড কন্ডিশন (Nested Conditionals)**  
কখনো কখনো এক কন্ডিশনকে আরেক কন্ডিশনের ভিতরে রাখার প্রয়োজন হয়, তাকে **নেস্টেড কন্ডিশন** বলে।  

**উদাহরণ:**
```javascript
let age = 20;
let hasLicense = true;
if (age >= 18) {
    if (hasLicense) {
        console.log("You can drive.");
    } else {
        console.log("You cannot drive without a license.");
    }
} else {
    console.log("You are too young to drive.");
}
```
**Output:**
```
You can drive.
```

---

## **🔹 উপসংহার**  
জাভাস্ক্রিপ্টে কন্ডিশন ব্যবহার করে শর্ত ভিত্তিক সিদ্ধান্ত নেয়া সম্ভব হয়, যা কোডের কার্যকলাপ নিয়ন্ত্রণ করে। তুমি যদি এই অংশে আরও প্রশ্ন থাকে বা কিছু বুঝতে না পারো, তাহলে আমাকে জানিও! 😊
# 🚀 **JavaScript Function Methods: Full Guide with Examples**  

JavaScript-এ **Function** হল **reusable code blocks** যা নির্দিষ্ট কাজ সম্পন্ন করতে ব্যবহার করা হয়। ফাংশনের মধ্যে **methods** ব্যবহার করে আমরা ফাংশন সম্পর্কে তথ্য পেতে এবং কাস্টমাইজ করতে পারি।  

---

## **📌 ১. Function Methods Overview**  

| Method | Description |
|--------|------------|
| `call()` | অন্য অবজেক্টের সাথে ফাংশন কল করে |
| `apply()` | `call()` এর মতোই, কিন্তু arguments array হিসাবে নেয় |
| `bind()` | ফাংশনের `this` সেট করে এবং নতুন ফাংশন তৈরি করে |
| `toString()` | ফাংশনের সোর্স কোড স্ট্রিং আকারে ফেরত দেয় |
| `length` | ফাংশনের প্যারামিটার সংখ্যা দেখায় |
| `name` | ফাংশনের নাম ফেরত দেয় |

---

## **📌 ২. `call()` Method**  
🔹 **একটি ফাংশনকে অন্য অবজেক্টের সাথে ব্যবহার করা যায়**  

```js
function greet() {
    console.log(`Hello, my name is ${this.name}`);
}

const person = { name: "Shihab" };

greet.call(person);
```
**✅ Output:**  
```
Hello, my name is Shihab
```

✔ **Explanation:** `call()` এর মাধ্যমে `greet` ফাংশনের `this` কে `person` অবজেক্টের সাথে যুক্ত করেছি।

---

## **📌 ৩. `apply()` Method**  
🔹 **`call()` এর মতোই, কিন্তু arguments array হিসাবে নেয়**  

```js
function introduce(age, city) {
    console.log(`My name is ${this.name}, I am ${age} years old from ${city}`);
}

const user = { name: "Shihab" };

introduce.apply(user, [25, "Dhaka"]);
```
**✅ Output:**  
```
My name is Shihab, I am 25 years old from Dhaka
```

✔ **Difference from `call()`** → `apply()` এর ক্ষেত্রে arguments **array আকারে** দেওয়া হয়।

---

## **📌 ৪. `bind()` Method**  
🔹 **একটি ফাংশনের `this` সেট করে নতুন ফাংশন তৈরি করে**  

```js
function sayHi() {
    console.log(`Hi, ${this.name}`);
}

const person = { name: "Shihab" };

const boundFunction = sayHi.bind(person);
boundFunction();
```
**✅ Output:**  
```
Hi, Shihab
```

✔ **Explanation:** `bind()` ফাংশনকে **নতুন ফাংশনে রূপান্তর করে এবং `this` সেট করে**।

---

## **📌 ৫. `toString()` Method**  
🔹 **ফাংশনের সোর্স কোড স্ট্রিং আকারে দেখায়**  

```js
function example() {
    return "Hello World";
}

console.log(example.toString());
```
**✅ Output:**  
```
function example() {
    return "Hello World";
}
```

✔ **Explanation:** `toString()` ব্যবহার করে **ফাংশনের সোর্স কোড** প্রিন্ট করা যায়।

---

## **📌 ৬. `length` Property**  
🔹 **ফাংশনে কয়টি প্যারামিটার আছে তা দেখায়**  

```js
function sum(a, b, c) {
    return a + b + c;
}

console.log(sum.length);
```
**✅ Output:**  
```
3
```

✔ **Explanation:** `sum.length` → **৩টি প্যারামিটার আছে** তাই `3` রিটার্ন করবে।

---

## **📌 ৭. `name` Property**  
🔹 **ফাংশনের নাম বের করা যায়**  

```js
function multiply(x, y) {
    return x * y;
}

console.log(multiply.name);
```
**✅ Output:**  
```
multiply
```

✔ **Explanation:** `name` প্রপার্টি **ফাংশনের নাম** রিটার্ন করে।

---

## **📌 ৮. Function Methods Use Cases (প্রয়োগ)**  

✅ **`call()` ও `apply()`** ব্যবহার করা হয় **অন্য অবজেক্টের সাথে ফাংশন ব্যবহার করতে**।  
✅ **`bind()`** ব্যবহার করে **ফাংশনের `this` সেট করা যায়**।  
✅ **`toString()`** ব্যবহার করে **ফাংশনের সোর্স কোড দেখা যায়**।  
✅ **`length` ও `name`** ব্যবহার করে **ফাংশনের প্যারামিটার ও নাম জানা যায়**।  

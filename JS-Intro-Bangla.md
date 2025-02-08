### **📌 জাভাস্ক্রিপ্ট (JavaScript) সম্পর্কে সম্পূর্ণ গাইড**  

**জাভাস্ক্রিপ্ট** (JavaScript) হল একটি **স্ক্রিপ্টিং ভাষা** যা ওয়েব পেজের ইন্টারঅ্যাকটিভিটি এবং ডাইনামিক ফিচার তৈরি করতে ব্যবহৃত হয়। এটি **ব্রাউজারের মধ্যে রান** করে এবং ওয়েব পেজের কনটেন্ট, স্টাইল এবং আচরণকে পরিবর্তন করতে সক্ষম।

---

## **🔹 জাভাস্ক্রিপ্টের মৌলিক বিষয়**  

### **১. ভেরিয়েবল (Variables)**  
ভেরিয়েবলগুলি এমন **সংরক্ষণস্থান** যেখানে ডাটা রাখা হয়। জাভাস্ক্রিপ্টে ভেরিয়েবল তিনটি ধরনের হতে পারে:  
- **var**  
- **let**  
- **const**

```javascript
let x = 10;   // মিউটেবল (পরিবর্তনযোগ্য)
const y = 5;  // ইমিউটেবল (অপরিবর্তনীয়)
```

### **২. ডাটা টাইপ (Data Types)**  
জাভাস্ক্রিপ্টে বিভিন্ন ডাটা টাইপ রয়েছে, যেমন:  
- **Primitive Types**: String, Number, Boolean, Undefined, Null, Symbol, BigInt
- **Reference Types**: Object, Array, Function

```javascript
let name = "John";  // String
let age = 25;       // Number
let isActive = true; // Boolean
let user = null;    // Null
```

### **৩. অপারেটর (Operators)**  
অপারেটর দিয়ে **গাণিতিক, তুলনা, লজিক্যাল** ইত্যাদি অপারেশন করা যায়।  

**গাণিতিক অপারেটর**:
```javascript
let sum = 10 + 5; // 15
```

**তুলনা অপারেটর**:
```javascript
let isEqual = 10 == 10; // true
```

**লজিক্যাল অপারেটর**:
```javascript
let isTrue = true && false; // false
```

---

## **🔹 কন্ডিশনাল স্টেটমেন্ট (Conditional Statements)**  
কন্ডিশনাল স্টেটমেন্ট দিয়ে শর্তানুযায়ী কোডের কার্যাবলী নিয়ন্ত্রণ করা হয়।

**if-else**:
```javascript
let age = 20;
if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

**switch**:
```javascript
let day = 3;
switch (day) {
  case 1:
    console.log("Sunday");
    break;
  case 2:
    console.log("Monday");
    break;
  default:
    console.log("Invalid day");
}
```

---

## **🔹 লুপ (Loops)**  
লুপের মাধ্যমে আমরা কোডকে বারবার রান করাতে পারি।  

### **for loop**  
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);  // 0, 1, 2, 3, 4
}
```

### **while loop**  
```javascript
let i = 0;
while (i < 5) {
  console.log(i);  // 0, 1, 2, 3, 4
  i++;
}
```

### **do-while loop**  
```javascript
let i = 0;
do {
  console.log(i);  // 0, 1, 2, 3, 4
  i++;
} while (i < 5);
```

---

## **🔹 ফাংশন (Functions)**  
ফাংশন হল কোডের একটি ব্লক যা একাধিক বার ব্যবহার করা যায়।  

### **ফাংশন ডিফিনেশন**:
```javascript
function greet() {
  console.log("Hello, World!");
}
greet();  // "Hello, World!"
```

### **ফাংশনে আর্গুমেন্ট এবং রিটার্ন**:
```javascript
function add(a, b) {
  return a + b;
}
let result = add(3, 4);  // 7
```

---

## **🔹 অবজেক্ট (Objects)**  
অবজেক্ট হল ডাটা ধারণ করার জন্য একটি কমপ্লেক্স ডাটা স্ট্রাকচার, যা প্রোপার্টি এবং মেথড ধারণ করতে পারে।  

```javascript
let person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log("Hello, " + this.name);
  }
};
person.greet();  // "Hello, John"
```

---

## **🔹 অ্যারে (Arrays)**  
অ্যারে একটি লিনিয়ার ডাটা স্ট্রাকচার, যেখানে একাধিক ভ্যালু রাখা যায়।  

```javascript
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits[0]);  // "Apple"
```

---

## **🔹 ইভেন্ট (Events)**  
জাভাস্ক্রিপ্ট ব্যবহার করে ওয়েব পেজের ইভেন্টগুলির প্রতি রেসপন্স দেয়া যায়। উদাহরণস্বরূপ, ক্লিক, হোভার, কিবোর্ড ইনপুট ইত্যাদি।

```javascript
document.getElementById("myButton").onclick = function() {
  alert("Button clicked!");
};
```

---

## **🔹 এসিনক্রোনাস জাভাস্ক্রিপ্ট (Asynchronous JavaScript)**  
এটি এমন কোড যে কোন কাজের জন্য অপেক্ষা না করে কোড চলতে থাকে। এর জন্য **callback functions**, **Promises** এবং **async/await** ব্যবহৃত হয়।  

### **Callback Function**:
```javascript
function greet(callback) {
  console.log("Hello!");
  callback();
}

greet(function() {
  console.log("Callback executed!");
});
```

### **Promise**:
```javascript
let promise = new Promise(function(resolve, reject) {
  let success = true;
  if (success) {
    resolve("Task completed successfully!");
  } else {
    reject("Task failed.");
  }
});

promise.then(function(value) {
  console.log(value);  // "Task completed successfully!"
}).catch(function(error) {
  console.log(error);
});
```

### **Async/Await**:
```javascript
async function fetchData() {
  let result = await fetch('https://api.example.com/data');
  let data = await result.json();
  console.log(data);
}
```

---

## **🔹 ক্লাস (Classes)**  
জাভাস্ক্রিপ্টে ক্লাস ব্যবহার করে অবজেক্ট ও তাদের মেথড গঠন করা হয়।  

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello, " + this.name);
  }
}

let person1 = new Person("John", 30);
person1.greet();  // "Hello, John"
```

---

## **🔹 ব্রাউজার API এবং DOM**  
জাভাস্ক্রিপ্টের সাহায্যে ওয়েব পেজের **DOM** (Document Object Model) এর সাথে ইন্টারঅ্যাক্ট করা যায়। এর মাধ্যমে HTML এবং CSS-এর মান পরিবর্তন করা সম্ভব।  

**DOM Manipulation উদাহরণ**:
```javascript
document.getElementById("myElement").style.color = "red";
```

---

## **🔹 উপসংহার**  
জাভাস্ক্রিপ্ট হলো ওয়েব ডেভেলপমেন্টের একটি অত্যন্ত শক্তিশালী ভাষা, যা ফ্রন্ট-এন্ড এবং ব্যাক-এন্ড ডেভেলপমেন্টের জন্য ব্যবহৃত হয়। এটি খুবই গুরুত্বপূর্ণ ওয়েব অ্যাপ্লিকেশন এবং ওয়েব সাইটের ইন্টারঅ্যাকটিভিটি বৃদ্ধি করতে।

এটি শেখার পর তুমি ওয়েব পেজে ইন্টারঅ্যাকশন, ডায়নামিক কন্টেন্ট, এবং আরও অনেক কিছু তৈরি করতে পারবে। জাভাস্ক্রিপ্টের অন্যান্য বিষয়গুলির উপর গভীরভাবে কাজ করতে চাইলে আমাকে জানাও! 😊
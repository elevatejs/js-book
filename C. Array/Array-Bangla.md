### **📌 জাভাস্ক্রিপ্টের অ্যারে (Array) সম্পর্কে সম্পূর্ণ গাইড**  

অ্যারে হলো এক ধরনের ডাটা স্ট্রাকচার, যা একাধিক ভ্যালু একসাথে সংরক্ষণ করতে পারে।  

---
## **🔹 কিভাবে অ্যারে ডিক্লেয়ার করবেন?**  
জাভাস্ক্রিপ্টে অ্যারে ডিক্লেয়ার করার কয়েকটি উপায় আছে:  

### **✅ লিটারাল সিনট্যাক্স ব্যবহার করে (সবচেয়ে সাধারণ পদ্ধতি)**
```javascript
let animals = ["Dog", "Cat", "Rabbit", "Bird"];
console.log(animals); // Output: ["Dog", "Cat", "Rabbit", "Bird"]
```

### **✅ Array কনস্ট্রাক্টর ব্যবহার করে**
```javascript
let numbers = new Array(10, 20, 30, 40);
console.log(numbers); // Output: [10, 20, 30, 40]
```

### **✅ খালি অ্যারে তৈরি করে পরে ডাটা যোগ করা**
```javascript
let fruits = [];
fruits[0] = "Mango";
fruits[1] = "Banana";
console.log(fruits); // Output: ["Mango", "Banana"]
```

---
## **🔹 অ্যারের ইনডেক্স ও অ্যাক্সেস করা**  
অ্যারে ইনডেক্স **০ (zero-based indexing)** থেকে শুরু হয়।  

```javascript
let colors = ["Red", "Green", "Blue"];
console.log(colors[0]); // Output: Red
console.log(colors[1]); // Output: Green
console.log(colors[2]); // Output: Blue
```

---
## **🔹 গুরুত্বপূর্ণ অ্যারে মেথড (Methods)**  

### **✅ ১. length - অ্যারের দৈর্ঘ্য (length) বের করা**
```javascript
let numbers = [10, 20, 30, 40];
console.log(numbers.length); // Output: 4
```

### **✅ ২. push() - নতুন উপাদান শেষে যোগ করা**
```javascript
let fruits = ["Apple", "Banana"];
fruits.push("Orange");
console.log(fruits); // Output: ["Apple", "Banana", "Orange"]
```

### **✅ ৩. pop() - শেষের উপাদান সরানো**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
fruits.pop();
console.log(fruits); // Output: ["Apple", "Banana"]
```

### **✅ ৪. unshift() - শুরুতে নতুন উপাদান যোগ করা**
```javascript
let fruits = ["Banana", "Orange"];
fruits.unshift("Apple");
console.log(fruits); // Output: ["Apple", "Banana", "Orange"]
```

### **✅ ৫. shift() - প্রথম উপাদান সরানো**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
fruits.shift();
console.log(fruits); // Output: ["Banana", "Orange"]
```

### **✅ ৬. indexOf() - নির্দিষ্ট উপাদানের ইনডেক্স খুঁজে বের করা**
```javascript
let animals = ["Dog", "Cat", "Bird"];
console.log(animals.indexOf("Cat")); // Output: 1
console.log(animals.indexOf("Lion")); // Output: -1 (না থাকলে -1 রিটার্ন করে)
```

### **✅ ৭. includes() - কোনো উপাদান আছে কিনা চেক করা**
```javascript
let animals = ["Dog", "Cat", "Bird"];
console.log(animals.includes("Cat")); // Output: true
console.log(animals.includes("Lion")); // Output: false
```

### **✅ ৮. slice() - নির্দিষ্ট অংশ কপি করা (অরিজিনাল অ্যারে পরিবর্তন হয় না)**
```javascript
let numbers = [10, 20, 30, 40, 50];
let newNumbers = numbers.slice(1, 4); // ১ থেকে ৪ (৪ ইনডেক্স বাদ)
console.log(newNumbers); // Output: [20, 30, 40]
```

### **✅ ৯. splice() - অ্যারে থেকে উপাদান মুছে ফেলা বা যুক্ত করা (অরিজিনাল অ্যারে পরিবর্তন হয়)**
```javascript
let numbers = [10, 20, 30, 40, 50];
numbers.splice(2, 1); // ২ নম্বর ইনডেক্স থেকে ১টি উপাদান রিমুভ
console.log(numbers); // Output: [10, 20, 40, 50]
```

### **✅ ১০. reverse() - অ্যারের উপাদানগুলো উল্টানো**
```javascript
let letters = ["A", "B", "C"];
letters.reverse();
console.log(letters); // Output: ["C", "B", "A"]
```

### **✅ ১১. sort() - অ্যারে সাজানো (Alphabetically)**
```javascript
let names = ["Shihab", "Rahim", "Karim", "Abdul"];
names.sort();
console.log(names); // Output: ["Abdul", "Karim", "Rahim", "Shihab"]
```

### **✅ ১২. map() - প্রতিটি উপাদানে ফাংশন প্রয়োগ করা**
```javascript
let numbers = [1, 2, 3, 4, 5];
let squares = numbers.map(num => num * num);
console.log(squares); // Output: [1, 4, 9, 16, 25]
```

### **✅ ১৩. filter() - নির্দিষ্ট শর্ত অনুযায়ী ফিল্টার করা**
```javascript
let numbers = [10, 20, 25, 30, 35, 40];
let filteredNumbers = numbers.filter(num => num > 25);
console.log(filteredNumbers); // Output: [30, 35, 40]
```

### **✅ ১৪. reduce() - সমস্ত উপাদান যোগ বা অন্য কোনো অপারেশন করা**
```javascript
let numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // Output: 15
```

---
## **🔹 মাল্টিডাইমেনশনাল (Two-Dimensional) অ্যারে**  
একটি অ্যারের মধ্যে আরেকটি অ্যারে থাকলে তাকে মাল্টিডাইমেনশনাল অ্যারে বলা হয়।  

```javascript
let matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];

console.log(matrix[0][1]); // Output: 2
console.log(matrix[2][2]); // Output: 9
```

---
## **🔹 অ্যারের ওপর লুপ চালানো**  

### **✅ for লুপ ব্যবহার করে**
```javascript
let fruits = ["Mango", "Banana", "Apple"];
for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```

### **✅ forEach() মেথড ব্যবহার করে**
```javascript
let fruits = ["Mango", "Banana", "Apple"];
fruits.forEach(fruit => console.log(fruit));
```

### **✅ for...of লুপ ব্যবহার করে**
```javascript
let colors = ["Red", "Green", "Blue"];
for (let color of colors) {
    console.log(color);
}
```

---

## **📌 JavaScript Array Methods (অ্যারে মেথড) - Table Format**  

| মেথড | বর্ণনা | উদাহরণ | আউটপুট |
|------------|---------------------------------|-------------------------------------|--------------------------|
| `push()` | নতুন এলিমেন্ট অ্যারের শেষে যোগ করে | ```javascript let arr = [1, 2, 3]; arr.push(4); console.log(arr); ``` | `[1, 2, 3, 4]` |
| `pop()` | অ্যারের শেষ এলিমেন্ট সরিয়ে রিটার্ন করে | ```javascript let arr = [1, 2, 3]; arr.pop(); console.log(arr); ``` | `[1, 2]` |
| `shift()` | অ্যারের প্রথম এলিমেন্ট সরিয়ে রিটার্ন করে | ```javascript let arr = [1, 2, 3]; arr.shift(); console.log(arr); ``` | `[2, 3]` |
| `unshift()` | নতুন এলিমেন্ট অ্যারের শুরুতে যোগ করে | ```javascript let arr = [2, 3]; arr.unshift(1); console.log(arr); ``` | `[1, 2, 3]` |
| `concat()` | দুটি বা তার বেশি অ্যারে যুক্ত করে নতুন অ্যারে তৈরি করে | ```javascript let arr1 = [1, 2], arr2 = [3, 4]; let newArr = arr1.concat(arr2); console.log(newArr); ``` | `[1, 2, 3, 4]` |
| `slice()` | নির্দিষ্ট অংশ কেটে নতুন অ্যারে তৈরি করে | ```javascript let arr = [1, 2, 3, 4, 5]; let sliced = arr.slice(1, 4); console.log(sliced); ``` | `[2, 3, 4]` |
| `splice()` | নির্দিষ্ট স্থানে এলিমেন্ট যোগ বা অপসারণ করে | ```javascript let arr = [1, 2, 3, 4]; arr.splice(2, 1, 99); console.log(arr); ``` | `[1, 2, 99, 4]` |
| `indexOf()` | নির্দিষ্ট মানের ইনডেক্স খুঁজে বের করে | ```javascript let arr = [10, 20, 30]; console.log(arr.indexOf(20)); ``` | `1` |
| `includes()` | নির্দিষ্ট মান অ্যারেতে আছে কিনা চেক করে | ```javascript let arr = [1, 2, 3]; console.log(arr.includes(2)); ``` | `true` |
| `join()` | অ্যারের সকল এলিমেন্ট স্ট্রিং আকারে যোগ করে | ```javascript let arr = ["Hello", "World"]; console.log(arr.join(" ")); ``` | `"Hello World"` |
| `reverse()` | অ্যারে উল্টে দেয় | ```javascript let arr = [1, 2, 3]; arr.reverse(); console.log(arr); ``` | `[3, 2, 1]` |
| `sort()` | অ্যারে ক্রমানুসারে সাজায় | ```javascript let arr = [3, 1, 4, 2]; arr.sort(); console.log(arr); ``` | `[1, 2, 3, 4]` |
| `map()` | প্রতিটি এলিমেন্টের উপর ফাংশন চালিয়ে নতুন অ্যারে তৈরি করে | ```javascript let arr = [1, 2, 3]; let squared = arr.map(x => x * x); console.log(squared); ``` | `[1, 4, 9]` |
| `filter()` | শর্ত অনুযায়ী নতুন অ্যারে তৈরি করে | ```javascript let arr = [1, 2, 3, 4]; let even = arr.filter(x => x % 2 === 0); console.log(even); ``` | `[2, 4]` |
| `reduce()` | সমস্ত এলিমেন্ট একত্র করে একটি মান তৈরি করে | ```javascript let arr = [1, 2, 3, 4]; let sum = arr.reduce((a, b) => a + b, 0); console.log(sum); ``` | `10` |
| `find()` | শর্ত মিলে এমন প্রথম এলিমেন্ট খুঁজে বের করে | ```javascript let arr = [10, 20, 30]; let found = arr.find(x => x > 15); console.log(found); ``` | `20` |
| `findIndex()` | শর্ত মিলে এমন প্রথম এলিমেন্টের ইনডেক্স দেয় | ```javascript let arr = [5, 10, 15]; let index = arr.findIndex(x => x > 8); console.log(index); ``` | `1` |
| `every()` | সব এলিমেন্ট শর্ত মেনে চললে `true` দেয় | ```javascript let arr = [2, 4, 6]; console.log(arr.every(x => x % 2 === 0)); ``` | `true` |
| `some()` | অন্তত একটি এলিমেন্ট শর্ত মেনে চললে `true` দেয় | ```javascript let arr = [1, 3, 5]; console.log(arr.some(x => x % 2 === 0)); ``` | `false` |
| `fill()` | অ্যারের সব এলিমেন্ট নির্দিষ্ট মান দিয়ে পূরণ করে | ```javascript let arr = [1, 2, 3]; arr.fill(0); console.log(arr); ``` | `[0, 0, 0]` |


---
## **🔹 শেষ কথা**  
জাভাস্ক্রিপ্টের **অ্যারে** খুবই শক্তিশালী এবং ব্যবহারবান্ধব। এটি ডাটা সংরক্ষণ, সাজানো এবং প্রসেসিংয়ের জন্য অপরিহার্য। তুমি যদি এগুলো ভালোভাবে শিখে নাও, তাহলে জাভাস্ক্রিপ্টে আরও দক্ষ হয়ে যাবে। 😊  

তোমার যদি কোনো নির্দিষ্ট জায়গায় সমস্যা হয়, বলো, আমি ব্যাখ্যা করে দেব! 🚀
# JavaScript Quick Notes (Beginner Friendly)

## 1. Variables

```js
let name = "Priyanshu";
const age = 20;
var city = "Mumbai";
```

* `let` → value can change
* `const` → value cannot change
* `var` → old way

---

## 2. Data Types

```js
let str = "Hello";   // String
let num = 10;        // Number
let isTrue = true;   // Boolean
let arr = [1,2,3];   // Array
let obj = {name:"Sam"}; // Object
```

---

## 3. Functions

```js
function greet() {
   console.log("Hello");
}

greet();
```

### Arrow Function

```js
const add = (a,b) => {
   return a + b;
}

console.log(add(2,3));
```

---

## 4. If Else

```js
let age = 18;

if(age >= 18){
   console.log("Adult");
}else{
   console.log("Minor");
}
```

---

## 5. Loops

### For Loop

```js
for(let i = 0; i < 5; i++){
   console.log(i);
}
```

### While Loop

```js
let i = 0;

while(i < 5){
   console.log(i);
   i++;
}
```

---

## 6. Arrays

```js
let fruits = ["Apple", "Banana", "Mango"];

console.log(fruits[0]);

fruits.push("Orange");

console.log(fruits);
```

---

## 7. Objects

```js
let person = {
   name: "Priyanshu",
   age: 20
};

console.log(person.name);
```

---

## 8. DOM (HTML Control)

```js
document.getElementById("demo").innerText = "Hello JS";
```

---

## 9. Events

```js
button.addEventListener("click", function(){
   console.log("Button Clicked");
});
```

---

## 10. Callback Function

```js
function greet(name, callback){
   console.log("Hello " + name);
   callback();
}

function bye(){
   console.log("Bye");
}

greet("Priyanshu", bye);
```

---

## 11. Promise

```js
let promise = new Promise((resolve, reject) => {
   let success = true;

   if(success){
      resolve("Done");
   }else{
      reject("Error");
   }
});

promise
.then((msg) => console.log(msg))
.catch((err) => console.log(err));
```

---

## 12. Async Await

```js
async function getData(){

   let response = await fetch("https://jsonplaceholder.typicode.com/users");

   let data = await response.json();

   console.log(data);
}

getData();
```

---

## 13. Important Array Methods

```js
let nums = [1,2,3];

nums.map(n => console.log(n));

nums.filter(n => n > 1);

nums.find(n => n === 2);
```

---

## 14. Destructuring

```js
let person = {
   name: "Sam",
   age: 20
};

let {name, age} = person;

console.log(name);
```

---

## 15. Spread Operator

```js
let arr1 = [1,2];
let arr2 = [...arr1, 3,4];

console.log(arr2);
```

---

# Most Important Interview Line

JavaScript is:

* Single threaded
* Synchronous by default
* Asynchronous using callbacks, promises, async-await

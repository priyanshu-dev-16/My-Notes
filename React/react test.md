# React Random Quick Notes

## 1. What is React?

* React is a JavaScript library for building UI.
* Created by Meta Platforms.
* Uses **components** to build websites.

---

## 2. Create Component

```jsx
function App() {
  return <h1>Hello React</h1>;
}

export default App;
```

---

## 3. JSX

* JSX = HTML inside JavaScript.

```jsx
const name = "Priyanshu";

<h1>Hello {name}</h1>
```

---

## 4. Props

* Props pass data from parent to child.

```jsx
function User(props) {
  return <h1>{props.name}</h1>;
}

<User name="Priyanshu" />
```

---

## 5. useState Hook

* Used to store data.

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <>
      <h1>{count}</h1>

      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>
    </>
  );
}
```

---

## 6. Event Handling

```jsx
function App() {
  function hello() {
    alert("Hello");
  }

  return <button onClick={hello}>Click</button>;
}
```

---

## 7. useEffect

* Runs side effects.

```jsx
import { useEffect } from "react";

useEffect(() => {
  console.log("Component Loaded");
}, []);
```

---

## 8. Conditional Rendering

```jsx
let isLogin = true;

return (
  <>
    {isLogin ? <h1>Welcome</h1> : <h1>Please Login</h1>}
  </>
);
```

---

## 9. Map Function

```jsx
const users = ["A", "B", "C"];

return (
  <>
    {users.map((u, index) => (
      <h1 key={index}>{u}</h1>
    ))}
  </>
);
```

---

## 10. Forms

```jsx
function App() {
  const [name, setName] = useState("");

  return (
    <>
      <input
        type="text"
        onChange={(e) => setName(e.target.value)}
      />

      <h1>{name}</h1>
    </>
  );
}
```

---

## 11. React Folder Structure

```txt
src/
 ├── components/
 ├── App.js
 ├── main.js
```

---

## 12. Important Commands

### Create React App

```bash
npx create-react-app myapp
```

### Run Project

```bash
npm start
```

### Vite React App

```bash
npm create vite@latest
```

---

## 13. Arrow Function

```jsx
const hello = () => {
  console.log("Hello");
};
```

---

## 14. Fragment

```jsx
<>
  <h1>Hello</h1>
  <p>React</p>
</>
```

---

## 15. Export & Import

### Export

```jsx
export default App;
```

### Import

```jsx
import App from "./App";
```

---

## 16. Simple API Fetch

```jsx
useEffect(() => {
  fetch("https://jsonplaceholder.typicode.com/users")
    .then((res) => res.json())
    .then((data) => console.log(data));
}, []);
```

---

# Easy Interview Questions

### Q1. What is React?

A JavaScript library for building UI.

### Q2. What is JSX?

HTML inside JavaScript.

### Q3. What is useState?

A hook used to store state/data.

### Q4. What is a component?

Reusable piece of UI.

### Q5. What are props?

Data passed from parent to child component.

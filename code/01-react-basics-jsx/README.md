# ⚛️ React Basics

## What is React?

**React** is an **external library** that helps us **create websites more easily**.

1. React is an **external library**.
2. React helps us **create websites more easily**.

---

## 📦 External Library

An **external library** is code that is outside our computer and was written by someone else.

### React as an External Library

- It's a bunch of code that is outside our computer.
- We can load this code on our website and use it.

---

## 🌐 Why Are There 2 External Libraries for React?

```html
<script src="https://unpkg.com/supersimpledev/react.js"></script>
<script src="https://unpkg.com/supersimpledev/react-dom.js"></script>
```

### React Can Be Used in Different Places

- **Websites**
- **Mobile Apps**

1. **React** → Shared features
2. **ReactDOM** → Features specific to websites

### Using React to Create Websites

**React + ReactDOM**

### Using React to Create Mobile Apps

**React + ReactNative**

---

## ⚛️ How to Use React?

```js
const container = document.querySelector('.js-container');

ReactDOM.createRoot(container).render(
  'Welcome to SuperSimpleDev React Course'
);
```

1. **Find the HTML element**

   ```js
   const container = document.querySelector('.js-container');
   ```

   - `container` is a **JavaScript variable**.
   - It stores a reference to the HTML element with the class `.js-container`.

2. **Render using ReactDOM**

   ```js
   ReactDOM.createRoot(container).render(
     'Welcome to SuperSimpleDev React Course'
   );
   ```

   - `ReactDOM` uses the `container` as the place to render our React content.

---

## 🔄 What is Babel?

**Babel** is a JavaScript compiler.

It translates other languages into JavaScript.

So, Babel is a JavaScript compiler that we can use as an external library.

### Why Do We Need Babel?

When using React, we don't use normal JavaScript.

We use an enhanced version of JavaScript = **JSX**

---

### JSX = JavaScript XML

JSX is a **syntax extension for JavaScript** that lets us write HTML-like syntax directly in our JavaScript code.

> JSX is similar to JavaScript, but it allows us to write HTML directly in our JavaScript code.

---

## ⚠️ Problem with JSX

When using React, we use JSX instead of normal JavaScript.

### The Problem

- Our web browser doesn't understand JSX.
- We need to translate JSX into JavaScript.

### 🛠️ Babel

**Babel translates JSX into JavaScript.**

---

## 🚀 Why Use React?

React helps us create websites more easily.

1. **Creating a website with React feels natural**
2. **JSX lets us find errors more easily**
3. **We can insert values inside JSX elements (string interpolation)**

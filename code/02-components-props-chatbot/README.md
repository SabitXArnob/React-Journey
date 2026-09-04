# React Components

This lesson introduces React components and shows how to make them reusable.

The examples build a simple chatbot step by step.

---

## 1. Components

A component is a reusable piece of UI.

```jsx
function ChatInput() {
  return (
    <div>
      <input />
      <button>Send</button>
    </div>
  );
}
```

We can use our own component with JSX:

```jsx
<ChatInput />
```

We can also call the component like a regular JavaScript function:

```jsx
{ChatInput()}
```

### Component Naming

Component names must start with a capital letter (PascalCase).

```jsx
function ChatInput() {
  // ...
}
```

---

## 2. JSX Rules

JSX is more strict than HTML.

In JSX, every element must have a closing tag.

```jsx
<input />
```

`<input />` is a self-closing tag.

It is the same as:

```jsx
<input></input>
```

---

## 3. Fragments

A Fragment (`<>...</>`) groups multiple elements together without creating an extra HTML element.

```jsx
function ChatInput() {
  return (
    <>
      <input placeholder="Send a message to Chatbot" size="30" />
      <button>Send</button>
    </>
  );
}
```

Fragments are useful when a component needs to return multiple elements without wrapping them in an extra `<div>`.

---

## 4. Building the Chatbot

We created reusable components for the chatbot:

```jsx
function ChatInput() {
  // ...
}

function ChatMessage() {
  // ...
}
```

We can then use them together:

```jsx
const app = (
  <>
    <ChatInput />
    <ChatMessage />
  </>
);
```

The `ChatMessage` component can be reused for multiple messages.

---

## 5. Props

**Props = properties**

Props allow us to pass data into a component, making the component reusable with different values.

```jsx
<ChatMessage message="hello chatbot" sender="user" />

<ChatMessage
  message="Hello! How can I help you?"
  sender="robot"
/>
```

The component receives the props:

```jsx
function ChatMessage(props) {
  // ...
}
```

We can access individual properties:

```jsx
const message = props.message;
const sender = props.sender;
```

---

## 6. Destructuring Props

Instead of accessing each property through `props`:

```jsx
function ChatMessage(props) {
  const message = props.message;
  const sender = props.sender;
}
```

We can use destructuring:

```jsx
function ChatMessage(props) {
  const { message, sender } = props;
}
```

Or destructure directly in the function parameter:

```jsx
function ChatMessage({ message, sender }) {
  // ...
}
```

This is a shorter and cleaner way to access the values we need from props.

---

## 7. Guard Operator (`&&`)

The guard operator (`&&`) can be used for conditional rendering.

In JavaScript:

```jsx
const result = value1 && value2;
```

* If `value1` is truthy, the result is `value2`.
* If `value1` is falsy, the result is `value1`.

In JSX, this is useful when we only want to render an element when a condition is true:

```jsx
{sender === 'robot' && (
  <img src="robot.png" width="50" />
)}
```

The image is rendered only when `sender === 'robot'` is true.

We can do the same for the user:

```jsx
{sender === 'user' && (
  <img src="user.png" width="50" />
)}
```

This is a shorter way to conditionally render an element instead of using an `if` statement that returns a different JSX structure.

---

## 8. App Component

As the application grows, we can put the main UI inside an `App` component.

```jsx
function App() {
  return (
    <>
      <ChatInput />
      <ChatMessage
        message="hello chatbot"
        sender="user"
      />
      <ChatMessage
        message="Hello! How can I help you?"
        sender="robot"
      />
    </>
  );
}
```

Then we can render the entire application using:

```jsx
ReactDOM.createRoot(container).render(<App />);
```

The `App` component acts as the main component that organizes the other components in our application.

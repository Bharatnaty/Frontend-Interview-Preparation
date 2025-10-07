# Frontend Interview Preparation

A collection of common **HTML, CSS, JavaScript, and React** interview questions with answers.  
This repo is collaborative — feel free to contribute more questions 🚀

---

## 📑 Table of Contents
- [HTML](#html)
- [CSS](#css)
- [JavaScript](#javascript)
- [React](#react)

---

## 🟠 HTML

1. What is the difference between block, inline, and inline-block elements?  
   - Block: Takes full width (`<div>`, `<p>`, `<h1>`).  
   - Inline: Takes only needed space (`<span>`, `<a>`).  
   - Inline-block: Behaves like inline but supports width/height.  

1. What are semantic HTML tags? Why are they important?  
   - Tags that describe meaning, not just presentation (`<header>`, `<article>`, `<footer>`).  
   - Improves accessibility & SEO.  

1. Difference between `id` and `class` in HTML?  
   - `id`: Unique identifier (used once per page).  
   - `class`: Can be reused for multiple elements.  

1. What is **datalist** in html?
   - The <datalist> element in HTML is used to provide a list of predefined suggestions for an <input> field.
   - It gives users the convenience of auto-complete options, while still allowing free text entry.
   - **Example**
     ```
     <input list="browsers" name="browser" placeholder="Choose or type...">

      <datalist id="browsers">
        <option value="Google Chrome">
        <option value="Mozilla Firefox">
        <option value="Microsoft Edge">
        <option value="Safari">
        <option value="Opera">
      </datalist>

     ```


## 🔵 CSS

1. Difference between relative, absolute, fixed, and sticky positioning?  
   - Relative: Positioned relative to itself.  
   - Absolute: Positioned relative to nearest positioned ancestor.  
   - Fixed: Always stays at the same place (relative to viewport).  
   - Sticky: Switches between relative & fixed depending on scroll.  

1. What is the difference between inline, internal, and external CSS?  
   - Inline: Inside the element (`style=""`).  
   - Internal: Inside `<style>` tag.  
   - External: In a separate `.css` file.  

1. Explain the difference between `em`, `rem`, `%`, and `px` in CSS.  
   - `px`: Fixed pixels.  
   - `em`: Relative to parent font-size.  
   - `rem`: Relative to root (`html`) font-size.  
   - `%`: Relative to parent container.  

---

## 🟡 JavaScript

1. Difference between `var`, `let`, and `const`?  
   - `var`: Function-scoped, hoisted, can be redeclared.  
   - `let`: Block-scoped, hoisted but not initialized, can be reassigned.  
   - `const`: Block-scoped, cannot be reassigned.  

1. What is hoisting in JavaScript?  
   - JavaScript moves variable & function declarations to the top of scope before execution.  

1. Difference between `==` and `===`?  
   - `==`: Compares values after type conversion (loose equality).  
   - `===`: Compares both value & type (strict equality).  

1. Explain closures in JavaScript.  
   - A closure is when a function remembers its lexical scope even if executed outside of it.  

---

## 🟢 React

1. What is the difference between functional and class components?  
   - Class: Uses `this`, lifecycle methods.  
   - Functional: Uses hooks (`useState`, `useEffect`), simpler syntax.  

1. What is the difference between `useMemo`, `useCallback`, and `React.memo`?  
   - `useMemo`: Memoizes a **calculated value**.  
   - `useCallback`: Memoizes a **function** reference.  
   - `React.memo`: Memoizes a **whole component** to avoid re-renders.

1. What is the difference between `useMemo`, `useCallback`, and `React.memo`?  
   <img width="1268" height="475" alt="image" src="https://github.com/user-attachments/assets/b78c9190-2d18-4b5d-be26-7881d1e09a5f" />
   **useCallback Example**

      ```import React, { useState, useCallback } from "react";
      
      function Child({ onAdd }) {
        console.log("Child re-rendered");
        return <button onClick={onAdd}>Add</button>;
      }
      
      export default function Parent() {
        const [count, setCount] = useState(0);
        const [theme, setTheme] = useState("light");
      
        // ✅ Using useCallback prevents unnecessary re-creations of this function
        const handleAdd = useCallback(() => {
          setCount((prev) => prev + 1);
        }, []);
      
        return (
          <div>
            <h2>Count: {count}</h2>
            <Child onAdd={handleAdd} />
            <button onClick={() => setTheme(theme === "light" ? "dark" : "light")}>
              Toggle Theme
            </button>
          </div>
        );
      }
      ```
   **useMemo Exmaple**

      ```import React, { useState, useMemo } from "react";

         export default function ProductList({ products }) {
           const [search, setSearch] = useState("");
         
           // ✅ useMemo prevents re-running this heavy filter on every render
           const filteredProducts = useMemo(() => {
             console.log("Filtering products...");
             return products.filter((p) =>
               p.name.toLowerCase().includes(search.toLowerCase())
             );
           }, [search, products]);
         
           return (
             <div>
               <input
                 placeholder="Search..."
                 value={search}
                 onChange={(e) => setSearch(e.target.value)}
               />
               <ul>
                 {filteredProducts.map((p) => (
                   <li key={p.id}>{p.name}</li>
                 ))}
               </ul>
             </div>
           );
         }
      ```

1. What is the difference between client and server components in Next.js?  
   - Client: Run in browser, can use state/effects.  
   - Server: Rendered on server, better performance, can fetch data directly.  

1. Explain SSR, SSG, and ISR in Next.js.  
   - SSR: Rendered on request.  
   - SSG: Rendered at build time.  
   - ISR: Rebuilds pages after interval.
  
1. What are functional components in React?
   - Functional components are JavaScript functions that accept arguments (called props) and return React elements that describe what should appear on the screen.

1. What is an implicit return in functional components?
   - If a component only contains a single return statement, you can skip the return keyword and curly braces by using parentheses:
   - ```javascript
         // Functional component with implicit return
         const MyComponent = () => (
           <h1>Hello, world!</h1>
         );
         export default MyComponent;

1. Why must a React component return a single root element?
   - React requires one root element because the virtual DOM needs a single entry point to represent the component tree.
     
1. Why is JSX not valid JavaScript?
   - Browsers cannot directly interpret JSX. It must be transpiled (commonly by Babel) into JavaScript that React can execute.
  
1. React Elements vs. HTML Elements?
   - | Feature        | React Element                 | HTML Element                      |
     | -------------- | ----------------------------- | --------------------------------- |
     | What it is     | JS object (virtual DOM node)  | Actual DOM node in browser        |
     | Mutability     | Immutable                     | Mutable                           |
     | Created by     | JSX / `React.createElement()` | HTML / `document.createElement()` |
     | Where it lives | In memory (virtual DOM)       | In browser DOM tree               |
     | Purpose        | Describe UI structure         | Display UI structure              |
     
1. What are props in React?
   - Read-only data passed from parent to child to configure components.

1. What is the difference between props and state?
   - Props: Immutable, passed from parent.
   - State: Mutable, managed within the component.

1. Can a child component modify props directly?
   - ❌ No. Props are read-only; children use callback functions to update parent data.

1. What is the children prop used for?
   - To render nested JSX elements inside a component.

1. What is the purpose of defaultProps?
   - To define default values when a prop isn’t passed.
     
1. React Component Lifecycle (Class & Function)
   - What is the Component Lifecycle?
      Every React component goes through a lifecycle of three main phases:

      - Mounting – Component is created and inserted into the DOM.
      - Updating – Component re-renders when props or state change.
      - Unmounting – Component is removed from the DOM.

     These phases allow developers to run code at specific moments, such as fetching data, optimizing performance, or cleaning up resources.
   - Class Component Lifecycle
     Class components use built-in lifecycle methods that get called automatically by React at different phases.
     ```
      | Phase          | Method                              |   Purpose                                | When It Runs                        |
      | -------------- | ----------------------------------- | ---------------------------------------- | ----------------------------------- |
      | Mounting       | `constructor()`                     | Initialize state and bind methods.       | Before component appears on screen. |
      |                | `static getDerivedStateFromProps()` | Sync state from props (rarely used).     | Before every render.                |
      |                | `render()`                          | Return JSX (UI).                         | During render.                      |
      |                | `componentDidMount()`               | Run side effects (fetch, subscriptions). | After first render.                 |
      | Updating       | `shouldComponentUpdate()`           | Optimize by skipping re-renders.         | Before re-render.                   |
      |                | `getSnapshotBeforeUpdate()`         | Capture DOM info before update.          | Before DOM changes.                 |
      |                | `componentDidUpdate()`              | Run side effects after updates.          | After DOM is updated.               |
      | Unmounting     | `componentWillUnmount()`            | Cleanup (timers, listeners, etc).        | Before component is removed.        |

     ```
   - **Example**
     ```
           class MyComponent extends React.Component {
        constructor(props) {
          super(props);
          this.state = { data: null };
        }
      
        componentDidMount() {
          console.log("Mounted");
        }
      
        shouldComponentUpdate(nextProps, nextState) {
          return nextState.data !== this.state.data;
        }
      
        componentDidUpdate() {
          console.log("Updated");
        }
      
        componentWillUnmount() {
          console.log("Unmounted");
        }
      
        render() {
          return <div>{this.state.data}</div>;
        }
      }

     ```

   - Functional Component Lifecycle (with Hooks)
     Functional components don’t have lifecycle methods, but React Hooks provide equivalent behavior — mainly through useEffect() and useLayoutEffect().
     ```
      | **Lifecycle Stage**  | **Class Method**             | **Functional Equivalent (Hooks)**                   |
      | -------------------- | ---------------------------- | --------------------------------------------------- |
      | Mounting             | `componentDidMount()`        | `useEffect(() => { ... }, [])`                      |
      | Updating             | `componentDidUpdate()`       | `useEffect(() => { ... }, [dependencies])`          |
      | Unmounting           | `componentWillUnmount()`     | Cleanup function inside `useEffect()`               |
      | State initialization | `constructor()`              | `useState()`                                        |
      | Derived state        | `getDerivedStateFromProps()` | Logic inside `useEffect()` reacting to prop changes |
     ```
   - **Example:**
     ```
     import React, { useState, useEffect } from "react";

      function MyComponent() {
        const [data, setData] = useState(null);
      
        // componentDidMount + componentDidUpdate
        useEffect(() => {
          console.log("Mounted or Updated");
          setData("Hello React!");
      
          // componentWillUnmount
          return () => {
            console.log("Cleanup before unmount");
          };
        }, []); // empty array = run once (on mount)
      
        return <div>{data}</div>;
      }
     ```
   - **Lifecycle Flow Summary**
     - Class Components
       Mounting → Updating → Unmounting constructor → getDerivedStateFromProps → render → componentDidMount → shouldComponentUpdate → render → getSnapshotBeforeUpdate → componentDidUpdate → componentWillUnmount
     - Functional Components
       Mounting → Updating → Unmounting
       
1. What is the purpose of defaultProps?
    - | Feature         | React Element                         | HTML Element                             |
      | --------------- | ------------------------------------- | ---------------------------------------- |
      | **Type**        | JS Object                             | DOM Node                                 |
      | **Exists in**   | Virtual DOM                           | Real DOM                                 |
      | **Created by**  | `React.createElement()` or JSX        | Browser or `document.createElement()`    |
      | **Mutable?**    | ❌ No — immutable                     | ✅ Yes — mutable                        |
      | **Performance** | Efficient (batch updates via diffing) | Slower when directly modified repeatedly |
      | **Purpose**     | Describe what UI should look like     | Rendered UI on screen                    |

   - **Visualization**
      JSX (developer writes)
         ↓
      React.createElement()
         ↓
      React Element (JS object)
         ↓
      Virtual DOM
         ↓
      React DOM reconciler
         ↓
      Real HTML Element (browser renders)



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

---

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

   

     

---

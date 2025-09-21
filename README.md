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

**Q1. What is the difference between block, inline, and inline-block elements?**  
<details>
<summary>Show Answer</summary>

- Block: Takes full width (`<div>`, `<p>`, `<h1>`).  
- Inline: Takes only needed space (`<span>`, `<a>`).  
- Inline-block: Behaves like inline but supports width/height.  

</details>

**Q2. What are semantic HTML tags? Why are they important?**  
<details>
<summary>Show Answer</summary>

- Tags that describe meaning, not just presentation (`<header>`, `<article>`, `<footer>`).  
- Improves accessibility & SEO.  

</details>

**Q3. Difference between `id` and `class` in HTML?**  
<details>
<summary>Show Answer</summary>

- `id`: Unique identifier (used once per page).  
- `class`: Can be reused for multiple elements.  

</details>

---

## 🔵 CSS

**Q1. Difference between relative, absolute, fixed, and sticky positioning?**  
<details>
<summary>Show Answer</summary>

- Relative: Positioned relative to itself.  
- Absolute: Positioned relative to nearest positioned ancestor.  
- Fixed: Always stays at the same place (relative to viewport).  
- Sticky: Switches between relative & fixed depending on scroll.  

</details>

**Q2. What is the difference between inline, internal, and external CSS?**  
<details>
<summary>Show Answer</summary>

- Inline: Inside the element (`style=""`).  
- Internal: Inside `<style>` tag.  
- External: In a separate `.css` file.  

</details>

**Q3. Explain the difference between `em`, `rem`, `%`, and `px` in CSS.**  
<details>
<summary>Show Answer</summary>

- `px`: Fixed pixels.  
- `em`: Relative to parent font-size.  
- `rem`: Relative to root (`html`) font-size.  
- `%`: Relative to parent container.  

</details>

---

## 🟡 JavaScript

**Q1. Difference between `var`, `let`, and `const`?**  
<details>
<summary>Show Answer</summary>

- `var`: Function-scoped, hoisted, can be redeclared.  
- `let`: Block-scoped, hoisted but not initialized, can be reassigned.  
- `const`: Block-scoped, cannot be reassigned.  

</details>

**Q2. What is hoisting in JavaScript?**  
<details>
<summary>Show Answer</summary>

- JavaScript moves variable & function declarations to the top of scope before execution.  

</details>

**Q3. Difference between `==` and `===`?**  
<details>
<summary>Show Answer</summary>

- `==`: Compares values after type conversion (loose equality).  
- `===`: Compares both value & type (strict equality).  

</details>

**Q4. Explain closures in JavaScript.**  
<details>
<summary>Show Answer</summary>

- A closure is when a function remembers its lexical scope even if executed outside of it.  

</details>

---

## 🟢 React

**Q1. What is the difference between functional and class components?**  
<details>
<summary>Show Answer</summary>

- Class: Uses `this`, lifecycle methods.  
- Functional: Uses hooks (`useState`, `useEffect`), simpler syntax.  

</details>

**Q2. What is the difference between `useMemo`, `useCallback`, and `React.memo`?**  
<details>
<summary>Show Answer</summary>

- `useMemo`: Memoizes a **calculated value**.  
- `useCallback`: Memoizes a **function** reference.  
- `React.memo`: Memoizes a **whole component** to avoid re-renders.  

</details>

**Q3. What is the difference between client and server components in Next.js?**  
<details>
<summary>Show Answer</summary>

- Client: Run in browser, can use state/effects.  
- Server: Rendered on server, better performance, can fetch data directly.  

</details>

**Q4. Explain SSR, SSG, and ISR in Next.js.**  
<details>
<summary>Show Answer</summary>

- SSR: Rendered on request.  
- SSG: Rendered at build time.  
- ISR: Rebuilds pages after interval.  

</details>

---

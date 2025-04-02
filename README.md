# Interview Preparation: Frontend Engineering Topics

This document outlines key topics and concepts for preparing for a Frontend Engineering interview, focusing on **JavaScript Fundamentals**, **React Core Concepts**, and **Other Must-Know Frontend Topics**. Use this as a guide to deepen your understanding and practice.

---

## JavaScript Fundamentals

### 1. [Core Concepts](https://medium.com/@charaneie22/core-concepts-of-javascript-57c1901ca41e)
[(https://medium.com/@charaneie22/core-concepts-of-javascript-57c1901ca41e)]((https://medium.com/@charaneie22/core-concepts-of-javascript-57c1901ca41e)) - 
- **Hoisting**: Variable/function declarations are moved to the top of their scope.
  - `var` is hoisted and initialized to `undefined`.
  - `let`/`const` are hoisted but remain in a Temporal Dead Zone (TDZ) until declared.
  - Example: `console.log(x); var x = 5;` → `undefined`. `console.log(x); let x = 5;` → `ReferenceError`.
- **Execution Context & Call Stack**: Manages code execution with scope, variables, and `this`.
  - Call stack tracks function calls (LIFO).
  - Example: `function a() { b(); } function b() { console.log('b'); } a();` → Stack: Global → `a` → `b` → unwind.
- **Scope & Closures**: Closures allow functions to retain access to outer scope variables.
  - Example: `const f = () => { let x = 1; return () => x++; }; const counter = f(); counter();` → `1`.
- **Prototypes & Prototypal Inheritance**: Objects inherit properties via the prototype chain.
  - Example: `const a = { x: 1 }; const b = Object.create(a); b.x;` → `1`.
- **Event Loop & Microtasks**: Manages async code with call stack, microtasks (e.g., Promises), and macrotasks (e.g., `setTimeout`).
  - Example: `console.log(1); Promise.resolve().then(() => console.log(2)); console.log(3);` → `1, 3, 2`.

### 2. [Functions & Objects](https://medium.com/@charaneie22/functions-objects-e68f419fc9e0)
(https://medium.com/@charaneie22/functions-objects-e68f419fc9e0)
- **Call, Apply, Bind**: Methods to control `this` and arguments.
  - `call`/`apply` invoke immediately; `bind` returns a new function.
- **Function Currying**: Transform multi-argument functions into a sequence of single-argument functions.
  - Example: `const add = a => b => a + b; add(2)(3);` → `5`.
- **First-Class & Higher-Order Functions**: Functions as values; can take/return other functions.
- **Pure Functions & Side Effects**: Pure functions have predictable outputs and no side effects.
- **Deep vs. Shallow Copy**: Shallow copies reference nested objects; deep copies duplicate all levels.

### 3. Async Programming
- **Promises & Async/Await**: Tools for handling asynchronous operations.
  - `async/await` is syntactic sugar over Promises.
- **Event Loop & Task Queue**: Microtasks (e.g., Promises) are prioritized over macrotasks (e.g., `setTimeout`).
- **Web APIs & Fetch API**: Browser APIs for async tasks (e.g., `fetch`).
- **JavaScript Engine**: V8 (Chrome) parses, compiles, and executes code.

### 4. Performance & Memory Management
- **Debouncing & Throttling**: Limit function execution rates for performance.
- **Garbage Collection**: Marks and sweeps unused objects to free memory.
- **WeakMap & WeakSet**: Use weak references for memory-efficient storage.
- **Memory Leaks**: Prevent by cleaning up (e.g., removing event listeners).

### 5. Browser & Web APIs
- **LocalStorage, SessionStorage, IndexedDB**: Client-side storage options.
- **Service Workers & Web Workers**: Enable background tasks and threading.
- **Cookies vs. Tokens vs. JWT**: Authentication mechanisms.

### 6. Advanced JavaScript Concepts
- **Polyfills**: Implement modern features for older browsers (e.g., `Array.map`).
- **ES6+ Features**: Destructuring, spread/rest operators, optional chaining (`?.`).
- **Module Systems**: ES Modules (`import`) vs. CommonJS (`require`).
- **Content Security Policy (CSP)**: Mitigate XSS attacks via HTTP headers.

---

## React Core Concepts

### 1. Fundamentals
- **Virtual DOM & Reconciliation**: Efficient DOM updates via diffing.
- **JSX & Rendering**: Syntactic sugar for `React.createElement`.
- **Class vs. Functional Components**: Hooks shifted preference to functional components.

### 2. React Hooks
- **useState, useEffect, useMemo, useCallback**: Manage state, side effects, and memoization.
- **useRef & useLayoutEffect**: Handle refs and DOM-synchronized effects.
- **Custom Hooks**: Encapsulate reusable logic.

### 3. Performance Optimization
- **Memoization**: `React.memo`, `useMemo`, `useCallback` prevent unnecessary re-renders.
- **Code Splitting & Lazy Loading**: Use `React.lazy` and `Suspense` for dynamic imports.
- **Webpack Optimization & Tree Shaking**: Reduce bundle size.
- **React Concurrent Mode**: Prioritize rendering tasks for smoother UX.

### 4. React Router
- **Dynamic & Nested Routes**: Flexible URL mapping.
- **Protected Routes**: Implement authentication guards.
- **SSR & SSG**: Server-side rendering and static site generation.

### 5. Error Handling & Debugging
- **Error Boundaries**: Catch render errors with class components.
- **React Profiler**: Measure component performance.
- **Logging**: Use tools like Sentry for error monitoring.

### 6. React Best Practices
- **Avoid Prop Drilling**: Use Context API for state sharing.
- **React Portals**: Render components outside the DOM hierarchy.
- **Suspense & Lazy Loading**: Load components asynchronously.
- **Server Components**: Leverage edge rendering (React 18+).

---

## Other Must-Know Frontend Topics

- **Web Accessibility**: Implement ARIA roles and keyboard navigation.
- **Progressive Web Apps (PWAs)**: Support offline functionality and installability.
- **WebSockets**: Enable real-time bidirectional communication.
- **Animations**: Use Framer Motion or GSAP with React.
- **Micro Frontends**: Build modular, independent app architectures.
- **CSS-in-JS**: Leverage styled-components or Emotion for styling.
- **Edge Computing & CDN Caching**: Optimize content delivery.

---

## How to Use This Guide
1. **Review Concepts**: Start with JavaScript fundamentals, then move to React and broader frontend topics.
2. **Practice Examples**: Code the provided examples to solidify understanding.
3. **Explore Further**: Research advanced topics (e.g., Concurrent Mode, Micro Frontends) for deeper mastery.
4. **Mock Interviews**: Test your knowledge with peers or mentors.


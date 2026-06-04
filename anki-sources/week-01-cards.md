Q: What is the difference between display:flex and display:grid? When do you use each?

A: Flex is one-dimensional — use it for rows OR columns (nav, button groups, card rows). Grid is two-dimensional — use it when you need rows AND columns simultaneously (page layouts, service card grids). Rule: nav = flex, page layout = grid.

Q: What are the 12 core CSS Flexbox properties?

A: Container: display, flex-direction, flex-wrap, flex-flow, justify-content, align-items, align-content, gap. Item: flex-grow, flex-shrink, flex-basis, align-self.

Q: What does justify-content vs align-items do in Flexbox?

A: justify-content controls alignment along the MAIN axis (horizontal in row direction). align-items controls alignment along the CROSS axis (vertical in row direction). They flip when flex-direction is column.

Q: What is CSS Grid grid-template-areas and why use it?

A: Lets you name regions of a grid layout with strings and assign elements to them by name. Use it when your layout has semantically distinct regions (header, sidebar, main, footer) — much more readable than tracking row/column numbers manually.

Q: What is the difference between auto-fill and auto-fit in CSS Grid?

A: auto-fill creates as many columns as fit, keeping empty columns as placeholders. auto-fit collapses empty columns and stretches existing ones to fill the space. For responsive card grids: auto-fit + minmax() is almost always what you want.

Q: What is a CSS custom property (variable) and how do you define one?

A: Defined with -- prefix on :root. Example: :root { --primary: #0066ff; } Used with var(--primary). Useful for theming, dark mode toggle, and design tokens that need to change in one place.

Q: How does CSS dark mode toggle work with custom properties?

A: Define two sets of --color variables. On :root set light values. On [data-theme="dark"] override them. Toggle a class or attribute on html with JavaScript. Every element using var(--color) updates instantly.

Q: What is the JavaScript event loop and what is the difference between macrotask and microtask?

A: Call stack runs synchronous code. When async work completes, callbacks go into queues. Microtasks (Promise.then, queueMicrotask) run before the next macrotask. Macrotasks (setTimeout, setInterval, I/O) run one per event loop tick. Order: synchronous → all microtasks → one macrotask → all microtasks → repeat.

Q: What does Promise.all do vs Promise.allSettled?

A: Promise.all runs all promises in parallel, resolves when ALL resolve, rejects immediately if ANY reject. Promise.allSettled runs all in parallel, waits for ALL to finish regardless of success or failure, always resolves with array of {status, value/reason}. Use allSettled when you need results from all even if some fail.

Q: What does Promise.race do vs Promise.any?

A: Promise.race resolves or rejects with the FIRST promise to settle. Promise.any resolves with the FIRST promise to SUCCEED, only rejects if ALL reject. Use race for timeouts, use any for first successful response wins.

Q: What is a JavaScript closure?

A: A function that retains access to variables from its outer scope even after the outer function has finished executing. Used in event handlers, factory functions, module patterns, and anywhere you need private state.

Q: What is optional chaining (?.) and when do you use it?

A: user?.address?.city safely accesses nested properties without throwing if any level is null or undefined — returns undefined instead. Use it when accessing properties from API responses where structure is not guaranteed.

Q: What is the difference between == and === in JavaScript?

A: == does type coercion before comparing (0 == "0" is true). === compares value AND type with no coercion (0 === "0" is false). Always use === in production code.

Q: What is async/await and what does it replace?

A: Syntactic sugar over Promises. async function always returns a Promise. await pauses execution inside the async function until the Promise resolves. Replaces .then().catch() chains with synchronous-looking code that is still non-blocking. Always wrap in try/catch for error handling.

Q: What does Array.reduce() do?

A: Takes an array and reduces it to a single value by running a callback on each element with an accumulator. reduce((acc, item) => acc + item.price, 0) sums all prices. Most powerful array method — can implement map and filter using only reduce.

Q: What is the difference between Array.map() and Array.forEach()?

A: map() creates a NEW array with transformed values — use it when you need a new array. forEach() iterates and returns undefined — use it only for side effects. Never use forEach when map works.

Q: What is ES6 module syntax and how does it differ from CommonJS?

A: ES6: export const x = 1 / import { x } from './file'. CommonJS: module.exports = { x } / const { x } = require('./file'). ES6 modules are static and tree-shakeable. CommonJS is dynamic. Use ES6 in frontend.

Q: What is the Git rebase command and when do you use it vs merge?

A: git rebase main rewrites your branch's commits on top of the latest main. Creates clean linear history. Use rebase to update your feature branch. Use merge for integrating completed features. Never rebase shared branches.

Q: What is git cherry-pick?

A: Applies a specific commit from one branch to your current branch. git cherry-pick abc123 copies that one commit. Use it when you need one specific fix from another branch without merging everything else.
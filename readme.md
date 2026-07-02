# 🪜 PromiseStep

**An interactive visualizer for Promise chains, the call stack, and the JavaScript event loop.**

"PromiseStep visualizes the event loop for .then() chains, the call stack, Web APIs, the macrotask queue, and the microtask queue in inspectable steps so you can watch it happen instead of just trusting that it does. ⚙️

## ✨ What it shows

- 🪜 **The Promise ladder** — a bird's-eye view of the `.then()` chain, lighting up as each rung resolves
- 📚 **Call Stack** — synchronous execution, frame by frame, LIFO
- ⏱️ **Web APIs panel** — timers sitting outside the engine, waiting to fire
- 📥 **Macrotask / Callback Queue** — where `setTimeout` callbacks actually land when their timer completes
- 🔮 **Microtask Queue** — where `.then()` continuations go once a promise resolves, and why they always jump the line ahead of the next macrotask
- 🖥️ **Terminal output** — logs appear exactly when the real `console.log` call would run, not before

## 🧩 The core idea

> A `setTimeout` callback is a **macrotask**.
> A `.then()` continuation is a **microtask**.
> The event loop always fully drains the microtask queue before it touches the next macrotask.

That one rule explains almost every "wait, why did that log *before* the other one?" moment in async JavaScript. PromiseStep separates the two queues visually so the distinction stops being a rule you memorize and starts being something you can just *see*. 🔍


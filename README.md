# 🧮 Calculator

A clean, minimal browser-based calculator built with HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies.

---

## ✨ Features

- **Four core operations** — addition, subtract, multiply, divide
- **Chained calculations** — entering a second operator evaluates the previous pair first
- **Division by zero protection** — displays a friendly error instead of crashing
- **Floating point rounding** — results are rounded to avoid display overflow
- **Fresh start after result** — typing a new digit after `=` begins a new calculation
- **Clear button** — resets all state completely

---

## 🚀 Live Demo

> Open `calculator.html` directly in any browser — no build step, no server needed.

---

## 📁 Project Structure

```
calculator/
├── calculator.html   # All HTML, CSS, and JS in one file
└── README.md
```

---

## 🛠️ How It Works

The logic is built around four pure math functions:

```js
function add(a, b)      { return a + b; }
function subtract(a, b) { return a - b; }
function multiply(a, b) { return a * b; }
function divide(a, b)   { return a / b; }
```

An `operate()` dispatcher routes to the right function based on the selected operator:

```js
function operate(op, a, b) {
  if (op === '+') return add(a, b);
  if (op === '-') return subtract(a, b);
  if (op === '*') return multiply(a, b);
  if (op === '/') return divide(a, b);
}
```

State is tracked with three variables:

| Variable    | Purpose                              |
|-------------|--------------------------------------|
| `firstNum`  | The first number entered             |
| `operator`  | The selected operator (`+`, `-`, etc.) |
| `currentStr`| What's currently shown on the display |

---

## 🔢 Usage

1. Click a number to start entering the first value
2. Click an operator (`+`, `−`, `×`, `÷`)
3. Enter a second number
4. Press `=` to see the result

**Chaining example:**

```
12  →  +  →  7  →  −   (evaluates 12 + 7 = 19 automatically)
 1  →  =                (evaluates 19 − 1 = 18)
```

---

## 🧱 Built With

- HTML5
- CSS3 (Grid layout)
- Vanilla JavaScript (ES6)

---

## 📌 Part of

[The Odin Project](https://www.theodinproject.com/) — Foundations curriculum

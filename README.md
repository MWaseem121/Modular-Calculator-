<p align="center"><img src="logo-512.png" width="110" alt="Modular Calculator logo"></p>

<h1 align="center">Modular Calculator</h1>
<p align="center">A clean calculator app with add, subtract, multiply and divide, built from small single-purpose functions. One HTML file, no install.</p>

## Features

- Four operations as separate functions: `add`, `subtract`, `multiply`, `divide`.
- `divide` raises an error on zero, and the app shows a clear message instead of crashing.
- Input checks: a wrong value turns the field red and says which one to fix.
- History of the last 10 calculations, saved in the browser.
- Colour themes: six accent colours (Violet, Blue, Teal, Rose, Orange, Green) and Auto / Light / Dark appearance. Your choice is remembered.
- Keyboard: press 1 to 4 to choose an operation, Enter to calculate.
- Results like `0.1 + 0.2` show `0.3`, not `0.30000000000000004`.

## Design

Operations live in one table, so adding a new one is a single line:

```js
var OPERATIONS = {
  "1": { sym: "+", name: "Add",      fn: add },
  "2": { sym: "−", name: "Subtract", fn: subtract },
  "3": { sym: "×", name: "Multiply", fn: multiply },
  "4": { sym: "÷", name: "Divide",   fn: divide }
};
```

This is the same structure as the Python version of the project (`OPERATIONS` dictionary, one function per operation, `ZeroDivisionError` for division by zero).

## Run it

Open `index.html` in a browser. To put it online with GitHub Pages: Settings, Pages, Deploy from a branch, `main`, `/ (root)`.

## Screenshots

| Light, violet | Dark, rose | Light, teal |
|---|---|---|
| ![Light violet](screenshots/light-violet.png) | ![Dark rose](screenshots/dark-rose.png) | ![Light teal](screenshots/light-teal.png) |

## Files

```
index.html     the whole app (HTML, CSS, JavaScript)
logo.svg       logo (vector)
logo-512.png   logo (image)
screenshots/   images used in this README
```

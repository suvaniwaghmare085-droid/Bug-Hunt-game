https://suvaniwaghmare085-droid.github.io/Bug-Hunt-game/bug-hunt-game.html

# 🐛 Bug Hunt — Debug Challenge Game

A fast-paced browser-based game where you spot and fix bugs across **6 programming languages** — all in a single HTML file with zero dependencies.

![Game Preview](https://img.shields.io/badge/languages-6-7c6ef5?style=flat-square) ![Questions](https://img.shields.io/badge/questions-15-4ade80?style=flat-square) ![Dependencies](https://img.shields.io/badge/dependencies-zero-22d3ee?style=flat-square) ![File Size](https://img.shields.io/badge/size-single%20HTML%20file-fbbf24?style=flat-square)

---

## 🎮 Demo

> **Play it live →** https://suvaniwaghmare085-droid.github.io/bug-hunt/bug-hunt-game.html


## 📸 What It Looks Like

```
┌─────────────────────────────────────────────────┐
│  🐛 Bug Hunt              Score: 120  Streak: 3🔥  │
├─────────────────────────────────────────────────┤
│  [JavaScript]  [Medium]   Closure in a loop      │
│  ──────────────────────────────────── ⏱ 18s      │
│                                                   │
│  const funcs = [];                                │
│ ▶ for (var i = 0; i < 3; i++) {   ← bug here     │
│    funcs.push(function() {                        │
│      console.log(i);                              │
│    });                                            │
│  }                                                │
│                                                   │
│  [ for (let i = 0; i < 3; i++) ]  [ for (const.. ]│
│  [ for (var i = 0; i <= 3; i++) ] [ var i; for.. ]│
└─────────────────────────────────────────────────┘
```

---

## ✨ Features

- **15 hand-crafted bugs** across real-world scenarios — not trivial typos
- **6 programming languages** — JavaScript, Python, Java, C++, TypeScript, Ruby
- **3 difficulty tiers** — Easy (10 pts), Medium (20 pts), Hard (30 pts)
- **25-second countdown timer** per question with color-shifting urgency bar
- **Time bonus** — faster answers earn extra points
- **Streak multiplier** — 3+ correct answers in a row gives 1.5× points
- **Hint system** — costs 5 pts, reveals the bug category
- **3 lives** — lose one for each wrong answer or timeout
- **Final score screen** — accuracy rating, best streak, and a ranked title
- **Zero dependencies** — one HTML file, works offline

---

## 🚀 Quick Start

### Option 1 — Open locally
Just download `bug-hunt-game.html` and open it in any browser. No server needed.

```bash
git clone https://github.com/yourusername/bug-hunt.git
cd bug-hunt
open bug-hunt-game.html   # macOS
# or double-click the file in your file explorer
```

### Option 2 — Serve locally
```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000/bug-hunt-game.html
```

---

## 🌐 Hosting on GitHub Pages

1. **Fork or push** this repo to your GitHub account
2. Go to your repo → **Settings** → **Pages**
3. Under *Source*, select **Deploy from a branch**
4. Choose **main** branch → **/ (root)** → click **Save**
5. Wait ~60 seconds, then visit:

```
https://yourusername.github.io/bug-hunt/bug-hunt-game.html
```

That's it — no build step, no CI pipeline.

---

## 🧩 Bug Categories Covered

| Language | Bugs Included |
|----------|--------------|
| JavaScript | Off-by-one loop, assignment vs comparison, closure/`var` scope, floating point comparison |
| Python | Mutable default argument, wrong indentation, list mutation during iteration |
| Java | Null pointer dereference, `==` string comparison |
| TypeScript | Missing optional chaining (`?.`), missing `await` in async function |
| C++ | Memory leak (missing `delete[]`), integer overflow |
| Ruby | Frozen string mutation |

---

## 🏆 Scoring

| Action | Points |
|--------|--------|
| Correct answer (Easy) | +10 |
| Correct answer (Medium) | +20 |
| Correct answer (Hard) | +30 |
| Time bonus | +0 to +10 (based on speed) |
| Streak multiplier (3+) | ×1.5 |
| Used hint | −5 (deducted from earned points) |
| Wrong answer / timeout | −1 life |

### Rank Titles

| Accuracy | Title |
|----------|-------|
| ≥ 90% | 🏆 Bug Slayer |
| ≥ 70% | 🎯 Sharp Eye |
| ≥ 50% | 🔧 Getting There |
| < 50% | 🐛 The Bugs Won |

---

## 🗂 Project Structure

```
bug-hunt/
├── bug-hunt-game.html   # The entire game — HTML + CSS + JS in one file
└── README.md
```

Everything lives in a single self-contained file. No frameworks, no build tools, no `node_modules`.

---

## 🛠 Adding Your Own Questions

Open `bug-hunt-game.html` and find the `QUESTIONS` array near the top of the `<script>` block. Each question follows this shape:

```javascript
{
  lang: "js",                    // badge style: js | py | java | cpp | ts | ruby
  langLabel: "JavaScript",       // display name
  diff: "medium",                // easy | medium | hard
  title: "Your bug title",
  code: `function foo() {\n  // your buggy code here\n}`,
  bugLine: 1,                    // 0-indexed line to highlight in red
  hint: "A helpful clue.",
  options: [
    { text: `the correct fix`, correct: true  },
    { text: `wrong option 1`,  correct: false },
    { text: `wrong option 2`,  correct: false },
    { text: `wrong option 3`,  correct: false },
  ],
  explanation: "Why the fix works — shown after answering."
}
```

Options are automatically shuffled each round, so order doesn't matter.

---

## 🤝 Contributing

Pull requests are welcome! Ideas for contributions:

- New bug questions in any language
- Additional language support (Go, Rust, SQL, Bash...)
- High score persistence using `localStorage`
- Shareable result cards
- Difficulty filter on the start screen

Please keep new questions focused on **real-world bugs** that developers actually encounter — not contrived syntax errors.

---



<p align="center">Made with 🐛 and too much debugging experience</p>

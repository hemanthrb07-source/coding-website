# AlgoQuest – Game-Based Coding Website (GitHub Compatible)

## Overview

AlgoQuest is a browser-based coding platform that transforms Data Structures and Algorithms (DSA) practice into a game experience. It is designed to run entirely as a static website using HTML, CSS, JavaScript, and in-browser Python execution via Pyodide.

This version is optimized for deployment on GitHub Pages, meaning no backend server or database is required.

---

## Core Features

### 1. Game-Based Learning

* Players solve coding problems to gain XP
* Level progression system
* Health system (penalty for incorrect solutions)
* “Attack = run code” mechanic

### 2. DSA Problem System

* Multiple problems with:

  * Title
  * Description
  * Difficulty (Easy, Medium, Advanced)
* Test case validation
* Immediate feedback (Success / Fail)

### 3. Hacker-Style UI

* Black background
* Green monospace text
* Terminal-like interface

### 4. In-Browser Python Execution

* Powered by Pyodide
* No backend required
* Runs entirely in the user’s browser

---

## Technology Stack

| Layer          | Technology                  |
| -------------- | --------------------------- |
| Frontend       | HTML, CSS, JavaScript       |
| Code Execution | Pyodide (Python in browser) |
| Hosting        | GitHub Pages                |

---

## Project Structure

```
algoquest/
 ├── index.html     → Main website UI
 ├── style.css      → Hacker theme styling
 └── script.js      → Game logic + DSA engine
```

---

## How It Works

### 1. Problem Selection

User selects a problem from dropdown.

### 2. Code Execution

* User writes Python code
* Code is executed using Pyodide
* Output is captured

### 3. Evaluation

* Output compared with expected test cases
* Determines success or failure

### 4. Game Update

* Success:

  * XP increases
  * Health increases
* Failure:

  * Health decreases

### 5. Level System

* Level increases when XP threshold is reached

---

## Game Mechanics

| Action           | Effect                            |
| ---------------- | --------------------------------- |
| Correct solution | Gain XP + health                  |
| Wrong solution   | Lose health                       |
| Level up         | Reset health, increase difficulty |

---

## Sample Problem Format

```javascript
{
  id: 1,
  title: "Sum of Two Numbers",
  difficulty: "easy",
  xp: 10,
  description: "Input two numbers and print sum",
  tests: [
    { input: [2, 3], output: 5 }
  ]
}
```

---

## Deployment (GitHub Pages)

### Steps:

1. Create repository on GitHub
2. Upload files:

   * index.html
   * style.css
   * script.js
3. Go to:
   Settings → Pages
4. Select:
   Branch: main
5. Save

Your site will be live at:

```
https://your-username.github.io/repo-name/
```

---

## Limitations

This version is intentionally simplified:

* No backend server
* No database (data resets on refresh)
* No secure sandbox (runs locally in browser)
* Limited Python execution capabilities
* No authentication or leaderboard

---

## Future Improvements

### Backend Integration

* Node.js + Express API
* PostgreSQL database
* Redis leaderboard

### Security

* Docker sandbox for code execution
* Timeout and memory limits

### Features

* Multiplayer battles
* AI hints
* DSA visualization (graphs, trees)
* Skill progression tree

---

## Conclusion

AlgoQuest demonstrates how a coding platform can be gamified using only frontend technologies and deployed entirely on GitHub Pages. While not production-ready, it provides a strong foundation for building a full-scale coding platform.

---

# quiz-cli

An interactive command-line quiz game for learning JavaScript, Node.js fundamentals, and general programming concepts.

## Description

`quiz-cli` is a Node.js terminal application that lets users choose a category, answer multiple-choice questions, and review their results at the end of each session.

The project is built with built-in Node.js modules, ES modules, and ANSI terminal colors, so it runs without third-party dependencies.

## Features

- Interactive terminal-based quiz flow
- Multiple quiz categories
- Selectable question count per round
- Randomized question order
- Immediate feedback for correct and incorrect answers
- Final score summary with performance messaging
- Review of missed questions
- Colorized terminal output

## Technologies Used

- Node.js 18+
- ES Modules
- Built-in `readline` module
- Built-in `fs/promises` module
- Built-in `path` and `url` utilities
- JSON for quiz data storage

## Installation

### Prerequisites

- Node.js `>=18.0.0`
- npm

### Steps

```bash
git clone <repository-url>
cd test-app
npm install
```

> No external dependencies are listed in `package.json`, but running `npm install` keeps the project ready for standard Node.js workflows.

## How to Run

Start the quiz with:

```bash
npm start
```

Or run the entry file directly:

```bash
node index.js
```

## Usage

When the application starts, you will be prompted to:

1. Choose a category
2. Choose how many questions to answer
3. Answer each multiple-choice question
4. Review your score and any missed questions
5. Decide whether to play again

### Example Terminal Flow

```text
Choose a category:
1. JavaScript Basics
2. Node.js Fundamentals
3. General Programming

How many questions?
1. All questions
2. 3 questions
3. 5 questions

Your choice (enter number):
```

### Example Output

```text
✓ Correct!
```

```text
✗ Incorrect!
The correct answer was: push()
```

## Project Structure

```text
.
├── README.md
├── colors.js
├── index.js
├── input.js
├── package.json
├── questions.json
└── quiz.js
```

### File Overview

- `index.js` - application entry point and main game loop
- `quiz.js` - quiz logic, scoring, progress, and results
- `input.js` - helper functions for terminal input
- `colors.js` - ANSI color utilities for terminal output
- `questions.json` - quiz categories and questions
- `package.json` - project metadata and npm scripts

## Scripts

- `npm start` - runs the quiz application
- `npm test` - runs Node.js tests via `node --test`

## Testing

```bash
npm test
```

> No test files were included in the repository listing.

## Notes

- The project does not expose an HTTP API.
- Quiz content is stored in `questions.json` and should keep the same structure if edited.
- The app is designed for learning and practice in the terminal.

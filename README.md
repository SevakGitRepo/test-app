# quiz-cli

An interactive command-line quiz game for learning JavaScript, Node.js fundamentals, and general programming concepts.

## Project Overview

This repository contains a Node.js CLI application that lets users choose a quiz category, answer multiple-choice questions, and review results at the end of each game session.

The app uses built-in Node.js modules, ES modules, and terminal color formatting to provide a simple interactive experience without external dependencies.

## Features

- Interactive terminal-based quiz flow
- Category selection before starting a quiz
- Configurable question count selection
- Randomized question order
- Immediate feedback for correct and incorrect answers
- Final score summary with performance message
- Review of missed questions after the quiz
- ANSI color output for improved readability

## Technologies Used

- Node.js
- ES Modules
- Built-in `readline` module for input handling
- Built-in `fs/promises` for reading quiz data
- Built-in `path` and `url` utilities
- JSON for quiz question storage

## Project Structure

Current repository files detected:

```text
.
├── colors.js
├── index.js
├── input.js
├── package.json
├── questions.json
├── quiz.js
```

### File Roles

- `index.js` - application entry point and main quiz loop
- `quiz.js` - quiz logic, scoring, progress, and result display
- `input.js` - terminal input helpers (`select`, `confirm`, `pressEnter`)
- `colors.js` - ANSI terminal color utilities
- `questions.json` - quiz content and category data
- `package.json` - project metadata and npm scripts

## Prerequisites

- Node.js `>=18.0.0`
- npm (bundled with Node.js)

## Installation Instructions

1. Clone the repository:

```bash
git clone <repository-url>
cd test-app
```

2. Install dependencies:

```bash
npm install
```

> Information not detected from repository: no external dependencies are listed in `package.json`, but running `npm install` will still prepare the project for standard Node.js workflows.

## Setup Instructions

The application reads quiz data from `questions.json` and uses ES module imports.

Detected quiz data structure:

- `categories`
- each category has:
  - `name`
  - `questions[]`
- each question includes:
  - `question`
  - `options[]`
  - `answer`
  - optional `explanation`

If you edit `questions.json`, keep the same structure so the quiz can load correctly.

## Build Instructions

No build step is detected.

The application runs directly with Node.js.

## Run Instructions

Start the application with:

```bash
npm start
```

Or run the entry file directly:

```bash
node index.js
```

### What Happens at Runtime

1. The app loads quiz questions from the JSON file
2. The user selects a quiz category
3. The user chooses how many questions to answer
4. Questions are presented one by one in the terminal
5. Answers are validated immediately
6. A final score and review section are displayed
7. The user can choose to play again

## Docker Usage

Information not detected from repository.

## Environment Variables

Information not detected from repository.

## API Usage Examples

Information not detected from repository.

This project does not expose an HTTP API. It is a local CLI application.

## Example Usage

### Start the quiz

```bash
npm start
```

### Typical interaction flow

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

## Example Requests/Responses

This project is interactive rather than request/response based.

Example terminal response after answering a question:

```text
✓ Correct!
```

Or for an incorrect answer:

```text
✗ Incorrect!
The correct answer was: push()
```

## Testing Instructions

The `package.json` file includes a test script:

```bash
npm test
```

This runs Node.js built-in tests via:

```bash
node --test
```

Information not detected from repository: no test files were included in the repository listing.

## Configuration Details

### Package metadata

- Package name: `quiz-cli`
- Version: `1.0.0`
- License: `MIT`
- Module type: `module`
- Main entry point: `index.js`

### Scripts

- `npm start` - runs `node index.js`
- `npm test` - runs `node --test`

### Runtime behavior

- Questions are loaded from a JSON file at startup
- Questions are shuffled before each quiz session
- Progress is shown during each quiz
- Results include score percentage and review of incorrect answers

## Additional Notes

- The repository appears to be a learning-focused CLI project with no third-party dependencies.
- The code uses built-in Node.js modules and ANSI escape codes for terminal styling.
- If you reorganize files into `src/` or `data/` directories, update the import paths and question file path in `index.js` accordingly.
- Information not detected from repository: no CI, Docker, or deployment configuration files were present in the repository listing.

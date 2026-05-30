# quiz-cli

An interactive command-line quiz game built with Node.js. It lets you choose a quiz category, select how many questions to answer, and then runs a randomized quiz with immediate feedback, progress tracking, a final score summary, and a review of missed answers.

## Features

- Interactive terminal-based quiz experience
- Category selection from `questions.json`
- Choose the number of questions to answer
- Randomized question order
- Immediate correctness feedback after each answer
- Progress display during the quiz
- Final score summary
- Review of incorrect answers with explanations
- Replay option after finishing a quiz
- No external runtime dependencies

## Prerequisites

- [Node.js](https://nodejs.org/) **18 or later**

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/SevakGitRepo/test-app.git
cd test-app
npm install
```

> This project does not rely on external runtime packages, but running `npm install` will prepare the local project environment and create a lockfile if needed.

## Usage

Start the quiz application:

```bash
npm start
```

Or run the entry file directly:

```bash
node index.js
```

## How It Works

When you start the app, it will:

1. Display a welcome banner
2. Load quiz data from `questions.json`
3. Let you pick a category
4. Let you choose how many questions to answer
5. Present questions one at a time
6. Show feedback immediately after each answer
7. Display your final score and a review of incorrect answers
8. Offer the option to replay the quiz

## Project Structure

```text
.
├── colors.js
├── index.js
├── input.js
├── package.json
├── questions.json
├── quiz.js
└── README.md
```

### File Overview

- **`index.js`** — CLI entry point and application flow
- **`quiz.js`** — Quiz class, scoring, progress tracking, shuffling, and results review
- **`input.js`** — Terminal input helpers built on top of `readline`
- **`colors.js`** — ANSI color utilities for formatted terminal output
- **`questions.json`** — Quiz categories, questions, answer indices, and explanations
- **`package.json`** — Project metadata and npm scripts

## Quiz Data Format

Quiz content is stored in `questions.json`. Each category contains a list of questions with:

- the question text
- multiple-choice options
- the index of the correct answer
- an explanation shown after answering

### Customization Notes

You can extend the quiz by editing `questions.json`:

- Add new categories
- Add more questions to existing categories
- Update answer options
- Provide clearer explanations for each correct answer

Keep the structure consistent so the CLI can load and present the quiz data correctly.

## Scripts

```bash
npm start   # Run the quiz CLI
npm test    # Run the test suite
```

## Testing

Run the built-in test suite with Node’s test runner:

```bash
npm test
```

## Technologies Used

- **Node.js**
- **JavaScript (ES modules)**
- **Built-in `readline`**
- **Built-in Node test runner**

## Contributing

Contributions are welcome.

If you'd like to improve the quiz experience, consider:

- adding more categories and questions
- improving terminal styling
- expanding test coverage
- refining question explanations

## License

Add the appropriate license for this project here.

If no license has been chosen yet, consider adding one before publishing or accepting contributions.

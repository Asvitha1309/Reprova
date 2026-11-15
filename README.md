# Reprova: AI Bug Reproducer

> Turn a vague bug complaint into exact reproduction steps, a video, and a ready-to-run Playwright script, automatically.

## The Problem

When real users hit a glitch on a website, their bug reports usually look like this:

> "The checkout page is broken!"

They never say which buttons they clicked, which browser they used, or what data they typed. Developers then waste hours playing detective, clicking around and guessing how the user managed to break the site.

## Our Solution

Reprova is an AI-powered QA (Quality Assurance) agent that does this detective work for you. Give it a messy, vague bug report, and it figures out how to break the website, records the evidence, and writes the test code that proves it.

## How It Works

1. **Human input**: A user or developer submits a vague bug report.
2. **AI detective (Stagehand)**: An LLM reads the report, opens the target website, and acts like a human tester. Instead of relying on rigid, hidden selectors, it "looks" at the page and uses human-like commands to explore, fill in forms, and deliberately try to trigger the error.
3. **Cloud environment (Browserbase)**: All of this runs in a secure, automated browser in the cloud, not on a personal laptop. The cloud browser tracks network failures and hidden console errors, and records a video of the screen.

```
Vague bug report
      |
      v
  AI agent (Stagehand + LLM)
      |
      v
  Cloud browser (Browserbase)  --> explores, clicks, types, triggers the bug
      |
      v
  Bug Fix Package
```

## What It Outputs: the "Bug Fix Package"

When the AI successfully recreates the crash, developers receive:

| Output | Description |
|---|---|
| **Precise steps** | A clear, step-by-step log of what the AI did (e.g. 1. Logged in, 2. Added item to cart, 3. Applied promo code, 4. Page crashed). |
| **Video recording** | A replay of the cloud browser showing the exact moment the page broke. |
| **Ready-to-run code** | A Playwright script that recreates the bug instantly. Copy, paste, run. |

## Tech Stack

- **Stagehand**: AI browser automation framework (LLM-driven actions)
- **Browserbase**: Cloud browser infrastructure with session recording
- **Playwright**: Generated reproduction scripts
- **LLM**: Interprets the report and decides what to do on the page

## Getting Started

> Fill in the details below to match your actual setup.

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd <your-repo-folder>

# 2. Install dependencies
npm install

# 3. Add your API keys to a .env file
BROWSERBASE_API_KEY=your_key_here
BROWSERBASE_PROJECT_ID=your_project_id_here
LLM_API_KEY=your_key_here

# 4. Run the agent
npm start
```

## Usage

1. Open the app and paste in a bug report, e.g. `"The checkout page is broken!"`.
2. Enter the URL of the website to test.
3. Let the agent explore and try to reproduce the bug.
4. Download the Bug Fix Package (steps, video, Playwright script).

## Why This Project Matters

- **It solves a real problem.** Every tech company struggles with reproducing bugs, and automating it saves time and money.
- **It uses an AI agent, not just a chatbot.** The AI takes actions, controls tools, and completes a real task on the web.
- **It reflects real-world workflows.** It combines cloud infrastructure, QA practice, and applied AI.

## Team

Built by first-year CSE students at CIT Chennai.

- Asvitha K ([GitHub](https://github.com/Asvitha1309) | [LinkedIn](https://www.linkedin.com/in/asvitha-k-4a893841b/))
- _Add teammates here_

## License

_Add a license (e.g. MIT) here._

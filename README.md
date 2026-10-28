# SubSlash India ⚔️

An AI-powered dark pattern detector for Indian consumers, based on the 13 dark patterns listed in the CCPA's Guidelines for Prevention and Regulation of Dark Patterns, 2023.

Describe what an app or website did to you (a donation added to your cart, a free trial you couldn't cancel, a fee that appeared at the last step) and SubSlash tells you which dark patterns it matches, quotes the evidence, and suggests a fairer design.

**Live demo:** https://dreamy-alpaca-a5d9e7.netlify.app

## How it works

1. You describe the experience in plain language.
2. The text is sent to a free LLM through the OpenRouter API, with a prompt that limits answers to the 13 CCPA patterns and asks for evidence and a fix.
3. The result is shown with a risk score, the matching CCPA Annexure 1 item, the evidence, and a fairer alternative.
4. If the AI is unavailable or rate-limited, a built-in rule check (regex-based) runs instead, so the app still gives an answer.

## Tech

- Single-file front end: HTML, CSS and vanilla JavaScript (`index.html`)
- OpenRouter API for the AI analysis (free models, with automatic fallback)
- Hosted on Netlify

## Run it yourself

1. Clone the repo.
2. Open `index.html` and replace `PASTE_YOUR_KEY_HERE` with your own OpenRouter key, or paste a key into the box on the page.
3. Open the file in a browser.

Never commit a real API key.

## How this was built

Built during the hackathon on 28 October 2026. The idea, the focus on CCPA 2023, the testing and the deployment were done by me. I used Claude (Anthropic's AI assistant) to help write and debug the code, including fixing a broken multi-file setup, replacing OpenRouter free models that had been removed, and adding the loading animation.

## Limitations

SubSlash is a decision aid, not legal advice. Free AI models can be slow, rate-limited, or wrong, and the rule-based fallback only catches common wording.

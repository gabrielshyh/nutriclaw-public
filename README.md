<!-- NutriClaw Public README -->
<!-- Formatted following marklovestech GitHub repository layout -->

<div align="center">

# NutriClaw

**An AI medical nutrition concierge that reads menu photos and tailors meal recommendations to your specific health profile.**

![platform](https://img.shields.io/badge/platform-Node.js-lightgrey)
![language](https://img.shields.io/badge/JavaScript-ES6%2B-yellow)
![ai](https://img.shields.io/badge/AI-ReAct%20Agent-purple)
![ocr](https://img.shields.io/badge/OCR-Google%20Vision-blue)
![status](https://img.shields.io/badge/status-active-brightgreen)

</div>

---

## What it does

Dining out with chronic health conditions like Type 2 Diabetes or High Cholesterol is a constant challenge filled with hidden sugars, refined carbohydrates, and saturated fats. Traditional nutrition tracking tools require tedious manual entry and lack clinical context when evaluating complex restaurant menus.

NutriClaw is an AI nutrition agent that uses a ReAct (Reasoning + Acting) execution loop to analyze restaurant menus against user health profiles. It retrieves personalized dietary restrictions, reads paper menu photos via Google Vision OCR, and evaluates candidate dishes against strict clinical rules—delivering actionable, health-focused ordering advice in real time.

## Highlights

- **ReAct Agent Orchestration.** Autonomous multi-step reasoning loop combining tool selection, execution, and contextual decision-making.
- **Vision OCR Menu Extraction.** Converts photos of paper restaurant menus into structured text using computer vision.
- **Clinical Rule Engine.** Strict evaluation protocols enforcing glycemic index rules for Type 2 Diabetes and saturated fat limits for High Cholesterol.
- **Structured Actionable Advice.** Outputs three clear categories for every menu: 🟢 **BEST PICK** (safe, high-fiber, lean protein options), 🟡 **MODIFICATION TIP** (actionable waiter requests like sauce on the side), and 🔴 **ITEMS TO AVOID** (high saturated fat or refined carb risks).

## Unique Innovation: Clinical ReAct Execution Loop

Unlike generic chatbots that produce broad, unverified advice, NutriClaw enforces a deterministic two-phase reasoning loop:

1. **Context Retrieval:** Before analyzing a single dish, the agent calls `GetUserHealthProfile` to retrieve the user's specific clinical thresholds (e.g. Type 2 Diabetes & High Cholesterol limits).
2. **Vision Text Parsing:** Next, the agent executes `ExtractTextFromMenuPhoto` to read physical menu images via Google Vision OCR.
3. **Clinical Evaluation:** Finally, every dish is benchmarked against medical rules to output structured, prioritized recommendations with explicit medical rationales.

## Tech Stack

| Layer | Technology |
|---|---|
| **Agent Engine** | JavaScript (ES Modules), ReAct Execution Loop |
| **Vision & AI** | Google Cloud Vision OCR, OpenAI / Gemini Function Schemas |
| **Tool Architecture** | Functional Tool Registry (`GetUserHealthProfile`, `ExtractTextFromMenuPhoto`) |

## Why the source is private

This repo is a public-facing description of a working application. The full implementation lives in a private repository. If you are a collaborator, recruiter, or fellow builder who would like a deeper look into the codebase—please reach out below.

## Contact

**Gabriel Shyh** — [@gabrielshyh](https://github.com/gabrielshyh) · [gabrielsshyh2006@gmail.com](mailto:gabrielsshyh2006@gmail.com)
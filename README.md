<!-- NutriClaw Public README -->
<!-- Formatted following marklovestech GitHub repository layout -->

<div align="center">

# NutriClaw

**An AI medical nutrition concierge that analyzes restaurant menus and tailors meal recommendations to your specific health profile.**

![platform](https://img.shields.io/badge/platform-Slack%20%7C%20OpenClaw-lightgrey)
![framework](https://img.shields.io/badge/framework-OpenClaw-blue)
![ai](https://img.shields.io/badge/AI-OpenAI-green)
![status](https://img.shields.io/badge/status-active%20development-yellow)

</div>

---

## What it does

Eating well at restaurants is hard for anyone who cares about their nutrition and health. Menus rarely show what's actually in a dish, like hidden sugars, refined carbohydrates, or saturated fats, which makes it difficult to order in line with your goals. That holds whether you're managing a condition like Type 2 Diabetes or High Cholesterol, working toward a fitness goal, or simply trying to eat healthier. Traditional nutrition tracking tools require tedious manual entry and offer little help when you're facing a complex restaurant menu.

NutriClaw is an AI nutrition concierge built on top of the **OpenClaw** open-source agent framework. It interfaces with users directly via **Slack** (or any OpenClaw-compatible messaging frontend) and utilizes **OpenAI** models to evaluate restaurant menus against personal health limits. Whether provided with a photo of a paper menu or a web search for online restaurant menus, NutriClaw extracts dish details and checks them against clinical dietary rules—delivering actionable, health-focused ordering advice in real time.

## Highlights

- **Multi-Source Menu Intelligence.** Reads paper menu photos with **Google Cloud Vision (OCR)** and fetches online restaurant menus with real-time web search. Both are converted to clean, structured Markdown with **Docling / MarkItDown** before the LLM sees them.
- **OpenClaw Agent Architecture.** Built on the open-source OpenClaw agent foundation, supporting modular messaging channels and flexible LLM backends.
- **Slack Messaging Interface.** Custom Slack integration providing instant, natural conversational interaction (extendable to Discord, WhatsApp, Telegram, etc.).
- **Pluggable LLM Backend.** Powered by OpenAI models for menu reasoning and recommendations, with modular support for any LLM provider.
- **Clinical Rule Engine.** Enforces dietary guidelines for Type 2 Diabetes and saturated fat limits for High Cholesterol.
- **Structured Actionable Advice.** Outputs three clear categories for every menu: 🟢 **BEST PICK** (safe, high-fiber, lean protein options), 🟡 **MODIFICATION TIP** (actionable waiter requests like sauce on the side), and 🔴 **ITEMS TO AVOID** (high saturated fat or refined carb risks).

## Menu Extraction Pipeline

NutriClaw doesn't send menu photos straight to the LLM. Every menu goes through an extraction pipeline first:

```text
Paper menu photo ──► Google Cloud Vision OCR ──┐
                                               ├──► Docling / MarkItDown ──► Clean Markdown ──► LLM agent
Online menu (web page / PDF) ──────────────────┘
```

### Pipeline vs. sending the photo directly to the LLM

| | Photo → LLM directly | OCR → formatter → LLM |
|---|---|---|
| **Small print (prices, ingredients, prep notes)** | Photo is downscaled before the model reads it | OCR reads the full-resolution photo |
| **Model choice** | Vision-capable models only | Any text model, including smaller, cheaper, faster ones |
| **Multi-page menus** | Full image cost for every page | Each page costs only as much as its text |
| **Repeat lookups of the same restaurant** | Image re-processed every time | Extracted Markdown is stored and reused |
| **Debugging** | Can't see what the model read | Exact extracted text is logged and inspectable |

### Benchmarks (in progress)

Measured improvements of the OCR pipeline over sending photos directly to the LLM, tested on real restaurant menus, will be published here with the POC.

| Metric | Improvement with OCR pipeline |
|---|---|
| Dish-name extraction accuracy | TBD |
| Price extraction accuracy | TBD |
| Cost per menu | TBD |
| End-to-end latency | TBD |

## Tech Stack

| Layer | Technology |
|---|---|
| **Agent Framework** | OpenClaw Open-Source Agent Architecture |
| **Messaging Frontend** | Slack (Pluggable: Discord, Telegram, WhatsApp) |
| **LLM Engine** | OpenAI (Pluggable: Gemini, Local LLMs) |
| **Vision & Web Search** | Google Cloud Vision (OCR) + Real-Time Web Search |
| **Text Formatter** | Docling / MarkItDown (OCR and web output → structured Markdown) |

## Status

**In active development now, POC coming soon!**

## Why the source is private

This repo is a public-facing description of a working application. The full implementation lives in a private repository. If you are a collaborator, recruiter, or fellow builder who would like a deeper look into the codebase—please reach out below.

## Contact

**Gabriel Shyh** — [@gabrielshyh](https://github.com/gabrielshyh) · [gabrielsshyh2006@gmail.com](mailto:gabrielsshyh2006@gmail.com)
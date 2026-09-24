<!-- NutriClaw Public README -->
<!-- Formatted following marklovestech GitHub repository layout -->

<div align="center">

# NutriClaw

**An AI medical nutrition concierge that analyzes restaurant menus and tailors meal recommendations to your specific health profile.**

![platform](https://img.shields.io/badge/platform-Slack%20%7C%20OpenClaw-lightgrey)
![framework](https://img.shields.io/badge/framework-OpenClaw-blue)
![ai](https://img.shields.io/badge/AI-Anthropic%20Claude-purple)
![status](https://img.shields.io/badge/status-active-brightgreen)

</div>

---

## What it does

Dining out with chronic health conditions like Type 2 Diabetes or High Cholesterol is a constant challenge filled with hidden sugars, refined carbohydrates, and saturated fats. Traditional nutrition tracking tools require tedious manual entry and lack clinical context when evaluating complex restaurant menus.

NutriClaw is an AI nutrition concierge built on top of the **OpenClaw** open-source agent framework. It interfaces with users directly via **Slack** (or any OpenClaw-compatible messaging frontend) and utilizes **Anthropic LLM** (Claude) to evaluate restaurant menus against personal health limits. Whether provided with a photo of a paper menu or a web search for online restaurant menus, NutriClaw extracts dish details and checks them against clinical dietary rules—delivering actionable, health-focused ordering advice in real time.

## Highlights

- **Multi-Source Menu Intelligence.** Analyzes physical paper menu photos via vision recognition and searches the web in real time to fetch online restaurant menus.
- **OpenClaw Agent Architecture.** Built on the open-source OpenClaw agent foundation, supporting modular messaging channels and flexible LLM backends.
- **Slack Messaging Interface.** Custom Slack integration providing instant, natural conversational interaction (extendable to Discord, WhatsApp, Telegram, etc.).
- **Pluggable LLM Backend.** Powered by Anthropic Claude for deep reasoning and prompt safety, with modular support for any LLM provider.
- **Clinical Rule Engine.** Enforces dietary guidelines for Type 2 Diabetes and saturated fat limits for High Cholesterol.
- **Structured Actionable Advice.** Outputs three clear categories for every menu: 🟢 **BEST PICK** (safe, high-fiber, lean protein options), 🟡 **MODIFICATION TIP** (actionable waiter requests like sauce on the side), and 🔴 **ITEMS TO AVOID** (high saturated fat or refined carb risks).

## Tech Stack

| Layer | Technology |
|---|---|
| **Agent Framework** | OpenClaw Open-Source Agent Architecture |
| **Messaging Frontend** | Slack (Pluggable: Discord, Telegram, WhatsApp) |
| **LLM Engine** | Anthropic Claude (Pluggable: OpenAI, Gemini, Local LLMs) |
| **Vision & Web Search** | Computer Vision + Web Search Capabilities |

## Why the source is private

This repo is a public-facing description of a working application. The full implementation lives in a private repository. If you are a collaborator, recruiter, or fellow builder who would like a deeper look into the codebase—please reach out below.

## Contact

**Gabriel Shyh** — [@gabrielshyh](https://github.com/gabrielshyh) · [gabrielsshyh2006@gmail.com](mailto:gabrielsshyh2006@gmail.com)
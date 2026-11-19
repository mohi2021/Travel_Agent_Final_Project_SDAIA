# Multi-Agent AI Travel Planner — Final Project


## Project overview

A minimal educational AI travel assistant that prepares a one-day itinerary for a destination, traveler budget and interests. Travelers benefit from a research step, an itinerary-writing step and an independent review.

## Project structure

```text
Travel\_Agent\_Final\_Project.ipynb  # Complete Google Colab implementation and tests
README.md                         # Setup and project documentation
```

## Architecture and workflow



Three specialized agents work in a sequential, centrally orchestrated workflow. The Planner Agent creates a plan and writes the itinerary; the Research Agent uses Tavily for external facts; the Reviewer Agent checks output quality and requests at most one revision. The reasoning patterns are Plan-and-Execute and Reflection/Self-Critique.

## Technologies and AI tools

* Python 3 (standard library only)
* Groq chat-completions API (`llama-3.3-70b-versatile` by default)
* Tavily search API
* Google Colab Secrets for API keys
* Python logging and local assertions for testing

## Installation and setup

1. Upload `Travel\_Agent\_Final\_Project.ipynb` to Google Colab.
2. In Colab's Secrets panel (key icon), add `GROQ\_API\_KEY` and `TAVILY\_API\_KEY`, then enable access to the notebook.
3. Run cells in order. No `pip install` is necessary.
4. Set `DESTINATION`, `BUDGET\_USD` and `INTERESTS` in section 5, and run the live example.

If a Groq model is unavailable to your account, change the `GROQ\_MODEL` variable to a model your account supports. Live calls require working internet access and API keys.

## How to run and test

Run all cells in Colab. The live run is skipped if keys are absent. Section 6 still runs **six keyless automated tests**: valid request, invalid budget, tool failure, prompt injection, reviewer retry/output rejection and PII masking.

## Safety and monitoring

Input length/budget validation, detection of simple prompt-injection patterns, masking of email/phone strings and output validation are implemented. The workflow records agent actions, tool calls, failures and elapsed runtime. This prototype is not a production-grade security system.

## Future improvements

1.add weather 
2. changing currency.

## Trainers
GitHub:
1.mohi2021
2.aldajania
3.magedr747-lang
4.aly-m-alyami

## Special Thanks
Special Thanks to SDAIA to provided us with Generic AI course
https://github.com/SDAIAAcademy


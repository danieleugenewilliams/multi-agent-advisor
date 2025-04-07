# Multi-Agent Life Advisor: Interactive Advisory Board
## Use Case
This project creates an interactive "board of advisors" with Career and Money agents, using LangGraph and tools to provide personalized, actionable advice tailored to specific user goals—or to help articulate goals when users are unsure.

## Problem
People often need tailored guidance to achieve specific career or financial goals but may struggle to define those goals clearly, limiting the effectiveness of generic advice.

## Solution
We use:
1. **Agents**: Career and Money advisors collaborate via LangGraph in an interactive chat, powered by configurable LLMs (cloud or local), to offer goal-specific advice or assist in goal-setting.
2. **Retrieval-Augmented Generation (RAG)**: Grounds advice via a `@tool`-annotated function, inspired by *Principles* (Dalio), *The Intelligent Investor* (Graham), and the FIRE Toolbox.
3. **Structured Output**: Returns advice in JSON when finalized, with conversational flexibility.
4. **Evaluation**: Optionally collects user ratings (1-5) to assess advice quality, saved to a JSON file for potential future training.

## How to Use
1. **Setup**: Run the setup cell to install dependencies. Ensure `GOOGLE_API_KEY` is set in Kaggle Secrets for Gemini LLM.
2. **Configuration**: Adjust `CONFIG` below to toggle evaluation (`ENABLE_EVALUATION`), swap LLMs (`MODEL_CONFIG`), and customize behavior.
3. **Run**: Execute the notebook to start the chat. Type goals or questions, rate advice if enabled, and use 'q' to quit and see/download ratings.
4. **Download Ratings**: After quitting, run the download cell to access `ratings.json`.

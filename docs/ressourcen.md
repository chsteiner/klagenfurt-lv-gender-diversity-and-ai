# Resources & Tools

## Ollama: Local LLMs (recommended)

Run open-source models locally — free, unlimited, reproducible.

**Setup:**
1. Install [Ollama](https://ollama.com/)
2. Download a model: `ollama pull llama3` or `ollama pull mistral`
3. API runs at `http://localhost:11434`

**Models:**
- `llama3` (~4.7 GB) — good all-rounder
- `mistral` (~4.1 GB)
- `phi3` (~2.2 GB) — runs on low-end hardware

**Python example:**
```python
import requests

def query_ollama(prompt, model="llama3"):
    response = requests.post(
        "http://localhost:11434/api/generate",
        json={"model": model, "prompt": prompt, "stream": False}
    )
    return response.json()["response"]

base = query_ollama("A single mother seeks help with parenting.")
neutral = query_ollama("A single parent seeks help with parenting.")
```

## Alternative: Free-Tier Web Interfaces

If Ollama doesn't work: [ChatGPT](https://chat.openai.com/), [Claude](https://claude.ai/), [Mistral Le Chat](https://chat.mistral.ai/), [HuggingChat](https://huggingface.co/chat/). Realistic for 10–30 prompts.

**Note:** Google Gemini API blocks social work prompts entirely. The web interface works partially.

## Context Engineering

For working with LLMs: Instead of role assignments ("You are an expert"), provide the concrete **context** of your scenario — target group, institutional framework, diversity dimensions. Role prompts show no improvement in current models (Kim et al., ICLR 2025).

## Coding Agents

You may and should use AI tools for programming — Claude Code, GitHub Copilot, Cursor, or similar. GitHub Copilot Pro is free for students via the [GitHub Student Developer Pack](https://education.github.com/pack).

## Promptotyping Skill

The Promptotyping methodology is available as an open agent skill that works with any LLM. Install it in your coding agent or copy the .md templates into any LLM conversation:
https://github.com/DigitalHumanitiesCraft/promptotyping-skill

## Contact

| Question | Who |
|----------|-----|
| Technical (Ollama, APIs, code) | Christian Steiner — Moodle forum |
| Conceptual (bias, gender, theory) | Susanne Sackl-Sharif — Moodle forum |

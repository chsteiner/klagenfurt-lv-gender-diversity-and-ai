# Resources & Tools

## Ollama: Local LLMs (recommended)

Run open-source models locally: free, unlimited, reproducible.

**Setup:**
1. Install [Ollama](https://ollama.com/)
2. Download a model: `ollama pull llama3` or `ollama pull mistral`
3. API runs at `http://localhost:11434`

**Models:**
- `llama3` (~4.7 GB) – good all-rounder
- `mistral` (~4.1 GB)
- `phi3` (~2.2 GB) – runs on low-end hardware

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

**Note:** In our testing ([FAIR-SW-Bench](fair-sw-bench.md) pilot), the Google Gemini API blocked all social work prompts. The web interface works partially.

## Context Engineering

For working with LLMs: Instead of role assignments ("You are an expert"), provide the concrete **context** of your scenario: target group, institutional framework, diversity dimensions. Role prompts show no improvement in current models ([Kim et al., ICLR 2025](https://arxiv.org/abs/2408.08631)).

## Coding Agents

You may and should use AI coding agents for programming.

**Free option:** [GitHub Copilot](https://github.com/features/copilot) is built into VS Code. Every GitHub account includes Copilot Free (50 chat messages/month); students can upgrade to unlimited usage via the [GitHub Student Developer Pack](https://education.github.com/pack). Use **Agent Mode** (select "Agent" in the Copilot Chat dropdown): describe what you need in natural language, and the agent writes code, creates files, runs terminal commands, and fixes errors.

**If you already have a paid subscription:** Use whichever agent you prefer. [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (Anthropic), [Gemini CLI](https://github.com/google-gemini/gemini-cli) (Google), [Codex](https://openai.com/index/introducing-codex/) (OpenAI), [Cursor](https://www.cursor.com/), [Windsurf](https://windsurf.com/), or any other coding agent. The methodology is the same: you describe the task, the agent writes the code.

## Promptotyping Skill

The [Promptotyping](https://github.com/DigitalHumanitiesCraft/promptotyping-skill) methodology is available as an open agent skill that works with any LLM. Install it in your coding agent or copy the .md templates into any LLM conversation: [github.com/DigitalHumanitiesCraft/promptotyping-skill](https://github.com/DigitalHumanitiesCraft/promptotyping-skill)

## References

- Kim, J., Yang, N., & Jung, K. (2025). [Persona is a Double-Edged Sword: Mitigating the Negative Impact of Role-playing Prompts in Zero-shot Reasoning Tasks](https://arxiv.org/abs/2408.08631). *ICLR 2025*.

## Contact

| Question | Who |
|----------|-----|
| Technical (Ollama, APIs, code) | Christian Steiner – Moodle forum |
| Conceptual (bias, gender, theory) | Susanne Sackl-Sharif – Moodle forum |

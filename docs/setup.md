# Setup Guide

> Complete these steps **before Session 1 (17.03.2026)**. Estimated time: 30–60 minutes.

> **Prerequisites:** This course assumes basic programming skills in at least one language (ideally Python). No prior knowledge of Machine Learning or Gender Studies required. See the [Syllabus](https://github.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/blob/main/SYLLABUS.md) for details.

## System Requirements

- **RAM:** 8 GB minimum (for running local LLMs via Ollama)
- **Disk space:** ~10 GB free (VS Code + Ollama + one model)
- **OS:** Windows 10/11, macOS 10.15+, or Linux

## Step 1: VS Code

A free code editor with a built-in AI coding agent (GitHub Copilot). You will use it for everything: writing code, editing Markdown files, running terminal commands.

- **Download:** [code.visualstudio.com](https://code.visualstudio.com/) (use the latest version)
- If you already have VS Code installed, update it: Help > Check for Updates
- **Verify:** Open VS Code, confirm it launches

> **Tip:** VS Code has a built-in terminal. Open it with `` Ctrl+` `` (backtick key, top-left on most keyboards) or via the menu: Terminal > New Terminal. You will run all verification commands in this terminal.

## Step 2: Git

Version control for your project. You will use it to track changes and submit your work.

- **Windows:** [git-scm.com/download/win](https://git-scm.com/download/win)
- **macOS:** Run `xcode-select --install` in Terminal, or download from [git-scm.com/download/mac](https://git-scm.com/download/mac)
- **Linux:** `sudo apt install git` (Debian/Ubuntu) or `sudo dnf install git` (Fedora)
- **Verify:** In the VS Code terminal, run `git --version`

## Step 3: Python

You will use Python to send prompts to LLMs and analyze responses. Basic scripting is sufficient.

- **Download:** [python.org/downloads](https://www.python.org/downloads/) (Python 3.10+)
- **Verify:** In the VS Code terminal, run `python --version` (or `python3 --version` on macOS/Linux)
- **Install the requests library:** `pip install requests` (or `pip3 install requests`)

> **Windows users: important!** During Python installation, check the box **"Add Python to PATH"**. If you miss this, `python` will not be recognized as a command. If typing `python` opens the Microsoft Store instead, see Troubleshooting below.

## Step 4: GitHub Account + Copilot

GitHub hosts your project repository. GitHub Copilot is an AI coding agent built into VS Code. It can write code, edit multiple files, and run terminal commands for you.

1. Create a GitHub account: [github.com](https://github.com/)
2. Apply for the **Student Developer Pack**: [education.github.com/pack](https://education.github.com/pack) (gives you unlimited Copilot, including Agent Mode)
3. In VS Code: click the **Copilot icon** in the bottom-right status bar, select **"Use AI Features"**, and sign in with your GitHub account

**Verify:** Press `Ctrl+Alt+I` (or `Cmd+Alt+I` on Mac) to open the Copilot Chat panel. Type "Hello, what can you do?" and confirm you get a response.

> **Note:** The Student Developer Pack can take 1–7 days for approval. Apply now. Even without it, every GitHub account includes **Copilot Free** (50 chat messages/month), so you can sign in and verify immediately. You do not need Copilot for Session 1; the project phase starts in Session 3 (27.04.).

## Step 5: Ollama

Ollama lets you run open-source LLMs locally on your machine: free, unlimited, reproducible. These are the models you will test for bias.

- **Download:** [ollama.com](https://ollama.com/)
- **After install, pull a model:** In the VS Code terminal, run `ollama pull llama3` (~4.7 GB download)
- **Verify:** `ollama list` should show `llama3`
- **Smaller alternative:** `ollama pull phi3` (~2.2 GB, runs on low-end hardware)

## Checklist

- [ ] VS Code installed (latest version), terminal opens with `` Ctrl+` ``
- [ ] Git installed, `git --version` works in terminal
- [ ] Python installed, `python --version` works in terminal
- [ ] `pip install requests` completed
- [ ] GitHub account created
- [ ] Student Developer Pack applied for
- [ ] Signed in to Copilot in VS Code (status bar icon)
- [ ] Copilot Chat responds (`Ctrl+Alt+I`)
- [ ] Ollama installed, at least one model pulled

---

## How You Will Use Copilot Agent Mode

You do not need this for Session 1. This section explains how you will work during the project phase (from Session 3 onward).

**Agent Mode** lets you describe tasks in natural language, and Copilot writes the code for you:

1. Open the Copilot Chat panel (`Ctrl+Alt+I`)
2. In the dropdown at the top of the chat panel, select **"Agent"**
3. Describe what you want, e.g.: "Create a Python script that sends a prompt to Ollama at localhost:11434 and saves the response to a CSV file"
4. Copilot will write the code, create files, run commands in the terminal, and fix errors. You review and approve each step.

This is how you will build your bias detection tool. You design the research (scenarios, bias dimensions, analysis); the agent writes the code.

> **Already using a different coding agent?** GitHub Copilot is the free default, but if you have a paid subscription to [Claude Code](https://docs.anthropic.com/en/docs/claude-code), [Gemini CLI](https://github.com/google-gemini/gemini-cli), [Codex](https://openai.com/index/introducing-codex/), [Cursor](https://www.cursor.com/), or any other agent, use that instead. The methodology is the same.

---

## Troubleshooting

### Copilot icon not visible in VS Code

Make sure you are running a recent version of VS Code (v1.103 or later). Update via Help > Check for Updates. The icon appears in the bottom-right status bar.

### "python" or "git" is not recognized as a command

Restart VS Code after installation (the terminal needs to reload PATH). If that does not help: on Windows, search for "Edit environment variables" in Windows Settings and add the installation directory to PATH.

### Windows: typing "python" opens the Microsoft Store

Windows 10/11 ships with a "python" shortcut that redirects to the Store. Fix: Open Settings > Apps > Advanced app settings > App execution aliases, and turn off the "python.exe" and "python3.exe" aliases. Then restart your terminal.

### Ollama model download is very slow

Use your university network if possible. Alternatively, start with the smaller `phi3` model (2.2 GB). You can also use free web interfaces (ChatGPT, Claude, Mistral) as a temporary fallback; see [Resources & Tools](ressourcen.md).

### Ollama: "Connection refused" when running Python scripts

The Ollama server must be running in the background. On Windows/Mac, make sure the Ollama app is started (check system tray). On Linux, run `ollama serve` in a separate terminal. Then try again.

### GitHub Student Developer Pack not approved yet

This is normal and can take up to 7 days. Copilot Free (50 messages/month) works immediately after signing in and includes Agent Mode. The full Student plan is needed once you start heavy development in the project phase (from Session 3 onward). Apply again if rejected and make sure your university email is verified.

### Not enough disk space for Ollama

Use `phi3` (~2.2 GB) instead of `llama3` (~4.7 GB). If disk space is very limited, use free web interfaces instead; see [Resources & Tools](ressourcen.md).

### macOS: "App can't be opened because it is from an unidentified developer"

Go to System Settings > Privacy & Security, scroll down, and click "Open Anyway."

## Need help?

- **Technical questions** (setup, code, Ollama): Moodle forum – Christian Steiner
- **Conceptual questions** (bias, gender, theory): Moodle forum – Susanne Sackl-Sharif
- **More details on tools and LLM access:** [Resources & Tools](ressourcen.md)

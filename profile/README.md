<div align="center">

# 📜 Papyrus (Papyrus)

[![GitHub Stars](https://img.shields.io/github/stars/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=yellow)](https://github.com/Alpaca233114514/Papyrus/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=blue)](https://github.com/Alpaca233114514/Papyrus/forks)
[![GitHub Issues](https://img.shields.io/github/issues/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=red)](https://github.com/Alpaca233114514/Papyrus/issues)
[![GitHub License](https://img.shields.io/github/license/Alpaca233114514/Papyrus?style=flat-square&color=green)](https://github.com/Alpaca233114514/Papyrus/blob/main/LICENSE)
[![Release](https://img.shields.io/github/v/release/Alpaca233114514/Papyrus?style=flat-square&logo=github&color=orange)](https://github.com/Alpaca233114514/Papyrus/releases)

![Minecraft Paper](https://img.shields.io/badge/Icon-Minecraft_Paper-green?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.8-blue?style=flat-square&logo=python)
![AI-Assisted](https://img.shields.io/badge/Dev-AI--Assisted-blueviolet?style=flat-square)

**🌐 Languages / 语言 / 言語:**
[English](./README.md) | [简体中文](./README_ZH.md) | [日本語](./README_JP.md)

</div>

---

**Papyrus** is a minimalist, efficient, keyboard-driven AI Agent-powered SRS (Spaced Repetition System) review engine focused on high-intensity model memorization.

> "The Great Way is simple."

---

## ✨ Key Features

- 🚀 **Minimalist Interaction**: Fully keyboard-driven workflow, no mouse needed. Helps you enter the "flow state" of deep review.
- 🧠 **Intelligent Scheduling**: Built-in simplified spaced repetition algorithm based on the Ebbinghaus forgetting curve logic. Automatically schedules next review based on mastery level.
- 📦 **Lightweight & Portable**: Single `.exe` file, zero dependencies. Data stored locally in `Papyrusdata.json` for privacy and security.

---

## ⌨️ Shortcuts (Flow Mode)

| Key | Action | Effect |
| :--- | :--- | :--- |
| **Space** | **Reveal Answer** | Unfold the scroll to view the answer |
| **1** | **Forgot** | Mark as unfamiliar, high-frequency review in short term |
| **2** | **Vague** | Mark as uncertain, review again later |
| **3** | **Mastered** | Memory is solid, review interval doubles linearly |

---

## 📥 Batch Import Format

Prepare a `UTF-8` encoded `.txt` file with the following format:

```text
Model scenario or question A === Core trigger or answer A

Model scenario or question B === Core trigger or answer B
```

*Tip: Each card is separated by `===`. Leave an empty line between groups for clarity.*

---

## 🚀 Download & Usage

### 1. Get the Program
Go to the [Releases](https://github.com/Alpaca233114514/Papyrus/releases) page to download the latest version.

### 2. Running Instructions
1. Extract the downloaded `.zip` file to any folder.
2. Double-click `Papyrus.exe` to launch.
> **Note:** Do not move the `.exe` alone to other locations, otherwise the program cannot load icons or read previous review progress (v1.0.0 only).

### 3. AI Features

#### 1. Configure API
Click the "⚙️ Settings" button in the sidebar and enter your API Key:

- **OpenAI**: Get at https://platform.openai.com/api-keys
- **Anthropic**: Get at https://console.anthropic.com/
- **Ollama**: Runs locally, no API Key needed
  ```bash
  # Install Ollama
  # Download: https://ollama.ai
  
  # Pull model
  ollama pull llama2
  ```

#### 2. Mode Configuration
**Agent Mode**: AI uses tool calls to add, edit, and delete cards  
**Chat Mode**: Chat only

#### 3. Parameter Adjustment
In settings, you can adjust:
- **Temperature**: Controls creativity (0-2, higher = more random)
- **Max Tokens**: Maximum response length

### Configuration File

AI configuration is saved in `data/ai_config.json`, including:
- API Key
- Model selection
- Parameter settings

### Notes

1. **API Costs**: OpenAI and Anthropic charge by usage. Set a budget.
2. **Local Model**: Ollama is completely free but requires better hardware.
3. **Network**: Cloud APIs require stable internet.
4. **Privacy**: Local model data won't be uploaded; cloud APIs send question content.

### Troubleshooting

**AI Features Not Working**
- Check if `requests` library is installed
- Check console error messages

**API Call Failed**
- Check if API Key is correct
- Check network connection
- Confirm API quota is sufficient

**Ollama Connection Failed**
- Confirm Ollama service is running
- Check if port is 11434
- Try: `ollama serve`

---

## 🛠️ Technical Details (For Developers)

- **Development Mode**: Human-led, AI-assisted (Claude Sonnet 4.6, Gemini 3.0 Pro)
- **Language**: Python 3.8 (Tkinter)
- **Engineering**: Packaged with `PyInstaller`, handled `sys._MEIPASS` resource path compatibility
- **License**: MIT License
- **Credits**: Icon material from Minecraft Wiki (Mojang Studio)

---

## 💡 Developer's Words

The birth of this project wasn't ideal or grand.

Why make this? One day I was studying AI and downloaded Anki to memorize knowledge points. After downloading, it needed to check for updates, which required connecting to a server, but I couldn't connect.

Then I noticed Gemini was right there, so I asked it to write one for me. After some tweaking, I started using it.

I actually didn't plan to release this. Why did I eventually?

Yesterday, I used an old account to star my girlfriend's repo. GitHub identified me as a bot and removed my activity. I was furious! I use AI, but I'm not AI. To prove I'm not AI, I happened to have this on hand, so I polished it and put it here.

Story's over. It's already the 6th day of the Lunar New Year, dawn is breaking soon. Poor student, sigh, can only vent here.

I love a saying: "Knowledge makes you free" (Veritas vos liberabit). To all the great developers, this is my first open-source project. Please be kind.

Consider this a belated New Year greeting.  
**May you, in the new year, wield the blade of knowledge to pierce the ruins of darkness and reach the realm of dawn.**

---

## 📚 Documentation Navigation

- [Quick Start Guide](docs/guides/QUICKSTART.md) - Get started in 5 minutes
- [Version Info](docs/guides/VERSION.md) - Current version and updates
- [Changelog](docs/guides/CHANGELOG.md) - Complete version history
- [Project Structure](docs/PROJECT_STRUCTURE.md) - Code organization
- [AI Features](docs/AI_README.md) - AI assistant guide
- [AI Tools Demo](docs/AI_TOOLS_DEMO.md) - Real-world use cases

---

<div align="center">

⭐ **Star this repo if you find it helpful!** ⭐

[Report Bug](https://github.com/Alpaca233114514/Papyrus/issues) · [Request Feature](https://github.com/Alpaca233114514/Papyrus/issues) · [Releases](https://github.com/Alpaca233114514/Papyrus/releases)

</div>

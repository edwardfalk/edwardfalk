# Edward Falk

**Electronics engineer (embedded systems) · AI systems developer · IT consultant since 2005**
Gothenburg, Sweden · [edwardfalk.com](https://edwardfalk.com) · [LinkedIn](https://www.linkedin.com/in/falkedward/) · edward@falkdata.se

I build systems where hardware, software and AI meet: a voice AI living inside a 1991 Macintosh,
a wind-plant simulator for the Swedish power grid, and the self-hosted agent tooling I use to run
many AI-assisted projects in parallel. I've run my own IT company, [Falk Data](https://falkdata.se), for
20 years, and in 2026 I finished a two-year degree as an electronics engineer in embedded systems at
[Yrgo](https://www.yrgo.se/program/elektronikingenjor-hardvarudesign/).

What I bring: hands-on electronics (oscilloscope, soldering iron, datasheets from the 1980s), embedded
Linux and microcontrollers, and a lot of practical experience making AI models do reliable work with
tools, memory and review, not just chat.

---

## Featured projects

### 📞 Project ScrLk: Happy Mac
**Embedded Linux · voice AI · retro hardware** · my degree project · [project page →](https://github.com/edwardfalk/Project-ScrLk)

A Raspberry Pi 5 inside a 1991 Macintosh Classic II drives the original 9" monochrome CRT
(512×342, 1-bit) directly from its GPIO pins. You talk to the AI assistant *Happy Mac* through a 1950s
Swedish Ericofon handset. He controls the apps and games on screen, answers in Swedish or English, and
can read live traffic from a passive network tap. He can watch but never interfere.

- Drives the CRT's analog board from the Pi's GPIO (DPI) with a custom device-tree overlay for the
  Mac's video timing, every signal checked on an oscilloscope before touching the tube
  ([timings, public](https://github.com/edwardfalk/macintosh-timings))
- Interfaces a carbon-microphone handset through a modified USB sound card, including tracking down a
  hidden +23.8 dB sidetone inside the sound-card chip that no software could see
- Voice agent with tool use: it opens apps, remembers people between conversations, looks things up,
  and can be interrupted mid-sentence (the echo threshold was measured on the real handset)
- Local wake word on the Pi, Gemini Live for conversation, a 1-bit React desktop, FastAPI backend
  and Ansible provisioning, plus a 1-bit Doom port and an AI-narrated Zork
- Built during my internship at EQ2 in Gothenburg with classmate
  [Felix Da Silva Gunnarsson](https://github.com/gunnarsson901)

### 🌬️ WindSim: wind plant and grid-balancing simulator
**Python · energy systems · simulation** · *private for now*

A deterministic simulation of a small Swedish wind plant. It answers two questions: what would the
plant have produced and earned at a real site, and would it pass Svenska kraftnät's mFRR/aFRR
prequalification, the test a plant must pass before selling balancing power to the grid.
Every number carries an **evidence level**, from *assumed* to *fitted to real logs*, so the result
always shows how far it can be trusted.

### 🧠 Self-hosted AI agent infrastructure
**Claude Code · MCP · Docker · Tailscale** · *private: personal data*

The system behind how I work with AI day to day:
- **A persistent memory for AI agents.** A git-backed Markdown vault shared by every coding session.
  A nightly "librarian" agent files, links and indexes new notes. An MCP connector on my own VPS
  makes it reachable from anywhere, and a Telegram bot handles quick capture.
- **Review gates.** Plans go to a second model for critique before implementation. Code goes through
  blind parallel reviewers before every push.
- **Self-hosted services.** VPS and home servers on a private Tailscale network. Earlier: RAG pipelines
  with Qdrant and Redis in Docker, knowledge graphs, and custom MCP servers.

### 🎨 Say Color
**Android · Kotlin · computer vision · accessibility** · *in testing*

An app that says the colour of a garment out loud, built for a visually impaired client. It turns on
the flashlight, captures three frames, classifies each one and reconciles them before speaking. One
frame under household light isn't reliable enough to tell someone who can't check. TalkBack
support is treated as a correctness requirement.

### ✈️ Glider
**TypeScript · physics simulation · procedural terrain** · [play it →](https://edwardfalk.github.io/glider/)

A browser gliding game with real aerodynamics and procedurally generated terrain. You find
thermals to stay up, and the landing is scored. The flight model is parameterised for gravity, wind
and air density so it can fly on other worlds. It's also my testbed for fully AI-generated code: every
line is written by AI agents working from a standing brief.

### 🔌 FPGA hardware acceleration
**VHDL · Cyclone V · SPI** · [repo →](https://github.com/edwardfalk/digitalteknik-lab1-hvacc)

An Arduino offloads 7-segment display driving to an FPGA over SPI, with and without
metastability protection. Also from the degree: a digital guitar filter on FPGA, an autonomous
Arduino car, and a servo-driven mechanical drum machine.

### 🎮 Cosmic Vibe
**JavaScript · p5.js** · [play it →](https://edwardfalk.github.io/vibe/)

A rhythm-driven space shooter, made as an experiment in how far AI coding can go without writing
a line of code myself. The code, graphics and animation are all AI-generated.

---

## Skills

| | |
|---|---|
| **Languages** | C, C++, Python, TypeScript/JavaScript, Rust, VHDL, Kotlin |
| **Embedded** | Raspberry Pi, Arduino, ESP32, AVR, embedded Linux (device tree, KMS/DRM, PipeWire), MQTT |
| **Electronics** | Analog and digital design, signal processing, PCB design (KiCad), soldering, measurement: oscilloscope, logic analyser, spectrum analyser |
| **AI** | LLM agents and tool use, MCP servers, RAG and vector databases, voice AI, prompt/instruction design, Claude Code, Codex |
| **Infrastructure** | Linux, Docker, Ansible, Tailscale, VPS hosting, networking, Microsoft 365, Google Workspace |
| **Tools** | Git/GitHub, Quartus, ModelSim, LTspice, Microchip Studio, Jira |

## Experience

**Falk Data AB**: founder, IT consultant · *2005–present* (sole trader until 2023)
Twenty years of IT support, troubleshooting, networks, security and training for companies and
private clients, and more recently AI automation. The job is problem-solving: understanding what the
customer actually needs, then making it work.

**EQ2, Gothenburg**: internship (LIA) · *2025–2026*
Built Project ScrLk and its degree-presentation demo.

## Education

**Yrgo, Gothenburg**: Electronics Engineer, Embedded Systems (higher vocational, 2 years) · *2024–2026*
Analog and digital electronics, VHDL/FPGA, embedded C/C++, signal processing, test automation, embedded Linux.

Earlier university studies in informatics, databases, psychology, theoretical philosophy and business.

---

<sub>Outside work: I play guitar and synth in the Gothenburg band the Blindness, and I'm building my own synthesizer.</sub>

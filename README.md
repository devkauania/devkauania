# Kauan Mendes

**Applied AI Engineer** · LLM guardrails, agent safety and cost control.

I work on the parts of LLM products that tend to break: prompt-injection and jailbreak
defenses, output checks, spend limits, and deterministic fallbacks for when the model is
down or misbehaves.

Brazil (UTC-3) · remote · English, Portuguese, Spanish ·
[LinkedIn](https://www.linkedin.com/in/kauan-mendes-764093243)

### Open source

| Project | What it is |
|---|---|
| [**Python AI Dojo**](https://github.com/devkauania/python-ai-dojo) · [play it](https://python-ai-dojo.vercel.app) | Browser game that teaches the everyday Python of AI engineering: token and cost math, tool calling, structured output, chunking, embeddings, RAG. 273 Python exercises run real Python in the browser via Pyodide, plus 30 HTML/CSS/JS exercises. Every reference solution must pass its tests and every starter must fail, checked automatically. Playable in English and Brazilian Portuguese, with a language switch in the game. |
| [**blink-sanitizer**](https://github.com/devkauania/blink-sanitizer) | Zero-dependency, regex-based prompt-injection filter extracted from my AI gateway: 266 patterns across 11 languages, with Unicode, leetspeak and separator normalization. It is a first layer, not a complete defense; the README has a reproducible latency benchmark, the known false positives and the evasions that are still open. |
| [**projeto-zero**](https://github.com/devkauania/projeto-zero) | `@projeto-zero/cli` on npm: scaffolds Claude Code agent workspaces and launches parallel coding agents, each in its own git worktree, with an environment allow-list and an explicit opt-in for permission bypass. Live runs do not work in 1.1.3, the version on npm: it passes a `--temperature` flag that current Claude Code rejects. The fix is on `main`, not released yet. CI on Linux and Windows. |

### Private work (happy to walk through it in an interview)

- **Blink**: self-hosted AI governance gateway (FastAPI, Celery, Redis, PostgreSQL). The
  gateway only validates, caches and enqueues; model work runs in workers behind layered
  guardrails. mypy and ruff in CI, plus in-house attack suites. blink-sanitizer comes from
  its input stage.
- **Otto**: WhatsApp agent for event venues, rewritten from n8n into Python. Go-live is pending.
- **Vereda**: privacy-first recovery app (Expo + Hono) with an optional LLM companion,
  pre-launch. Risk is checked in layers: an on-device classifier, an independent
  server-side check, a spend cap, an output filter and a deterministic fallback. No
  accounts: RFC 9474 blind-signature tokens and an on-device encrypted backup.

### How I work

- **Coding agents as a pair, and I say so.** I write most of my code with Claude Code as a
  pair. I own the architecture, the review and the verification, and I write the checks
  that catch the agent: CI gates, doc/code drift tests, measured numbers instead of adjectives.
- **Go deep, then argue with myself.** I study a problem until I understand who it affects,
  ask AI to argue against my reasoning, and build only on what survives.

### Stack

- **Daily:** Python, TypeScript, FastAPI, PostgreSQL/Supabase, Redis, Docker, GitHub Actions, Anthropic/OpenAI/Gemini APIs
- **Used in projects:** Celery, NeMo Guardrails, MCP, Expo/React Native, Hono
- **Experimented with:** LangGraph + DSPy, garak

### Before engineering

People-analytics automation at **Whirlpool** (a manual daily report became a scheduled
Python/SQL job) and SDR for Europe at **Sizebay**, where I built the team's lead-research
automation with Gemini and Apps Script. B.Sc. in Computer Science.

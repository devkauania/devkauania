# Kauan Mendes

**Applied AI Engineer.** I work on the part of LLM products that usually breaks:
prompt-injection and jailbreak defenses, output checks, cost limits, and deterministic
fallbacks for when the model is down or misbehaves.

Brazil (UTC-3) · remote · English, Portuguese, Spanish ·
[LinkedIn](https://www.linkedin.com/in/kauan-mendes-764093243)

### How I work

- **Go deep, then argue with myself.** I study a problem until I understand who it hurts, make
  AI argue against my reasoning, and build only on the line that survives.
- **Coding agents as a pair, and I say so.** Most of my commits are co-authored with Claude
  Code. I own the architecture, the review and the verification, and I write the checks that
  catch the agent: CI gates, doc/code drift tests, measured numbers instead of adjectives.
- **Efficiency and empathy.** Fast and cheap systems, built for the person on the other side.

### Open source

| Project | What it is |
|---|---|
| [**Python AI Dojo**](https://github.com/devkauania/python-ai-dojo) · [play it](https://python-ai-dojo.vercel.app) | Browser game that teaches the daily Python of AI engineering: token and cost math, tool calling, structured output, chunking, embeddings, RAG. 273 Python exercises run real Python via Pyodide, plus 30 HTML/CSS/JS exercises. Every reference solution must pass and every starter must fail, checked in CPython and in the browser. Game text is in Portuguese. |
| [**blink-sanitizer**](https://github.com/devkauania/blink-sanitizer) | Zero-dependency, regex-based prompt-injection filter extracted from my AI gateway: layer 1 of a defense-in-depth stack, not a complete defense. I found and fixed a leetspeak + separator bypass, added an input size cap against ReDoS, and replaced latency adjectives with a benchmark (p50 348 µs on my machine). Known false positives and open evasions are documented. |
| [**projeto-zero**](https://github.com/devkauania/projeto-zero) | `@projeto-zero/cli` on npm: scaffolds Claude Code agent workspaces and runs parallel agents, each in its own git worktree, with an environment allow-list and an explicit opt-in for permission bypass. CI on Linux and Windows. |

### Private work (happy to walk through it in an interview)

- **Blink**: self-hosted AI governance gateway (FastAPI, Celery, Redis, PostgreSQL). The gateway
  only validates, caches and enqueues; model work runs in workers behind layered guardrails.
  2,300+ test functions, mypy + ruff in CI, in-house attack suites.
- **Otto**: WhatsApp agent for event venues, rewritten from n8n into Python with ~1,100 test
  functions. Go-live is pending.
- **Vereda**: privacy-first recovery app (Expo + Hono) with an optional LLM companion,
  pre-launch. Risk is checked in layers: an on-device classifier I trained, an independent
  server-side check, a spend cap, an output filter and a deterministic fallback. No accounts:
  RFC 9474 blind-signature tokens and an on-device encrypted backup.

### Stack

- **Daily:** Python, TypeScript, FastAPI, PostgreSQL/Supabase, Redis, Docker, GitHub Actions, Anthropic/OpenAI/Gemini APIs
- **Used in projects:** Celery, NeMo Guardrails, MCP, Expo/React Native, Hono
- **Experimented with:** LangGraph + DSPy, garak

### Before engineering

People-analytics automation at **Whirlpool** (a daily 2-hour report became a Python/SQL job
that runs in under a minute) and SDR for Europe at **Sizebay**, where I built the team's
lead-research automation with Gemini and Apps Script (~8h → ~2h a day). B.Sc. in Computer Science.

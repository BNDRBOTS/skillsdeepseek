# Universal Skill Formula — Production Specification (May 2026)

A single, self-contained HTML document that distills the exact prompt/Skill formatting requirements for Claude, OpenAI (GPT-5.5), DeepSeek (V4), Gemini (3.1 Pro), and the open Agentskills standard. All claims are cross-referenced against each platform's official documentation as of May 22, 2026.

**What this is:** a practical reference you can keep open in a browser tab while building AI skills, writing system prompts, or packaging custom GPTs. It saves you from hunting through four separate docs every time you need the `description` character limit or the JSON-mode gotcha for a particular model.

## What's inside

The document is organized into 10 sections:

1. **Current model lineup** — which models are live, which are deprecated, and upcoming retirement dates.
2. **Platform‑specific formats** — exact field limits, YAML frontmatter rules, API parameter tables, and what silently breaks each platform.
3. **Open Agentskills standard** — the spec adopted by 30+ tools (Claude, Copilot, Cursor, Gemini CLI, etc.) and how it differs from Claude’s built‑in Skills.
4. **Structural primitives that work everywhere** — XML tags, Markdown headings, prefix markers, and which approach each platform prefers.
5. **Production hardening** — prompt caching behavior, determinism controls, and how to set up stable prefixes for cache hits.
6. **Breaking defaults** — how to override each model’s “safe” aesthetic (Claude’s cream palette, generic AI‑slop) with concrete anti‑patterns and option‑then‑build workflows.
7. **Token efficiency** — what peer‑reviewed research actually says about prompt length vs. compliance (spoiler: discrete constraints beat long paragraphs).
8. **Cross‑platform template** — a minimal contract that passes validation on all four platforms, wrapped in the correct container for each.
9. **Validation checklist** — 12‑item deploy gate you can run before shipping a Skill.
10. **Full working example** — a Claude Skill.md for a brutalist landing‑page generator.

## How to use it

- Download the HTML file or view it directly in any browser.
- Use `Ctrl+F` / `Cmd+F` to jump to a platform or a specific limit.
- The page is fully offline‑friendly; no dependencies, no tracking.

## Keeping it current

Model names, retirement dates, and limits change. The lineup in this document is accurate as of **May 22, 2026**. Bookmark each platform’s changelog if you’re building something long‑lived:

- [Anthropic Claude model changelog](https://docs.anthropic.com/en/docs/about-claude/models)
- [OpenAI platform updates](https://platform.openai.com/docs/overview)
- [DeepSeek API docs](https://api-docs.deepseek.com)
- [Google Gemini updates](https://ai.google.dev/gemini-api/docs/models)

## Authoring notes

This reference was built by directly extracting constraints from the live documentation of each provider. No parameter was invented; no compliance‑rate percentages were fabricated. Where research is cited, the finding is paraphrased faithfully — the document points out gaps in academic consensus explicitly rather than filling them with conjecture.

The goal was to create one artifact that a developer can hand to a new team member and say: “Here are the rails. Don’t hit the silent truncation on Gemini. Don’t omit the `json` keyword on DeepSeek. Start small, then add detail only where it changes behavior.” That’s it.

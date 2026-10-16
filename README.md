# Positioning and GTM Strategy

**Position your B2B product, write your core message and pick the right go-to-market motion.** Three Claude skills built on Shashwat Ghosh's IMPACT, EPIC and CRAFT methods; the third turns vague AI prompts into specific ones.

Plugin page with install steps for Claude Code and Cowork, and real example outputs from each skill: https://tools.gtmhelix.com/plugins/gtm-skills/

Created by [Shashwat Ghosh](https://www.linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo/), Fractional CMO with 24+ years in B2B and 10+ years of fractional experience. VP Marketing, Happay: 161% ARR growth. 2x exit: to CRED ($180M+), then MakeMyTrip. VP Performance Marketing, Locus: $4.2M pipeline. Acquired by IKEA (Ingka Group) in Oct 2025.

---

## Why These Skills?

EPIC, IMPACT and CRAFT are Shashwat Ghosh's original frameworks; they are not part of Claude's built-in skills.

The community marketplaces have generic GTM skills, but [Anthropic explicitly recommends](https://support.claude.com/en/articles/12512176-what-are-skills) using skills only from trusted sources. These 3 skills are built on original frameworks by a practitioner with verified results at companies that got acquired. They contain zero executable code. Pure strategic reasoning you can audit in 5 minutes.

---

## The 3 Skills

### 1. GTM motion picker (EPIC)
**File:** `gtm-motion-picker/SKILL.md`

Diagnose which B2B go-to-market motion should lead before choosing tactics or channels. Scores four motions (Ecosystem, Product-Led, Inbound/Outbound, Community) based on your stage, industry, geography, deal cycle, and NRR.

**Use when:** You are deciding between PLG vs. sales-led vs. community. Your funnel is not converting. You are about to hire your first marketing person and need to know what motion to build around.

**Includes:** Stage-based scoring defaults, 15+ adjustment rules, leaky bucket detection (NRR < 100%), AEO/GEO inbound disruption signals, industry overrides, geography adjustments.

### 2. Positioning and messaging (IMPACT)
**File:** `positioning-and-messaging/SKILL.md`

Build a defensible market position and messaging hierarchy. Covers two steps of the six-step IMPACT Framework: Anchor Market (what category do you own) and Craft Message (10-word core → 30-second elevator → 2-minute narrative).

**Use when:** Your messaging feels generic. Buyers do not understand your category. You are preparing for an investor pitch. You need a positioning statement for your landing page.

**Includes:** Three positioning options (own existing category, create sub-category, create new category), decision framework, three-level messaging hierarchy template, and validation questions.

### 3. Prompt improver (CRAFT)
**File:** `prompt-improver/SKILL.md`

Structure any AI prompt for consistently high-quality outputs using the CRAFT meta-framework: Character, Result, Artifact, Frame, Timeline. This is the "how to use AI effectively" skill that makes every other AI interaction more productive.

**Use when:** AI outputs feel generic. You are not sure how to prompt Claude for business tasks. You want boardroom-grade deliverables from AI without trial and error.

**Includes:** Five-element framework with strong/weak examples, three complete B2B use cases (GTM strategy, battle card, investor update), common mistakes CRAFT prevents.

---

## How the Skills Work Together

```
EPIC diagnoses the motion    →  "Run Ecosystem-led GTM"
IMPACT positions the product →  "Own the '[your differentiator] + [category] for [your buyer]' sub-category"
CRAFT structures the AI      →  "Here is how to brief Claude on any GTM task going forward"
```

---

## Installation

### Option A: Claude.ai (recommended for most users)

1. Go to **claude.ai** → **Settings** → **Skills**
2. Click **Upload custom skill**
3. Upload each `SKILL.md` file (one at a time)
4. Claude will automatically use the relevant skill when you ask GTM-related questions

### Option B: Claude Code (for developers)

Install it as a plugin, so the skills and their shared reference files stay together:

```
/plugin marketplace add shashwatgtm/gtm-claude-skills
/plugin install gtm-skills@gtm-claude-skills
```

### Option C: Copy-paste (zero installation)

Open any `SKILL.md` file, copy the content, and paste it into Claude as context at the start of your conversation. Then ask your GTM question. You will get the same structured output.

---

## Quick Start (No Installation Needed)

Paste this into Claude right now:

```
I want you to diagnose my GTM motion using the EPIC Framework.

Score my company across four motions:
E (Ecosystem & ABM), P (Product-Led Growth), 
I (Inbound/Outbound), C (Community-Led Advocacy).

Here is my context:
- Company: [your company]
- Product: [what you sell]
- Stage: [seed/series A/B/C]
- Target buyer: [who buys]
- ACV: [average deal size]
- Deal cycle: [how long to close]
- NRR: [above or below 100%]
- Current GTM: [what you do today]
- Geography: [primary market]
- Biggest challenge: [what is not working]

Score each motion 1-10, tell me which should lead, 
and give me 3 actions for Monday morning.
```

---

## The Value Ladder

These skills are the free diagnostic layer. Here is how they connect to deeper tools:

| Layer | What | Where |
|-------|------|-------|
| **Free** (this repo) | 3 Claude Skills (diagnostic frameworks) | You are here |
| **Free** | 50 CRAFT templates (Notion Marketplace) | [notion.com/templates](https://www.notion.com/templates/ai-context-engineering-craft-framework) |
| **Free** | GTM Alpha scored report | [GTM Alpha](https://shashwatgtm.github.io/gtm-alpha-consultation/) |
| **Self-serve** | 6 MCP servers (tool-grade execution) | [@shashwatgtmalpha on NPM](https://www.npmjs.com/~shashwatgtmalpha) |
| **Consulting** | Fractional CMO engagement | [gtmhelix.com/about](https://gtmhelix.com/about/) |

---

## Frameworks

**EPIC** (Ecosystem, Product-Led Growth, Inbound/Outbound, Community) — GTM motion diagnosis

**IMPACT** (Identify Champions, Map Alternatives, Pinpoint Value, Anchor Market, Craft Message, Translate Execution) — Strategic positioning

**CRAFT** (Character, Result, Artifact, Frame, Timeline) — AI context engineering

---

## Claim ledger and delivery check (what runs on your computer)

From this version each skill ends every answer with a claim ledger: a small Python script in the skill's folder (`skills/<skill>/scripts/claim_ledger.py`, standard library only) that Claude runs on the exact text it will deliver (the chat reply and every saved file, Word, PowerPoint and Excel files included). It lists every sentence about you, your company, your customers, buyers or deals, a named company or a person, every figure and every label, and marks the lines that go past what you wrote, the pages Claude opened, the search results it labelled and the scripts' printed output. Claude fixes those lines (quotes your words, labels a search result, turns a guess into a question or a "[User to add: ...]" slot) and delivers exactly the text the last run printed. The script reads only the files Claude passes to it (a copy of your message, the page text and search results Claude saved in a scratch folder named ledger-check, the reply and the saved files), writes no file, makes no network call and reads no environment variable.

In Claude Code the plugin also installs a Stop hook (`hooks/hooks.json`, `hooks/delivery_check.py`, standard library only). When one of this plugin's skills ran its claim ledger in the current turn, the hook compares the reply Claude is about to send with the text the ledger last checked and sends Claude back (at most twice a turn) when they differ. It reads the hook input and the session transcript on your computer, keeps one small counter file per session next to the session transcript in Claude Code's own folder, sends nothing anywhere and makes no network call; its Python code reads no environment variable (the hook command in hooks.json uses ${CLAUDE_PLUGIN_ROOT}, the plugin folder Claude Code sets). It also sends Claude back when a file saved in the turn was not checked, and, in a conversation where one of this plugin's skills is in use, when a later answer about the same work (it shares words with your request) saves a file or says more than a short line without the ledger. To find saved files it looks at the names of files changed in your working folder during that turn (three levels down); it opens none of them. Hooks run in Claude Code only: in the Claude apps (claude.ai, desktop, mobile) there is no hook, and the skill's last step (the --final run) is the check. Because this plugin sits in a subfolder of its repository (`plugins/<name>/`), a directory reviewer may hold the hook for a manual look ("Scripts the validator couldn't follow"); that is a hold for review, not a block.

The tests for the script and the hook are in `tests/` at the repository root, outside the plugin folder; they are not installed with the plugin.

## For reviewers

What the shipped code does, for anyone reviewing this plugin (directory reviewers included). Everything below is checked in the files of this version.

- `skills/<skill>/scripts/claim_ledger.py` (the same file in every skill, Python standard library only) reads only the files Claude names on its command line: a copy of the user's message, the page text and search results Claude saved, the reply and the saved files (Word, PowerPoint and Excel files are opened as zip archives with the standard library and read as text). It writes no file, sends nothing, opens no network connection, starts no program and reads no environment variable.
- `hooks/delivery_check.py` (the Stop hook, Claude Code only, standard library only) reads the hook input on standard input and the session transcript file that input names, and writes one small counter file per session next to that transcript. It sends nothing, opens no network connection, starts no program and reads no environment variable; hooks.json runs it with `python3 -I` (isolated mode, so Python ignores PYTHON* variables and the user's site folder). The hook is new in the 1.2.x updates on purpose: it is the check that the reply the user receives is the text the claim ledger checked.
- Words a scanner may read as network or credential use, and why they are there (kept, because the behaviour needs them):
  - "export" and "exports" are ordinary words in the claim ledger's list of common words (as in "a CRM export"); the script never runs a shell command.
  - `curl https?://...` is part of a regular expression in the claim ledger that recognises an instruction planted in a pasted page or file (for example a hidden line telling an assistant to send data to an address), so the skill can tell the user and ignore it. It is text the script looks for, never a command it runs.
  - "curl" and "wget" in the hook are patterns that recognise a page Claude downloaded to read, so that file is treated as an input and not as a deliverable. The hook runs nothing.
- From this version the claim ledger reads Office files by element name, so it holds no web address at all, and Strict Open XML files are read like Transitional ones (before, a Strict file read as empty).

## Security

The skills are markdown instruction files plus one small Python script each (the claim ledger) and one Stop hook script for Claude Code, described in the section above. They make no API call and send no data anywhere. You can read every word before installing. They follow the [Agent Skills open standard](https://agentskills.io) published by Anthropic.

To report a security problem, email shashwat@gtmhelix.com with the subject "Security report: gtm-skills". Please do not open a public issue for it. The plugin sends no data anywhere.

---

## About

Shashwat Ghosh is a Fractional CMO and GTM Expert with 24+ years in B2B and 10+ years of fractional experience. Creator of the EPIC, IMPACT, and CRAFT frameworks. LinkedIn Top Product Marketing Voice, #10 India and #52 Worldwide (2024). VP Marketing, Happay: 161% ARR growth. 2x exit: to CRED ($180M+), then MakeMyTrip. VP Performance Marketing, Locus: $4.2M pipeline. Acquired by IKEA (Ingka Group) in Oct 2025.

- LinkedIn: [linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo](https://www.linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo/)
- Website: [gtmhelix.com/about](https://gtmhelix.com/about/)
- GTM Alpha: [shashwatgtm.github.io/gtm-alpha-consultation](https://shashwatgtm.github.io/gtm-alpha-consultation/)
- Twitter: [@Shashwat_Ghosh](https://twitter.com/Shashwat_Ghosh)

---

## License

Released under the MIT License. See [LICENSE](LICENSE) for the full terms. Copyright (c) 2026 Shashwat Ghosh / Helix GTM Consulting.

The EPIC, IMPACT, and CRAFT frameworks were created by Shashwat Ghosh / Helix GTM Consulting. As the MIT License requires, keep the copyright notice and permission notice in all copies or substantial portions of these skills. The shared operating principles in `plugins/gtm-skills/references/operating-principles.md` are adapted from the operating principles co-authored by Optise and Helix GTM Consulting.

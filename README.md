# Positioning and GTM Strategy

**Decide which go-to-market motion should lead, which category to own and what your core message is.** Three Claude skills for B2B founders, CMOs and product marketers, built on Shashwat Ghosh's IMPACT, EPIC and CRAFT methods. You give them your product, buyers, stage and market; you get the four motions scored with the one that should lead, a positioning and three level message hierarchy, and, with the third skill, vague AI prompts turned into specific ones.

The plugin also includes the four skills of B2B Deal Execution, for account executives, founders who sell, sales engineers and sales leaders. They help you decide whether a live deal is on track, what to ask on the next call, who else must be in the deal, what to concede on price and what to send next. You give them your own deal facts; you get a deal health score, a close plan, discovery questions, a buying group map, concession costs, a champion asset or an email sequence. The same four skills are also published on their own: https://github.com/shashwatgtm/b2b-deal-execution

This plugin runs in Claude Code and Claude Cowork. The same skills are also bundled in the Helix GTM Suite for Gemini CLI and Antigravity: https://github.com/shashwatgtm/helix-gtm-suite

Plugin page with install steps for Claude Code and Cowork, and real example outputs from each skill: https://tools.gtmhelix.com/plugins/gtm-skills/

Created by [Shashwat Ghosh](https://www.linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo/), Fractional CMO with 24+ years in B2B and 10+ years of fractional experience. VP Marketing, Happay: 161% ARR growth. 2x exit: to CRED ($180M), then MakeMyTrip. VP Global Performance Marketing, Locus: $4.2M pipeline. Acquired by IKEA (Ingka Group) in Oct 2025.

---

## Why These Skills?

EPIC, IMPACT and CRAFT are Shashwat Ghosh's original frameworks; they are not part of Claude's built-in skills.

The community marketplaces have generic GTM skills, but [Anthropic explicitly recommends](https://support.claude.com/en/articles/12512176-what-are-skills) using skills only from trusted sources. The 3 strategy skills are built on original frameworks by a practitioner with verified results at companies that got acquired. They contain no executable code: strategic reasoning you can audit in 5 minutes. The 4 Deal Execution skills add small Python scripts for the parts that must be exact (see Security below).

---

## The 7 Skills

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

### 4 to 7. Deal Execution
**Files:** `deal-review-and-close-plan/`, `discovery-and-buying-group/`, `negotiation-and-champion/`, `sales-sequences/`

**deal-review-and-close-plan** scores the health of one deal from your facts (champion, economic buyer, days in stage, competitors, blockers) by script, with every point shown and labelled, ranks the risks, checks the stage against its exit evidence, and gives dated next actions. It builds the mutual close plan with the buyer on a working day calendar and the 30, 60 and 90 day account plan.

**discovery-and-buying-group** writes discovery questions in the framework you use (MEDDPICC, BANT, SPICED, Challenger, Gap Selling), one question per pain you named, in your buyer's words, with an opening and a close for the call; and maps the buying group from the people you named: seats, concerns, the champion test and the seats still missing.

**negotiation-and-champion** helps you hold the price in a new deal. It works out what each concession costs on your own figures by script, pairs every concession with a trade, and gives you the words for the next conversation. It also writes your champion's internal asset in the champion's own voice (an email to their CFO, a memo, talking points) with one decision requested.

**sales-sequences** writes outbound and deal stage email sequences (cold outreach, warm follow up, post demo, proposal follow up, re-engagement, referral requests). Send days come from a script as example defaults, and your own days and number of emails always win; every claim appears once with its source.

Every Deal Execution skill keeps your figures exactly as you typed them, labels every number a script uses as an example default you can change, and never invents a buyer fact, a statistic or a competitor detail.

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
3. Upload each `SKILL.md` file (one at a time). For the 4 Deal Execution skills, upload the whole skill folder as a ZIP so its `references/` and `scripts/` files come with it
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
| **Free** (this repo) | 7 Claude Skills (3 diagnostic frameworks and 4 Deal Execution skills) | You are here |
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

## Security

The 3 strategy skills are markdown instruction files with no code. The 4 Deal Execution skills add small Python scripts (standard library only) for the parts that must be exact: deal_health.py, close_plan.py, concession_math.py and sequence_days.py. The scripts read only the values and files you give them, use no network and write no files of their own. Nothing is sent, scheduled or written to a CRM. You can read every word before installing. They follow the [Agent Skills open standard](https://agentskills.io) published by Anthropic.

To report a security problem, email shashwat@gtmhelix.com with the subject "Security report: gtm-skills". Please do not open a public issue for it. The plugin sends no data anywhere.

---

## About

Shashwat Ghosh is a Fractional CMO and GTM Expert with 24+ years in B2B and 10+ years of fractional experience. Creator of the EPIC, IMPACT, and CRAFT frameworks. LinkedIn Top Product Marketing Voice, #10 India and #52 Worldwide (2024). VP Marketing, Happay: 161% ARR growth. 2x exit: to CRED ($180M), then MakeMyTrip. VP Global Performance Marketing, Locus: $4.2M pipeline. Acquired by IKEA (Ingka Group) in Oct 2025.

- LinkedIn: [linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo](https://www.linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo/)
- Website: [gtmhelix.com/about](https://gtmhelix.com/about/)
- GTM Alpha: [shashwatgtm.github.io/gtm-alpha-consultation](https://shashwatgtm.github.io/gtm-alpha-consultation/)
- Twitter: [@Shashwat_Ghosh](https://twitter.com/Shashwat_Ghosh)

---

## License

Released under the MIT License. See [LICENSE](LICENSE) for the full terms. Copyright (c) 2026 Shashwat Ghosh / Helix GTM Consulting.

The EPIC, IMPACT, and CRAFT frameworks were created by Shashwat Ghosh / Helix GTM Consulting. As the MIT License requires, keep the copyright notice and permission notice in all copies or substantial portions of these skills. The shared operating principles in `plugins/gtm-skills/references/operating-principles.md` are adapted from the operating principles co-authored by Optise and Helix GTM Consulting.

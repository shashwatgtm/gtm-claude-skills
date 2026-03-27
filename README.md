# GTM Claude Skills Pack

**3 proprietary B2B go-to-market frameworks for Claude.** Diagnose your GTM motion, position your product, and structure every AI interaction for boardroom-grade outputs.

Created by [Shashwat Ghosh](https://www.linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo/), Fractional CMO with 24+ years B2B experience. Former VP Marketing at Happay (2x exit: CRED, MakeMyTrip) and Locus (acquired by Ingka Group/IKEA).

---

## Why These Skills?

There are 17 official Anthropic skills. None cover GTM strategy.

The community marketplaces have generic GTM skills, but [Anthropic explicitly recommends](https://support.claude.com/en/articles/12512176-what-are-skills) using skills only from trusted sources. These 3 skills are built on proprietary frameworks by a practitioner with verified results at companies that got acquired. They contain zero executable code. Pure strategic reasoning you can audit in 5 minutes.

---

## The 3 Skills

### 1. EPIC Motion Diagnostic
**File:** `epic-motion-diagnostic/SKILL.md`

Diagnose which B2B go-to-market motion should lead before choosing tactics or channels. Scores four motions (Ecosystem, Product-Led, Inbound/Outbound, Community) based on your stage, industry, geography, deal cycle, and NRR.

**Use when:** You are deciding between PLG vs. sales-led vs. community. Your funnel is not converting. You are about to hire your first marketing person and need to know what motion to build around.

**Includes:** Stage-based scoring defaults, 15+ adjustment rules, leaky bucket detection (NRR < 100%), AEO/GEO inbound disruption signals, industry overrides, geography adjustments.

### 2. IMPACT Quick Positioning
**File:** `impact-quick-positioning/SKILL.md`

Build a defensible market position and messaging hierarchy. Covers two steps of the six-step IMPACT Framework: Anchor Market (what category do you own) and Craft Message (10-word core → 30-second elevator → 2-minute narrative).

**Use when:** Your messaging feels generic. Buyers do not understand your category. You are preparing for an investor pitch. You need a positioning statement for your landing page.

**Includes:** Three positioning options (own existing category, create sub-category, create new category), decision framework, three-level messaging hierarchy template, and validation questions.

### 3. CRAFT Context Engineering Guide
**File:** `craft-context-engineering/SKILL.md`

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

```bash
# Clone the repo
git clone https://github.com/shashwatgtm/gtm-claude-skills.git

# Copy to your Claude Code skills directory
cp -r gtm-claude-skills/* ~/.claude/skills/
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
| **Consulting** | Fractional CMO engagement | [gtmexpert.com](https://www.gtmexpert.com) |

---

## Frameworks

**EPIC** (Ecosystem, Product-Led Growth, Inbound/Outbound, Community) — GTM motion diagnosis

**IMPACT** (Identify Champions, Map Alternatives, Pinpoint Value, Anchor Market, Craft Message, Translate Execution) — Strategic positioning

**CRAFT** (Character, Result, Artifact, Frame, Timeline) — AI context engineering

---

## Security

These skills contain zero executable code, zero scripts, zero API calls. They are pure markdown instruction files. You can read every word before installing. They follow the [Agent Skills open standard](https://agentskills.io) published by Anthropic.

---

## About

Shashwat Ghosh is a Fractional CMO and GTM Expert with 24+ years of B2B marketing experience. Creator of the EPIC, IMPACT, and CRAFT frameworks. Top 30 PLG Creator Worldwide (Favikon). Former VP Marketing at Happay and Locus.

- LinkedIn: [linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo](https://www.linkedin.com/in/shashwatghosh-ai-b2b-gtm-fractionalcmo/)
- Website: [gtmexpert.com](https://www.gtmexpert.com)
- GTM Alpha: [shashwatgtm.github.io/gtm-alpha-consultation](https://shashwatgtm.github.io/gtm-alpha-consultation/)
- Twitter: [@Shashwat_Ghosh](https://twitter.com/Shashwat_Ghosh)

---

## License

These skills are provided for personal and organizational use. The EPIC, IMPACT, and CRAFT frameworks are proprietary IP of Shashwat Ghosh / Helix GTM Consulting. Attribution required for any derivative work.

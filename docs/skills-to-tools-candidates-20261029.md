# Skills to deterministic tools: design candidates

29 October 2026. W2. Draft design only.

This review covers all 37 SKILL.md files across the nine repositories below. Each file was fetched in full through the GitHub connector at the stated default branch commit and read as source material. No skill workflow or repository script was executed. References and scripts named inside a skill are leads for a later implementation review, not evidence that their implementation was tested here.

Only narrow computations and parsers qualify. Inputs must contain the decisions, categories and evidence labels needed for the computation. A model must not silently supply them. Each result needs a versioned rule, traceable intermediate values and an exact test oracle. A score computes a chosen rule. It does not prove the rule predicts business outcomes.

Candidate labels below are design labels, not new registered tool names. Owners are proposed Helix MCP homes, not claims about their current capabilities. Sales candidates remain design notes while in review. This document authorizes no implementation or packaging.

## Coverage inventory

All tree responses had truncated=false. Discovery selected every path whose basename is SKILL.md. Source IDs below resolve to immutable paths and commits. Counts by repository are 3, 3, 5, 6, 4, 3, 4, 5 and 4, for 37 in total. No repository was inaccessible.

### gtm-claude-skills

Default branch: `main`. Commit: `9fea3be414e21879df969ba5f5a5e760266f6e54`.

- S01: [plugins/gtm-skills/skills/gtm-motion-picker/SKILL.md](https://github.com/shashwatgtm/gtm-claude-skills/blob/9fea3be414e21879df969ba5f5a5e760266f6e54/plugins/gtm-skills/skills/gtm-motion-picker/SKILL.md)
- S02: [plugins/gtm-skills/skills/positioning-and-messaging/SKILL.md](https://github.com/shashwatgtm/gtm-claude-skills/blob/9fea3be414e21879df969ba5f5a5e760266f6e54/plugins/gtm-skills/skills/positioning-and-messaging/SKILL.md)
- S03: [plugins/gtm-skills/skills/prompt-improver/SKILL.md](https://github.com/shashwatgtm/gtm-claude-skills/blob/9fea3be414e21879df969ba5f5a5e760266f6e54/plugins/gtm-skills/skills/prompt-improver/SKILL.md)

### b2b-sales-enablement

Default branch: `main`. Commit: `ba3e5b67b40a0a468c4c5ffecb6aaef7ea230993`.

- S04: [plugins/b2b-sales-enablement/skills/competitive-intelligence/SKILL.md](https://github.com/shashwatgtm/b2b-sales-enablement/blob/ba3e5b67b40a0a468c4c5ffecb6aaef7ea230993/plugins/b2b-sales-enablement/skills/competitive-intelligence/SKILL.md)
- S05: [plugins/b2b-sales-enablement/skills/meeting-prep-debrief/SKILL.md](https://github.com/shashwatgtm/b2b-sales-enablement/blob/ba3e5b67b40a0a468c4c5ffecb6aaef7ea230993/plugins/b2b-sales-enablement/skills/meeting-prep-debrief/SKILL.md)
- S06: [plugins/b2b-sales-enablement/skills/sales-proposal-builder/SKILL.md](https://github.com/shashwatgtm/b2b-sales-enablement/blob/ba3e5b67b40a0a468c4c5ffecb6aaef7ea230993/plugins/b2b-sales-enablement/skills/sales-proposal-builder/SKILL.md)

### b2b-customer-success

Default branch: `main`. Commit: `4ead2112e7ef4418a40f8aa9cab3108198114706`.

- S07: [plugins/b2b-customer-success/skills/account-health-check/SKILL.md](https://github.com/shashwatgtm/b2b-customer-success/blob/4ead2112e7ef4418a40f8aa9cab3108198114706/plugins/b2b-customer-success/skills/account-health-check/SKILL.md)
- S08: [plugins/b2b-customer-success/skills/onboarding-plan/SKILL.md](https://github.com/shashwatgtm/b2b-customer-success/blob/4ead2112e7ef4418a40f8aa9cab3108198114706/plugins/b2b-customer-success/skills/onboarding-plan/SKILL.md)
- S09: [plugins/b2b-customer-success/skills/qbr-prep/SKILL.md](https://github.com/shashwatgtm/b2b-customer-success/blob/4ead2112e7ef4418a40f8aa9cab3108198114706/plugins/b2b-customer-success/skills/qbr-prep/SKILL.md)
- S10: [plugins/b2b-customer-success/skills/renewal-save-plan/SKILL.md](https://github.com/shashwatgtm/b2b-customer-success/blob/4ead2112e7ef4418a40f8aa9cab3108198114706/plugins/b2b-customer-success/skills/renewal-save-plan/SKILL.md)
- S11: [plugins/b2b-customer-success/skills/upsell-and-expansion/SKILL.md](https://github.com/shashwatgtm/b2b-customer-success/blob/4ead2112e7ef4418a40f8aa9cab3108198114706/plugins/b2b-customer-success/skills/upsell-and-expansion/SKILL.md)

### optise-helix-aeo-skills

Default branch: `master`. Commit: `ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e`.

- S12: [plugins/optise-helix-aeo-toolkit/skills/optise-helix-aeo-tracker/SKILL.md](https://github.com/shashwatgtm/optise-helix-aeo-skills/blob/ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e/plugins/optise-helix-aeo-toolkit/skills/optise-helix-aeo-tracker/SKILL.md)
- S13: [plugins/optise-helix-aeo-toolkit/skills/optise-helix-bluf-writer/SKILL.md](https://github.com/shashwatgtm/optise-helix-aeo-skills/blob/ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e/plugins/optise-helix-aeo-toolkit/skills/optise-helix-bluf-writer/SKILL.md)
- S14: [plugins/optise-helix-aeo-toolkit/skills/optise-helix-eu-trust-centre/SKILL.md](https://github.com/shashwatgtm/optise-helix-aeo-skills/blob/ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e/plugins/optise-helix-aeo-toolkit/skills/optise-helix-eu-trust-centre/SKILL.md)
- S15: [plugins/optise-helix-aeo-toolkit/skills/optise-helix-fitq-audit/SKILL.md](https://github.com/shashwatgtm/optise-helix-aeo-skills/blob/ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e/plugins/optise-helix-aeo-toolkit/skills/optise-helix-fitq-audit/SKILL.md)
- S16: [plugins/optise-helix-aeo-toolkit/skills/optise-helix-prompt-pack-builder/SKILL.md](https://github.com/shashwatgtm/optise-helix-aeo-skills/blob/ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e/plugins/optise-helix-aeo-toolkit/skills/optise-helix-prompt-pack-builder/SKILL.md)
- S17: [plugins/optise-helix-aeo-toolkit/skills/optise-helix-race-audit/SKILL.md](https://github.com/shashwatgtm/optise-helix-aeo-skills/blob/ec239fa04df62fcdb0fd9bb79a3d20f6dfd4c26e/plugins/optise-helix-aeo-toolkit/skills/optise-helix-race-audit/SKILL.md)

### b2b-events-pr-and-launches

Default branch: `main`. Commit: `ea375e3d617e656a526e12f67b4976f6dd629205`.

- S18: [plugins/b2b-events-pr-and-launches/skills/event-follow-up-engine/SKILL.md](https://github.com/shashwatgtm/b2b-events-pr-and-launches/blob/ea375e3d617e656a526e12f67b4976f6dd629205/plugins/b2b-events-pr-and-launches/skills/event-follow-up-engine/SKILL.md)
- S19: [plugins/b2b-events-pr-and-launches/skills/event-planner/SKILL.md](https://github.com/shashwatgtm/b2b-events-pr-and-launches/blob/ea375e3d617e656a526e12f67b4976f6dd629205/plugins/b2b-events-pr-and-launches/skills/event-planner/SKILL.md)
- S20: [plugins/b2b-events-pr-and-launches/skills/event-speaker-kit/SKILL.md](https://github.com/shashwatgtm/b2b-events-pr-and-launches/blob/ea375e3d617e656a526e12f67b4976f6dd629205/plugins/b2b-events-pr-and-launches/skills/event-speaker-kit/SKILL.md)
- S21: [plugins/b2b-events-pr-and-launches/skills/pr-launch-pack/SKILL.md](https://github.com/shashwatgtm/b2b-events-pr-and-launches/blob/ea375e3d617e656a526e12f67b4976f6dd629205/plugins/b2b-events-pr-and-launches/skills/pr-launch-pack/SKILL.md)

### b2b-personal-branding

Default branch: `main`. Commit: `893624da965279be056610c9a1f51e95a7f53748`.

- S22: [plugins/b2b-personal-branding/skills/handcrafted-voice-audit/SKILL.md](https://github.com/shashwatgtm/b2b-personal-branding/blob/893624da965279be056610c9a1f51e95a7f53748/plugins/b2b-personal-branding/skills/handcrafted-voice-audit/SKILL.md)
- S23: [plugins/b2b-personal-branding/skills/newsletter-creation-curation/SKILL.md](https://github.com/shashwatgtm/b2b-personal-branding/blob/893624da965279be056610c9a1f51e95a7f53748/plugins/b2b-personal-branding/skills/newsletter-creation-curation/SKILL.md)
- S24: [plugins/b2b-personal-branding/skills/personal-branding-authority/SKILL.md](https://github.com/shashwatgtm/b2b-personal-branding/blob/893624da965279be056610c9a1f51e95a7f53748/plugins/b2b-personal-branding/skills/personal-branding-authority/SKILL.md)

### b2b-research-market-and-account

Default branch: `main`. Commit: `915bd73e5c665a04ecb89888bd10c3e52a892a54`.

- S25: [plugins/b2b-research-market-and-account/skills/account-research/SKILL.md](https://github.com/shashwatgtm/b2b-research-market-and-account/blob/915bd73e5c665a04ecb89888bd10c3e52a892a54/plugins/b2b-research-market-and-account/skills/account-research/SKILL.md)
- S26: [plugins/b2b-research-market-and-account/skills/claims-fact-check/SKILL.md](https://github.com/shashwatgtm/b2b-research-market-and-account/blob/915bd73e5c665a04ecb89888bd10c3e52a892a54/plugins/b2b-research-market-and-account/skills/claims-fact-check/SKILL.md)
- S27: [plugins/b2b-research-market-and-account/skills/evidence-research-asset/SKILL.md](https://github.com/shashwatgtm/b2b-research-market-and-account/blob/915bd73e5c665a04ecb89888bd10c3e52a892a54/plugins/b2b-research-market-and-account/skills/evidence-research-asset/SKILL.md)
- S28: [plugins/b2b-research-market-and-account/skills/second-opinion-review/SKILL.md](https://github.com/shashwatgtm/b2b-research-market-and-account/blob/915bd73e5c665a04ecb89888bd10c3e52a892a54/plugins/b2b-research-market-and-account/skills/second-opinion-review/SKILL.md)

### b2b-icp-and-customer-insight

Default branch: `main`. Commit: `fe8fbd84bcb46daf779dc24cca14bd7d6eee01f6`.

- S29: [plugins/b2b-icp-and-customer-insight/skills/buying-role-hypotheses/SKILL.md](https://github.com/shashwatgtm/b2b-icp-and-customer-insight/blob/fe8fbd84bcb46daf779dc24cca14bd7d6eee01f6/plugins/b2b-icp-and-customer-insight/skills/buying-role-hypotheses/SKILL.md)
- S30: [plugins/b2b-icp-and-customer-insight/skills/customer-interviews/SKILL.md](https://github.com/shashwatgtm/b2b-icp-and-customer-insight/blob/fe8fbd84bcb46daf779dc24cca14bd7d6eee01f6/plugins/b2b-icp-and-customer-insight/skills/customer-interviews/SKILL.md)
- S31: [plugins/b2b-icp-and-customer-insight/skills/icp-review/SKILL.md](https://github.com/shashwatgtm/b2b-icp-and-customer-insight/blob/fe8fbd84bcb46daf779dc24cca14bd7d6eee01f6/plugins/b2b-icp-and-customer-insight/skills/icp-review/SKILL.md)
- S32: [plugins/b2b-icp-and-customer-insight/skills/lead-scoring-model/SKILL.md](https://github.com/shashwatgtm/b2b-icp-and-customer-insight/blob/fe8fbd84bcb46daf779dc24cca14bd7d6eee01f6/plugins/b2b-icp-and-customer-insight/skills/lead-scoring-model/SKILL.md)
- S33: [plugins/b2b-icp-and-customer-insight/skills/pmf-check/SKILL.md](https://github.com/shashwatgtm/b2b-icp-and-customer-insight/blob/fe8fbd84bcb46daf779dc24cca14bd7d6eee01f6/plugins/b2b-icp-and-customer-insight/skills/pmf-check/SKILL.md)

### b2b-deal-execution

Default branch: `main`. Commit: `5822f07799d7a7a38f4c80e9359f493009e6ea7c`.

- S34: [plugins/b2b-deal-execution/skills/deal-review-and-close-plan/SKILL.md](https://github.com/shashwatgtm/b2b-deal-execution/blob/5822f07799d7a7a38f4c80e9359f493009e6ea7c/plugins/b2b-deal-execution/skills/deal-review-and-close-plan/SKILL.md)
- S35: [plugins/b2b-deal-execution/skills/discovery-and-buying-group/SKILL.md](https://github.com/shashwatgtm/b2b-deal-execution/blob/5822f07799d7a7a38f4c80e9359f493009e6ea7c/plugins/b2b-deal-execution/skills/discovery-and-buying-group/SKILL.md)
- S36: [plugins/b2b-deal-execution/skills/negotiation-and-champion/SKILL.md](https://github.com/shashwatgtm/b2b-deal-execution/blob/5822f07799d7a7a38f4c80e9359f493009e6ea7c/plugins/b2b-deal-execution/skills/negotiation-and-champion/SKILL.md)
- S37: [plugins/b2b-deal-execution/skills/sales-sequences/SKILL.md](https://github.com/shashwatgtm/b2b-deal-execution/blob/5822f07799d7a7a38f4c80e9359f493009e6ea7c/plugins/b2b-deal-execution/skills/sales-sequences/SKILL.md)

## Candidate contracts

All examples here are synthetic. No example describes a real account or person. Unless stated otherwise, reject nonfinite numbers, duplicate IDs, ambiguous units and malformed structures. Missing is distinct from zero. Return typed errors with field paths. Rule changes require a new rule version and new expected outputs.

### C01. Win and loss counts

Source: S04, Win/Loss Analysis Framework. Proposed owner: `revenue-enablement-mcp`.

Input: unique deal IDs, closed outcome enum, period and caller-assigned reason codes. Result: wins, losses, denominator, win rate and counts by reason. Rule: win_rate=100*wins/(wins+losses); count each deal once. Return null for a zero denominator. Exclude open deals explicitly and report their count. Sort tied reasons by reason code while preserving equal rank.

Synthetic oracle: 3 wins and 2 losses give 60%; two losses tagged price give price=2. An empty period gives null. Validation limit: the caller assigns reasons. The tool cannot explain why a deal was lost, research a competitor or write a battle card.

### C02. Office style metadata extraction

Source: S06, Brand Style Discovery, Path A1. Proposed owner: `revenue-enablement-mcp`.

Input: bounded PPTX or DOCX bytes and format enum. Result: explicit theme colour slots, declared fonts, page or slide dimensions and source XML member paths. Rule: parse the allowlisted OOXML parts without archive extraction, network access or external entity resolution. Preserve distinct theme, inherited and direct declarations rather than guessing a dominant style. Report absent declarations as missing.

Synthetic oracle: a PPTX theme declaring accent1=112233 and major Latin font=Test Sans returns those exact values and member paths. A ZIP entry named ../escape.xml is rejected. Validation limit: logos, visual prominence, PDF style estimation and brand matching require judgement. Byte limits, decompression limits and XML precedence need a later parser specification. No parser was built here.

### C03. Renewal milestone dates

Source: S10, Workflow Step 3. Proposed owner: `revenue-enablement-mcp`.

Input: renewal date and as_of as ISO calendar dates, plus a set of completed milestone IDs. Result: dates for the 180, 120, 90, 60 and 30 day milestones and the due, future or completed state of each. Rule: milestone_date=renewal_date-offset calendar days. Due means date<=as_of and not completed. Reject unknown completion IDs. These are milestone dates, not a renewal probability.

Synthetic oracle: renewal=2026-12-28 and as_of=2026-10-29 make the 60 day milestone due that day. Marking it complete clears its due state. Validation limit: this is a proposed exact calendar interpretation of the source cadence. It does not infer whether a conversation happened or recommend a save strategy. Holiday shifting is outside this contract.

### C04. AEO observation arithmetic

Source: S12, Workflow Step 4 and Section 5 formulas. Proposed owner: `craft-gtm-mcp`.

Input: rows keyed by prompt ID, week and engine, with mentioned boolean, prominence integer 1 to 4 when mentioned, and one or two competitor booleans. Result: per-prompt and per-week mention rate, mean prominence and competitor count delta, with denominators. Rule: 100*sum(mentioned)/row_count; sum(prominence)/sum(mentioned); sum(mentioned)-mean(competitor mention counts). Reject duplicate keys and incomplete competitor cells when delta is requested.

Synthetic oracle: 4 rows, 2 mentions at ranks 1 and 3, competitor counts 1 and 3 give 50%, 2 and 0. No mentions gives null prominence. Validation limit: the source calls mention rate citation rate although linked citations are separate. Preserve that distinction. No grades or working/dead classifications are proposed. Measurements and engine coverage must be supplied, never fabricated or gathered by paid calls.

### C05. Literal text checks

Sources: S13, Section 7 rule 4; S19, Steps 3 and 8; S21, Steps 3 and 6; S22, scan mode. Proposed owner: `craft-content-mcp`.

Input: Unicode text, explicit excluded spans for quotes, a versioned literal banned phrase list and caller-supplied field limits. Result: whitespace word counts, Unicode code point counts, U+2013 and U+2014 positions, literal phrase hits and limit violations. Rule: count nonempty whitespace tokens; count code points, not bytes; match whole phrases case-insensitively with declared word boundaries. Quote exclusions affect phrase hits only; report full-field counts separately.

Synthetic oracle: "Alpha beta" is 10 code points and 2 words. "Alpha\u2014beta" produces a dash hit at zero-based code point offset 5. A limit of 9 flags the first string. Validation limit: this checks explicit text rules. It cannot decide whether prose sounds human, detect AI authorship, interpret a metaphor or rewrite a voice.

### C06. Event funnel calculator

Source: S19, Step 5 and Example 1. Proposed owner: `craft-gtm-mcp`.

Input: event count, contacts per event, relevant share, stage conversion rates, cost per event, overall accepted-lead target and event contribution share. Result: total contacts, expected accepted leads, total cost, cost per accepted lead and target shortfall. Rule: multiply contacts through the caller's rates; target_for_events=target*event_share; shortfall=max(0,target_for_events-expected). Events needed=ceil(target_for_events/expected_per_event), when positive and computable. Do not round intermediate expected leads.

Synthetic oracle: one event, 12 relevant contacts, 50% then 50% conversion and cost 15000 give 3 accepted and cost per accepted=5000. Target 40 with share 25% gives shortfall 7 and 4 events needed. Validation limit: rates are assumptions, not forecasts. Zero accepted leads yields null unit cost. Positive target with zero conversion is an infeasible error, not zero events.

### C07. Research table coverage checks

Source: S25, Step 7 and Files this skill uses. Proposed owner: `icp-intelligence-mcp`.

Input: expected account IDs, expected field IDs, research rows and explicit banned domains. Result: missing account-field pairs, duplicate rows, invalid status/value combinations and banned-source hits. Rule: expected pairs minus observed pairs; exact account IDs only; compare parsed hostname to banned domain or its subdomains, never substring matches. Preserve original rows and return issue codes.

Synthetic oracle: expected accounts A and B, field HQ, only A/HQ observed gives missing=[B/HQ]. Source https://blocked.example/x is flagged for blocked.example; https://notblocked.example is not. Validation limit: source counts do not establish source independence or truth. This tool never upgrades a row to verified, resolves corporate aliases or researches an account.

### C08. Fixed benchmark aggregation

Source: S27, Workflow Step 6 and Example 4. Proposed owner: `gtm-alpha-secure`.

Input: unique criterion IDs with nonnegative finite points, unique entity-criterion rows with yes/no/unknown, evidence URL and caller-assigned evidence tier, plus cut labels and minimum base. Result: score sums, missing criteria, tier counts and cuts below the supplied minimum. Rule: sum points only for yes rows meeting the explicitly supplied tier policy. Unknown remains unknown. Reject duplicate criteria or evidence pairs rather than double counting.

Synthetic oracle: points Q1=2 and Q2=3, entity A yes/no, gives 2 of 5 with full coverage. A cut with base 2 and supplied minimum 3 is flagged low base. Validation limit: whether evidence supports yes, its quality and sample suitability remain human decisions. No company lookup, proprietary framework or causal ranking is included.

### C09. Structured number lock validation

Source: S27, Steps 3 and 7. Proposed owner: `craft-content-mcp`.

Input: approved lock rows with ID, decimal value, unit, base, period and approved display form; asset occurrences with lock ID and the same fields. Result: exact mismatch and unresolved-ID reports with asset offsets. Rule: compare decimal values and metadata field by field; an approved rounded form needs its own lock ID. This structured form deliberately avoids inferring a number's meaning from prose.

Synthetic oracle: lock L1=12.5 percent, base=survey-A, period=2026-Q3. An occurrence of 12.5 percent with base=survey-B fails base_match. 12 percent fails value_match. Validation limit: this does not extract every claim from a report or verify a publisher. Supplying correct occurrence metadata still needs review. This is narrower than the source's prose scanner and has an exact oracle.

### C10. Interview tallies

Source: S30, Workflow Steps 2b and 3. Proposed owner: `icp-intelligence-mcp`.

Input: unique interview IDs, role labels, caller-normalized item IDs and hypothesis verdict enums. Result: counts, shares, ties, role counts and hypothesis verdict counts. Rule: each item contributes at most once per interview; share=count/number_of_interviews. Keep tied items tied. Count unasked hypotheses separately from no_evidence. Return a small-sample flag for fewer than five interviews, as the source states.

Synthetic oracle: interviews [A,A,B], [A], [B] give A=2/3 and B=2/3, tied. They do not give A=3/3. Validation limit: merging phrases by meaning, assigning verdicts and choosing quotations remain caller decisions. Do not label a hypothesis confirmed. An empty set has null shares. This does not synthesize raw transcripts with hidden model judgement.

### C11. Intersection count bounds

Source: S31, Workflow Step 2. Proposed owner: `icp-intelligence-mcp`.

Input: integer total N and k>=2 marginal counts c_i, each between 0 and N. Result: minimum and maximum possible count meeting all criteria. Rule: lower=max(0,sum(c_i)-(k-1)*N); upper=min(c_i). Return bounds, not an invented overlap count. Reject negative counts, fractions and counts above N.

Synthetic oracle: N=100, counts 70 and 60 give [30,60]. Counts 70,60,50 give [0,50]. Validation limit: no independence assumption is valid without evidence. This cannot say which accounts fit or whether ICP categories are meaningful. It only bounds overlap from supplied margins.

### C12. Target gap arithmetic

Sources: S31, Step 3; S33, Steps 2 and 3. Proposed owner: `icp-intelligence-mcp`.

Input: metric ID, current value, target, better=higher/lower, unit and basis; optional business model. Result: met/behind/missing, raw gap, relative gap and tied largest relative gaps. Rule: higher gap=100*(target-current)/abs(current); lower gap=100*(current-target)/abs(current). NPS uses target-current points and is never ranked with percentages. Decide status from raw values before rounding. Zero current makes a needed relative increase undefined. Reject mismatched bases.

Synthetic oracle: current 18, target 30, higher gives 66.666...% needed; 95 to 60 lower gives 36.842...% reduction. NPS 10 to 30 gives 20 points. Validation limit: use only supplied targets. Activation is not applicable for services, connectivity and investment under S33. No PMF stage, benchmark, cause or ICP rewrite follows from the arithmetic.

### C13. Explicit fit scoring

Source: S32, Workflow Steps 3 and 4. Proposed owner: `icp-intelligence-mcp`.

Input: criteria with explicit weights, ordered values or explicit points, caller-set tier percentages and lead values. Result: per-criterion points, maximum, total and tier, or incomplete/pending. Rule for n>=2 graded values at position j: round_half_up(weight*(n-1-j)/(n-1)). Tier lower bounds are ceil(maximum*percent/100). Match values by case and spaces only, with a specified normalization policy. An unlisted value is pending; a missing value is incomplete. Neither receives a tier.

Synthetic oracle: weight 25 with three values gives [25,13,0]. Two criteria weighing 25 and 15 give maximum 40. Caller tiers [80,60,40] give A from 32. A raw number 4500 against a text band stays pending. Validation limit: the caller owns criteria, weights and mappings. No predictive accuracy, engagement scoring or CRM routing is claimed.

### C14. Concession arithmetic

Source: S36, Workflow Step 2. Proposed owner: `revenue-enablement-mcp`. Sales design note only.

Input: decimal contract value, discount percentage, currency and term, plus separately labelled caller-valued trades. Result: concession amount, discounted value and a separate scenario sum including priced trades. Rule: concession=value*discount/100; discounted=value-concession; scenario_sum=discounted+sum(priced_trades). Keep unpriced trades out of the sum and list them. Use decimal arithmetic and caller-specified currency precision; no exchange conversion.

Synthetic oracle: value 100000, discount 20%, trade valuation 5000 give 20000, 80000 and scenario_sum=85000. An unpriced case-study trade stays unpriced. Validation limit: a trade valuation is not booked revenue or ROI. No approval, walk-away price, negotiation recommendation or competitor price research is included. Reject percentages outside 0 to 100.

### C15. Sequence date calculation

Source: S37, Workflow Step 2. Proposed owner: `revenue-enablement-mcp`. Sales design note only.

Input: strictly increasing integer day offsets, explicit first_send or trigger_date, declared calendar zone and optional expected count. Result: dated sequence with original and moved dates. Rule: first_send mode uses first_send+(offset-first_offset) calendar days. Trigger mode uses trigger_date+offset days. Move Saturday/Sunday to Monday. If a moved date is not after the prior send, advance to the next working day. Refuse count mismatch. No email is sent or scheduled.

Synthetic oracle: first_send=2026-10-30, offsets [1,3,4] gives 2026-10-30, 2026-11-02 and 2026-11-03. Trigger=2026-10-30 and offset [1] gives 2026-11-02. Validation limit: local holidays and recipient consent are not inferred. Offsets are supplied, not recommended. This does not write persuasive emails or choose recipients.

### C16. Message length validation

Source: S02, Messaging Hierarchy and Anti-Hallucination Rules. Proposed owner: `impact-mcp`.

Input: three already-written strings labelled core, elevator and narrative. Result: whitespace word counts and length flags. Rule: core<=10 words; elevator target 60 to 80; narrative target 250 to 300, with a hard ceiling of 300. Report target misses separately from hard violations. Share the counting primitive with C05 instead of creating a second implementation.

Synthetic oracle: an 11 word core violates its ceiling; a 300 word narrative passes length; 301 fails. Validation limit: a short message can still be poor positioning. No category choice, buyer outcome judgement, jargon assessment, proof verification or copy generation is included.

## Grouped exclusions and review limits

- S01: do not turn the whole EPIC diagnostic into a tool yet. The priority text says referrals lead regardless of stage, while the additive scoring can leave another motion higher. The industry cap appears before additive adjustments but also as an override. Bounds are checked before later negative overrides. Natural language triggers and complexity-based tie breaks need judgement. These need an approved numeric contract before a score oracle is stable. The proposed future home would be gtm-alpha-secure; no candidate is accepted here.
- S02 and S03: positioning, category ownership, prompt diagnosis and prompt rewriting require judgement. C16 only checks lengths. A five-field form that repeats a prompt is not a computed strategy tool. No CRAFT prompt generator is proposed for craft-gtm-mcp.
- S04 to S06: battle cards, objections, meeting briefs, inferred buying signals and proposal narratives are subjective. C01 and C02 isolate counts and parsing. No research on prospects is needed for them.
- S07 to S11: account health, risk type, renewal probability, expansion readiness, onboarding customization and QBR narratives require evidence interpretation. S07's numeric Critical band also has a corroborating-signal gate. Summing points alone would misrepresent the workflow. C03 only computes cadence dates; it does not score health or probability.
- S12 to S17: no prompt generation, semantic FITq/RACE score, compliance declaration, voice matching or legal page drafting. Intent match, expertise and proof quality require judgement. FITq's field table and later scoring summary differ on individual credits. AEO mention counts do not prove linked citations. C04 and C05 stay within observable arithmetic and literal checks. Grade boundaries and minimum coverage rules need separate review before any classification.
- S18 to S21: event choice, follow-up specifications, consent decisions, launch claims, speakers' words and editorial priorities stay human work. Weights, stage rules and send timing must come from the user. C05 and C06 do not select those values or execute a journey.
- S22 to S24: voice judgement, newsletter selection, claim strength, personal brand positioning and rewriting stay subjective. Literal counts and phrase hits qualify under C05. A passing scanner is not evidence of human authorship or factual truth.
- S25 to S28: no automated truth verdict, source independence judgement, personality inference, second opinion, research narrative or study interpretation. C07 to C09 only validate explicit structures and aggregate accepted inputs. Prose extraction is not assumed complete.
- S29 to S33: role hypotheses, interview questions, semantic merging, causal diagnosis and ICP changes stay with reviewers. C10 to C13 compute only after those inputs are explicit. Fit scoring is separate from event engagement scoring.
- S34 to S37: champion tests, risk interpretation, deal stage mapping, close-plan phase allocation, negotiation advice and email drafting remain excluded. Deal-health points can compute a checklist but its input mapping and provisional Healthy label need a separate contract review. C14 and C15 remain sales design notes. No sales tool is implemented, enabled or submitted.

## Official documentation read

Read directly through the connected web tool on 29 October 2026:

- https://developers.openai.com/plugins/build/chatgpt-ui
- https://developers.openai.com/plugins/deploy/app-review

The .md variants failed with unsupported content type; the HTML pages opened. The UI guide describes MCP Apps metadata, the shared bridge and structured results. If a later authorized workstream adds UI, use _meta.ui.resourceUri, ui/initialize, notifications and tools/call, returning structuredContent with a useful text result. Use text/html;profile=mcp-app resources and an exact-domain CSP. The optional separate-render-tool example is outside the user's requested attachment pattern. No render tool is proposed here.

The review guide requires exact-domain CSP for UI and precise tests of actual advertised behavior. Reading it is not a submission or a compliance declaration. This work makes no server, endpoint, authentication, tool name, version, UI or package change. Text-only hosts remain unchanged.

## Review receipts and boundary audit

Base: main at 9fea3be414e21879df969ba5f5a5e760266f6e54. Branch: codex/skills-to-tools-20261029. Only repository change: docs/skills-to-tools-candidates-20261029.md. The delivery head SHA and draft PR URL are recorded in the handoff and PR metadata, since a file cannot contain the SHA of its own commit.

Repository instructions: read root CLAUDE.md and README.md at the base. The complete target tree contains no AGENTS.md, .github workflow, deployment configuration or executable build script. No parent AGENTS.md was present in /workspace or /. The user supplied the manual deployment register and authorized this branch and a draft PR. The write is limited to one docs file. No workflow is dispatched. The connector rejected the actions/workflows and deployments collection URLs as unsupported; the automation inspection therefore relies on the complete pinned tree and the user's register, not those API collections.

Remote shell check: `git ls-remote https://github.com/shashwatgtm/gtm-claude-skills.git HEAD` failed, exit 128. Cause: connection to configured proxy port 8080 refused. No network bypass was attempted. Branch discovery, trees, full source reads and delivery use the connected GitHub tools. Source links were verified by matching each pinned path and blob SHA against its complete tree and fetched bytes, rather than assuming that a URL string exists.

Cloud-only commands for design validation:

```text
python /workspace/work/w2/write_doc.py
python /workspace/work/w2/check_doc.py
git diff --no-index --check /dev/null /workspace/work/w2/draft/docs/skills-to-tools-candidates-20261029.md
```

Validation: 66 checks passed, 0 failed, 0 skipped. These include 37 pinned source blob/link checks and 29 structural or synthetic oracle checks. Runtime suites: 0 passed, 0 failed, 3 skipped (design only). Whitespace diff check passed. Source .md web fetch failures and the shell proxy failure are access receipts, not passing tests.

The formula checks use independent synthetic arithmetic. They do not execute the candidate tools or source skill scripts. Implementation tests, builds and browser checks are skipped as three suites: this is one documentation file with no runtime or UI. UI description: a Markdown review note with an inventory, 16 candidate contracts, exclusions, documentation links and receipts. No product screenshot applies.

Boundaries: no deploy command, DNS change, default branch write, force push, merge, ready-for-review transition, challenge file or headers edit, video change, endpoint/auth/version change, workflow dispatch, paid model call, shell MCP tool, package upload, skill installation, OpenAI package skill, directory submission, publication or legal declaration. No secret was read or written. Only synthetic test data is used. No client or prospect is named in this note. Existing skills and unrelated work remain untouched.

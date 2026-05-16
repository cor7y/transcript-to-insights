---
name: transcript-to-insights
description: >
  Analyze meeting/interview transcripts to extract structured research outputs: business context,
  user personas, behavioral archetypes, and insights.
  Use this skill whenever the user has qualitative research transcripts (meeting notes, user interviews,
  field research, stakeholder conversations) and wants to synthesize findings.
---

# Transcript-to-Insights Analysis

You are a qualitative research analyst. A transcript can yield up to four types of output — but not every transcript supports all four. Your first job is to assess what the material actually contains, then produce only what's grounded in the data.

**Four output types:**
1. **业务场景** — The operational reality: what the business does, how it works, what constraints it operates under
2. **用户画像** — Concrete profiles of the people: who they are, what they do day-to-day, what tools they use, what frustrates them
3. **行为原型** — Abstract behavioral patterns: how people relate to change, authority, risk, and technology
4. **洞察** — Non-obvious interpretations: tensions, contradictions, and unmet needs that explain WHY things are the way they are

---

## Step 0: Assess what the transcript supports

Before producing any output, read the transcript and ask:

- Does it describe the business's operations, systems, or processes in enough detail? → **业务场景** is viable
- Do speakers describe their own work, tools, or daily reality in enough detail? → **用户画像** is viable
- Are there enough speakers (or enough behavioral richness in one speaker) to identify a meaningful pattern? → **行为原型** is viable
- Are there surprising statements, contradictions, or tensions that go beyond what's obvious? → **洞察** is viable

**If a section isn't supported by the material, skip it entirely.** Don't produce thin outputs to fill a template. A note like "本次转录不足以支撑用户画像" is more useful than a fabricated profile.

---

## 业务场景 (Business Context)

Describe the operational reality as it emerges from the transcript. This is factual and descriptive — what is actually happening, not what should be happening.

**What to capture:**
- Core business activity and what success looks like for them
- Key workflows or processes mentioned (especially the ones that are broken or manual)
- Systems and tools currently in use
- Structural constraints: org structure, decision-making flow, accountability gaps
- Where technology fits (or doesn't) in their current reality

**What to avoid:**
- Don't describe the industry in general — describe *this* organization as revealed in *this* transcript
- Don't fill gaps with assumptions; if something wasn't mentioned, don't include it

**Output format:**
```
## 业务场景

**核心业务：** [What they do and what operational success means to them]

**关键流程：** [The workflows that came up — especially broken or manual ones]

**现有系统与工具：** [What they're using now]

**结构性约束：** [Org, decision-making, accountability structures that shape behavior]

**技术现状：** [Where digital/AI fits in their current reality — or why it doesn't]
```

---

## 用户画像 (User Personas)

Concrete profiles grounded in what speakers explicitly said about their work. One persona per distinct role or perspective in the transcript.

The difference from archetypes: a persona describes *who this person is and what their work looks like*. An archetype describes *how they behave in relation to change or technology*. A transcript might support one without the other.

**What to capture:**
- Role and position in the organization (use what was said, not inferred titles)
- Daily workflow: what do they actually do? What takes most of their time?
- Tools and systems they interact with
- Pain points: what slows them down, frustrates them, or creates risk for them
- Goals: what are they trying to achieve in their work?

**What to avoid:**
- Don't invent workflow details that weren't mentioned
- Don't conflate two speakers into one persona if their situations differ
- Don't describe what they're "responsible for" in org-chart language — describe what they actually do

**Output format:**
```
## 用户画像

### [Role label — descriptive, not a job title]
**身份：** [Their position and context in the organization, as described]
**日常工作：** [What they actually do — the tasks, the rhythm, the tools]
**痛点：** [What frustrates them or creates friction in their work]
**目标：** [What they're trying to achieve — immediate and longer-term]
**信息来源：** [Where they get information to make decisions, if mentioned]
```

---

## 行为原型 (Behavioral Archetypes)

Abstract behavioral patterns — how people relate to change, authority, risk, and technology. More interpretive than personas; requires enough behavioral signal to generalize.

An archetype is NOT a job title with a description. It is a behavioral pattern — a way of relating to the world.

**Bad archetype:**
> 发言人2 — 负责参观引导，了解公司整体情况

**Good archetype:**
> **The Translator** — Sits at the boundary between management directives and floor reality. Doesn't make decisions but controls what information flows in each direction. Primary concern: maintaining credibility with both sides without being blamed when things go wrong.

**When to skip archetypes:** If there's only one speaker and their behavioral pattern isn't rich enough to generalize, or if all speakers behave similarly (no meaningful variation), skip this section.

### Archetype modeling process

**Step 1: Define behavioral axes** — Identify 2–3 dimensions where you actually see variation across participants. Examples for factory/AI research:
- Relationship to new technology: Eager adopter ↔ Proven-first skeptic
- Decision-making authority: Autonomous ↔ Approval-dependent
- Risk posture: Protect current state ↔ Willing to experiment

**Step 2: Map speakers** — For each speaker, note their position on each axis with direct evidence.

**Step 3: Cluster** — Group speakers with similar behavioral profiles. Aim for 3–5 archetypes.

**Step 4: Name** — Name by behavioral trait or role in the system, not job title. The name should be immediately evocative.

Common naming patterns:
- By role in the system: The Gatekeeper, The Translator, The Operator
- By relationship to change: The Pragmatist, The Skeptic, The Champion
- By decision style: The Optimizer, The Risk-Avoider, The Delegator

**Output format:**
```
## 行为原型

### [Archetype Name]
**核心动机：** [What drives their decisions — not their job KPI, but their underlying concern]
**典型行为：** [How they act in the context of the research topic — specific, observable]
**对变化的态度：** [How they respond to new tools, processes, or ideas]
**核心张力：** [The central unresolved conflict or need this archetype carries]
**依据：** [Which speakers, what they said]
```

---

## 洞察 (Insights)

Non-obvious interpretations that explain WHY things are the way they are. Not summaries — interpretations.

**Bad insight** (summary):
> "Users said they use Excel to track production data."

**Good insight** (interpretation):
> "Operators cling to familiar tools even when they know better options exist — the switching cost isn't technical, it's the fear of being exposed as incompetent during the learning curve."

The test: *Would a smart person who wasn't in the room be surprised by this?* If the insight is obvious from the job title or industry, it's a description, not an insight.

### Insight extraction process

1. **First pass** — Flag notable moments: surprising statements, contradictions, emotional language, workarounds, complaints, moments of pride or frustration
2. **Cluster** — Group observations that share an underlying tension or root cause
3. **Synthesize** — For each cluster, write ONE insight. Start with the interpretation, not the evidence
4. **Quality filter** — Apply the "so what?" test: Does it point to a design opportunity or strategic implication? Is it specific to this context? Would it change how you'd design something? If no to all three, cut or merge

**Target: 5–8 insights per session.** More than that means you're summarizing, not synthesizing.

**Output format:**
```
## 洞察

### [Short memorable label]
[One sentence: the core observation, stated as a non-obvious truth about behavior, motivation, or tension]

**依据：** [2–3 specific quotes or behaviors, with speaker reference]
**含义：** [What this means for product design, strategy, or the next research question]
```

---

## Context-specific guidance: factory / industrial B2B

When analyzing manufacturing or industrial B2B research, watch for:

**Common behavioral axes:**
- Relationship to digital/AI tools (distrust of "black box" vs. curiosity)
- Proximity to production floor (hands-on operator vs. management layer)
- Accountability structure (who gets blamed when things go wrong)
- Time horizon (immediate production pressure vs. long-term transformation)

**Common archetypes in this context:**
- **The Pragmatist**: "Show me it works on my line, then we'll talk." Not resistant to change — resistant to unproven change.
- **The Gatekeeper**: Controls information flow between management and floor. Primary concern: not being caught in the middle.
- **The Champion**: Wants transformation but lacks authority. Compensates by building internal coalitions.
- **The Operator**: Focused on immediate task completion. Has the most granular knowledge of actual workflows.

These are starting points — derive archetypes from the data, not from this list.

---

## Isolation rule

When working with multi-session research, analyze each session independently. Don't let one session's archetypes or business context contaminate another's.

---

## Output checklist

Before presenting results:
- [ ] Skipped any section where the transcript didn't provide enough material (and noted why)
- [ ] 业务场景 describes *this* organization, not the industry in general
- [ ] 用户画像 describes what people actually do, not what they're "responsible for"
- [ ] Archetypes are named by behavioral trait, not job title; each has a "核心张力"
- [ ] Insights are interpretations (reveal WHY or a tension), not summaries
- [ ] Insight count is 5–8; each has specific evidence and an implication

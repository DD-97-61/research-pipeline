# Routine #12: Research Gap 综合分析

**Schedule:** Daily 4:00 PM
**Repos:** windsurf
**Connectors:** Slack

---

## Prompt

You are a senior research strategist. Your task is to synthesize findings across all literature radar routines from the past 7 days and identify the most promising research gaps. Unlike individual radar routines that report papers one by one, you take a bird's-eye view: What patterns emerge? What questions keep appearing? What intersections are underexplored?

### Input — Read All Radar Files (Last 7 Days)

Scan all files in `research_pipeline/literature_radar/` from the past 7 days:
- `*_branding_core.md`
- `*_ai_brand.md`
- `*_brand_international.md`
- `*_brand_competitiveness.md`
- `*_social_media_consumer.md`
- `*_working_papers.md`

Also read the previous gap synthesis reports: `research_pipeline/idea_factory/YYYY-MM-DD_gap_synthesis.md` (last 3 reports if available).

### Analysis Framework

Perform three levels of analysis:

**Level 1 — Within-stream gaps:**
For each research stream (branding, AI×brand, internationalization, competitiveness, social media):
- What topics appear repeatedly? (indicates active interest)
- What topics are mentioned as "future research" by multiple authors?
- Where do recent papers disagree? (conflicting findings = research opportunity)

**Level 2 — Cross-stream gaps (highest value):**
Look for gaps at the INTERSECTION of two or more streams:
- Branding × AI: How does AI-generated content affect brand equity? (is this studied?)
- Internationalization × Social media: How do brands use social media differently in home vs. foreign markets?
- Competitiveness × AI: Can AI tools predict brand competitive dynamics?
- Social media × Internationalization: Cross-border social media branding strategies
- Any other intersections that emerge from the data

**Level 3 — Methodological gaps:**
- Are there topics studied only with experiments/surveys that could benefit from secondary data approaches?
- Are there contexts studied only in Western markets that need Chinese market evidence?
- Are there theories tested only with one DV that could be enriched with multi-dimensional outcomes?

### Output Format

```markdown
# Research Gap Synthesis — YYYY-MM-DD (Week of MM-DD to MM-DD)

## Executive Summary
[3-5 sentences: what's hot, what's missing, where are the biggest opportunities]

## Top 5 Research Gaps This Week

### Gap #1: [Descriptive title]
- **Type:** within-stream / cross-stream / methodological
- **Streams involved:** [which research areas]
- **Evidence:** [which papers point to this gap — cite 2-3 specific papers from radar files]
- **Why it matters:** [theoretical and practical significance]
- **Why it's doable:** [what makes this feasible with secondary data]
- **Estimated competition:** [Low / Medium / High — based on how many working papers address this]
- **Priority:** [A / B / C]

### Gap #2: ...
[same format]

## Emerging Trends
[What directions seem to be gaining momentum? These aren't gaps yet but could become important]

## Gaps Carried Forward
[Gaps from previous synthesis reports that are still unaddressed — update status]

## Gaps Resolved
[Gaps from previous reports that new publications have now addressed — remove from active tracking]
```

### Save Results

Save to: `research_pipeline/idea_factory/YYYY-MM-DD_gap_synthesis.md`

### Slack Notification

Send to channel `C0ATR6EDGF3`:

```
[Research Gap综合] YYYY-MM-DD
本周分析 N 篇论文，识别 5 个关键gap

Top 3 gaps:
1. [Priority A] [Title] — [type] — [why it matters in one sentence]
2. [Priority A/B] [Title] — ...
3. [Priority B] [Title] — ...

新兴趋势: [one sentence]
详情: research_pipeline/idea_factory/YYYY-MM-DD_gap_synthesis.md
```

### Important Rules

- Cross-stream gaps are almost always more valuable than within-stream gaps. Prioritize intersections.
- Be honest about competition level. If 5 working papers already address a gap, it's not a gap anymore.
- Every gap must have evidence from specific papers in the radar files. No speculative gaps.
- Compare with previous synthesis reports to show evolution — are gaps opening or closing?
- Before saving, ensure directories exist: `mkdir -p research_pipeline/idea_factory`
- Git workflow: create branch `claude/ideas-YYYY-MM-DD` if not exists, commit with the specified message, push to origin.
- If the branch already exists (from earlier routines today), reuse it and add a new commit.

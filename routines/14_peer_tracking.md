# Routine #14: 同行/竞争者 追踪

**Schedule:** Daily 6:00 PM
**Repos:** windsurf
**Connectors:** Slack

---

## Prompt

You are a competitive intelligence analyst for academic research. Your task is to monitor what active researchers in branding, marketing, and related fields are publishing, presenting, and working on. This helps avoid duplicating someone else's ongoing work and also provides inspiration.

### Monitoring Targets

**Tier 1 — Direct competitors (co-branding / brand collaboration researchers):**
Search Google Scholar for recent publications by researchers who have published on co-branding, brand alliances, or brand collaboration in top journals in the past 3 years.

**Tier 2 — Method innovators (computational marketing):**
Search for researchers who apply NLP, ML, causal inference, or computational methods to marketing/consumer behavior.

**Tier 3 — Domain leaders (branding, social media marketing):**
Search for prolific/highly-cited researchers in brand management, social media marketing, consumer engagement.

### Search Process

1. Search Google Scholar for recent papers (last 7 days) by known active researchers in these areas
2. Search for new papers citing key foundational works in co-branding (e.g., Simonin & Ruth 1998, Helmig et al. 2008)
3. Check conference programs: AMA, ACR, EMAC, CIST, INFORMS Marketing Science (if any upcoming/recent)
4. Search for recent PhD dissertations on branding topics (these signal emerging researchers and fresh directions)
5. Check for new research grants announced (NSF, NSFC for China) related to branding/marketing

### Output Format

```markdown
# Peer Tracking Report — YYYY-MM-DD

## New Publications by Active Researchers

### [Author Name] — [Affiliation]
- **Paper:** [Title]
- **Venue:** [Journal/Conference]
- **Topic:** [brief description]
- **Overlap with our interests:** [High/Medium/Low — explain]
- **Implication for us:** [does this affect any of our ideas? preempt or complement?]

## Conference Activity
[Any upcoming presentations, special sessions, or calls for papers relevant to our streams]

## New Citing Papers
[Papers that cite foundational co-branding/brand collaboration works — these are our closest competitors]

## PhD Dissertations
[New dissertations on branding/marketing topics — signals where the next generation is heading]

## Grant Activity
[New funded projects in our domain — indicates institutional investment in certain directions]

## Competitive Landscape Summary
- **Getting crowded:** [topics where many people are publishing — higher competition]
- **Still open:** [topics with few active researchers — lower competition, potential opportunity]
- **New entrant alert:** [any new researcher or team entering our space]
```

### Save Results

Save to: `research_pipeline/idea_factory/YYYY-MM-DD_peer_tracking.md`

### Slack Notification

Send to channel `C0ATR6EDGF3`:

```
[同行追踪] YYYY-MM-DD

新发现:
- [Author] published on [topic] in [venue]
- ...

竞争态势:
- 拥挤领域: [list]
- 机会窗口: [list]

详情: research_pipeline/idea_factory/YYYY-MM-DD_peer_tracking.md
```

If a competitor publishes something directly overlapping with our DEVELOP ideas: Add "ALERT: [Author] published on [topic] — 与IDEA-XXX高度重叠，建议评估"

### Important Rules

- Only report verified publications with actual links/DOIs.
- Don't list every paper by famous scholars — only papers relevant to our research streams.
- The most valuable output is the "overlap with our interests" assessment — be specific about which of our ideas might be affected.
- Update idea_portfolio.md if a competitor publication makes an idea less viable (change status to HOLD or ABANDON with reason).
- Commit output with message: "track: peers YYYY-MM-DD"

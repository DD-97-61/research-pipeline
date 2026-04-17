# Routine #2: AI × Brand 前沿雷达

**Schedule:** Daily 7:30 AM
**Repos:** windsurf
**Connectors:** Slack

---

## Prompt

You are a research assistant tracking the intersection of artificial intelligence and branding/marketing. Your daily task is to find the latest papers exploring how AI technologies are reshaping brand management, consumer behavior, and marketing strategy.

### Search Scope

**Target journals & venues:**
- Marketing Science, JMR, JCR, JM, JAMS (marketing top journals)
- MISQ, ISR (IS journals publishing AI-marketing work)
- Journal of Interactive Marketing, International Journal of Research in Marketing
- Computers in Human Behavior, Technological Forecasting and Social Change
- arXiv (cs.AI, cs.CL sections with marketing applications)

**Keywords (search each):**
- AI branding / artificial intelligence brand / AI marketing strategy
- AI-generated content (AIGC) brand / LLM consumer behavior
- AI endorser / virtual influencer / AI spokesperson
- algorithmic marketing / algorithmic recommendation brand
- ChatGPT marketing / generative AI advertising
- machine learning brand perception / NLP brand analysis
- AI personalization / AI customer experience

**Time range:** Last 7 days; expand to 14 if nothing found.

### Search Process

1. Google Scholar search for each keyword group
2. Check arXiv cs.AI and cs.CL for new preprints mentioning "brand" or "marketing"
3. Check SSRN Marketing eJournal for AI-related working papers
4. Cross-reference to remove duplicates

### Output Format

For each paper:

```markdown
### [Paper Title]
- **Authors:** [names]
- **Venue:** [journal/conference/preprint] | **Year:** [year]
- **AI technology involved:** [LLM / computer vision / recommender system / NLP / etc.]
- **Brand/marketing application:** [what branding problem it addresses]
- **Abstract summary:** [2-3 sentences]
- **Methodology:** [method used]
- **Key findings:** [1-2 sentences]
- **Potential for our research:** [how this could inspire new research ideas for us]
- **Relevance:** [1-5 stars]
```

### Save Results

Save to: `research_pipeline/literature_radar/YYYY-MM-DD_ai_brand.md`

### Slack Notification

Send to channel `C0ATR6EDGF3`:

```
[AI×Brand雷达] YYYY-MM-DD
发现 N 篇新论文

Top findings:
1. [Title] — [Venue] — [AI tech]: [one-line summary]
2. ...

详情: research_pipeline/literature_radar/YYYY-MM-DD_ai_brand.md
```

### Important Rules

- Only include papers you can verify exist. Never fabricate citations.
- This is a fast-moving field — preprints and working papers are welcome, but label them clearly.
- Pay special attention to papers that combine AI methods with secondary/observational data (not just lab experiments).
- Before saving, ensure directories exist: `mkdir -p research_pipeline/literature_radar`
- Git workflow: create branch `claude/radar-YYYY-MM-DD` if not exists, commit with the specified message, push to origin.
- If the branch already exists (from earlier routines today), reuse it and add a new commit.

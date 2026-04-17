# Routine #7: IS 计算方法 扫描

**Schedule:** Daily 11:00 AM
**Repos:** windsurf
**Connectors:** Slack

---

## Prompt

You are a research methodology scout. Your task is to find new computational and quantitative methods published in Information Systems journals that could be borrowed and applied to marketing/branding research. The goal is cross-disciplinary method transfer — finding analytical tools from IS that marketing scholars haven't widely adopted yet.

### Search Scope

**Target journals:**
- MIS Quarterly (MISQ)
- Information Systems Research (ISR)
- Journal of Management Information Systems (JMIS)
- Decision Support Systems (DSS)
- Journal of the Association for Information Systems (JAIS)
- Information & Management
- European Journal of Information Systems (EJIS)
- Journal of Strategic Information Systems

**Keywords — method-focused:**
- text mining / text analytics / topic modeling / sentiment analysis
- deep learning / neural network / transformer model (applied to business)
- causal inference / causal machine learning / treatment effect estimation
- network analysis / social network / graph analytics
- natural language processing / NLP / large language model application
- computer vision / image analysis (for business/marketing)
- time series / panel data / longitudinal analysis (new approaches)
- ensemble methods / random forest / gradient boosting (applied to behavior)
- design science / computational design / algorithmic decision

**Time range:** Last 7 days; expand to 14 if nothing found.

### Search Process

1. Check each journal's latest issue / online-first page
2. Google Scholar search for method keywords within these journals
3. Focus on METHODOLOGY sections — what is the analytical approach, not just the topic

### Output Format

For each paper:

```markdown
### [Paper Title]
- **Authors:** [names]
- **Journal:** [journal] | **Year:** [year]
- **Method introduced/used:** [specific method name and brief description]
- **Original application context:** [what IS problem it was applied to]
- **Potential marketing application:** [how this method could be used in branding/consumer research]
- **Data requirements:** [what type of data does this method need]
- **Compatible with secondary data?** [Yes / No / Partially — explain]
- **Technical complexity:** [Low / Medium / High — for a marketing researcher to implement]
- **Key innovation:** [what makes this method better than existing alternatives]
- **Relevance for us:** [1-5 stars]
```

### Save Results

Save to: `research_pipeline/methods_arsenal/YYYY-MM-DD_is_methods.md`

### Slack Notification

Send to channel `C0ATR6EDGF3`:

```
[IS方法扫描] YYYY-MM-DD
发现 N 个潜在可用方法

Top methods:
1. [Method name] — from [Journal] — [potential marketing application]
2. ...

详情: research_pipeline/methods_arsenal/YYYY-MM-DD_is_methods.md
```

### Important Rules

- Only include verified papers. Never fabricate citations.
- Focus on METHOD novelty, not topic relevance. A paper about healthcare IT is relevant if its method could work for brand text analysis.
- Explicitly evaluate whether the method can work with observational/secondary data. Methods requiring controlled experiments are low priority.
- Note the programming language/tools needed (Python, R, specific packages).
- Commit output with message: "methods: is-computational YYYY-MM-DD"

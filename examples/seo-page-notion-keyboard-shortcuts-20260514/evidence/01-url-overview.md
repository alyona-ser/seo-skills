# 01 — URL overview

Tool: `mcp__claude_ai_SE_Ranking__DATA_getUrlOverviewWorldwide` · Input: `url=https://www.notion.com/help/keyboard-shortcuts`, `fields=keywords,traffic,price`

**Status:** SE Ranking MCP authentication unavailable in this session. The tool returns `Missing API_TOKEN` for every call. Re-run `/seo-page https://www.notion.com/help/keyboard-shortcuts` from a session where the SE Ranking MCP server has been authenticated (`mcp__plugin_seo-skills_se-ranking__authenticate`) to populate this evidence file with the live response.

Expected shape (per SKILL.md step 2):
```
{
  "keywords_total": <int>,
  "traffic_estimate": <int>,
  "paid_keywords": <int>,
  "paid_traffic": <int>,
  "top_regions": [<region_obj>]
}
```

What this number means for the verdict: the traffic estimate plus keyword count establish whether the page is a high-leverage asset (justifies REFRESH investment) or a low-traffic page (consider KILL). Given the live SERP probes show this URL holding **position 1** for three head queries with substantial demand, the qualitative read is "high leverage" — but the exact monthly number is owed to a re-run.

# Next Week Plan — Week 16, 2026 (13–19 Apr)

## Blog Post

**Topic**: From Ratings to Revenue
**Slug**: from-ratings-to-revenue
**Language**: English
**Priority**: High

**Why this topic**:
- The case study was freshly published on 8–9 Apr 2026.
- A full 24-chart dashboard and AI assistant are already live — the blog post is the missing piece that drives organic and CH-B lead traffic.
- Writing now while the case study is new maximises the content cluster effect (case study + dashboard + AI assistant + blog + LinkedIn).
- No blog post exists for this slug yet.

**Next steps**:
1. Run `pau-analytics-blog-write` skill with source: `case-study/from-ratings-to-revenue.html`
2. Save draft to `blog/drafts/from-ratings-to-revenue-en.md`
3. Run `new-pau-analytics-blog-publish` to publish to the site
4. Run `linkedit-post-writer` on the published blog post to generate a LinkedIn draft

---

## LinkedIn

**Status**: No drafts exist. LinkedIn posting has not started.
**Action**: After the blog post above is written, run `linkedit-post-writer` to create the first LinkedIn draft.
**Target post date**: Wednesday 22 Apr (next week's Buffer slot)

---

## Lead Pipeline

**Action**: Run `/check-leads` from a local Claude Code session to get real lead data.
The Railway API is blocked in the cloud environment — use desktop app or CLI on your machine.

---

## Content Queue

Run `content-scheduler` after this week's blog post is published to queue the topic for the week after.

---

*Generated: 17 Apr 2026 — Week 15 coordinator report*

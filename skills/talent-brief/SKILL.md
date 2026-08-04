---
name: talent-brief
description: Use when the user provides Feishu/Lark interview notes, meeting transcripts, PDF or text resumes, chat notes, candidate summaries, or prior recommendation blurbs and asks to draft, revise, calibrate, or accumulate a Chinese candidate recommendation brief for founders, HRDs, or hiring groups.
---

# Talent Brief

## Overview

Turn messy candidate conversation notes into a short Chinese talent brief that can be forwarded to founders, HRDs, or hiring groups.

Default to a group-ready brief: concise, natural, privacy-safe, and directly usable. Do not turn the brief into a candidate scorecard, interview evaluation, or matching report.

## Required Reference

Before drafting, revising, or calibrating, read `references/style-guide.md`.

## Source Handling

- Read every supplied source before drafting. For a PDF resume, extract the full text and inspect the rendered layout only when text order or section ownership is unclear.
- When both a resume and conversation notes are available, use the resume for dates, total experience, employers, titles, projects, and metrics; use the conversation for current status, role preference, base, motivation, and evidenced working style.
- Treat the user's added judgment, target company, target JD, and recommendation context as explicit editorial input. Use them to select, order, or omit facts rather than treating every request as a generic group brief.
- If sources conflict, prefer the latest explicit statement for current status. For unresolved factual conflicts, omit the claim or add one `建议补问` line.
- Never retain the resume, transcript, or identifying details in the skill.

## Modes

### Draft Mode

Use when the user provides Feishu/Lark records, interview notes, a resume fragment, or mixed candidate material and asks for a recommendation.

1. Decide the audience before selecting facts: generic founder/HRD group or a specific company/JD. For a specific target, front-load evidence that answers why the candidate fits that role.
2. Choose the opening by career stage. For experienced candidates, use total experience plus current employer/responsibility. For students, recent graduates, or candidates in their first short full-time role, lead with graduation cohort and strongest education, then state the current role.
3. Use actual employer names and the specific business, team, or project supported when the user indicates they are shareable. Prefer `在<公司>支持<具体业务>` over `在500强/大厂任职`.
4. If exact years are unavailable, start with concrete employer and role facts. Do not substitute vague seniority phrases such as `多年经验`、`长期深耕`、`资深`.
5. Keep employer, duration, title, and responsibility associations exact. Do not attach a role or capability to a company unless the source explicitly links them.
6. Add at most one or two target-relevant proof points, prioritizing direct work, projects, ownership, measurable results, and useful talent-domain coverage over broad interpretation.
7. For early-career candidates, keep one strongest pre-graduation experience category by default. Omit internship counts, employer names, and project details unless they materially improve the match, using phrasing such as `毕业前有过一级投资机构实习经历`.
8. For AI, embodied-intelligence, robotics, or other technical HR roles, prioritize algorithm/R&D hiring experience, supported technical teams, senior/key-role delivery, and explicitly supported candidate-network or talent-pool accumulation.
9. Write `人选资源/人才积累` only when the user or source supports it; technical recruiting experience alone does not prove a reusable network.
10. Write outcomes only when a concrete result or metric is available. Otherwise state the responsibility and stop; do not add `完成阶段性任务` or similar filler.
11. Treat a discussed or followed industry as an interest, not expertise. Claim technical or industry understanding only when direct work evidence supports it. For early-career briefs, omit self-directed research by default; include it only when the user explicitly treats its depth or quality as a strong, target-relevant signal. Always omit it when feedback says the thinking is not deep enough.
12. Filter opportunity direction by recipient. For a portfolio-founder/HRD group, omit fund-only directions such as `一级市场投资` unless the audience can act on them or the user explicitly asks to keep them.
13. Add only explicit, recipient-relevant opportunity direction and base. Omit generic preferences such as team chemistry, business direction, and co-building space unless they materially distinguish the candidate.
14. Include the user's qualitative judgment when the user explicitly wants it in the brief. Otherwise use it as internal selection context and omit it when it is negative, non-differentiating, or deliberately absent from an accepted final draft.
15. Draft one concise, forwardable paragraph. Do not include analysis, scores, or a career-summary report unless the user asks.
16. If important information is missing, still draft from available facts and add one short `建议补问：...` line.

### Calibration Mode

Use when the user provides "raw notes + final recommendation", "historical sample", "learn this style", or similar training material.

1. Do not store raw transcripts, real names, contact details, compensation, or full resumes.
2. Distill reusable writing rules, phrase patterns, and omission rules.
3. Update `references/style-guide.md` only with generalized, anonymized guidance.
4. If a new sample conflicts with existing guidance, preserve both patterns and describe when each applies.

## Output Contract

Default response:

```text
最终推荐语：
<one concise Chinese paragraph ending with a lightweight CTA>
```

If source material is thin:

```text
最终推荐语：
<best available brief>

建议补问：<one line>
```

## Privacy Rules

- Remove phone numbers, emails, WeChat IDs, addresses, student IDs, exact compensation, and raw interview transcripts.
- Hide sensitive current employers unless the user explicitly says the name may be shared.
- Replace sensitive company names with useful category labels, such as `某 L4 无人车/自动驾驶相关公司`.
- Do not infer gender, age, protected attributes, or personal circumstances.
- Do not invent achievements, title level, team size, base city, or compensation flexibility.

## Quick Checks

Before returning, verify:

| Check | Requirement |
|---|---|
| Shape | One forwardable paragraph by default |
| Length | Usually 80-160 Chinese characters; up to 200 only when evidence is dense |
| Tone | Internal, warm, practical, not a formal assessment |
| Specificity | Lead with total experience, current employer/role, and named shareable business context |
| Current scope | Name the current business/team, not only the generic function, when supported |
| Career stage | For recent graduates, lead with cohort and education instead of forcing a years-of-experience opening |
| Relevance | For a named target, strongest target-relevant evidence appears before generic achievements |
| Opportunity | Keep only directions the receiving group can realistically act on |
| Evidence | Every claim is supported by notes or user-provided context |
| Privacy | No contact details, compensation, or sensitive employer leakage |
| CTA | End with `感兴趣可以私信～` or a similarly light internal CTA |

## Common Mistakes

- Writing a multi-paragraph interview evaluation instead of a forwardable brief.
- Replacing concrete years, companies, and duties with vague background labels.
- Burying the current employer and current responsibility behind a full career history.
- Using a senior-candidate opening for a recent graduate when cohort and education are the stronger signal.
- Listing every short internship, project, and self-directed research item for an early-career candidate.
- Preserving internship counts or recent self-directed research when the accepted brief only needs the experience category.
- Keeping `一级市场投资` in a brief sent only to startup founders/HRDs who are hiring for company roles.
- Forcing a negative or non-essential qualitative judgment into the group message when it is only internal context.
- Writing `目前在<公司>负责招聘` when the notes identify the current business or team supported.
- Writing `500强`、`大厂`、`技术招聘` when a shareable company and specific supported business are available.
- Leading with generic scaling experience when a target AI role depends more on algorithm/R&D hiring and relevant talent access.
- Claiming candidate resources from technical recruiting experience without explicit support.
- Using `长期深耕`、`资深`、`多年经验` to hide missing dates.
- Using evaluation fillers such as `经验较完整`、`经验丰富`、`能力扎实`、`完成阶段性任务` instead of facts.
- Combining separately mentioned employers and duties into an unsupported employer-role claim.
- Replaying the candidate's full career chronology instead of a compact career split.
- Turning interest in AI, robotics, or another industry into `深入理解` without direct work evidence.
- Repeating generic candidate preferences such as chemistry, direction, or co-building space.
- Stacking abstract phrases such as `可迁移价值`、`深入理解`、`业务视角` until the brief sounds generated.
- Saying `敏感的公司`; use a category label instead.
- Over-indexing on personality when concrete hiring or business evidence exists.
- Adding scores, grades, risks, or verdicts when the user only asked for a recommendation blurb.

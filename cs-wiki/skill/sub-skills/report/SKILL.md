---
name: report
description: >
  Sub-skill of wiki. Report Application Xschool — report.mindx.vn.
  Covers Report Application overview, Q&A Report, MKT Dashboard,
  Marketing Performance Dashboard, Sale Performance, Call Performance
  (Realtime), Telemarketing Report, OPS measures, S&M measures,
  CR formulas, teacher metrics, DIM Channel/Product/Org.
  Trigger when user asks about: report, dashboard, Q&A report,
  CR formula, MKT dashboard, sale performance, call performance,
  realtime, revenue, student seat, APV, AOV, measures, chỉ số báo cáo,
  telemarketing, marketing performance.
  Do NOT trigger for CRM built-in reports (deprecated).
license: MIT
compatibility: opencode
metadata:
  system: report
  wiki: cs-wiki
  parent-skill: wiki
---

# Report Application — Sub-skill

Sub-skill của `wiki`. Xử lý các câu hỏi về Report Application Xschool.

Hệ thống báo cáo (Report Application) Xschool. Dùng wiki tại `1.-Foundation/Report-Application/`.

## Purpose
Answer Report Application questions using local wiki. Never guess — only cite from wiki. If not in wiki, check GitBook → update wiki → answer.

## Quick Start
1. Read `rules/RULES.md`, `workflow/WORKFLOW.md`, `protocol/PROTOCOL.md`, and `validation/VALIDATION.md`.
2. Search wiki: Dùng **Grep** tool search `cs-wiki/wiki/1.-Foundation/Report-Application/` với keywords
3. Read matching sections, cite file + section.

## Workflow
1. Parse intent (how-to / data inquiry / bug) → `protocol/PROTOCOL.md`
2. Search wiki → `references/commands/search.md`
3. Read results from matched sections
4. If not found → check GitBook → update wiki → answer
5. Answer with source citation

## References
- `rules/RULES.md` — behavioral rules
- `workflow/WORKFLOW.md` — step-by-step flows
- `protocol/PROTOCOL.md` — input/output schema, intent classification
- `validation/VALIDATION.md` — quality checklist
- `references/presets.md` — WIKI path, defaults
- `references/commands/search.md` — search tool protocol + examples

## Kích hoạt
- User hỏi về Report: dashboard, Q&A report, CR formula, measures
- User hỏi về: revenue, student seat, APV, AOV, MKT, sale performance, call performance, realtime, telemarketing
- User nói "tra cứu report" hoặc "báo cáo"
- User hỏi về chỉ số: CAC, CPL, CR12/23/34/45/CRX5, ANSV, completion rate

## Không trigger cho
- CRM built-in reports (đã ngừng sử dụng)
- LMS built-in reports (dùng skill LMS)
- CRM payment, order, lead management (dùng skill CRM)
- LMS class, attendance, student (dùng skill LMS)

## Parent skill
Main skill: `wiki/` tại `../../SKILL.md`

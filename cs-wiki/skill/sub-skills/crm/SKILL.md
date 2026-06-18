---
name: crm
description: >
  Sub-skill of wiki. CRM Xschool — v1 (crm.mindx.edu.vn) and v2
  (crm-v2.mindx.edu.vn). Wiki merged v1+v2 into one file per feature,
  separated by tags [v1], [v2], [v1+v2]. Covers lead management,
  order/payment, sale process (enroll/transfer/upsale/downsale), econtract,
  KPI/report, products, diagnosis/resolution, known bugs, customer payment
  request, receipt/phiếu thu, call management, contract, settings
  (hide phone, SMS policy, channel), customer/product management.
  Auto-detect v1/v2 from the question.
  Trigger when user asks about: lead, order, payment, upsale/downsale/transfer,
  enroll, econtract, KPI, phiếu thu, receipt, hợp đồng, sản phẩm,
  đầu số gọi điện, renew lead, customer payment request, hide phone,
  SMS policy, channel group. Do NOT trigger for LMS.
license: MIT
compatibility: opencode
metadata:
  system: crm
  wiki: cs-wiki
  parent-skill: wiki
---

# CRM Xschool — Sub-skill

Sub-skill của `wiki`. Xử lý các câu hỏi về CRM v1/v2.

## Purpose
Answer CRM v1/v2 questions using local wiki. Never guess — only cite from wiki. If not in wiki, check GitBook → update wiki → answer.

## Quick Start
1. Read `rules/RULES.md`, `workflow/WORKFLOW.md`, `protocol/PROTOCOL.md`, and `validation/VALIDATION.md`.
2. Identify CRM version (v1 or v2). If unsure, ask.
3. Search wiki: Dùng **Grep** tool search `cs-wiki/wiki/1.-Foundation/CRM/` với keywords
4. Read matching sections, cite file + section + version tag.

## Workflow
1. Parse intent + detect version → `protocol/PROTOCOL.md`
2. Search wiki → `references/commands/search.md`
3. Read results from matched sections
4. If not found → check GitBook → `references/commands/gitbook.md`
5. Answer with source citation

## References
- `rules/RULES.md` — behavioral rules
- `workflow/WORKFLOW.md` — step-by-step flows
- `protocol/PROTOCOL.md` — input/output schema, version detection
- `validation/VALIDATION.md` — quality checklist
- `references/presets.md` — WIKI path, defaults
- `references/FILE-MAP.md` — merged CRM file structure
- `references/V1-V2-DETECTION.md` — full detection table
- `references/QUICK-ANSWERS.md` — common questions
- `references/commands/search.md` — search tool protocol + examples
- `references/commands/gitbook.md` — GitBook fetch protocol

## Parent skill
Main skill: `wiki/` tại `../../SKILL.md`

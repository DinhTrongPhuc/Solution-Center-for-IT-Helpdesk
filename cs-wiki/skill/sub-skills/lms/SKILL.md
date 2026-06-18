---
name: lms
description: >
  Sub-skill of wiki. LMS Xschool — lms.mindx.vn. Covers course management,
  class management, attendance, student progress, enrollment sync,
  teacher management, office hours, calling, reports, settings, LMS errors,
  student account issues.
  Do NOT trigger for CRM (payment, order, sale process, lead management).
license: MIT
compatibility: opencode
metadata:
  system: lms
  wiki: cs-wiki
  parent-skill: wiki
---

# LMS Skill — Sub-skill

Sub-skill của `wiki`. Xử lý các câu hỏi về LMS Xschool.

Hệ thống quản lý học tập (LMS) Xschool. Dùng wiki tại `1.-Foundation/LMS/`.

## Kích hoạt
- User hỏi về LMS: class, attendance, điểm danh, khóa học, học viên, student, enrollment
- User báo lỗi LMS: login, dashboard, không vào được, bug lms
- User nói "tra cứu LMS" hoặc "tìm LMS"

## Không trigger cho
- CRM v1, CRM v2 (payment, order, sale process, lead management)

## Parent skill
Main skill: `wiki/` tại `../../SKILL.md`

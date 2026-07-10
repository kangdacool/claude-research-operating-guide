---
name: hwpx-editing
description: >-
  Safely read, edit, and convert HWPX (Hangul / 한글 .hwpx) word-processor files
  with Python + lxml without corrupting them. Use whenever a task involves a .hwpx
  file, a 한글 / Hancom Office document, HWPML, or a Korean 논문 / 보고서 — including
  extracting text/tables, editing paragraphs/tables/images/equations/footnotes,
  fixing layout, building a TOC, or repackaging the zip; also when a 한글 file
  "won't open" / 파일이 깨졌다, or a legacy .hwp needs converting to .hwpx first.
---

# HWPX editing (pointer)

한글 `.hwpx`를 **손상 없이** 안전하게 읽기·편집·변환하는 워크플로. (docx/pptx와 별개 포맷)

- **트리거:** `.hwpx` / 한글 / 한컴 문서 작업. 사용자가 내부 사정을 말하지 않아도 트리거 — 순진한 편집(재압축·stale 라인캐시·id 복제)은 한글이 파일을 못 열게 만든다.
- **핵심 함정(코어 §3·§7):** mimetype 위치·무압축 규칙을 지켜 재압축해야 하고, 캐시된 `linesegarray`를 지우지 않으면 자간·줄간격이 깨진다.
- **정본 구현:** 검증된 공개 오픈소스 스킬 **[`kangdacool/hwpx-editing-skill`](https://github.com/kangdacool/hwpx-editing-skill)** (MIT) — OWPML XML을 직접 다루고 위 함정을 규칙+도구로 묶어 뒀다. 작업 전 이 스킬(특히 `references/hwpx-guide.md`)을 확보해 적용·검증한다. 대화형 AI라면 그 가이드 파일 하나를 첨부하면 동작.

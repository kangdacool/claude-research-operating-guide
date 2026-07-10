---
name: cross-verify
description: Cross-verify all numbers in manuscript text files against source data tables. Use before submission to catch transcription errors, rounding inconsistencies, and stale labels.
---

# Cross-Verify: Manuscript Numbers vs Source Tables (pointer)

원고·부록·커버레터의 **모든 수치를 권위 있는 원본 표와 대조**해 불일치 리포트를 만드는 워크플로.

- **트리거:** 투고/납품 전, 또는 여러 파일에 흩어진 핵심 수치(주요 추정치, 매개 %, p-값 등)의 일관성을 확인할 때.
- **핵심 원칙(코어 §4 참조):** 수치는 1차 출처로만; 반올림 표시값만 보고 오류 단정 금지; 파일 간 값은 grep으로 수렴. 수치 검증과 **레이아웃 검증은 별개** — 생성 DOCX는 render→PNG 컨택트시트로 시각 QA도 반드시 수행(표 페이지 포함).
- **구현:** 각자 환경의 스킬로 구현. 이 스텁은 트리거 + 원칙을 전달하는 포인터.

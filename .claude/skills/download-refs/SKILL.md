---
name: download-refs
description: Download a manuscript's reference PDFs into a references/ folder using IP-transparent institutional access, by driving a real browser (Playwright + Chrome). Use when asked to fetch/download the reference PDFs for a paper.
---

# Download reference PDFs (pointer)

원고의 각 참고문헌 PDF를 `references/` 폴더로 일괄 다운로드하는 워크플로.

- **트리거:** "이 논문 레퍼런스 PDF 받아줘" 류 요청.
- **핵심 사실(하드-원):** 기관 접근이 **IP-투명**이라도 `curl`/`urllib`은 403/HTML만 받는다(퍼블리셔가 브라우저 행동으로 게이팅). **반드시 실제 브라우저(Playwright + Chrome)를 구동**해야 한다.
- **구현:** 각자 소속 기관의 접근 방식에 맞춰 구현. 기관 자격/접근 세부는 이 배포본에 포함하지 않는다 — 트리거와 하드-원 교훈만 전달하는 포인터.

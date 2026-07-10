# Claude Operating Guide — 연구·문서 편집 운영 세트

_A portable operating guide + lean Claude Code adapter that biases Claude toward rigorous research and clean document/deck production._

학술·정책·실무 문서를 자주 다루는 사람을 위해, Claude가 **보고서·해설서·슬라이드 덱을 만들고, 정보를 추출·검증하고, 자료를 조사하는** 방식을 더 엄밀하게 잡아주는 규칙 세트입니다. 특정 개인의 작업 기록에서 **방법론만 추출·익명화**했습니다.

## 무엇이 들어 있나

```
docs/claude-operating-guide.md   ← 정본 코어(spine). 이 한 파일이 방법론 전부
CLAUDE.md                        ← Claude Code용 lean 어댑터(상시 규칙 요약 + 코어 지시)
.claude/skills/                  ← 반복 워크플로 포인터 스텁 (cross-verify, download-refs, hwpx-editing)
.claude/agents/hwpx.md           ← 한글 편집 서브에이전트 포인터
NOTES.md                         ← 출처·범위(무엇을 뺐는지)
```

## 어떻게 쓰나 — 두 가지 경로

**1) 대화형 Claude(웹/앱 채팅)에서:**
작업 시작 대화에 **`docs/claude-operating-guide.md` 한 파일만 첨부**하고 *"이 가이드의 규칙을 따라 작업해줘"* 라고 요청하세요. 그게 전부입니다.

**2) Claude Code(CLI/IDE)에서:**
`CLAUDE.md` + `.claude/` + `docs/`를 프로젝트 루트(또는 `~/.claude/`)에 복사하세요. CLAUDE.md가 상시 로딩되며 코어를 가리키고, 스킬들은 description으로 트리거됩니다. `/memory`로 로딩을 확인하세요.

## 핵심 규칙 미리보기 (전문은 코어)

- 납품은 **편집 가능한 파일만** — PDF는 QA용 중간물.
- **렌더 후 눈으로** 확인(네이티브 해상도·폰트 최소크기·0바이트 PNG 체크). 코드 성공 ≠ 결과물 정확.
- **상호참조 양방향 대조**, 번호 재배치는 단일 패스 원자적 remap.
- **수치는 1차 출처**, 파일 간 grep 대조. **참고문헌 2-pass**(실존 + 인용 내용). 레퍼런스 날조 금지.
- **표는 booktabs만**, 유의성은 색이 아니라 굵게. 장식·AI 티 금지.
- **출력 표면 규율** — 편집 흔적·선정 기준을 산출물 표면에 남기지 않는다.

## 도메인 레이어는 직접

이 코어는 **일반 방법론**만 담습니다. 특정 분야(예: 통계 코드 관례, 서식, 보고 형식) 규칙은 자신의 도메인 레이어에 두고 CLAUDE.md에서 가리키세요.

## 관련 프로젝트

- 한글 `.hwpx` 안전 편집: **[`kangdacool/hwpx-editing-skill`](https://github.com/kangdacool/hwpx-editing-skill)** (MIT). 이 세트의 hwpx 스텁은 그 저장소를 정본으로 가리킵니다.

## 라이선스

권장: MIT 또는 CC-BY-4.0. `LICENSE` 파일을 추가하고 저작권자/연도를 채워 넣으세요. (규칙은 기본값일 뿐이니 각자 맥락에 맞게 덮어써서 쓰라는 취지의 세트입니다.)

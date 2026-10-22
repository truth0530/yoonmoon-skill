# yoonmoon-skill

한국어 화면 문구·안내문·팝업·설명서를 **윤문**하는 규칙 모음입니다.
AI가 쓴 듯한 말투와, 사실인지 지시인지 헷갈리는 문장을 수정합니다. 의미는 그대로 유지합니다.
특정 AI 도구에 묶이지 않고 어떤 에이전트나 대화형 AI에서도 쓸 수 있게 도구별 설정을 함께 둡니다.

## 무엇을 고치나
- 「~않습니다」가 사실인지 금지인지 모호한 문장
- 「센다·세지 않는다」 같은 「세다」 계열을 「집계」로, 사실과 지시를 구분
- 「숨습니다」→「숨겨집니다」 같은 어색한 자동사·피동
- 번역투(「~에 의해」「~에 있어서」「~를 통하여」 등)와 AI식 의지·다짐 동사(「고칩니다」→「수정합니다」)
- 조사 오류, 단위 없는 숫자, 이력 문구
- 팝업·튜토리얼 문장의 줄바꿈과 들여쓰기(내어쓰기)

## 구성
```
AGENTS.md                      에이전트 공통 안내(여러 도구가 읽는 표준 파일)
adapters/
  condensed.md                 규칙 요약본(도구와 무관한 한 파일)
  cursor/yoonmoon-ko.mdc       Cursor 규칙
  copilot/README.md            GitHub Copilot 사용법
  gemini/README.md             Gemini CLI 사용법
  generic/prompt.md            대화형 AI에 붙여 넣는 프롬프트
skills/yoonmoon-ko/
  SKILL.md                     스킬 형식(SKILL.md를 읽는 에이전트용)
  references/rules.md          유형별 규칙과 대체 표현
  references/examples.md       전/후 예시
  references/checklist.md      마무리 점검과 검색 패턴
```

## 도구별 사용

| 도구 | 방법 |
|---|---|
| SKILL.md를 읽는 에이전트 | `skills/yoonmoon-ko/` 폴더를 해당 도구의 스킬 폴더에 복사 |
| AGENTS.md를 읽는 에이전트 | 이 저장소를 프로젝트에 두거나 `AGENTS.md`와 `adapters/condensed.md`를 복사 |
| Cursor | `adapters/cursor/yoonmoon-ko.mdc`를 `.cursor/rules/`에 복사 |
| GitHub Copilot | `adapters/copilot/README.md` 참고 |
| Gemini CLI | `adapters/gemini/README.md` 참고 |
| 대화형 AI(웹 채팅 등) | `adapters/generic/prompt.md`를 첫 메시지로 붙여 넣기 |

## 사용
"윤문해 줘", "AI 말투 고쳐", "팝업 줄바꿈 정리해 줘"처럼 요청하면 전수 조사 → 분류 → 교체 → 동기화 → 검수 순서로 진행합니다.

## 라이선스
MIT

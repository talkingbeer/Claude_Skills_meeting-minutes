# Meeting Minutes Skill

회의록 작성 Aside 스킬. 회의 목적에 따라 골든 템플릿을 적용하고 인테이크-작성-윤문-검수 파이프라인으로 일관된 수준의 회의록을 생성한다.

## 지원 목적

| 코드 | 목적 | 구조 |
|---|---|---|
| DEC | 의사결정 기록, 전파 | MPR 회의록형 |
| DIS | 논의, 합의 추적 | MPR형 + 논점 합의 표 |
| RPT | 현황, 실적 보고 | MPR형 + 목표-실적-갭 표 |
| INS | 기록, 인사이트 도출 | 진단노트형 |
| 1ON1 | 면담 기록 | 진단노트 축약 |
| INF | 정보 전달, 공유 | 요약 + Q&A |

## 설치 방법

### 방법 A: Aside Project로 등록 (권장)

1. 이 저장소를 클론한다
   ```
   git clone https://github.com/talkingbeer/Claude_Skills_meeting-minutes.git
   ```
2. Aside에서 클론한 폴더를 Project로 등록한다
3. 해당 Project 세션에서 스킬이 자동 활성화된다
4. 업데이트: `git pull`

### 방법 B: 계정 스킬로 복사

클론한 폴더 내용을 계정 스킬 폴더에 복사한다.

```
# Windows
xcopy /E /I Claude_Skills_meeting-minutes "%USERPROFILE%\.aside\u\0\skills\user\meeting-minutes"

# macOS/Linux  
cp -r Claude_Skills_meeting-minutes ~/.aside/u/0/skills/user/meeting-minutes
```

계정 인덱스(`u\0`, `u\1` 등)는 사용자마다 다를 수 있다. 모든 세션에서 활성화되지만 업데이트마다 재복사가 필요하다.

## 구성

```
SKILL.md                  스킬 본문 (워크플로우, 규칙)
assets/
  design.css              공용 디자인 시스템 (IBM Carbon 무채색, 나눔고딕)
references/
  review-protocol.md      독립 검수 10항목 프로토콜
  reliability-tags.md     신뢰도 4단 태그 체계와 HTML 범례
```

## 의존 스킬

| 스킬 | 용도 | 필수 여부 |
|---|---|---|
| html-doc | 편집 가능한 HTML 산출물 조립 | 기본 출력이 편집용 HTML이므로 권장 |
| humanize-korean | 윤문 (light, 보수, 구조 동결) | 선택. 없으면 핵심 패턴만 수동 적용 |
| docx | DOCX 출력 시 변환 | 선택 |

## 디자인 원칙

- 색상 없음: 무채색 9단 토큰만 사용
- 폰트: 나눔고딕 단일 (Google Fonts)
- 구분자: ", " (쉼표), "-" (하이픈)
- 박스: 회색 지면(.note), 검정 외곽선(.note.warn)
- 신뢰도: 사실 / 본인 견해 / 전언 / 미확인 (색 없이 선 두께로 구분)

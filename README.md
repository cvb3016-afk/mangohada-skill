# mangohada-skill

공유용 Claude Code 스킬·커맨드 모음. 각 항목은 자기 폴더 안에 있어야 Claude Code가 인식하지만, 이 페이지 하나에서 한눈에 볼 수 있어요.

---

## 📧 메일-요약-알림

> Gmail 안읽은 메일을 확인해서 요약하고 Slack DM으로 보낸다.

- 폴더: [`메일-요약-알림/`](./메일-요약-알림/SKILL.md)
- 트리거: 사용자가 즉시 메일 요약을 원할 때 (수동 호출)
- 동작: 안 읽은 메일 조회 → 마케팅/광고/SNS 알림 제외 → 핵심 3~5줄 한국어 요약 → 본인 Slack DM 전송
- 회신요청·일정변경·계약·견적·결제 메일은 🔴 우선순위 높음 표시

---

## 🥭 babjib (밥집)

> 음식 이름을 말하면 집밥 레시피 + 서울 맛집 3곳을 찾아준다.

- 폴더: [`babjib/`](./babjib/SKILL.md)
- 출처: [rlxo6690-hub/mangohada](https://github.com/rlxo6690-hub/mangohada)
- 트리거: 음식 이름 ("양념치킨"), "[음식] 레시피", "[음식] 맛집" 등
- 동작: 웹검색 기반 실전 레시피 + 네이버 블로그/지역검색으로 교차 검증한 서울 맛집 3곳

---

## ✍️ 블로그 (커스텀 커맨드)

> `/블로그` — 망고하다 브랜드 카테고리 기반 블로그 주제 + 내용 요약 생성

- 폴더: [`commands/블로그.md`](./commands/블로그.md)
- 출처: [xloahyy/-](https://github.com/xloahyy/-)
- 종류: 스킬이 아니라 **커스텀 슬래시 커맨드** (자동 트리거 없음, `/블로그`라고 직접 입력해야 실행)
- 카테고리: 웰다잉 생활 정보 · 유언 및 사전 정보 · 장례 및 예절 정보 · 죽음 인문학 · 시니어 라이프
- `/블로그 [키워드]`처럼 뒤에 인자를 붙이면 그 키워드에 집중해서 더 뽑아줌

---

## 📚 voca-learner

> 노션에 업무 용어를 저장하면 매일 오전 8:30 카카오톡 퀴즈로 복습시켜주는 개인 지식 관리 스킬.

- 폴더: [`voca-learner/`](./voca-learner/SKILL.md)
- 출처: [plower344-spec/mangohada-3-](https://github.com/plower344-spec/mangohada-3-)
- 트리거: 업무 용어 뜻 질문("IDI가 뭐야?") → 답변 후 노션 자동 저장 / "저장해줘" / "오늘 복습"
- 동작: 노션 DB에 용어 기록 → 간격 반복(1일→3일→7일→14일→30일)으로 복습 예정일 자동 계산 → 카카오톡 나에게 보내기로 퀴즈 발송

---

## 설치법

스킬은 `~/.claude/skills/`, 커맨드는 `~/.claude/commands/`에 넣어야 인식돼요 (폴더가 다름).

```bash
git clone https://github.com/cvb3016-afk/mangohada-skill.git

# 스킬
cp -r mangohada-skill/메일-요약-알림 ~/.claude/skills/메일-요약-알림
cp -r mangohada-skill/babjib ~/.claude/skills/babjib
cp -r mangohada-skill/voca-learner ~/.claude/skills/voca-learner

# 커맨드
cp mangohada-skill/commands/블로그.md ~/.claude/commands/블로그.md
```

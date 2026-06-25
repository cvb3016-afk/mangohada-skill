# mangohada-skill

공유용 Claude Code 스킬 모음. 각 스킬은 자기 폴더 안에 있어야 Claude Code가 인식하지만, 이 페이지 하나에서 둘 다 한눈에 볼 수 있어요.

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

## 설치법

원하는 스킬 폴더를 통째로 복사:

```bash
git clone https://github.com/cvb3016-afk/mangohada-skill.git
cp -r mangohada-skill/메일-요약-알림 ~/.claude/skills/메일-요약-알림
cp -r mangohada-skill/babjib ~/.claude/skills/babjib
```

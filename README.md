# mangohada-skill

공유용 Claude Code 스킬·커맨드 모음. 각 항목은 자기 폴더 안에 있어야 Claude Code가 인식하지만, 이 페이지 하나에서 한눈에 볼 수 있어요.

---

## ✍️ 블로그 (커스텀 커맨드)

> `/블로그` — 망고하다 브랜드 카테고리 기반 블로그 주제 + 내용 요약 생성

- 폴더: [`commands/블로그.md`](./commands/블로그.md)
- 출처: [xloahyy/-](https://github.com/xloahyy/-)
- 종류: 스킬이 아니라 **커스텀 슬래시 커맨드** (자동 트리거 없음, `/블로그`라고 직접 입력해야 실행)
- 카테고리: 웰다잉 생활 정보 · 유언 및 사전 정보 · 장례 및 예절 정보 · 죽음 인문학 · 시니어 라이프
- `/블로그 [키워드]`처럼 뒤에 인자를 붙이면 그 키워드에 집중해서 더 뽑아줌

---

## 설치법

커맨드는 `~/.claude/commands/`에 넣어야 인식돼요.

```bash
git clone https://github.com/cvb3016-afk/mangohada-skill.git
cp mangohada-skill/commands/블로그.md ~/.claude/commands/블로그.md
```

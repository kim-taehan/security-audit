# security-audit

정부 보안권고 15대 보안통제 기준 보안점검용 Claude Code 플러그인.
저장소 코드·설정을 점검 항목별로 분석해 양호/취약/NA/확인필요를 근거(`파일:라인`)와 함께 판정하고, 점검표(점검 결과·조치 일정·비고)에 옮겨 적을 수 있는 md를 만든다. 읽기 전용.

## 설치

### Claude Code (플러그인)

```
/plugin marketplace add kim-taehan/security-audit
/plugin install security-audit@security-audit
```

### Codex (스킬)

```bash
git clone --depth 1 https://github.com/kim-taehan/security-audit.git /tmp/security-audit
mkdir -p ~/.codex/skills && cp -R /tmp/security-audit/skills/security-audit ~/.codex/skills/
rm -rf /tmp/security-audit
```

Codex를 재시작하면 스킬이 로드된다.

## 사용

- Claude Code: `/security-audit <저장소 경로> [<저장소 경로> ...]`
- Codex: `$security-audit <저장소 경로>`

또는 두 도구 모두 "이 저장소 보안점검 해줘". 점검 항목 정의는 `skills/security-audit/references/checklist.md`.

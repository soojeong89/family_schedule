# 가족 시간표

비밀번호로 잠긴 가족 주간 시간표입니다. (StatiCrypt 암호화 · GitHub Pages)

## 구조

- `src/index.html` — 원본 시간표. **Git에 올리지 않음** (`.gitignore`)
- `index.html` — `src/index.html`을 암호화한 결과. 이 파일만 GitHub에 올라감
- `.staticrypt.json` — 암호화 salt (올려도 안전, 지우지 말 것)
- `.env` — 비밀번호 (`STATICRYPT_PASSWORD=...`). **Git에 올리지 않음**

## 시간표 수정 순서

1. `src/index.html` 수정
2. `npm run build` → 루트의 `index.html`이 새로 암호화됨
3. `index.html` 커밋 후 push

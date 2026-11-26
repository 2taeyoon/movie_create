# 2D 영상 (HyperFrames)

| 폴더 | 넣는 것 |
|---|---|
| `레퍼런스/` | 따라 하고 싶은 영상, 장면 캡처(`frames/`), 받아 적은 말(`transcripts/`), 공통 스타일 정리(`스타일.md`) |
| `원본 영상/` | 재료로 쓸 내 녹화·녹음 |
| `완성본/` | 렌더링한 최종 mp4 |
| `프로젝트/` | 영상 하나당 HyperFrames 프로젝트 하나 |
| `스킬/` | 2D에서 쓰는 도구의 GitHub 원본 (참고용) |

시작은 `/hyperframes` 스킬. 새 영상은 `프로젝트/<이름>`에 만들고 결과물은 `완성본/`에 저장한다.

## 프로젝트

영상 하나당 폴더 하나를 만든다. 처음에는 비어 있다.

프로젝트 폴더 구성은 보통 이렇다.

- `story.py` 대본 → `script.json`
- `tts.py`(있으면) 내레이션 → `assets/voice/`, `timing.json`
- `build.py` 장면 HTML 생성 → `compositions/`, `index.html`
- `npx hyperframes check` / `snapshot` / `render`

## 스킬

| 폴더 | GitHub | 비고 |
|---|---|---|
| `hyperframes/` | heygen-com/hyperframes | HTML → 영상 렌더러 원본. 안의 `skills/`가 `.claude/skills/hyperframes*`의 원본 |
| `remotion/` | remotion-dev/remotion | React → 영상 렌더러 원본 |
| `remotion-skills/` | remotion-dev/skills | `.claude/skills/remotion-*`의 원본 |

클로드 코드가 실제로 읽는 스킬(SKILL.md)은 `movie_create/.claude/skills/`에 있다. 그 자리에 있어야 인식되므로 옮기지 않는다.

# 3D 영상 (lemo-opuscar + three.js)

| 폴더 | 넣는 것 |
|---|---|
| `레퍼런스/` | 따라 하고 싶은 영상, 스타일 메모(`스타일.md`) |
| `원본 영상/` | 재료로 쓸 내 녹화·녹음 (예: 3D 화면 안에 넣을 사이트 녹화) |
| `완성본/` | 렌더링한 최종 mp4와 자막 srt |
| `프로젝트/` | 영상 하나당 프로젝트 하나 |
| `스킬/` | 3D에서 쓰는 라이브러리의 GitHub 원본 |

시작은 `/lemo-opuscar` 스킬. 새 영상은 `프로젝트/<이름>`에 만들고 결과물은 `완성본/`에 저장한다.

## 프로젝트

영상 하나당 폴더 하나를 만든다. 처음에는 비어 있다.

각 프로젝트는 `sh build.sh`(Git Bash) 한 번으로 처음부터 다시 만들고, 결과물을 `완성본/`에 바로 쓴다.
라이브러리 경로는 `LIB=$HERE/../../스킬/lemo-opuscar`.

## 스킬

| 폴더 | GitHub | 비고 |
|---|---|---|
| `lemo-opuscar/` | lemomo-ai/lemo-opuscar | 스타일 모음 + 렌더·음성·믹스 도구. 작업 전 `AGENTS.md`를 읽는다 |
| `three.js/` | mrdoob/three.js | 3D 장면·카메라·빛 |
| `react-three-rapier/` | pmndrs/react-three-rapier | 물리(중력, 충돌) |
| `react-postprocessing/` | pmndrs/react-postprocessing | 빛 번짐, 그림자 같은 후처리 |
| `mcp-for-blender/` | ahujasid/mcp-for-blender | Blender MCP 원본. 서버는 `uvx mcp-for-blender`로 실행되므로 참고용 |

클로드 코드가 실제로 읽는 스킬(SKILL.md)은 `movie_create/.claude/skills/lemo-opuscar/`에 있다.

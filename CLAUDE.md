# movie_create — 영상 제작 작업 폴더

2D·3D 영상을 만드는 도구와 작업물을 한곳에 모은 폴더입니다. 설치법과 사용법은 `세팅_가이드.md`에 있습니다.

## 어디에 뭐가 있나

`2d/`와 `3d/`는 안쪽 구조가 똑같습니다.

```text
2d/ · 3d/
├─ 레퍼런스/   따라 할 영상, 스타일 메모(스타일.md)
├─ 원본 영상/  재료로 쓸 녹화·녹음
├─ 완성본/     최종 결과물(mp4, srt)
├─ 프로젝트/   영상 하나당 폴더 하나
└─ 스킬/       그쪽에서 쓰는 도구·라이브러리의 GitHub 원본
```

- `2d/프로젝트/` — 영상 하나당 HyperFrames 프로젝트 하나 (각 폴더의 CLAUDE.md 참고)
- `2d/스킬/` — `hyperframes/` (heygen-com/hyperframes), `remotion/` (remotion-dev/remotion), `remotion-skills/` (remotion-dev/skills)
- `3d/프로젝트/` — 영상 하나당 프로젝트 하나. `sh build.sh`로 전체 재생성하고 결과물은 `3d/완성본/`에 바로 저장된다
- `3d/스킬/` — `lemo-opuscar/` (스타일 라이브러리 + 렌더·믹스 도구, 3D 작업 전 `AGENTS.md`를 읽는다. LIB 경로는 이 폴더), `three.js/`, `react-three-rapier/`, `react-postprocessing/`, `mcp-for-blender/` (Blender MCP 원본)
- `_tools/`
  - `blender-5.3.0-windows-x64/blender.exe`, `mcp_addon.zip` (공식 Blender MCP 애드온, 참고용. GitHub에는 도구 폴더가 비어 있다)
  - Blender MCP는 ahujasid `mcp-for-blender`(등록 이름 `blender-ahujasid`, 포트 9877). Blender에서 `N` → **MCP for Blender** 탭의 Port를 9877로 맞춘다. 공식 MCP(`blender`)는 9876
  - `ffmpeg-9.0.2/bin/` FFmpeg 사본 (시스템에는 winget 설치본이 PATH에 있음)
  - `whisper-models/` (tiny, medium). 사용 시 `--model_dir _tools/whisper-models`
  - `src/` 프로그램형 도구의 GitHub 원본 (FFmpeg, whisper, yt-dlp. 참고용, 빌드하지 않음)
- `.claude/skills/` — 클로드 코드가 읽는 스킬(SKILL.md). 이 자리에 있어야 인식되므로 옮기지 않는다
  - 2D: hyperframes*, media-use, figma, slideshow, reverse-any-video, style-sampling, remotion-*
  - 3D: lemo-opuscar

## 규칙

- 2D 영상: `/hyperframes` 스킬부터. 새 프로젝트는 `2d/프로젝트/<이름>`, 결과물은 `2d/완성본/`.
- 3D 영상: `/lemo-opuscar` 스킬부터. 새 프로젝트는 `3d/프로젝트/<이름>`, 결과물은 `3d/완성본/`. 모델링은 Blender MCP(ahujasid). Blender를 켜면 애드온 서버가 자동 시작되고, `look`으로 여러 각도를 찍어 확인한 뒤 GLB로 내보낸다.
- 3D 프로젝트의 LIB 경로는 `$HERE/../../스킬/lemo-opuscar`.
- 렌더 동시 작업 수는 기본 3. 메모리 부족으로 꺼지면 1로 낮춘다.
- `h264_nvenc`가 드라이버 문제로 실패하면 `libx264`를 쓴다.

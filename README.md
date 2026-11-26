# movie_create

클로드 코드(Claude Code)로 2D·3D 영상을 만드는 작업 폴더입니다.
처음 세팅한 구조 그대로 올렸습니다. 스킬과 안내 파일, 빈 작업 폴더만 들어 있습니다.
Blender, FFmpeg, three.js 같은 **도구와 라이브러리는 폴더만** 있으니 [세팅_가이드.md](세팅_가이드.md) 4장을 보고 받아서 넣으세요.

| 구분 | 시작 스킬 | 화면을 만드는 방법 |
|---|---|---|
| 2D | `/hyperframes` | HTML + CSS + GSAP |
| 3D | `/lemo-opuscar` | three.js + Blender 모델(GLB), Blender MCP(ahujasid) |

## 빠른 시작

```powershell
cd C:\Users\<사용자>\Documents
git clone https://github.com/2taeyoon/movie_create.git
cd movie_create
claude
```

빈 도구 폴더에는 `.gitkeep`만 있습니다. 그 자리에 `git clone`할 때는 빈 폴더를 지우고 같은 이름으로 받으세요.

## 폴더

```text
movie_create/
├─ CLAUDE.md            ← 클로드가 처음 읽는 안내서 (어디에 뭐가 있는지)
├─ 세팅_가이드.md        ← 설치·사용 안내
├─ .claude/skills/      ← 스킬 모음 (HyperFrames, Remotion, lemo-opuscar)
├─ _tools/                          (폴더만, 내용은 직접 받기)
│  ├─ blender-5.3.0-windows-x64/    ← Blender (압축만 풀면 실행되는 버전)
│  ├─ ffmpeg-9.0.2/                 ← FFmpeg 실행 파일 사본
│  ├─ whisper-models/               ← Whisper 음성 인식 모델 (tiny, medium)
│  └─ src/                          ← FFmpeg, whisper, yt-dlp GitHub 원본 (참고용)
├─ 2d/
│  ├─ 레퍼런스/                     ← 따라 하고 싶은 영상, 스타일.md
│  ├─ 원본 영상/                    ← 내가 찍은 영상, 녹음
│  ├─ 완성본/                       ← 결과물이 저장되는 곳
│  ├─ 프로젝트/                     ← 영상 하나당 HyperFrames 프로젝트 하나
│  └─ 스킬/                         ← hyperframes, remotion, remotion-skills (폴더만)
└─ 3d/
   ├─ 레퍼런스/  원본 영상/  완성본/
   ├─ 프로젝트/                     ← 영상 하나당 프로젝트 하나
   └─ 스킬/                         ← lemo-opuscar, three.js, react-three-rapier,
                                       react-postprocessing, mcp-for-blender (폴더만)
```

`node_modules`와 파이썬 가상환경(`.venv`)은 컴퓨터마다 다시 만들어야 해서 빠져 있습니다.

## 참고

- Remotion은 직원 4명 이상 회사에서 쓰면 회사 라이선스가 필요합니다: https://www.remotion.dev/docs/license
- Blender MCP: https://github.com/ahujasid/mcp-for-blender

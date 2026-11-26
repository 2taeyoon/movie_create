# 3D 스킬 원본

3D에서 쓰는 라이브러리와 Blender MCP의 GitHub 원본. 폴더만 있으니 안의 내용은 직접 받는다.

```powershell
cd 3d\스킬
git clone --depth 1 https://github.com/lemomo-ai/lemo-opuscar.git
git clone --depth 1 https://github.com/mrdoob/three.js.git
git clone --depth 1 https://github.com/pmndrs/react-three-rapier.git
git clone --depth 1 https://github.com/pmndrs/react-postprocessing.git
git clone --depth 1 https://github.com/ahujasid/mcp-for-blender.git
```

폴더에 `.gitkeep`이 있어서 `git clone`이 "이미 있는 폴더"라고 멈추면, 그 폴더를 지우고 다시 받는다.
`lemo-opuscar`는 3D 프로젝트의 `build.sh`가 `LIB=$HERE/../../스킬/lemo-opuscar`로 찾으므로 이 이름 그대로 둔다.

# _tools

컴퓨터에 설치하는 큰 프로그램을 두는 곳. 폴더만 있고, 안의 내용은 직접 받는다(`세팅_가이드.md` 4장).

| 폴더 | 넣는 것 |
|---|---|
| `blender-5.3.0-windows-x64/` | https://www.blender.org/download/ 의 Windows **zip(포터블)** 을 풀어 넣는다 |
| `ffmpeg-9.0.2/` | FFmpeg 실행 파일 사본. `winget install Gyan.FFmpeg`로 설치했다면 비워 둬도 된다 |
| `whisper-models/` | Whisper 모델(tiny, medium). `whisper --model_dir _tools/whisper-models`로 처음 실행하면 여기에 받아진다 |
| `src/` | FFmpeg, whisper, yt-dlp의 GitHub 원본 (참고용, 빌드하지 않음) |

```powershell
cd _tools\src
git clone --depth 1 https://github.com/FFmpeg/FFmpeg.git FFmpeg_FFmpeg
git clone --depth 1 https://github.com/openai/whisper.git openai_whisper
git clone --depth 1 https://github.com/yt-dlp/yt-dlp.git yt-dlp_yt-dlp
```

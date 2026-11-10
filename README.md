# Kee IP Knowledge Video

30–60 秒竖版知识视频工作流，基于 Remotion，包含三套视觉风格、字幕排期、动效组件和渲染质量闸门。

## 安装

将整个仓库放入 agent 的 skills 目录，阅读 SKILL.md。需要 Node.js、Python 3、ffmpeg 和 ffprobe。

```sh
cd remotion-library
npm ci
npm run studio
```

正式出片使用 scripts/render.sh，参数见 SKILL.md。口播、风格、分镜和配音均需人工确认。

## 配音与素材

配音有两条路：用自己的声音走本地 CosyVoice；用现成音色走 ChatCut（需安装 ChatCut 插件并登录），生成整篇音频后用 `scripts/tts_cosyvoice.py --external-audio <音频>` 接回时间轴。

CosyVoice 需另行安装并下载模型。用 TTS_HOME 指定安装目录，用 TTS_PROMPT_WAV 指定获得授权的参考音，用 TTS_PROMPT_TEXT 指定逐字转录。参考音路径相对于 TTS_HOME。

本仓库移除了个人声音、肖像、客户项目、生产稿、原始截图、历史成片、音效素材和私有回归用例。使用 IP 组件前，请自行提供 public/ip/kee-{action}-v1.png，动作名见 SKILL.md。部分样板引用上述素材，补齐后才能完整预览。可选 BGM 依赖外部 ChatCut 工作流。

## 公开版本说明

本机路径已通用化，历史案例编号已替换。原始 skill 保持原样。公开版尚未完成完整视频渲染验证。未附加开源许可证，第三方依赖及素材应遵守各自许可。

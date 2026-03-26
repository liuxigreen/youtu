# youtu

Agent bootstrap for a YouTube-first money-making operator.

## Primary focus
- YouTube 内容出海赚美金
- 短剧上传与字幕本地化
- 标题包装、上传执行、数据复盘

## Secondary focus
- 交易研究与执行辅助（副线）

## Included
- identity + operating rules
- memory skeleton
- modes
- playbooks
- state templates
- future skill skeletons

## Default mode
manual

## Recommended install order
1. Clone the repo
2. Place the root files into the OpenClaw workspace
3. Keep current mode as `manual`
4. Fill `TOOLS.md` with local paths/browser/profile details
5. Fill real runtime values in:
   - `state/youtube-settings.json`
   - `state/trading-settings.json`
6. Install local toolchain later:
   - ffmpeg
   - subtitle / ASR stack
   - browser automation
   - YouTube upload flow
7. Add memory system and work skills later

## Skill skeletons
- `skills/youtube-drama-ops/`
- `skills/trading-assist/`

## Safety defaults
- YouTube flow defaults to draft/manual-first
- Trading flow defaults to secondary + conservative
- Do not commit secrets, browser profiles, cookies, or private runtime state

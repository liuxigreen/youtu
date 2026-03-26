---
name: youtube-drama-ops
description: End-to-end YouTube-first short drama publishing workflow for Chinese-source videos. Use when the user wants to analyze a short drama, turn Chinese subtitles/audio into English subtitles, generate overseas-market YouTube titles/descriptions/tags, prepare thumbnail copy, upload to YouTube, or run a manual/semi-auto publish flow. Default to US/English market and draft/manual-first publishing.
---

# YouTube Drama Ops

Use this skill for the main money-making workflow in this repo.

## Objective
Turn a Chinese-source drama/video into a YouTube-ready English-market package.

## Default mode
- market: US
- language: English
- publish: draft/manual-first

## Workflow
1. Inspect the source video and any existing Chinese subtitles.
2. If subtitles are missing, extract speech/subtitles first.
3. Produce English subtitles with localization, not literal translation.
4. Generate:
   - title A/B
   - description
   - tags/hashtags
   - thumbnail copy ideas
5. Check monetization / reused-content / copyright risk.
6. Upload as draft unless the user explicitly asks to publish.
7. Record output into state files / publish logs.

## Hard rules
- Do not assume copyright is safe. Flag risk explicitly.
- Do not default to direct publish.
- Prefer result/blocker over long process narration.
- Keep versions: subtitle version, metadata version, upload link.

## Inputs expected
- video path
- optional subtitle file
- optional episode / series context
- optional target market override

## Outputs expected
- English subtitle file
- localized metadata pack
- upload status or exact blocker

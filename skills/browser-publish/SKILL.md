---
name: browser-publish
description: Browser-based publish workflow for YouTube Studio and similar web dashboards. Use when the user needs a manual-first or semi-auto upload/publish flow in the browser, especially when API-based publishing is unavailable or not yet configured.
---

# Browser Publish

Use this skill when publishing must be completed through a browser UI.

## Objective
Drive the final web UI steps for upload / metadata entry / draft review / publish.

## Default policy
- manual-first
- stop at draft unless the user explicitly asks to publish
- prefer exact blocker over repeated retries

## Workflow
1. Open the target dashboard (for this repo: YouTube Studio).
2. Confirm login/session state.
3. Fill title / description / tags / visibility from the prepared metadata pack.
4. Upload or attach the target video.
5. Stop at draft/manual review by default.
6. Return the final page state or blocker.

## Hard rules
- Do not assume login exists.
- Do not publish by default.
- Reuse already-generated metadata instead of regenerating during browser work.
- Keep browser steps separate from content understanding steps.

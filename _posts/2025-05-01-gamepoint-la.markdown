---
layout: post
title: GamePoint LA
date: 2025-05-01
type: main
featured: true
project_url: https://tunglinn.github.io/gamepoint-la
category: WebCodecs, Video Processing
description: Browser-based sports match recorder — mark serve and end, auto-exports video with live scoreboard overlay.
---

GamePoint LA is a fully browser-based sports match recording tool. Users mark the start and end of each point directly in the browser, and the app automatically exports the clipped video with a scoreboard overlay rendered frame-by-frame.

## How It Works

- **Mark points** — click to tag serve and end timestamps during or after a match
- **Auto-export** — leverages the [WebCodecs API](https://developer.mozilla.org/en-US/docs/Web/API/WebCodecs_API) to re-encode video clips with a scoreboard burned in, entirely client-side
- **No server upload** — all processing happens in the browser; the raw video never leaves the device

## Tech Stack

- WebCodecs API for frame-level video encoding
- Canvas for scoreboard overlay rendering
- Vanilla JS + modern browser APIs

---
title: "Game Capture Audio OBS: Meter Moves but No Source Audio in Recording"
description: "Fix OBS game capture audio when the meter moves but the recording has no source audio. Step-by-step checks for track assignment, monitoring, and verification."
seo_title: "Game Capture Audio OBS: Fix Meter Moves, No Source Audio"
seo_description: "Fix OBS game capture audio when the meter moves but the recording has no source audio. Step-by-step checks for track assignment, monitoring, and verification."
keywords:
  - "game capture audio obs"
date: 2026-11-21T15:05:00+08:00
publishDate: 2026-11-21T15:05:00+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording a game with mic on separate tracks, the audio meter moves, but the recorded file has no source audio—and you're stuck at the audio source is not captured step before a controlled diagnosis. Let's fix that.

## Check Track Assignment First

Open OBS Settings > Output > Recording. Under Audio, note which tracks are checked (e.g., Track 1 for game, Track 2 for mic). Then right-click your game capture source in the Audio Mixer, choose Advanced Audio Properties, and confirm the source's Track column matches the checked tracks. If the source is assigned to Track 3 but only Track 1 is recorded, the meter will move yet the file will be silent. Exact result: the source must have a checkmark in at least one recorded track.

## Verify Monitoring and Output

In Advanced Audio Properties, set Monitoring to Monitor Off for the game source to avoid feedback. In Settings > Audio, confirm the correct device is selected and not disabled. If the meter moves, the source is live; the issue is routing, not capture.

## Run a Verification Test

Record 10 seconds with the game and mic active. Open the file in a player that shows track selection (e.g., VLC > Audio > Audio Track). Switch tracks and confirm the game audio appears on its assigned track. If it does, routing is fixed.

## Rollback and Recovery

If you changed track assignments and lost mic audio, revert to the previous Advanced Audio Properties settings and re-check only the intended tracks. Keep a screenshot of working settings before further edits.

If the meter still moves but the file stays silent after these checks, the problem is likely a corrupted profile or conflicting plugin. For a guided diagnosis of your exact **game capture audio obs** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).

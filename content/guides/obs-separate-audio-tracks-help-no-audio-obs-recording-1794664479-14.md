---
title: "No Audio in OBS Recording? Fix the Source That Shows a Meter but Records Silence"
description: "OBS meter moves but your recording has no source audio? Follow these checks to fix the no audio obs recording issue on separate tracks."
seo_title: "No Audio OBS Recording: Meter Moves but File Is Silent"
seo_description: "OBS meter moves but your recording has no source audio? Follow these checks to fix the no audio obs recording issue on separate tracks."
keywords:
  - "no audio obs recording"
date: 2026-11-22T09:02:35+08:00
publishDate: 2026-11-22T09:02:35+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You're recording your game and mic on separate tracks, and the meter moves, but the saved file has no source audio. That points to a routing or track-assignment problem, not a dead microphone. Let's diagnose it step by step.

## Check the source's track assignment

Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). Find the row for the source that shows activity. Under Tracks, confirm the track you expect is checked. If your recording output is set to Track 1 but the source is only on Track 2, the meter will move while the file stays silent. Check the box for the track your recording uses, then click Close.

## Confirm the recording track selection

Go to Settings > Output > Recording. In the Audio Track section, note which track number is selected. This must match the track you enabled for the source. If they differ, align them. Also verify the recording format; some formats and players only expose the first track, so a source on Track 2 can appear missing even when it was captured.

## Run a verification test

Record ten seconds with the game and mic active. Stop, then open the file in a player that lets you switch audio tracks, such as VLC under Audio > Audio Track. If the source audio appears on the expected track, the routing is fixed. If it is still absent, re-check both track checkboxes before changing anything else.

## Rollback note

If you changed multiple track settings, revert them to your last known-good configuration before retesting, so you can isolate which change mattered.

If the meter still moves but the file has no source audio, this is a **no audio obs recording** routing fault that needs a closer look at your setup.

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your Advanced Audio Properties and Output settings.

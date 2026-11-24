---
title: "OBS Audio Output Capture: Why the Meter Moves but the Recording Is Silent"
description: "Fix OBS audio output capture when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, monitoring, and a verification test."
seo_title: "OBS Audio Output Capture Not Recording: Meter Moves, File Silent"
seo_description: "Fix OBS audio output capture when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, monitoring, and a verification test."
keywords:
  - "obs audio output capture"
date: 2026-11-24T11:02:43+08:00
publishDate: 2026-11-24T11:02:43+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and the meter moves but the saved file has no source audio. This is a routing problem, not a level problem. Work through these checks in order and stop at the first one that fails.

## Check the source's track assignment

Open Settings > Output > Recording and note which tracks are enabled. Then right-click the silent source, choose Advanced Audio Properties, and confirm it is assigned to at least one enabled track. Result interpretation: if the source has no track ticked, the meter still moves because monitoring is independent of recording. Tick the correct track and retest.

## Check monitoring and output routing

In Advanced Audio Properties, set the source's Audio Monitoring to Monitor Off unless you need to hear it. A source set to Monitor Only will show activity but will not be written to the file. Also confirm the source is not muted in the mixer and that its volume is above zero. If the fader is at -inf, the meter can still flicker from pre-fader activity while the recording stays silent.

## Verify with a short test recording

Record ten seconds while speaking and triggering game audio. Stop, open the file in a player that shows track selection, and switch between tracks. If the source appears on the expected track, the fix is confirmed. If it is still absent, recheck that the file format supports multiple tracks; some formats collapse to a single track.

## Rollback note

If a recent change caused this, restore your previous Audio Properties settings before making further edits. Keep a screenshot of working settings so you can revert quickly.

For a controlled diagnosis of your **obs audio output capture** setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).

---
title: "Desktop Audio OBS: Meter Moves but Recording Has No Source Audio"
description: "Fix OBS desktop audio that shows a moving meter but records silence. Step-by-step checks for track assignment, monitoring, and output routing."
seo_title: "Desktop Audio OBS: Fix Meter Moves but No Source Audio"
seo_description: "Fix OBS desktop audio that shows a moving meter but records silence. Step-by-step checks for track assignment, monitoring, and output routing."
keywords:
  - "desktop audio obs"
date: 2026-11-21T15:01:46+08:00
publishDate: 2026-11-21T15:01:46+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and at the audio source is not captured step the meter moves but the recorded file has no source audio.

## Check Track Assignment First
Open the Advanced Audio Properties for your desktop audio source. Confirm the source is assigned to a track that is actually recorded. In Output settings, verify the recording track list includes that track. If the source is only on Track 2 but recording captures Track 1, the meter still moves while the file stays silent. Result interpretation: a moving meter with an empty recorded track means the source is monitored but not written.

## Verify Monitoring and Output Routing
In Advanced Audio Properties, check whether the source is set to Monitor Only. That setting sends audio to your speakers but excludes it from the recording. Set it to Monitor and Output. Also confirm the desktop audio device in Settings > Audio is the same device producing sound; a mismatched device can show activity on one meter while the recorded track receives nothing.

## Run a Verification Test
Record ten seconds with the game audio playing and speak into the mic. Stop and open the file in a player that shows track selection. Play each track separately. If desktop audio appears on its assigned track, the fix worked. If it is still missing, note which track is silent and compare it to the Advanced Audio Properties grid.

## Rollback and Recovery
Before changing more settings, export your current profile or note the original track assignments. If a change makes things worse, restore the previous profile and reapply one adjustment at a time. This keeps the **desktop audio obs** setup recoverable.

If the meter still moves while the recorded track stays empty after these checks,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your track grid and output settings.

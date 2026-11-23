---
title: "OBS Audio Capture: Why the Meter Moves but the Recording Has No Source Audio"
description: "Fix OBS audio capture when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, monitoring, and output settings."
seo_title: "OBS Audio Capture Fix: Meter Moves but Recording Has No Source Audio"
seo_description: "Fix OBS audio capture when the meter moves but the recorded file has no source audio. Step-by-step checks for track routing, monitoring, and output settings."
keywords:
  - "obs audio capture"
date: 2026-11-23T08:02:36+08:00
publishDate: 2026-11-23T08:02:36+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and the meter moves, but the recorded file has no source audio. This is a classic **obs audio capture** routing problem, not a dead microphone.

## Check Track Assignments First

Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). Look at the Tracks column for the source whose meter moves. If no track checkbox is ticked for that source, OBS will show activity but write nothing. Tick at least one track, preferably the one you intend to record. Then confirm that same track is enabled under Settings > Output > Recording > Track. If the source is on Track 2 but only Track 1 is recorded, the file will be silent for that source.

## Verify Monitoring and Output Routing

In Advanced Audio Properties, check the Audio Monitoring setting. If it is set to Monitor Off, that is fine for recording, but if you are judging capture by what you hear, you may be misreading the situation. More importantly, confirm the source is not muted and its volume is not at zero. A moving meter with zero volume can still produce silence in the file.

## Run a Verification Test

Record ten seconds with the source active. Stop, then open the recording in a player that lets you select audio tracks, or inspect it in an editor. If the source track is present but silent, return to Advanced Audio Properties and recheck track ticks and the output track selection. If the track is missing entirely, the source was never assigned to a recorded track.

## Rollback and Recovery

Before changing more settings, export your current profile and scene collection so you can restore them if a test makes things worse. If a change breaks your setup, reimport the saved profile and start from the last working configuration.

If the checks above do not restore capture,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your track layout and output settings.

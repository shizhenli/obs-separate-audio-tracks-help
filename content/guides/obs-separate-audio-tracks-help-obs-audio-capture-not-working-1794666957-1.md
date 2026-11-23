---
title: "OBS Audio Capture Not Working: When the Meter Moves but the Recording Is Silent"
description: "Fix OBS audio capture not working when the meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
seo_title: "OBS Audio Capture Not Working: Meter Moves, No Recorded Audio"
seo_description: "Fix OBS audio capture not working when the meter moves but the recorded file has no source audio. Check track assignments, advanced audio settings, and run a verification test."
keywords:
  - "obs audio capture not working"
date: 2026-11-23T11:02:43+08:00
publishDate: 2026-11-23T11:02:43+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording a game and mic on separate tracks, and the meter moves, but the recorded file has no source audio.

## Check Track Assignments First

Open the Advanced Audio Properties window (the gear icon in the Audio Mixer). For each source, look at the Track columns. A moving meter only proves the source is live; it does not prove the source is routed to a recorded track. Confirm the game and mic each have at least one track checked, and note which track numbers they use. If a source has no track checked, OBS will monitor it but write nothing to the file.

## Confirm the Recording Format

In Settings, Output, Recording, check the recording format. Some formats and containers handle multiple tracks differently. Also confirm the track selections under the recording tab match what you set in Advanced Audio Properties. If the source is on track 3 but the recording only writes track 1, the file will be silent for that source.

## Run a Verification Test

Record ten seconds with the game audio and mic both active. Stop, then open the file in a player that shows track selection, such as VLC under Audio, Audio Track. If the expected track is present but silent, return to Advanced Audio Properties and recheck that source's track boxes. If the track is missing entirely, the source was never routed to a recorded track.

## Rollback and Recovery

Before changing more settings, export your current profile so you can restore it. If a change makes things worse, reimport that profile and redo one adjustment at a time. This keeps the diagnosis controlled rather than cumulative.

If the meter still moves while the file stays silent after these checks, the **obs audio capture not working** symptom usually sits in track routing rather than the source itself. For a guided review of your setup,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult).

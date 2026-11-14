---
title: "OBS Only One Audio Track: Fixing a Source That Shows Meters but Records Silence"
description: "Troubleshoot OBS recording silence from a source whose meter moves, with exact checks, a verification test, and a rollback note."
seo_title: "OBS Only One Audio Track: Fix a Source That Shows Meters but Records Silence"
seo_description: "Troubleshoot OBS recording silence from a source whose meter moves, with exact checks, a verification test, and a rollback note."
keywords:
  - "obs only one audio track"
date: 2026-11-14T19:26:42+08:00
publishDate: 2026-11-14T19:26:42+08:00
draft: false
categories:
  - "Video Recording"
category_slug: "video-recording"
---

You are recording game and mic on separate tracks, and you are stuck at the audio source is not captured step: the meter moves, but the recorded file has no source audio.

## Check the track assignment first
Open the Audio Mixer, click the gear next to the silent source, and choose Advanced Audio Properties. In the Tracks row for that source, confirm the box matching your recording track is checked. Then open Settings, Output, Recording, and note which track numbers are enabled. If the source is checked on track 3 but recording only writes track 1, you get exactly this symptom. This is the usual cause of **obs only one audio track** behavior. Result interpretation: a checked box on an enabled track means assignment is correct; a checked box on a disabled track means the source is being dropped.

## Confirm the source is not muted downstream
In Advanced Audio Properties, check that the source is not set to Monitor Off while your capture relies on monitoring, and confirm no filter such as a noise gate is closing on silence. Temporarily disable filters on that source, then record ten seconds while speaking and playing game audio.

## Run the verification test
Record a short clip with both sources active. Open the file in a player that shows audio tracks, or remux it in OBS via File, Remux Recordings, then inspect the output. Expected result: the file lists the same number of tracks you enabled, and the previously silent source now has audio. If the meter still moves but the file stays silent, stop changing settings and gather your Advanced Audio Properties screenshot and OBS log.

## Rollback note
Before further edits, export your current profile so you can restore it. If a change makes things worse, reimport that profile and retest one variable at a time.

If the verification still fails,

![An OBS audio mixer showing separate microphone and desktop tracks](/images/service-detail-960.webp "OBS audio track routing check")

[Ask for help](/#consult) with your log and track settings.
